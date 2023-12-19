<script setup lang="ts">
const popap = usePopap();

const state = reactive({
  name: "",
  phone: "",
  comment: "",
  currancy: "BUN",
  budget: "",
});

const sendForm = async () => {
  const text = `
        <b>Имя: </b><i> ${state.name} </i>\n
        <b>Телефон: </b> <i> ${state.phone}</i> \n
        <b>Валюта: </b> <i> ${state.currancy}</i> \n
        <b>Бюджет: </b> <i> ${state.budget}</i> \n
        <b>Коментарий: </b> <i> ${state.comment}</i> \n
    `;

  try {
    const result = await $fetch("/api/bot/send", {
      method: "POST",
      body: JSON.stringify(text),
    });
    // console.log(result);
  } catch (error) {
  } finally {
    popap.value.buttonTrigger = !popap.value.buttonTrigger;
  }
};
</script>

<template>
  <div class="wrapper">
    <div class="count__price">
      <div class="count__price-top">
        <h2>Расчет стоимости</h2>
        <button @click="() => (popap.buttonTrigger = !popap.buttonTrigger)" class="close">
          &times;
        </button>
      </div>
      <form class="count__price-inputs" @submit.prevent="sendForm">
        <div class="input__group">
          <label for="name">Имя / Название компании</label>
          <input v-model="state.name" id="name" name="name" type="text" />
        </div>
        <div class="input__group">
          <label for="phone">Номер телефона</label>
          <input v-model="state.phone" id="phone" name="phone" type="text" />
        </div>
        <div class="input__group">
          <label>Ваш бюджет</label>

          <div class="curancy">
            <button
              :class="state.currancy === 'BUN' ? 'btn btn_active' : 'btn'"
              @click="() => (state.currancy = 'BUN')"
              type="button">
              BUN
            </button>
            <button
              :class="state.currancy === 'USD' ? 'btn btn_active' : 'btn'"
              @click="() => (state.currancy = 'USD')"
              type="button">
              USD
            </button>
          </div>
          <div v-if="state.currancy === 'USD'" class="budget">
            <button
              :class="state.budget === 'до 150 $' ? 'btn_budget btn_active' : 'btn_budget'"
              @click="() => (state.budget = 'до 150 $')"
              type="button">
              до 150 $
            </button>
            <button
              :class="state.budget === '150-260 $' ? 'btn_budget btn_active' : 'btn_budget'"
              @click="() => (state.budget = '150-260 $')"
              type="button">
              150-260 $
            </button>
            <button
              :class="state.budget === 'от 280 $' ? 'btn_budget btn_active' : 'btn_budget'"
              @click="() => (state.budget = 'от 280 $')"
              type="button">
              от 280 $
            </button>
          </div>
          <div class="budget" v-else>
            <button
              :class="state.budget === 'до 460 BUN' ? 'btn_budget btn_active' : 'btn_budget'"
              @click="() => (state.budget = 'до 460 BUN')"
              type="button">
              до 460 BUN
            </button>
            <button
              :class="state.budget === 'до 460-800 BUN' ? 'btn_budget btn_active' : 'btn_budget'"
              @click="() => (state.budget = 'до 460-800 BUN')"
              type="button">
              до 460-800 BUN
            </button>
            <button
              :class="state.budget === 'от 800 BUN' ? 'btn_budget btn_active' : 'btn_budget'"
              @click="() => (state.budget = 'от 800 BUN')"
              type="button">
              от 800 BUN
            </button>
          </div>
        </div>
        <div class="input__group">
          <label for="comment">Комментарий</label>

          <textarea v-model="state.comment" id="comment" name="comment"></textarea>
        </div>
        <button class="calc" type="submit">
          <span>Расчитать стоимость</span>
          <span>></span>
        </button>
      </form>
    </div>
  </div>
</template>

<style scoped lang="scss">
.wrapper {
  width: min(100%, 1028px);
  height: min(100%, 964px);
  display: grid;
  place-content: center;
  background: #fff;
}
.count__price {
  /*  width: min(100%, 868px); */
  /*   display: grid;
  grid-template-columns: 1fr; */
  &-top {
    display: flex;
    align-items: flex-start;
    justify-content: space-between;
    & h2 {
      font-size: 48px;
      font-style: normal;
      font-weight: 400;
      line-height: 109.8%;
      margin-top: 0;
    }
    & button {
      width: 30px;
      height: 30px;
      display: grid;
      place-content: center;

      background: transparent;
      font-size: 48px;
      border: none;
    }
  }
  &-inputs {
    display: grid;
    row-gap: 40px;
    & .input__group {
      display: flex;
      align-items: center;
      column-gap: 20px;

      & label {
        width: 203px;
        font-size: 16px;
        font-style: normal;
        font-weight: 300;
        line-height: 109.8%;
      }
      & input {
        width: min(100%, 645px);

        height: 58px;

        border-radius: 5px;
        font-size: 18px;
        padding-left: 10px;
        padding-right: 10px;

        border: 1px solid #b1b1b1;
      }
    }
    & .input__group:nth-child(3) {
      display: grid;
      row-gap: 40px;
      & .curancy,
      .budget {
        display: flex;
        column-gap: 10px;
      }
    }
    & .input__group:nth-child(4) {
      & textarea {
        font-size: 18px;
        padding-left: 10px;
        /*  padding-right: 10px; */
        width: 645px;

        height: 217px;
        border-radius: 5px;
        border: 1px solid #b1b1b1;
      }
    }
    & .calc {
      justify-self: end;
    }
  }
}

.btn {
  color: #1536df;
  background: transparent;
  border-radius: 5px;
  border: 1px solid #1536df;
  display: flex;
  width: 89px;
  height: 38px;

  justify-content: center;
  align-items: center;
  gap: 10px;
  flex-shrink: 0;
  &:hover {
    color: #fff;
    background: #1536df;
  }
}
.btn_budget {
  height: 38px;
  display: inline-flex;
  padding: 10px 46px;
  justify-content: center;
  align-items: center;
  gap: 10px;
  border-radius: 5px;
  background: #f9f9fe;
  border: none;
  &:hover {
    border: 1px solid #1536df;

    background: #f9f9fe;
  }
}
.btn_active {
  color: #fff;
  background: #1536df;
  &:hover {
    color: #fff;
    background: #1536df;
  }
}
</style>

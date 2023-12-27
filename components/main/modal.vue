<script setup lang="ts">
const popap = usePopap();

const state = reactive({
  name: "",
  phone: "",
  comment: "",
});

const isEnableComputed = computed(() => {
  if (state.name && state.phone && state.comment) {
    return true;
  } else {
    return false;
  }
});

const sendForm = async () => {
  if (isEnableComputed.value) {
    const text = `
        <b>Имя/Название проекта: </b><i> ${state.name} </i>\n
        <b>Телефон: </b> <i> ${state.phone}</i> \n
        <b>Коментарий: </b> <i> ${state.comment}</i> \n
    `;
    try {
      const result = await $fetch("/api/bot/send", {
        method: "POST",
        body: JSON.stringify(text),
      });

      popap.value.timerTrigger = !popap.value.timerTrigger;
    } catch (error) {
      console.log(error);
    }
    console.log("send forme");
  } else {
    console.log("error");
  }
};
</script>

<template>
  <div>
    <div class="forms" id="modal">
      <div class="left">
        <div>
          <h3>Расчет<br />стоимости</h3>
          <p>Мы свяжемся с вами в течении 20 минут</p>
        </div>
        <div class="social__form asdzz">
          <p>Или напишите нам в соц.сети</p>
          <div class="icons__form">
            <UiElementsIcons
              icon-name="basil:telegram-solid"
              color-icon="white"
              size-width="28px"
              size-heigth="28px" />
            <UiElementsIcons
              icon-name="basil:viber-solid"
              color-icon="white"
              size-width="28px"
              size-heigth="28px" />
            <UiElementsIcons
              icon-name="fa6-brands:square-instagram"
              color-icon="white"
              size-width="28px"
              size-heigth="28px" />
            <UiElementsIcons
              icon-name="basil:vk-solid"
              color-icon="white"
              size-width="28px"
              size-heigth="28px" />
          </div>
        </div>
      </div>
      <div class="right">
        <form @submit.prevent="sendForm">
          <div>
            <input
              v-model="state.name"
              type="text"
              name="name"
              placeholder="Имя/Название проекта" />
            <input disabled type="text" placeholder="Мы свяжемся с вами в течении 20 минут" />
            <input v-model="state.phone" type="text" name="phone" placeholder="Номер телефона" />
            <textarea v-model="state.comment" name="comment" class="textaria"></textarea>
          </div>
          <button type="submit">Расчитать стоимость</button>
        </form>
        <div class="social__form zzz">
          <p>Или напишите нам в соц.сети</p>
          <div class="icons__form">
            <UiElementsIcons
              icon-name="basil:telegram-solid"
              color-icon="white"
              size-width="28px"
              size-heigth="28px" />
            <UiElementsIcons
              icon-name="basil:viber-solid"
              color-icon="white"
              size-width="28px"
              size-heigth="28px" />
            <UiElementsIcons
              icon-name="fa6-brands:square-instagram"
              color-icon="white"
              size-width="28px"
              size-heigth="28px" />
            <UiElementsIcons
              icon-name="basil:vk-solid"
              color-icon="white"
              size-width="28px"
              size-heigth="28px" />
          </div>
        </div>
      </div>
      <div></div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.forms{
  align-items: center !important;
  justify-content: center !important;
}
.textaria{
  height: 200px;
  margin-bottom: 40px;
  background: transparent;
}
.social__form {
  display: flex;
  flex-direction: column;
  row-gap: 40px;
  & p {
    color: white;
    padding-top: 100px;
  }
}
.icons__form {
  display: flex;
  column-gap: 26px;
}
.right form div {
  display: flex;
  flex-direction: column;
  row-gap: 40px;
  & input {
    background: none;
    color: #fff;
    width: 100%;
    border: none;
    width: 700px;
    height: 70px;
    border-bottom: 1px solid;
    &::-moz-placeholder {
      color: red;
    }
    &::-webkit-input-placeholder {
      color: #fff;
      line-height: 26px; /* 162.5% */
      font-family: "Inter";
      font-size: 16px;
      font-style: normal;
      font-weight: 100;
    }
    &:nth-child(4) {
      border: 1px solid;
      height: 200px;
      margin-bottom: 40px;
    }
  }
}
.right form {
  & button {
    color: #fff;
    padding: 16px 21px;
    font-family: "Inter";
    font-size: 16px;
    font-style: normal;
    font-weight: 700;
    line-height: normal;
    border-radius: 5px;
    background: #1536df;
    border: none;
  }
}
.forms {
  width: 100%;
  border-radius: 25px;
  background: #000;
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  justify-content: space-between;
  margin-top: 100px;
}

h3 {
  color: #fff;
  font-size: 60px;
  font-weight: 250;
  line-height: 109.8%; /* 65.88px */
  margin: 0;
  padding-bottom: 20px;
}
.left,
.right {
  padding: 100px 30px;
}
.left {
  display: flex;
  flex-direction: column;
  row-gap: 227px;
  & p {
    color: #fff;
    font-size: 16px;
    font-weight: 100;
    line-height: 26px; /* 162.5% */
    font-family: "Inter";
  }
}
.zzz {
  display: none;
}
@media screen and (max-width: 1100px) {
  .asdzz {
    display: none;
  }
  .zzz {
    display: flex;
  }
}
@media screen and (max-width: 780px) {
  .right form div {
    & input {
      width: 600px;
    }
  }
}
@media screen and (max-width: 667px) {
  .right form div {
    & input {
      width: 500px;
    }
  }
}
@media screen and (max-width: 582px) {
  .right form div {
    & input {
      width: 400px;
    }
  }
  h3 {
    font-size: 36px;
  }
}
@media screen and (max-width: 480px) {
  .right form div {
    & input {
      width: 200px;
    }
    & input:nth-child(2){
      display: none;
    }
  }
}
</style>

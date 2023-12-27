<template>
    <header>
      <div class="header__up">
        <div class="logo">
          <nuxt-link to="/" class="logo__img">WizSol</nuxt-link>
          <p>Наше видение вашего успеха!</p>
        </div>
        <div class="header__button__ui">
          <div>
            <nuxt-link to="/" class="header__button header__button__one">Заказать сайт</nuxt-link>
          </div>
          <div>
            <nuxt-link to="/" class="header__button header__button__two">Заказать продвижение</nuxt-link>
          </div>
        </div>
      </div>
      <div class="menu">
        <nav>
          <ul>
            <li><nuxt-link to="">Как мы работаем</nuxt-link></li>
            <li class="submenu">
              <nuxt-link to="/servises">
                Услуги 👇
              </nuxt-link>
                <ul class="services">
                  <li class="ul__li__point"><nuxt-link to="/servises/development">Разработка</nuxt-link></li>
                  <li class="ul__li__point"><nuxt-link to="/servises/marketing">Продвижение</nuxt-link></li>
                  <li class="ul__li__point"><nuxt-link to="/servises/design">Дизайн</nuxt-link></li>
                </ul>
            </li>
            <li><nuxt-link to="/">Тарифы</nuxt-link></li>
            <li><nuxt-link to="/">Помощь</nuxt-link></li>
          </ul>
        </nav>
      </div>
    </header>
</template>
<script setup>
const show = ref(false)
</script>
<style lang="scss" scoped>
header{
  display: flex;
}
.logo__img{
  color: #ffffff;
  font-size: 36px;
  font-weight: 800;
}
.logo{
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  column-gap: 8px;
}
.header__button__ui{
  display: flex;
  column-gap: 21px;
}
.header__button{
  width: 200px;
  border-radius: 50px;
  padding: 8px 0;
  display: flex;
  align-items: center;
  justify-content: center;
}
.header__button__one{
  border: 2px solid #7F5AF0;
}
.header__button__two{
  border: 2px solid #2CB67D;
}
.submenu ul{
  display: flex;
  flex-direction: column;
  padding: 0 !important;
  padding: 14px 24px !important;
  position: absolute;
  background: #1e1e1e;
  border-radius: 12px;
  border: 0.1rem solid #fff;
  transform: translateX(-10px);
  cursor: default;
  & li{
    padding: 4px 0;
    font-size: 17px;
    font-weight: 700;
    & a:hover{
      color: #2CB67D;
      cursor: pointer;
    }
  }
}
li {
  cursor: pointer;
}
li.submenu ul {
  display: none;
  margin: 0;
}
li.submenu:hover ul {
  display: block;
}
.header__up{
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 12px 0;
}
header{
  display: flex;
  flex-direction: column;
}
.menu{
  border: 0.1rem solid #fff;
  border-radius: 50px;
  padding: 0 24px;
  & nav{
    &> ul{
      display: flex;
      justify-content: space-between;
      margin: 12px;
    }
  }
}
</style>
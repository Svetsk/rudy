<template>
  <div style="margin: 0 20px;">
    <h1>Блог студии Rudy</h1>
    <p>В нашем блоге вы сможете больше узнать о<br />создании сайта. Дизайне и акциях студии</p>
  </div>
</template>

<style lang="scss" scoped>
h1 {
  color: #000;
  font-family: "Museo Sans Cyrl 500";
  font-size: 60px;
  font-weight: 400;
  line-height: 109.8%; /* 65.88px */
  margin: 0;
  margin: 80px 0 20px 0;
}
p {
  color: #767676;
  font-family: 'Inter';
  font-size: 24px;
  font-style: normal;
  font-weight: 400;
  line-height: normal;
}
@media screen and (max-width: 600px) {
  h1{
    color: #000;
    font-size: 36px;
    font-weight: 400;
    line-height: 109.8%; /* 39.528px */
  }
  p{
    font-size: 24px;
    font-weight: 400;
  }
}
</style>

<template>
  <div class="requ">
    <UiElementsTitle title="Видео отзывы" />
    <div>
      <div class="qqq">
        <div class="video__flex">
          <a href="https://www.youtube.com/shorts/AjZApYwWG88">
            <div class="posit">
              <NuxtImg class="absol" src="/image/Strelka.png" height="64px" />
            <iframe
            class="qqq"
              srcdoc="<style>*{padding:0;margin:0;overflow:hidden}
                          html,body{height:100%}
                          img,span{position:absolute;width:100%;top:0;bottom:0;margin:auto}
                          span{text-align:center;font:48px/1.5 sans-serif;color:white;text-shadow:0 0 0.5em black}
                          .xueviy__hover{transform: translateX(-40px); display:none;}
                          </style>
                          <a href=https://www.youtube.com/shorts/AjZApYwWG88?autoplay=1>
                          <img src=image/videoOne.png alt='video'>
                          <span class='xueviy__hover'><img class='xui' src=image/Strelka.png alt='video' style='width:88px'></span>
                          </a>"
              frameborder="0"
              allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
              allowfullscreen
              title="Demo video">
            </iframe>
            </div>
          </a>
          <div class="video__text">
            <p>LaForme</p>
            <p>Отзыв от Данилы, владелец бренда LaForme</p>
          </div>
        </div>
        <div class="video__flex">
          <div class="posit">
            <NuxtImg class="absol" src="/image/Strelka.png" height="64px" />
            <iframe
              src="https://www.youtube.com/embed/izvIofkLD4w?si=5IhTlsa4nQcktx8-"
              srcdoc="<style>*{padding:0;margin:0;overflow:hidden}
                          html,body{height:100%}
                          img,span{position:absolute;width:100%;top:0;bottom:0;margin:auto}
                          span{text-align:center;font:48px/1.5 sans-serif;color:white;text-shadow:0 0 0.5em black}
                          .xueviy__hover{transform: translateX(-40px); display: none;}  
                        </style>
                          <a href=https://www.youtube.com/embed/izvIofkLD4w?si=5IhTlsa4nQcktx8-?autoplay=1>
                          <img src=image/videoTwo.png alt='Demo video'>
                          <span class='xueviy__hover'><img class='xui' src=image/Strelka.png alt='video' style='width:88px'></span>
                          </a>"
              frameborder="0"
              allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
              allowfullscreen
              title="Demo video">
            </iframe>
          </div>
          <div class="video__text">
            <p>AsaiVapeShop</p>
            <p>Отзыв от Владислава, владелец Asaivapeshop</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.posit{
  position: relative;
  & .absol{
    position: absolute;
    z-index: 2;
    left: 45%;
    transform: translateX(-50%);
    bottom: 50%;
    transform: translateY(50%);
    visibility: hidden;
  }
  &:hover .absol{
    visibility: visible;
  }
}
iframe {
  width: 560px;
  height: 315px;
}
.requ {
  padding-top: 120px;
}
.video__text {
  //padding-top: 40px;
  display: flex;
  flex-direction: column;
  row-gap: 20px;

  & p:nth-child(1) {
    color: #000;
    font-family: "Museo Sans Cyrl 500";
    font-size: 24px;
    font-weight: 400;
    line-height: 109.8%; /* 26.352px */
    padding-top: 20px;
  }
  & p:nth-child(2) {
    color: #000;
    font-family: "Museo Sans Cyrl 500";
    font-size: 16px;
    font-weight: 300;
    line-height: 109.8%; /* 17.568px */
  }
}
.qqq {
  display: flex;
  justify-content: space-between;
  gap: 12px;
  overflow: hidden;

  & iframe {
    border-radius: 25px;
    width: 709px;
    height: 320px;
  }
}
@media screen and (max-width: 760px) {
  .qqq iframe {
    width: 340px !important;
    height: 190px !important;
  }
  .video__text {
    padding: 0;
  }
  .qqq{
    flex-direction: column;
  }
}
@media screen and (max-width: 660px) {
  .qqq {
    flex-direction: column;
  }
  .video__text p:nth-child(1){
    padding-top: 4px;
  }
}
</style>

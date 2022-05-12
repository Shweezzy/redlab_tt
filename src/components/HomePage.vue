<template>
  <div class="home">
    <div class="home__caption">
      <div class="caption-image">
        <img src="../assets/images/art01.png" alt="art01" />
      </div>
      <div class="caption-text">
        <h1>
          Уборка<br />
          квартир<br />
          в Киеве
        </h1>

        <h3>
          Мы уберем у вас дома или в офисе.<br />
          Наведем чистоту после ремонта и<br />
          проведем генеральную уборку.
        </h3>
      </div>
    </div>
    <div class="home__circle">
      <span
        >Заказать<br />
        уборку</span
      >
    </div>
    <div class="home__cards">
      <div id="homeCard1" data-aos="fade-up" class="cards-item">
        <p class="cards-item__text">Тщательно отобранный персонал</p>
        <img class="cards-item__image" src="../assets/images/icon1.png" alt="card image" />
        <div class="cards-item__back">
          <p>Не нужно тратить время, силы и ресурсы на разме- щение вакансий, проведе- ние собеседований, про- верку кандидатов на должность уборщицы. За счет больших объемов мы можем сделать это эффективнее.</p>
        </div>
      </div>
      <div id="homeCard2" data-aos="fade-up" data-aos-delay="100" class="cards-item">
        <p class="cards-item__text">Качественная эко-химия</p>
        <img class="cards-item__image" src="../assets/images/icon2.png" alt="card image" />
        <div class="cards-item__back">
          <p>
            Старайтесь пользоваться универсальными средствами. Так вы сократите количество бутылок на полке, а уборка станет проще и быстрее. Покупайте понравившуюся вам бытовую химию в больших упаковках. Это экономит не только деньги и время: меньше
            использованных бутылок — меньше мусора.
          </p>
        </div>
      </div>
      <div id="homeCard3" data-aos="fade-up" data-aos-delay="200" class="cards-item">
        <p class="cards-item__text">Контролируем качество</p>
        <img class="cards-item__image" src="../assets/images/icon3.png" alt="card image" />
        <div class="cards-item__back">
          <p>В полночь качество наших работ ничем не хуже чем утром ;)</p>
        </div>
      </div>
      <div id="homeCard4" data-aos="fade-up" data-aos-delay="300" class="cards-item">
        <p class="cards-item__text">Работаем круглосуточно</p>
        <img class="cards-item__image" src="../assets/images/icon4.png" alt="card image" />
        <div class="cards-item__back">
          <p>Вы можете оставить заявку на уборку в любое время дня или ночи :)</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Home-page",
  data() {
    return {
      msg: "hello kurwa",
    };
  },
};
</script>
<style lang="scss" scoped>
.home {
  .home__caption {
    width: 100%;
    height: 800px;
    display: flex;

    .caption-image {
      width: 50%;

      img {
        width: 100%;
        height: 100%;
      }
    }

    .caption-text {
      width: 50%;
      display: flow-root;
      align-self: center;
      box-sizing: border-box;
      padding-left: 155px;

      h1 {
        font-weight: 400;
        font-size: 76px;
        line-height: 110%;
        height: fit-content;
        padding-bottom: 30px;
      }

      h3 {
        font-weight: 400;
        font-size: 18px;
        line-height: 140%;
        height: fit-content;
      }
    }
  }

  .home__circle {
    position: absolute;
    width: 195px;
    height: 195px;
    background: #5a30f0;
    border-radius: 50%;
    left: 622px;
    top: 586px;
    display: flex;
    justify-content: center;
    align-items: center;

    animation: swimming 2s linear infinite;

    span {
      font-size: 18px;
      font-weight: 500;
      line-height: 23px;
      letter-spacing: 0.03em;
      text-align: center;
      color: #ffffff;
      text-transform: uppercase;
      transform: rotate(-15deg);
    }
    // &:hover:before {
    //   content: "";
    //   position: absolute;
    //   border: #e1e1e1 solid 4px;
    //   top: 0;
    //   right: 0;
    //   bottom: 0;
    //   left: 0;
    //   -webkit-transition-duration: 0.3s;
    //   transition-duration: 0.3s;
    //   -webkit-transition-property: top, right, bottom, left;
    //   transition-property: top, right, bottom, left;
    // }
  }

  .home__cards {
    width: 97%;
    padding-top: 72px;
    margin: auto;
    display: flex;
    justify-content: space-evenly;

    .cards-item {
      position: relative;
      height: 328px;
      width: 300px;
      border-radius: 8px;
      background: #f3f6fb;
      display: flex;
      flex-wrap: wrap;
      align-content: baseline;
      padding-top: 21px;
      box-sizing: border-box;

      &:hover .cards-item__back {
        opacity: 1;
      }
    }

    .cards-item__image {
      display: block;
      position: absolute;
      bottom: 0px;
    }

    .cards-item__text {
      font-family: TTTravels;
      font-style: normal;
      font-weight: 500;
      font-size: 24px;
      line-height: 130%;
      text-align: center;
      color: #404040;
      width: 210px;
      margin: auto;
    }

    #homeCard1 {
      img {
        margin-left: 64px;
        width: 151px;
        height: 151px;
      }
    }
    #homeCard2 {
      img {
        margin-left: 55px;
        width: 188px;
        height: 154px;
      }
    }
    #homeCard3 {
      img {
        margin-left: 45px;
        width: 211px;
        height: 174px;
      }
    }
    #homeCard4 {
      img {
        margin-left: 46px;
        width: 202px;
        height: 149px;
      }
    }

    .cards-item__back {
      position: absolute;
      opacity: 0;
      width: 100%;
      height: 100%;
      background: #5a30f0;
      padding: 30px;
      box-sizing: border-box;
      top: 0px;
      color: #ffffff;
      transition: all 0.2s linear;
    }
  }
}

// animation
@keyframes swimming {
  0% {
    transform: translate3d(0px, 0px, 0px);
  }
  25% {
    transform: translate3d(0px, +1px, 0px);
  }
  75% {
    transform: translate3d(0px, -1px, 0px);
  }
  100% {
    transform: translate3d(0px, 0px, 0px);
  }
}
</style>

<template>
  <header class="header">
    <div class="header-caption d-f">
      <div class="header-caption__logo">
        <img src="../assets/images/logo.svg" alt="Logo" />
      </div>
      <div class="header-caption__button">
        <input class="button-checkbox" type="checkbox" />
        <label class="button-label" for="">
          <span class="button-label__span">Дом</span>
        </label>
      </div>
    </div>
    <nav class="header-nav d-f">
      <ul class="header-nav__list">
        <li class="header-nav__item"><a target="_blank" href="#">После ремонта</a></li>
        <li class="header-nav__item"><a target="_blank" href="#">Генеральная уборка</a></li>
        <li class="header-nav__item"><a target="_blank" href="#">Регулярная уборка</a></li>
        <li class="header-nav__item"><a target="_blank" href="#">Мойка окон</a></li>
      </ul>
    </nav>
    <div class="header-contacts d-f">
      <span class="header-contacts__number">+380 67 401 69 77</span>
      <img src="../assets/images/line.svg" alt="line" />
      <span class="header-contacts__period">24/7</span>
      <img src="../assets/images/menu-icon.svg" alt="menu icon" />
    </div>
  </header>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.header {
  display: flex;
  justify-content: space-between;
  width: 100%;
  height: 70px;
  background: transparent;
  position: absolute;

  .d-f {
    display: flex;
    align-items: center;
  }
}

.header-caption {
  width: 336px;
  height: 100%;

  .header-caption__logo {
    display: block;
    width: 160px;

    img {
      width: 99px;
      height: 25px;
      display: block;
      margin: auto;
      margin-left: 54px;
    }
  }

  .header-caption__button {
    background: rgba(255, 255, 255, 0.56);
    border-radius: 30px;
    overflow: hidden;
    height: 36px;
    width: 127px;
    text-align: center;
    font-size: 14px;
    position: relative;
    left: 16px;
    color: #fff;
    border: 1px solid #e2e8f0;
    font-weight: 400;

    &:before {
      content: "Офис";
      position: absolute;
      top: 0;
      bottom: 0;
      right: 0px;
      width: 60px;
      display: flex;
      align-items: center;
      justify-content: center;
      z-index: 3;
      pointer-events: none;
      color: black;
    }

    .button-checkbox {
      cursor: pointer;
      position: absolute;
      top: 0;
      left: 0;
      bottom: 0;
      width: 100%;
      height: 100%;
      opacity: 0;
      z-index: 2;

      &:checked + .button-label:before {
        transform: translateX(71px);
        transition: transform 200ms;
      }
      &:checked + .button-label {
        color: #636c81;
      }
      & + .button-label {
        position: relative;
        display: block;
        user-select: none;
        pointer-events: none;

        &:before {
          content: "";
          background: #5a30f0;
          height: 31px;
          width: 55px;
          position: absolute;
          left: 0;
          top: 2px;
          border-radius: 40px;
          transform: translateX(0);
          transition: transform 200ms;
        }

        .button-label__span {
          position: relative;
          right: 36px;
          top: 9px;
        }
      }
    }
  }
}

.header-nav {
  width: 755px;

  .header-nav__list {
    display: flex;
  }

  .header-nav__item {
    list-style: none;
    font-weight: 500;
    font-size: 16px;
    letter-spacing: 0.2px;
    margin-right: 32.3px;
    display: inline-block;
    position: relative;

    a {
      color: #404040;
      text-decoration: none;

      display: inline-block;
      padding: 5px 0;

      &:after {
        background: none repeat scroll 0 0 transparent;
        bottom: 0;
        content: "";
        display: block;
        height: 2px;
        left: 50%;
        position: absolute;
        background: #404040;
        transition: width 0.3s ease 0s, left 0.3s ease 0s;
        width: 0;
      }

      &:hover:after {
        width: 100%;
        left: 0;
      }
    }
  }
}
.header-contacts {
  width: 322px;
  font-size: 16px;
  font-weight: 700;
  letter-spacing: 0.2px;

  .header-contacts__number {
    width: 173px;
  }

  .header-contacts__period {
    width: 67px;
    text-align: center;
    margin-right: 23px;
  }
}
</style>

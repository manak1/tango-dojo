<template>
  <header class="l-header s3 p1">
    <div class="c-wrapper l-header__wrapper">
      <div class="l-header__left">
        <h1 class="l-header__logo">
          <img
            src="@/assets/img/header/header_logo.png"
            class="l-header__logoImg"
            alt="header-logo"
          />
          <img
            src="@/assets/img/header/header_text.png"
            class="l-header__logoText"
            alt="header-text"
          />
        </h1>
      </div>
      <div class="l-header__right">
        <a href="" class="l-header__button c-button c-button--shadow"
          >ログイン</a
        >
      </div>
    </div>
  </header>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
@import '@/assets/scss/mixins.scss';
.l-header {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  background-color: $color-white;
  padding: 4px;

  &__logo {
    font-size: 24px;
    display: flex;
    align-items: center;
  }

  &__logoImg {
    width: 45px;
    height: 45px;
  }

  &__logoText {
    width: 210px;
    height: auto;
  }

  &__wrapper {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
}
</style>

/* eslint-disable no-unused-vars */
<template>
  <section class="p-hero ">
    <div class="p-hero__wrapper c-wrapper">
      <h2 class="p-hero__title">
        楽しみながら英単語を学習しよう！
      </h2>

      <lottie
        :options="defaultOptions"
        :height="400"
        :width="400"
        v-on:animCreated="handleAnimation"
        class="p-hero__animation"
      />

      <p class="p-hero__text">
        タンゴドウジョウは手軽に英単語を学習することができるサービスです。<br />
        利用者の英語力に合わせて問題が出題されるため。<br />
        初心者から上級者の方までお楽しみいただけると思います。
      </p>

      <div class="p-hero__buttons">
        <a
          href=""
          class="c-button--round c-button--large p-hero__button c-button--shadow"
          >ためしてみる</a
        >
        <a href="#" class="p-hero__buttonText">デモを試してみる(登録なし)</a>
      </div>
    </div>
  </section>
</template>

<script>
import Lottie from '~/components/lottie'
import * as animationData from '~/assets/img/hero/a.json'
export default {
  components: {
    Lottie
  },
  data() {
    return {
      // データを定義
      defaultOptions: { animationData },
      animationSpeed: 1
    }
  },
  methods: {
    handleAnimation(anim) {
      this.anim = anim
    }
  }
}
</script>

<style lang="scss" scoped>
@import '@/assets/scss/mixins.scss';

.p-hero {
  margin-top: 53px;
  text-align: center;
  background-color: $color-secondary;
  &__wrapper {
    padding: 72px;
  }

  &__title {
    @include text-large;
    margin-bottom: 16px;
    letter-spacing: 2px;
  }

  &__text {
    @include text-default;
    line-height: 33px;
    margin-top: 1rem;
  }

  &__buttons {
    margin-top: 4.8rem;
    display: flex;
    flex-direction: column;
    justify-content: center;
  }

  &__button {
    width: 20%;
    margin: 0 auto;
  }

  &__buttonText {
    @include text-small;
    color: $color-primary;

    text-decoration: none;
    display: inline-block;
    margin: 0 auto;
    margin-top: 2.4rem;
    width: 200px;
    display: inline-block;

    &:hover {
      opacity: 0.7;
      transition: 0.3s;
    }
  }
}
</style>

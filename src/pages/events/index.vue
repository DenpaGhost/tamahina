<template>
  <div>
    <div class="container bg-white fill-right index-shadow-lb mt-5 slide-in-from-right">
      <div class="row">
        <div class="col-12 col-lg-6 mb-3 pb-3">
          <h1 class="font-expletus text-strong index-shadow-lb-sm">
            Events
          </h1>
          <p class="font-weight-bold">
            タマクラとヒナクラの詳細
          </p>
        </div>
      </div>

      <div class="row justify-content-around">
        <div class="col-12 col-lg-6 mb-3 text-center">
          <nuxt-link to="/events/tmkr00">
            <img src="/img/logos/tmkr00_logo.png"
                 alt="タマクラ0"
                 class="img-fluid"/>
          </nuxt-link>
        </div>

        <div class="col-12 col-lg-6 mb-3 text-center">
          <nuxt-link to="/events/tmkr01">
            <img src="/img/logos/tmkr01_logo.png"
                 alt="タマクラ1"
                 class="img-fluid"/>
          </nuxt-link>
        </div>

        <div class="col-12 col-lg-6 mb-3 text-center">
          <nuxt-link to="/events/tmkr02">
            <img src="/img/logos/tmkr02_logo.png"
                 alt="タマクラ2"
                 class="img-fluid"/>
          </nuxt-link>
        </div>

        <div class="col-12 col-lg-6 mb-3 text-center">
          <nuxt-link to="/events/tmkr02-5">
            <img src="/img/logos/tmkr02.5_logo.png"
                 alt="タマクラ2.5"
                 class="img-fluid"/>
          </nuxt-link>
        </div>

        <div class="col-12 col-lg-6 mb-3 text-center">
          <nuxt-link to="/events/tmkr03">
            <img src="/img/logos/tmkr03_logo.png"
                 alt="タマクラ3"
                 class="img-fluid"/>
          </nuxt-link>
        </div>


        <div class="col-12 col-lg-6 mb-3 text-center">
          <nuxt-link to="/events/bimitmsushi">
            <img src="/img/logos/bimitmsushi.png"
                 alt="美味しいタマゴ寿司"
                 class="img-fluid"/>
          </nuxt-link>
        </div>

        <div class="col-12 col-lg-6 mb-3 text-center">
          <nuxt-link to="/events/kmkr">
            <img src="/img/logos/kmkr.png"
                 alt="カメクラ"
                 class="img-fluid"/>
          </nuxt-link>
        </div>

        <div class="col-12 col-lg-6 mb-3 text-center">
          <nuxt-link to="/events/tmkr03-5">
            <img src="/img/logos/tmkr03-5_logo.png"
                 alt="タマクラ3.5"
                 class="img-fluid"/>
          </nuxt-link>
        </div>

        <div class="col-12 col-lg-6 mb-3 text-center">
          <nuxt-link to="/events/tmkr04">
            <img src="/img/logos/tmkr04_logo.png"
                 alt="タマクラ4"
                 class="img-fluid"/>
          </nuxt-link>
        </div>

        <div class="col-12 col-lg-6 mb-3 text-center">
          <nuxt-link to="/events/tmkr04-5">
            <img src="/img/logos/tmkr04.5_logo.png"
                 alt="タマクラ4.5"
                 class="img-fluid"/>
          </nuxt-link>
        </div>

        <div class="col-12 col-lg-6 mb-3 text-center">
          <nuxt-link to="/events/tmkrf">
            <img src="/img/logos/tmkrF_logo.png"
                 alt="タマクラF"
                 class="img-fluid"/>
          </nuxt-link>
        </div>

        <div class="col-12 col-lg-6 mb-3 text-center">
          <nuxt-link to="/events/hnkr0">
            <img src="/img/logos/hnkr0_logo.png"
                 class="img-fluid"
                 alt="ヒナクラ0">
          </nuxt-link>
        </div>

        <div class="col-12 col-lg-6 mb-3 text-center">
          <nuxt-link to="/events/hnkr">
            <img src="/img/logos/hnkr.png"
                 alt="ヒナクラ"
                 class="img-fluid"/>
          </nuxt-link>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import {mapMutations} from "vuex";

export default {
  name: "events",
  mounted() {
    this.setVisitIn('events');
    this.setBackgroundColor('#FAFAFA');
  },
  methods: {
    ...mapMutations({
      setBackgroundColor: 'setBackgroundColor',
      setVisitIn: 'setVisitIn'
    })
  },
  head() {
    return {
      title: 'events',
      meta: [
        {
          hid: 'title',
          name: 'title',
          content: 'events | ヒナクラ'
        },
        {
          hid: 'description',
          name: 'description',
          content: '開催されたイベントの一覧です。'
        },
        {
          hid: 'og:url',
          property: 'og:url',
          content: `${process.env.BASE_URL / this.$route.fullPath}`,
        },
        {
          hid: 'og:type',
          property: 'og:type',
          content: 'article',
        },
        {
          hid: 'og:title',
          property: 'og:title',
          content: 'events | ヒナクラ',
        },
        {
          hid: 'og:image',
          property: 'og:image',
          content: `${process.env.BASE_URL}/img/logos/hnkr.png`,
        },
        {
          hid: 'og:description',
          property: 'og:description',
          content: '開催されたイベントの一覧です。',
        }
      ]
    }
  }
}
</script>

<style lang="scss">
.img-fluid {
  max-width: 100%;
  max-height: 10em;
  object-fit: contain;
}

.img-container {
  max-height: 4em;
  max-width: 100%;
}
</style>
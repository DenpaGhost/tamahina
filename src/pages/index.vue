<template>
  <div>
    <div class="container mt-5">
      <div class="row">
        <div class="col-12 d-flex justify-content-center fade-in">
          <img src="/img/fliers/hnkr0.png" class="index-flier index-shadow-lb" alt="ヒナクラゼロ">
        </div>
      </div>
    </div>

    <div class="bg-white my-5 container fill-left index-shadow-lb slide-in-from-left">
      <div class="row">
        <div class="col-12 pb-3">
          <h1 class="font-expletus text-hi index-shadow-rb-sm">
            ヒナクラゼロ 開催！
          </h1>
          <p>
            ── DJのタマゴ、激励 ───
          </p>
          <div class="text-right">
            <tama-button to="/events/hnkr0" nuxt-link>
              show more
            </tama-button>
          </div>
        </div>
      </div>
    </div>

    <div class="bg-white my-5 container fill-right index-shadow-rb slide-in-from-right">
      <div class="row">
        <div class="col-12 pb-3">
          <h1 class="font-expletus text-hi index-shadow-rb-sm">
            Introduction
          </h1>
          <p>
            タマクラ / ヒナクラって何？
          </p>
          <div class="text-right">
            <tama-button to="/about" nuxt-link>
              more
            </tama-button>
          </div>
        </div>
      </div>
    </div>

  </div>
</template>

<script>
import DummyImage from "../components/samples/DummyImage";
import TamaButton from "../components/buttons/TamaButton";
import {mapMutations} from "vuex";

export default {
  name: "index",
  components: {TamaButton, DummyImage},
  head() {
    return {
      meta: [
        {
          hid: 'title',
          name: 'title',
          content: 'ヒナクラ | ⚡大17代の卒業祝いアニクラ'
        },
        {
          hid: 'description',
          name: 'description',
          content: '⚡大17代の卒業祝いアニクラとして2021/03/06に「ヒナクラ」を開催！また、ヒナクラ参加DJの練習としてDJの"タマゴ"向けオンラインアニクラ「タマクラ」も定期的に開催！'
        },
        {
          property: 'og:url',
          content: `${process.env.BASE_URL / this.$route.fullPath}`
        },
        {
          property: 'og:type',
          content: 'website',
        },
        {
          property: 'og:title',
          content: 'ヒナクラ | ⚡大17代の卒業祝いアニクラ',
        },
        {
          property: 'og:image',
          content: `${process.env.BASE_URL}/img/fliers/hnkr0.png`,
        },
        {
          property: 'og:description',
          content: '⚡大17代の卒業祝いアニクラとして2021/03/06に「ヒナクラ」を開催！また、ヒナクラ参加DJの練習としてDJの"タマゴ"向けオンラインアニクラ「タマクラ」も定期的に開催！',
        },
        {
          hid: 'twitter:card',
          name: 'twitter:card',
          content: 'summary_large_image'
        },
      ]
    }
  },
  mounted() {
    this.setVisitIn(this.$route.name);
    this.setBackgroundColor('#FAFAFA');
  },
  methods: {
    ...mapMutations({
      setBackgroundColor: 'setBackgroundColor',
      setVisitIn: 'setVisitIn'
    })
  }
}
</script>

<style lang="scss">
.index-flier {
  max-width: 800px;
  width: 100%;
  object-fit: contain;
}
</style>
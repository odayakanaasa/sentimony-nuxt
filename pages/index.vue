<template>
  <div class="home">

    <div class="hero">
      <div class="hero__wrapper">
        <div class="hero__title">{{ siteTitle }}</div>
        <div class="hero__description">{{ siteDescription }}</div>
      </div>
    </div>

    <SwiperReleaseList/>

    <div class="about">
      <div class="about__wrapper">
        <p><img class="about__logo" src="https://content.sentimony.com/assets/img/svg-icons/sentimony-records-logo.svg" alt="Sentimony Records Logo SVG"></p>
        <p>Sentimony Records is an independent record label started in Kyiv, Ukraine during the autumn 2006 by Ihor Orlovskyi also known as <router-link to="/artist/irukanji/">Irukanji</router-link>.</p>
        <p>{{ aboutDescription }}</p>
      </div>
    </div>

    <SwiperArtistList/>

  </div>
</template>

<script>
import SwiperReleaseList from '~/components/SwiperReleaseList.vue'
import SwiperArtistList from '~/components/SwiperArtistList.vue'

export default {
  components: {
    SwiperReleaseList,
    SwiperArtistList
  },
  data: () => ({
    siteTitle: 'Sentimony Records',
    siteDescription: 'Psychedelic Music Label',
    aboutDescription: "The main label's mission is to contribute the growth of the psychedelic chillout and trance scenes."
  }),
  head: {
    title: 'Home',
    meta: [
      { name: 'description', content: 'Home of Sentimony Records' },
      { property: 'og:image', content: 'https://content.sentimony.com/assets/img/og-images/sentimony/home.jpg' }
    ]
  }
}
</script>

<style lang="scss">
@import '../node_modules/coriolan-ui/tools/variables';
@import '../node_modules/coriolan-ui/mixins/media';

.hero {
  position: relative;
  background: linear-gradient(to bottom, transparent 0%, rgba(#000,.5) 100%);
  padding: 7.5em 0;

  @include media(S) {
    padding: 8.5em 0;
  }

  @include media(M) {
    padding: 9.5em 0;
  }

  @include media(L) {
    padding: 10.5em 0;
  }

  @include media(XL) {
    padding: 11.5em 0;
  }

  &__wrapper {
    max-width: 777px;
    margin: 0 auto;
    padding: 0 10px;
    box-sizing: border-box;
  }

  &__title {
    font-family: 'Julius Sans One', sans-serif;
    color: #fff;
    margin-bottom: .2em;
    font-weight: 400;
    font-size: 40px;
    letter-spacing: 2px;
    text-transform: uppercase;

    @include media(S) {
      font-size: 55px;
      letter-spacing: 5px;
    }

    @include media(M) {
      font-size: 70px;
      letter-spacing: 8px;
    }

    @include media(L) {
      font-size: 85px;
      letter-spacing: 11px;
    }

    @include media(XL) {
      font-size: 100px;
      letter-spacing: 14px;
    }
  }

  &__description {
    font-family: 'Julius Sans One', sans-serif;
    color: #fff;
    font-weight: 400;
    line-height: 2;
    font-size: 12px;
    letter-spacing: 4px;

    @include media(S) {
      font-size: 14px;
      letter-spacing: 8px;
    }

    @include media(M) {
      font-size: 16px;
      letter-spacing: 12px;
    }

    @include media(L) {
      font-size: 18px;
      letter-spacing: 16px;
    }

    @include media(XL) {
      font-size: 20px;
      letter-spacing: 20px;
    }
  }
}

.about {
  background-color: rgba(#000,.5);
  position: relative;

  &__logo {
    display: block;
    width: 60px;
    height: auto;
    margin: 0 auto;
  }

  &__wrapper {
    max-width: 460px;
    margin: 0 auto;
    padding: 5em 10px;
    box-sizing: border-box;

    p {

      a {
        color: #ff595e;

        &:hover {
          color: red;
        }
      }
    }
  }
}

// @import '../node_modules/coriolan-ui/tools/variables';
// @import '../node_modules/coriolan-ui/mixins/media';

// .home {
//   padding-top: 4em;

//   &__logo {
//     display: block;
//     max-width: 130px;
//     margin: 0 auto;
//     position: relative;
//   }

//   &__title {
//     margin: .2em 0;
//     text-transform: uppercase;
//     letter-spacing: 2px;
//     font-size: 2em;

//     @include media(M) {
//       letter-spacing: 3px;
//       font-size: 3em;
//     }
//   }

//   &__subtitle {
//     margin: .4em 0;
//     text-transform: uppercase;
//     letter-spacing: 4px;
//     font-size: .8em;

//     @include media(M) {
//       letter-spacing: 16px;
//       font-size: 1.2em;
//     }
//   }
// }
</style>

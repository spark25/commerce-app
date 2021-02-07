<template>
  <div class="section__home">
    <!-- top nav  -->
    <navbar />

    <!-- hero section  -->
    <section class="section__hero d_flex">
      <div class="hero_text flex_1 d_flex flex_column">
        <h1 class="hero_title montserrat font-bold">
          Anyone, anywhere can start an ecommerce website
        </h1>
        <p class="hero_subtitle">
          Commerce is a customizable, open-source eCommerce platform built on
          WordPress.<wbr /><br />
          Get started quickly and make your way.
        </p>
        <div class="d_flex align_center cta_group">
          <button class="btn btn__cta primary">
            <span class="btn_text"> Start a New Store </span>
          </button>
          <span class="hero_subtitle">Or</span>
          <button class="btn btn__cta text d_flex align_center">
            <span class="btn_text"> Customize &amp; Extend</span>
          </button>
        </div>
      </div>
      <!-- contains the hero preview image as background  -->
      <div class="hero_image flex_1"></div>
    </section>

    <!-- feature section  -->
    <section class="section__feature">
      <div class="section_title">
        Your eCommerce <br />
        made simple
      </div>
      <feature-cards />
    </section>

    <!-- more features section  -->
    <section class="section__moreinfo">
      <more-info />
    </section>

    <sector class="section__support">
      <div class="section_title">Supported by real people</div>
      <div class="section_subtitle">
        Our team of Engineers works remotely from 44 countries providing
        customer<wbr>support across multiple time zones.
      </div>
      <support />
    </sector>
  </div>
</template>

<script>
import FeatureCards from "../components/FeatureCards.vue";
import MoreInfo from "../components/MoreInfo.vue";
import Navbar from "../components/Navbar.vue";
import Support from "../components/Support.vue";

export default {
  name: "Home",
  components: {
    Navbar,
    FeatureCards,
    MoreInfo,
    Support,
  },

  data() {
    return {};
  },
};
</script>

<style lang="scss">
.section__home {
  background: linear-gradient(
    180deg,
    #e5efff 0%,
    rgba(229, 239, 255, 0.262661) 83.7%,
    rgba(229, 239, 255, 0) 100%
  );
  min-height: 400px;

  .section__hero {
    height: 830px;
    padding-top: 95px;
    .hero_text {
      padding-left: 220px;
      .hero_title {
        color: #272d4e;
        font-size: 85px;
        line-height: 95px;
        justify-self: end;
        margin-bottom: 30px;
        white-space: pre-line;
      }

      .hero_subtitle {
        font-family: Roboto;
        font-size: 18px;
        font-style: normal;
        font-weight: 400;
        line-height: 25px;
        letter-spacing: 0em;
        text-align: left;
        color: #94a2b3;
        white-space: pre-line;
      }

      .cta_group {
        margin-top: 30px;

        .primary {
          margin-right: 12px;
        }

        .light {
          margin-left: 12px;
        }

        .text {
          margin-left: 12px;
        }
      }
    }
    .hero_image {
      background-image: url("../assets/images/featured-image.svg");
      display: block;
      // height: 430px;
      background-size: contain;
      background-repeat: no-repeat;
      background-position: center center;
    }
  }

  .section__feature {
  }

  .section_title {
    font-family: "Montserrat", sans-serif;
    font-size: 48px;
    font-style: normal;
    font-weight: 700;
    line-height: 70px;
    letter-spacing: 0em;
    text-align: center;
    color: #272d4e;
    margin-bottom: 69px;
  }

  .section_subtitle {
    font-family: "Roboto";
    font-style: normal;
    font-weight: normal;
    font-size: 18px;
    line-height: 25px;
    text-align: center;
    color: #94a2b3;
    white-space: pre-wrap;
    margin: 0 auto;
    max-width: 660px;
  }

  .section__support {
    .section_title {
      margin-bottom: 35px;
    }
  }
}
.section__moreinfo {
  height: 1182px;
  background-image: url("../assets/images/curve_bg_w_text.svg");
  background-position: center;
  background-repeat: no-repeat;
  margin-top: 124px;
  display: grid;
  grid-template-columns:
    minmax(1rem, 220px)
    minmax(500px, 1480px)
    minmax(1rem, 220px);
}

.btn__cta {
  .btn_text {
    position: relative;
    &::after {
      content: "";
      opacity: 0;
      background-image: url("../assets/icons/arrow-right.svg");
      position: absolute;
      left: 100%;
      top: 50%;
      transform: translateY(-50%);
      height: 14px;
      width: 14px;
      background-size: contain;
      transition: all 0.25s ease;
      pointer-events: none;
    }
  }

  &.text {
    .btn_text {
      &::after {
        background-image: url("../assets/icons/arrow-right-blue.svg");
      }
    }
  }

  &:hover {
    .btn_text {
      &::after {
        opacity: 1;
        margin-left: 8px;
      }
    }
  }
}
</style>

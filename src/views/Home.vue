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

    <!-- testimonial section  -->
    <section class="section__testimonials">
      <div class="section_title">
        Trusted by Agencies<br />&amp; Store Owners
      </div>
      <testimonial />
    </section>

    <!-- support/people section  -->
    <section class="section__support">
      <div class="section_title">Supported by real people</div>
      <div class="section_subtitle">
        Our team of Engineers works remotely from 44 countries providing
        customer<wbr />support across multiple time zones.
      </div>
      <support />
    </section>
  </div>
</template>

<script>
import FeatureCards from "../components/FeatureCards.vue";
import MoreInfo from "../components/MoreInfo.vue";
import Navbar from "../components/Navbar.vue";
import Support from "../components/Support.vue";
import Testimonial from "../components/Testimonial.vue";

export default {
  name: "Home",
  components: {
    Navbar,
    FeatureCards,
    MoreInfo,
    Support,
    Testimonial,
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

    @include sm {
      height: 100vh;
      padding-top: 1rem;
      flex-direction: column;
    }
    .hero_text {
      padding-left: 220px;
      @include sm {
        padding: 1rem;
      }
      .hero_title {
        color: #272d4e;
        font-size: 85px;
        line-height: 95px;
        margin-bottom: 30px;
        // max-width: 80%;
        @include sm {
          font-size: 42px;
          line-height: 42px;
          margin-bottom: 1rem;
          // text-align: center;
        }
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
        @include sm {
          font-size: 16px;
          line-height: 18px;
          // text-align: center;
        }
      }

      .cta_group {
        margin-top: 30px;
        @include sm {
          margin-top: 2rem;
          flex-direction: column;
        }

        .primary {
          margin-right: 12px;
          @include sm {
            width: 100%;
            margin-right: 0px;
          }
        }

        .light {
          margin-left: 12px;
        }

        .text {
          margin-left: 12px;
          justify-content: center;
          @include sm {
            margin-bottom: 0.5rem;
          }
        }
        .hero_subtitle {
          padding: 0.5rem 0;
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
      @include sm {
        background-size: cover;
        background-position: top;
      }
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

    @include sm {
      font-size: 32px;
      line-height: 42px;
    }
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
    @include sm {
      margin-top: 6rem;
    }
    .section_title {
      margin-bottom: 35px;
    }
  }
}
.section__moreinfo {
  min-height: 1182px;
  background-image: url("../assets/images/curve_bg_w_text.svg");
  background-position: center;
  background-repeat: no-repeat;
  margin-top: 124px;
  display: grid;
  overflow-x: hidden;

  @include sm {
    min-height: max-content;
    grid-template-columns: 1fr !important;
  }
}

.section__testimonials {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 206px 0px;
  margin-bottom: 167px;
  background: linear-gradient(
    180deg,
    rgba(236, 240, 253, 0) 0%,
    rgba(236, 240, 253, 0.53) 14.32%,
    #ecf0fd 45.83%,
    rgba(236, 240, 253, 0.43) 84.33%,
    rgba(236, 240, 253, 0) 100%
  );

  @include sm {
    padding: 4rem 1rem;
    min-height: 100vh;
    margin-bottom: 0px;
  }
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

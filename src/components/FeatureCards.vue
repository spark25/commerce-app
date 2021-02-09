<template>
  <div class="feature_card_container container">
    <div class="vertical_card __wp hideMe">
      <div class="__image">
        <img src="../assets/images/feature1.svg" alt="" srcset="" />
      </div>
      <div class="__title">All You Need to Start</div>
      <div class="__desc">
        Add Commerce plugin to any WordPress site and set up a new store in
        minutes.
      </div>
      <div class="__actions">
        <button class="btn btn__cta text d_flex align_center">
          <span class="btn_text">Ecommerce for Wordpress</span>
        </button>
      </div>
      <span class="feature_image __apple-pay">
        <img src="../assets/images/apply_pay_feature.svg" alt="" />
      </span>
    </div>

    <div class="vertical_card __ext hideMe">
      <div class="__image">
        <slot name="image">
          <img src="../assets/images/feature2.svg" alt="" srcset="" />
        </slot>
      </div>
      <div class="__title">Customize and Extend</div>
      <div class="__desc">
        From subscriptions to gym classes to luxury cars, Commerce is fully
        customizable.
      </div>
      <div class="__actions">
        <button class="btn btn__cta text d_flex align_center">
          <span class="btn_text">Browse Extensions</span>
        </button>
      </div>

      <span class="feature_image __pay-sq">
        <img src="../assets/images/pay_sq.svg" alt="" />
      </span>
      <span class="feature_image __fb">
        <img src="../assets/images/fb.svg" alt="" />
      </span>
      <span class="feature_image __jetpack">
        <img src="../assets/images/jetpack.svg" alt="" />
      </span>

      <span class="feature_image __google-ads">
        <img src="../assets/images/ads.svg" alt="google ads" />
      </span>
      <span class="feature_image __mc">
        <img src="../assets/images/mail-chimp.svg" alt="google ads" />
      </span>
    </div>

    <div class="vertical_card __forum hideMe">
      <div class="__image">
        <slot name="image">
          <img src="../assets/images/feature3.svg" alt="" srcset="" />
        </slot>
      </div>
      <div class="__title">Active Community</div>
      <div class="__desc">
        Commerce is one of the fastest-growing eCommerce communities.
      </div>
      <div class="__actions">
        <button class="btn btn__cta text d_flex align_center">
          <span class="btn_text">Check our Forums</span>
        </button>
      </div>

      <span class="feature_image __collab1">
        <img src="../assets/images/collab1.svg" alt="google ads" />
      </span>
      <span class="feature_image __collab2">
        <img src="../assets/images/collab2.svg" alt="google ads" />
      </span>
      <span class="feature_image __collab3">
        <img src="../assets/images/collab3.svg" alt="google ads" />
      </span>
    </div>
  </div>
</template>

<script>
export default {
  components: {},
  data() {
    return {};
  },
};
</script>

<style lang="scss">
.feature_card_container {
  display: flex;
  justify-content: center;
  @include sl {
    display: grid;
    grid-template-columns: 1fr 1fr;
    justify-items: center;
    align-content: center;
    row-gap: 0;
  }
  @include lg {
    display: grid;
    grid-template-columns: 1fr 1fr;
    justify-items: center;
    align-content: center;
    row-gap: 0;
  }

  @include md {
    display: grid;
    grid-template-columns: 1fr;
    justify-items: center;
    align-content: center;
    row-gap: 4rem;
  }

  @include sm {
    display: grid;
    justify-items: center;
    align-content: center;
    row-gap: 4rem;
  }

  .vertical_card {
    display: flex;
    flex-direction: column;
    width: 430px;
    margin-right: 70px;
    margin-top: 74px;
    position: relative;

    &:first-child {
      margin-top: 0px;
    }
    &:last-child {
      margin-top: 148px;
      margin-right: 0;
    }

    @include sl {
      margin-right: 0;
    }
    @include lg {
      margin-right: 0;
    }
    @include sm {
      width: calc(100vw - 2rem);
      margin: 0 auto !important;
      margin-top: 74px !important;
    }

    .__image {
      width: 430px;
      height: 293px;
      box-shadow: 0px 18px 52.8537px rgba(215, 228, 249, 0.5);
      border-radius: 20px;
      margin-bottom: 40px;
      overflow: hidden;
      position: relative;
      @include sm {
        width: 350px;
        align-self: center;
      }

      img {
        width: 100%;
        height: 100%;
        object-fit: cover;
        transition: transform 0.25s ease;
        &:hover {
          transform: scale(1.1);
        }
      }
    }

    .__title {
      font-family: Montserrat;
      font-size: 36px;
      font-style: normal;
      font-weight: 500;
      line-height: 70px;
      letter-spacing: 0em;
      text-align: left;
      color: #272d4e;
      margin-bottom: 5px;

      @include sm {
        font-size: 28px;
        line-height: 36px;
        text-align: center;
      }
    }

    .__desc {
      font-family: Roboto;
      font-size: 18px;
      font-style: normal;
      font-weight: 400;
      line-height: 30px;
      letter-spacing: 0em;
      text-align: left;
      color: #94a2b3;
      margin-bottom: 25px;
      @include sm {
        font-size: 16px;
        line-height: 20px;
        text-align: center;
      }
    }

    .__actions {
      .btn__cta {
        @include sm {
          text-align: center;
          justify-content: center;
        }
      }
    }

    .feature_image {
      position: absolute;
      z-index: 9;
      display: block;
      img {
        width: 100%;
        height: 100%;
      }
    }
    &.__wp {
      .feature_image.__apple-pay {
        top: 0;
        left: -101px;

        @include sl {
          top: -20%;
          left: 0;
        }
        @include lg {
          top: -20%;
          left: 0;
        }
        @include md {
          top: -10%;
          left: -20%;
        }
        @include sm {
          width: 155px;
          height: 300px;
          top: 0;
          left: 0;
        }
      }
    }

    &.__ext {
      .feature_image {
        box-shadow: 0px 18px 52.8537px rgba(215, 228, 249, 0.5);
        border-radius: 10px;
      }
      .__pay-sq {
        width: 105px;
        height: 68.97px;
        left: 48px;
        top: -40px;
      }

      .__fb {
        width: 105px;
        height: 69.32px;
        left: 48px;
        top: 112px;
        @include sm {
          left: 0;
          top: 112px;
        }
      }

      .__jetpack {
        width: 105px;
        height: 69.32px;
        top: 134px;
        right: 96px;
        @include sm {
          right: 0;
          top: 112px;
        }
      }

      .__google-ads {
        width: 105px;
        height: 69.32px;
        top: 249px;
        left: 153px;
      }
      .__mc {
        width: 105px;
        height: 69.32px;
        top: 19px;
        right: 36px;
      }
    }

    &.__forum {
      .feature_image {
        box-shadow: 0px 18px 52.8537px rgba(215, 228, 249, 0.5);
        border-radius: 10px;
      }

      .__collab1 {
        width: 140px;
        height: 95px;
        left: 32px;
        top: -47.5px;
      }
      .__collab2 {
        width: 114px;
        height: 77px;
        right: 32px;
        top: -56px;
      }
      .__collab3 {
        width: 170px;
        height: 116px;
        left: 352px;
        top: 115px;
        @include sm {
          left: 0;
          top: 200px;
        }
      }

      @include sl {
        grid-column: 1/3;
      }
      @include lg {
        grid-column: 1/3;
      }
      @include md {
        grid-column: 1;
      }
    }
  }
}
</style>
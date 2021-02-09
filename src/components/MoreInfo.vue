<template>
  <div class="cards_container container">
    <div class="horizontal_card __develop hideMe">
      <div class="__image">
        <img src="../assets/images/develop_w_limits.svg" alt="" />
      </div>
      <div class="__content">
        <div class="__title">Develop<br />Without Limits</div>
        <div class="__desc">
          Commerce is developer friendly, too. Built with a REST API, Commerce
          is scalable and can integrate with virtually any service. Design a
          complex store from scratch, extend a store for a client, or simply add
          a single product to a WordPress site—your store, your way.
        </div>
        <div class="__cta">
          <button class="btn btn__cta success small d_flex place_center">
            <span class="btn_text">Read the Documentation</span>
          </button>
        </div>
      </div>

      <!-- elements  -->
      <div class="__matrix"></div>
      <div class="__ellipse __ellipse1 hideMe"></div>
      <div class="__ellipse __ellipse2 hideMe"></div>
    </div>

    <div class="horizontal_card __community hideMe">
      <div class="__image">
        <img src="../assets/images/our_community.svg" alt="" />
      </div>
      <div class="__content">
        <div class="__title">Know our<br />Global Community</div>
        <div class="__desc">
          Commerce is one of the fastest-growing eCommerce communities. We’re
          proud that the helpfulness of the community and a wealth of online
          resources are frequently cited as reasons our users love it. There are
          80+ meetups worldwide!
        </div>
        <div class="__cta">
          <button class="btn btn__cta success small d_flex place_center">
            <span class="btn_text">Read the Documentation</span>
          </button>
        </div>
      </div>

      <div class="__matrix"></div>
      <div class="__ellipse __ellipse1 hideMe"></div>
      <div class="__ellipse __ellipse2 hideMe"></div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss">
.cards_container {
  padding: 0px 126px;

  @include lg {
    padding: 0px;
  }
  @include sm {
    grid-column: 1 !important;
    padding: 0px;
  }

  .horizontal_card {
    display: flex;
    position: relative;

    @include md {
      flex-direction: column;
      justify-items: center;
      align-content: center;
      overflow: hidden;
    }

    @include sm {
      flex-direction: column;
      justify-items: center;
      align-content: center;
      overflow: hidden;
    }
    .__image {
      min-width: 430px;
      height: 548px;
      border-radius: 20px;
      position: relative;
      z-index: 9;
      @include sl {
        min-width: 430px;
        height: 548px;
        align-self: center;
      }
      @include lg {
        min-width: 430px;
        height: 548px;
        align-self: center;
      }
      @include md {
        min-width: 350px;
        height: 348px;
        align-self: center;
      }
      @include sm {
        min-width: 350px;
        height: 348px;
        align-self: center;
      }
      // overflow: hidden;
      img {
        height: 100%;
        width: 100%;
        object-fit: cover;
        @include sl {
          object-fit: contain;
        }
        @include lg {
          object-fit: contain;
        }
        @include md {
          object-fit: contain;
        }
        @include sm {
          object-fit: contain;
        }
      }

      &::after {
        position: absolute;
        width: 372px;
        height: 474px;
        top: 97px;
        left: 50%;
        transform: translateX(-50%);
        overflow: hidden;
        object-fit: contain;
        border-radius: 20px;
        z-index: -1;
        filter: blur(25px);
        @include sl {
          width: 200px;
          height: 310px;
          top: 20px;
          left: 50%;
        }
        @include lg {
          width: 200px;
          height: 310px;
          top: 20px;
          left: 50%;
        }
        @include md {
          width: 200px;
          height: 310px;
          top: 20px;
          left: 50%;
          filter: blur(16px);
        }
        @include sm {
          width: 200px;
          height: 310px;
          top: 20px;
          left: 50%;
          filter: blur(16px);
        }
      }
    }

    .__content {
      flex-direction: column;
      justify-content: center;
      padding: 120px 250px 70px 70px;
      position: relative;
      // padding-right: 250px;
      z-index: 5;

      @include sl {
        padding: 0;
        padding: 0 2rem;
        align-self: flex-end;
      }
      @include lg {
        padding: 0;
        padding: 0 2rem;
        align-self: flex-end;
      }

      @include md {
        padding: 0;
        padding: 0 1rem;
      }
      @include sm {
        padding: 0;
        padding: 0 1rem;
      }
    }

    .__title {
      font-family: "Montserrat";
      font-style: normal;
      font-weight: 500;
      font-size: 36px;
      line-height: 44px;
      color: #ffffff;
      margin-bottom: 17px;
      z-index: 9;

      @include lg {
        // text-align: center;
        // margin-top: 2rem;
      }
      @include md {
        font-size: 28px;
        line-height: 36px;
        text-align: center;
        margin-top: 2rem;
      }
      @include sm {
        font-size: 28px;
        line-height: 36px;
        text-align: center;
        margin-top: 2rem;
      }
    }

    .__desc {
      font-family: "Roboto";
      font-style: normal;
      font-weight: normal;
      font-size: 18px;
      line-height: 30px;
      color: #ffffff;
      margin-bottom: 39px;
      z-index: 9;

      @include lg {
        // text-align: center;
      }
      @include md {
        font-size: 16px;
        line-height: 20px;
        text-align: center;
      }
      @include sm {
        font-size: 16px;
        line-height: 20px;
        text-align: center;
      }
    }

    .__matrix,
    .__ellipse {
      position: absolute;
      background-size: contain;
      background-position: center;
      background-repeat: no-repeat;
      // z-index: -1;
    }
    &.__develop {
      margin-bottom: 55px;
      .__image {
        &::after {
          content: url("../assets/images/develop_after.svg");
        }
      }

      .__matrix {
        background-image: url("../assets/images/develop_mat.svg");
        width: 213.76px;
        height: 472.16px;
        left: -100px;
        top: 417px;

        @include sl {
          transform: scale(0.8);
          opacity: 0.7;
          top: -100px;
          right: 20px;
          z-index: -1;
        }
        @include lg {
          transform: scale(0.8);
          left: unset;
          top: -100px;
          right: 20px;
          z-index: -1;
        }
        @include md {
          transform: scale(0.8);
          left: unset;
          top: 0;
          right: 0;
          z-index: -1;
        }
        @include sm {
          transform: scale(0.8);
          left: unset;
          top: 0;
          right: 0;
          z-index: -1;
        }
      }

      .__ellipse1 {
        background-image: url("../assets/images/EllipseXl.svg");
        width: 401px;
        height: 401px;
        left: -108px;
        top: 213px;
        @include md {
          left: -108px;
          top: 0;
          // z-index: -1;
        }
        @include sm {
          left: -108px;
          top: 0;
          // z-index: -1;
        }
      }
      .__ellipse2 {
        background-image: url("../assets/images/Ellipse36.svg");
        width: 65px;
        height: 65px;
        left: -128px;
        top: 127px;
      }
    }

    &.__community {
      flex-direction: row-reverse;

      @include md {
        flex-direction: column-reverse;

        .__image {
          margin-top: 2rem;
          padding-bottom: 2rem;
        }
      }
      @include sm {
        flex-direction: column-reverse;

        .__image {
          margin-top: 2rem;
          padding-bottom: 2rem;
        }
      }
      .__content {
        padding: 70px 70px 120px 250px;
        @include sl {
          padding: 0;
          padding: 0 2rem;
          align-self: unset;

          .__title {
            margin-top: 0;
          }
        }
        @include lg {
          padding: 0;
          padding: 0 2rem;
          align-self: unset;

          .__title {
            margin-top: 0;
          }
        }
        @include md {
          padding: 0;
          padding: 0 1rem;

          .__title {
            margin-top: 0;
          }
        }
        @include sm {
          padding: 0;
          padding: 0 1rem;

          .__title {
            margin-top: 0;
          }
        }
      }

      .__image {
        box-shadow: none;
        &::after {
          content: url("../assets/images/community_after.svg");
        }
      }

      .__matrix {
        background-image: url("../assets/images/develop_mat.svg");
        width: 213.76px;
        height: 472.16px;
        right: -50px;
        bottom: 0px;
        transform-origin: center;
        @include sl {
          opacity: 0.8;
          transform: scale(0.8);
          right: 300px;
          bottom: -100px;
        }
        @include lg {
          opacity: 0.8;
          transform: scale(0.8);
          right: 300px;
          bottom: -100px;
        }
        @include md {
          right: 0;
          bottom: 0px;
          transform: scale(0.8);
        }
        @include sm {
          right: 0;
          bottom: 0px;
          transform: scale(0.8);
        }
      }

      .__ellipse1 {
        background-image: url("../assets/images/EllipseXl.svg");
        width: 262px;
        height: 262px;
        right: -129px;
        bottom: 312px;

        @include sl {
          right: 500px;
          top: 312px;
        }
        @include lg {
          right: 500px;
          top: 312px;
        }
        @include md {
          right: 300px;
          top: 312px;
        }
        @include sm {
          right: 300px;
          top: 312px;
        }
      }
      .__ellipse2 {
        background-image: url("../assets/images/Ellipse36.svg");
        width: 65px;
        height: 65px;
        right: 273px;
        bottom: 531px;
        z-index: 9;
        @include md {
          left: 0;
          top: 0;
        }
        @include sm {
          left: 0;
          top: 0;
        }
      }
    }
  }
}
</style>
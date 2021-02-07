<template>
  <div class="cards_container">
    <div class="horizontal_card __develop">
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
          <button class="btn btn__cta success small d_flex align_center">
            <span class="btn_text">Read the Documentation</span>
          </button>
        </div>
      </div>

      <!-- elements  -->
      <div class="__matrix"></div>
      <div class="__ellipse __ellipse1"></div>
      <div class="__ellipse __ellipse2"></div>
    </div>
    <div class="horizontal_card __community">
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
          <button class="btn btn__cta success small d_flex align_center">
            <span class="btn_text">Read the Documentation</span>
          </button>
        </div>
      </div>

      <div class="__matrix"></div>
      <div class="__ellipse __ellipse1"></div>
      <div class="__ellipse __ellipse2"></div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss">
.cards_container {
  grid-column: 2 / 3;
  padding: 0px 126px;
  //   background: #bada55;
  //   display: grid;

  .horizontal_card {
    display: flex;
    position: relative;
    .__image {
      min-width: 430px;
      height: 548px;
      box-shadow: -25px 20px 44px rgba(84, 48, 209, 0.4);
      box-shadow: -25px 20px 44px 0px #5430d1 40%;
      border-radius: 20px;
      position: relative;
      z-index: 9;
      // overflow: hidden;
      img {
        height: 100%;
        width: 100%;
        object-fit: cover;
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
      }
    }

    .__content {
      flex-direction: column;
      justify-content: center;
      padding: 120px 250px 70px 70px;
      // padding-right: 250px;
    }

    .__title {
      font-family: "Montserrat";
      font-style: normal;
      font-weight: 500;
      font-size: 36px;
      line-height: 44px;
      color: #ffffff;
      margin-bottom: 17px;
    }

    .__desc {
      font-family: "Roboto";
      font-style: normal;
      font-weight: normal;
      font-size: 18px;
      line-height: 30px;
      /* or 167% */

      color: #ffffff;
      margin-bottom: 39px;
    }

    .__matrix,
    .__ellipse {
      position: absolute;
      background-size: contain;
      background-position: center;
      background-repeat: no-repeat;
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
      }

      .__ellipse1 {
        background-image: url("../assets/images/EllipseXl.svg");
        width: 401px;
        height: 401px;
        left: -108px;
        top: 213px;
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
      .__content {
        padding: 70px 70px 120px 250px;
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
        transform: rotate(90deg);
        transform-origin: center;
      }

      .__ellipse1 {
        background-image: url("../assets/images/EllipseXl.svg");
        width: 262px;
        height: 262px;
        right: -129px;
        bottom: 312px;
      }
      .__ellipse2 {
        background-image: url("../assets/images/Ellipse36.svg");
        width: 65px;
        height: 65px;
        right: 273px;
        bottom: 531px;
        z-index: 9;
      }
    }
  }
}
</style>
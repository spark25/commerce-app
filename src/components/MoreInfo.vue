<template>
  <div class="cards_container">
    <div class="horizontal_card __develop">
      <div class="__image">
        <img src="../assets/images/develop_w_limits.svg" alt="" />
      </div>
      <div class="__content">
        <div class="__title">Develop Without Limits</div>
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
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss">
.cards_container {
  grid-column: 2 / 3;
  //   background: #bada55;
//   display: grid;

  .horizontal_card {
      display: flex;
    .__image {
      width: 430px;
      height: 548px;
      box-shadow: -25px 20px 44px rgba(84, 48, 209, 0.4);
      box-shadow: -25px 20px 44px 0px #5430d1 40%;
    //   flex:1;

      border-radius: 20px;
      position: relative;
      z-index: 9;
      overflow: hidden;
      img {
        height: 100%;
        width: 100%;
        object-fit: cover;
      }
    }

    .__content{
        flex: 1;
        display: flex;
        flex-direction: column;
        // align-items: center;
        justify-content: center;
        padding:70px
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
      font-family: 'Roboto';
      font-style: normal;
      font-weight: normal;
      font-size: 18px;
      line-height: 30px;
      /* or 167% */

      color: #ffffff;
      margin-bottom: 39px;
    }

    &.__develop {
      .__image {
        &::after {
          content: url("../assets/images/develop_after.svg");
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
          filter: blur(50px);
        }
      }
    }
  }
}
</style>
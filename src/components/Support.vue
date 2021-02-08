<template>
  <div class="support">
    <div class="support_image d_flex align_center justify_center">
      <img src="../assets/images/support_people.svg" alt="" />
    </div>
    <div class="__message d_flex align_center">
      <div class="__msg">
        Commerce - the most customizable eCommerce<br />
        platform for building your online business.
      </div>
      <button class="btn btn__cta light">
        <span class="btn_text">GET STARTED</span>
      </button>

      <!-- Elements  -->
      <div class="_ellipse _ellipse__1"></div>
      <div class="_ellipse _ellipse__2"></div>
      <div class="_ellipse _ellipse__3"></div>
      <div class="_ellipse _ellipse__4"></div>

      <!-- matrix dots  -->
      <div class="_matrix _matrix__right"></div>
      <div class="_matrix _matrix__left"></div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss">
.support{
  @include sm{
    margin-top: 4rem;
  }
}
.support_image {
  background-image: url("../assets/images/white_ellipse.svg");
  background-repeat: no-repeat;
  background-position: top -110% right 50%;
  // background-size: cover;
  margin-top: 16px;
  // padding: 0px 304px;
  z-index: 9;

  img {
    object-fit: contain;
    width: 100%;
    max-width: 1311px;
    min-width: 300px;
  }
}
.__message {
  padding: 75px 345px;
  justify-content: space-around;
  position: relative;
  @include sm {
    padding: 75px 2rem;
    display: grid !important;
    row-gap: 2rem;
    place-items: center;
  }

  .__msg {
    font-family: "Roboto";
    font-style: normal;
    font-weight: normal;
    font-size: 36px;
    line-height: 52px;
    color: #ffffff;

    @include sm {
      font-size: 22px;
      line-height: 32px;
      text-align: center;
    }
  }

  background: #5f37ef;

  ._ellipse,
  ._matrix {
    position: absolute;
    background-size: contain;
    background-position: center;
    background-repeat: no-repeat;
    img {
      width: 100%;
      height: 100%;
      object-fit: contain;
    }
  }

  ._ellipse__1 {
    background-image: url("../assets/images/Ellipse.svg");
    width: 89px;
    height: 88px;
    right: 144px;
    top: 194px;
    @include sm {
      right: 1rem;
      top: 90%;
    }
  }
  ._ellipse__2 {
    background-image: url("../assets/images/Ellipse-sm.svg");
    width: 34px;
    height: 34px;
    left: 194px;
    top: -62px;
    @include sm {
      left: 50%;
      top: 0;
    }
  }

  ._ellipse__3 {
    background-image: url("../assets/images/Ellipse36.svg");
    width: 61.18px;
    height: 61.18px;
    left: 100px;
    top: -148px;
    @include sm {
      left: 50%;
      bottom: 100%;
    }
  }
  ._ellipse__4 {
    background-image: url("../assets/images/Ellipse34.svg");
    width: 43px;
    height: 43px;
    right: 263px;
    top: -215px;
    @include sm {
      left: 10px;
      top: -90%;
    }
  }
  ._matrix {
    z-index: -1;
  }
  ._matrix__right {
    background-image: url("../assets/images/red-dots.svg");
    width: 473px;
    height: 214px;
    right: 144px;
    bottom: 195px;
    @include sm {
      right: -100px;
      top: 30px;
      z-index: -1;
      transform: rotate(90deg) scale(0.8);
    }
  }

  ._matrix__left {
    background-image: url("../assets/images/green-dots.svg");
    height: 162.08px;
    width: 265.44px;
    left: 83px;
    bottom: 137px;
    @include sm {
      left: -50px;
      top: -70px;
      z-index: -1;
      transform: rotate(90deg) scale(0.8);
    }
  }
}
</style>
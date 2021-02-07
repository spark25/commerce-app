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
      <button class="btn btn__cta light">GET STARTED</button>

      <!-- Elements  -->
      <div class="_ellipse _ellipse__1">
        <!-- <img src="../assets/images/Ellipse.svg" alt="" /> -->
      </div>
      <div class="_ellipse _ellipse__2">
        <!-- <img src="../assets/images/Ellipse.svg" alt="" /> -->
      </div>
      <div class="_ellipse _ellipse__3">
        <!-- <img src="../assets/images/Ellipse.svg" alt="" /> -->
      </div>
      <div class="_ellipse _ellipse__4">
        <!-- <img src="../assets/images/Ellipse.svg" alt="" /> -->
      </div>

      <!-- matrix dots  -->
      <div class="_matrix _matrix__right">
        <!-- <img src="../assets/images/Ellipse.svg" alt="" /> -->
      </div>
      <div class="_matrix _matrix__left">
        <!-- <img src="../assets/images/Ellipse.svg" alt="" /> -->
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss">
.support_image {
  background-image: url("../assets/images/white_ellipse.svg");
  background-repeat: no-repeat;
  background-position: top -110% right 50%;
  // background-size: cover;
  margin-top: 16px;
  // padding: 0px 304px;

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

  .__msg {
    font-family: "Roboto";
    font-style: normal;
    font-weight: normal;
    font-size: 36px;
    line-height: 52px;
    color: #ffffff;
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
  }
  ._ellipse__2 {
    background-image: url("../assets/images/Ellipse-sm.svg");
    width: 34px;
    height: 34px;
    left: 194px;
    top: -62px;
  }

  ._ellipse__3 {
    background-image: url("../assets/images/Ellipse36.svg");
    width: 61.18px;
    height: 61.18px;
    left: 100px;
    top: -148px;
  }
  ._ellipse__4 {
    background-image: url("../assets/images/Ellipse34.svg");
    width: 43px;
    height: 43px;
    right: 263px;
    top: -215px;
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
  }

  ._matrix__left {
    background-image: url("../assets/images/green-dots.svg");
    height: 162.08px;
    width: 265.44px;
    left: 83px;
    bottom: 137px;
  }
}
</style>
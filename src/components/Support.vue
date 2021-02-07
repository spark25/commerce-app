<template>
  <div class="support">
    <div class="support_image d_flex align_center justify_center">
      <img src="../assets/images/support_people.svg" alt="" />
    </div>
    <div class="__message d_flex align_center">
      <div class="__msg">
        Commerce - the most customizable eCommerce<br> platform for building your
        online business.
      </div>
      <button class="btn btn__cta light">GET STARTED</button>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss">

.support_image{
    background-image: url('../assets/images/white_ellipse.svg');
    background-repeat: no-repeat;
    background-position: top -110% right 50%;
    // background-size: cover;
    margin-top: 16px;
    // padding: 0px 304px;

    img{
        object-fit: contain;
        width: 100%;
        max-width: 1311px;
        min-width: 300px;
    }
}
.__message {
    padding: 75px 345px;
    justify-content: space-around;
  .__msg {
    font-family: 'Roboto';
    font-style: normal;
    font-weight: normal;
    font-size: 36px;
    line-height: 52px;
    color: #ffffff;
  }
  background: #5f37ef;
}
</style>
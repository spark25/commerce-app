<template>
  <div class="testimonial__container container">
    <slider :slides="testimonials">
      <!-- slides go here  -->
    </slider>

    <!-- elements  -->
    <!-- people  -->
    <div class="_people _people-1">
      <img src="../assets/images/t_dp1.svg" alt="" />
    </div>
    <div class="_people _people-2">
      <img src="../assets/images/t_dp2.svg" alt="" />
    </div>
    <div class="_people _people-3">
      <img src="../assets/images/t_dp3.svg" alt="" />
    </div>
    <div class="_people _people-4">
      <img src="../assets/images/t_dp4.svg" alt="" />
    </div>
    <div class="_people _people-5">
      <img src="../assets/images/t_dp5.svg" alt="" />
    </div>
    <div class="_people _people-6">
      <img src="../assets/images/t_dp6.svg" alt="" />
    </div>
  </div>
</template>

<script>
import Slider from "./common/Slider.vue";
export default {
  components: {
    Slider,
  },

  data() {
    return {
      testimonials: [
        {
          text:
            "No other eCommerce platform allows people to start for free and grow their store as their business grows. More importantly, Commerce doesn't charge you a portion of your profits as your business grows!",
        },
        {
          text:
            "Watch your thoughts; they become words. Watch your words; they become actions. Watch your actions; they become habits. Watch your habits; they become character. Watch your character; it becomes your destiny.",
        },
        {
          text:
            "If you’re not stubborn, you’ll give up on experiments too soon. And if you’re not flexible, you’ll pound your head against the wall and you won’t see a different solution to a problem you’re trying to solve.",
        },
      ],
    };
  },
};
</script>

<style lang="scss">
.testimonial__container {
  display: flex;
  // flex-direction: column;
  align-items: center;
  justify-content: center;
  position: relative;

  @include md {
    padding-top: 6rem;
  }
  @include sm {
    padding-top: 6rem;
  }

  ._people {
    position: absolute;
    z-index: 9;
    display: block;

    @include sm {
      // position: relative;
    }
    img {
      width: 100%;
      height: 100%;
    }

    &::after {
      position: absolute;
      top: 10px;
      left: 0;
      filter: blur(16px);
      z-index: -1;
    }

    &._people-1 {
      width: 155px;
      height: 155px;
      top: -173px;
      left: -214px;
      &::after {
        position: absolute;
        content: url("../assets/images/t_dp1.svg");
        width: 130px;
        height: 130px;
        top: 10px;
        left: 0;
        filter: blur(16px);
        z-index: -1;
      }

      @include lg {
        transform: scale(0.8);
        top: -200px;
        left: -100px;
        z-index: 0;
      }
      @include md {
        transform: scale(0.5);
        top: -40px;
        left: 0;
        z-index: 0;
      }
      @include sm {
        transform: scale(0.5);
        top: -40px;
        left: 0;
        z-index: 0;
      }
    }
    &._people-2 {
      width: 105px;
      height: 105px;
      top: 105px;
      left: -370px;
      &::after {
        position: absolute;
        content: url("../assets/images/t_dp2.svg");
        width: 90px;
        height: 90px;
        top: 10px;
        left: 0;
        filter: blur(16px);
        z-index: -1;
      }

      @include lg {
        transform: translateY(-50%) scale(0.6);
        top: 50%;
        left: -100px;
        z-index: 0;
      }

      @include md {
        transform: translateX(-50%) scale(0.6);
        top: -75px;
        left: 50%;
        z-index: 0;
      }
      @include sm {
        transform: translateX(-50%) scale(0.6);
        top: -75px;
        left: 50%;
        z-index: 0;
      }
    }
    &._people-3 {
      width: 105px;
      height: 105px;
      top: 311px;
      left: -334px;
      &::after {
        position: absolute;
        content: url("../assets/images/t_dp3.svg");
        width: 97px;
        height: 97px;
        top: 10px;
        left: 0;
        filter: blur(16px);
        z-index: -1;
      }

      @include lg {
        transform: scale(0.8);
        top: 100%;
        left: -100px;
        z-index: 0;
      }
      @include md {
        transform: scale(0.8);
        top: -10px;
        left: unset;
        bottom: unset;
        right: 0;
        z-index: 0;
      }
      @include sm {
        transform: scale(0.8);
        top: -10px;
        left: unset;
        bottom: unset;
        right: 0;
        z-index: 0;
      }
    }
    &._people-4 {
      width: 95px;
      height: 95px;
      top: -172px;
      right: -148px;
      &::after {
        position: absolute;
        content: url("../assets/images/t_dp4.svg");
        width: 70px;
        height: 70px;
        top: 10px;
        left: 0;
        filter: blur(16px);
        z-index: -1;
      }

      @include lg {
        // transform: scale(0.8);
        top: -150px;
        left: 100%;
        z-index: 0;
      }
      @include md {
        // transform: scale(0.8);
        top: unset;
        left: unset;
        bottom: -80%;
        right: 20px;
        z-index: 0;
      }
      @include sm {
        // transform: scale(0.8);
        top: unset;
        left: unset;
        bottom: -80%;
        right: 20px;
        z-index: 0;
      }
    }
    &._people-5 {
      width: 155px;
      height: 155px;
      top: 49px;
      right: -334px;
      &::after {
        position: absolute;
        content: url("../assets/images/t_dp5.svg");
        width: 140px;
        height: 140px;
        top: 10px;
        left: 0;
        filter: blur(16px);
        z-index: -1;
      }

      @include lg {
        transform: translateX(-50%) scale(0.8);
        top: 120%;
        bottom: -100%;
        left: 50%;
        z-index: 0;
      }

      @include md {
        transform: translateX(50%) scale(0.5);
        top: unset;
        left: unset;
        bottom: -100%;
        right: 50%;
        z-index: 0;
      }
      @include sm {
        transform: translateX(50%) scale(0.5);
        top: unset;
        left: unset;
        bottom: -100%;
        right: 50%;
        z-index: 0;
      }
    }
    &._people-6 {
      width: 105px;
      height: 105px;
      top: 100%;
      right: -206px;
      &::after {
        content: url("../assets/images/t_dp6.svg");
      }

      @include lg {
        transform: scale(0.8);
        top: 50%;
        right: -120px;
        left: unset;
        bottom: unset;
        z-index: 0;
      }
      @include md {
        transform: scale(0.5);
        top: unset;
        right: unset;
        bottom: -80%;
        left: 20px;
        z-index: 0;
      }
      @include sm {
        transform: scale(0.5);
        top: unset;
        bottom: -80%;
        right: unset;
        left: 20px;
        z-index: 0;
      }
    }
  }
}
</style>
<template>
  <div class="carousel">
    <div class="carousel__track">
      <!-- Active slides  -->
      <div class="carousel__slide __active-slide" :key="'first'">
        {{ activeSlide.length > 0 ? activeSlide[0].text : "" }}
      </div>

      <!-- Next slides  -->
      <div
        class="carousel__slide __next-slide"
        :class="`__next-slide--` + i"
        v-for="(slide, i) in nextQueue"
        :key="i"
      >
        {{ slide.text }}
      </div>
    </div>

    <!-- slide controls  -->
    <button
      :disabled="nextQueue.length <= 0"
      class="icon carousel__btn __up"
      @click="carouselSlideUp"
    >
      <svg
        width="25"
        height="52"
        viewBox="0 0 25 52"
        fill="none"
        xmlns="http://www.w3.org/2000/svg"
      >
        <path
          fill-rule="evenodd"
          clip-rule="evenodd"
          d="M0.136329 13.1847C0.226332 13.4016 0.358243 13.5987 0.524504 13.7645C0.690345 13.9308 0.887358 14.0627 1.10426 14.1527C1.32116 14.2427 1.55368 14.289 1.78851 14.289C2.02335 14.289 2.25587 14.2427 2.47277 14.1527C2.68967 14.0627 2.88668 13.9308 3.05253 13.7645L10.7151 6.099L10.7151 49.9439C10.7151 50.4174 10.9032 50.8715 11.238 51.2063C11.5728 51.5412 12.0269 51.7292 12.5004 51.7292C12.9739 51.7292 13.4281 51.5412 13.7629 51.2063C14.0977 50.8715 14.2858 50.4174 14.2858 49.9439L14.2858 6.09896L21.9484 13.7645C22.2836 14.0997 22.7383 14.2881 23.2124 14.2881C23.6865 14.2881 24.1412 14.0997 24.4764 13.7645C24.8117 13.4293 25 12.9746 25 12.5005C25 12.0264 24.8117 11.5717 24.4764 11.2365L13.7645 0.52452C13.5986 0.358261 13.4016 0.226352 13.1847 0.136348C12.9678 0.0463442 12.7353 1.47021e-05 12.5005 1.47124e-05C12.2656 1.47226e-05 12.0331 0.0463442 11.8162 0.136348C11.5993 0.226352 11.4023 0.358261 11.2365 0.52452L0.524504 11.2365C0.358243 11.4023 0.226332 11.5993 0.136329 11.8162C0.0463252 12.0331 -1.72501e-06 12.2657 -1.71474e-06 12.5005C-1.70448e-06 12.7353 0.0463253 12.9678 0.136329 13.1847Z"
          fill="black"
        />
      </svg>
    </button>
    <button
      :disabled="previousQueue.length <= 0"
      class="icon carousel__btn __down"
      @click="carouselSlideDown"
    >
      <svg
        width="25"
        height="52"
        viewBox="0 0 17 32"
        fill="none"
        xmlns="http://www.w3.org/2000/svg"
      >
        <path
          fill-rule="evenodd"
          clip-rule="evenodd"
          d="M0.916143 23.6424C0.97135 23.5093 1.05226 23.3885 1.15424 23.2867C1.25597 23.1848 1.37681 23.1039 1.50985 23.0486C1.64289 22.9934 1.78552 22.965 1.92956 22.965C2.0736 22.965 2.21623 22.9934 2.34927 23.0486C2.48232 23.1039 2.60316 23.1848 2.70488 23.2867L7.40496 27.9886L7.40496 1.09484C7.40496 0.804406 7.52033 0.525867 7.7257 0.320499C7.93107 0.115131 8.20961 -0.000244463 8.50004 -0.000244476C8.79048 -0.000244488 9.06902 0.115131 9.27438 0.320499C9.47975 0.525867 9.59513 0.804406 9.59513 1.09484L9.59513 27.9887L14.2953 23.2867C14.5009 23.0811 14.7798 22.9656 15.0706 22.9656C15.3614 22.9656 15.6403 23.0811 15.8459 23.2867C16.0515 23.4924 16.1671 23.7713 16.1671 24.0621C16.1671 24.3529 16.0515 24.6318 15.8459 24.8374L9.2754 31.4079C9.17367 31.5099 9.05283 31.5908 8.91979 31.646C8.78674 31.7012 8.64412 31.7296 8.50008 31.7296C8.35603 31.7296 8.21341 31.7012 8.08037 31.646C7.94732 31.5908 7.82648 31.5099 7.72476 31.4079L1.15424 24.8374C1.05226 24.7357 0.97135 24.6148 0.916143 24.4818C0.860937 24.3487 0.832521 24.2061 0.832521 24.0621C0.832521 23.918 0.860937 23.7754 0.916143 23.6424Z"
          fill="black"
        />
      </svg>
    </button>
    <!-- elements  -->
    <!-- matrix dots  -->
    <div class="_matrix _matrix__right"></div>
    <div class="_matrix _matrix__left"></div>
  </div>
</template>

<script>
export default {
  props: ["slides"],

  data() {
    return {
      previousQueue: [],
      activeSlide: [],
      nextQueue: [],
    };
  },

  methods: {
    carouselSlideUp() {
      let currActiveSlide = this.activeSlide[0];
      let nextInQueue = this.nextQueue[0];
      this.activeSlide = [nextInQueue];
      this.nextQueue = this.nextQueue.slice(1, this.nextQueue.length);
      this.previousQueue.push(currActiveSlide);
    },
    carouselSlideDown() {
      let activeSlide = this.activeSlide[0];
      let prevInQueue = this.previousQueue[this.previousQueue.length - 1];
      this.previousQueue.pop();
      this.activeSlide = [prevInQueue];
      this.nextQueue.unshift(activeSlide);
    },
  },

  mounted() {},
  created() {
    if (this.slides.length > 0) {
      this.activeSlide.push(this.slides[0]);
      this.nextQueue = this.slides.slice(1, this.slides.length);
    }
  },
};
</script>

<style lang="scss">
.carousel {
  position: relative;
  .carousel__track {
    @include md {
      display: flex;
      align-items: center;
      justify-content: center;
    }
    @include sm {
      display: flex;
      align-items: center;
      justify-content: center;
    }
    .carousel__slide {
      border-radius: 20px;
      font-family: "Montserrat";
      font-style: normal;
      font-weight: 500;
      font-size: 26.7px;
      line-height: 39px;
      text-align: center;
      color: #94a2b3;
      background: #ffffff;
      width: 730px;
      height: 391px;
      transition: all 0.5s ease;
      @include md {
        width: calc(100vw - 4rem);
        height: 239px;
        font-size: 18px;
        line-height: 20px;
      }
      @include sm {
        width: calc(100vw - 4rem);
        height: 239px;
        font-size: 18px;
        line-height: 20px;
      }
      &.__active-slide {
        top: 0;
        // left: 0;
        width: 730px;
        height: 391px;
        position: relative;
        background-image: url("../../assets/icons/quotes.svg");
        background-repeat: no-repeat;
        background-position: top 28px center;
        box-shadow: 0px 18px 52.8537px rgba(215, 228, 249, 0.5);
        padding: 105px 82px 50px 82px;
        z-index: 9;
        @include md {
          width: calc(100vw - 4rem);
          height: 280px;
          padding: 2rem 1rem 1rem 1rem;
          display: flex;
          align-items: center;
          justify-content: center;
        }
        @include sm {
          width: calc(100vw - 4rem);
          height: 239px;
          padding: 2rem 1rem 1rem 1rem;
          display: flex;
          align-items: center;
          justify-content: center;
        }
      }

      &.__next-slide {
        position: absolute;
      }

      &.__next-slide.__next-slide--0 {
        z-index: 5;
        top: 36px;
        transform: scale(0.95);
        box-shadow: 0px 18px 52.8537px rgba(215, 228, 249, 0.5);
        // background: red;
        @include md {
          top: 75px;
        }
        @include sm {
          top: 36px;
        }
      }
      &.__next-slide.__next-slide--1 {
        z-index: 1;
        top: 76px;
        transform: scale(0.85);
        box-shadow: 0px 18px 52.8537px rgba(215, 228, 249, 0.5);
        @include md {
          top: 115px;
        }
        @include sm {
          top: 76px;
        }
      }
    }
  }

  .carousel__btn {
    position: absolute;
    right: -59px;
    transform: scale(1);
    transition: all 0.2s ease;
    z-index: 9;
    svg {
      path {
        fill: black;
      }
    }
    &:disabled {
      transform: scale(0.5);
      cursor: not-allowed;
      svg {
        path {
          fill: #888;
        }
      }
    }

    &:active {
      transform: scale(0.9);
    }
    &.__up {
      top: 357px;
      @include md {
        top: 150%;
        right: 50%;
      }
      @include sm {
        top: 150%;
        right: 50%;
      }
    }
    &.__down {
      top: 437px;
      @include md {
        top: 150%;
        left: 50%;
      }
      @include sm {
        top: 150%;
        left: 50%;
      }
    }
  }

  //   elements
  ._matrix {
    position: absolute;
    background-size: contain;
    background-position: center;
    background-repeat: no-repeat;

    &._matrix__right {
      background-image: url("../../assets/images/red-dots.svg");
      width: 473px;
      height: 214px;
      left: 385px;
      top: 0;
      @include sl {
        left: 0;
        top: -80px;
        transform: rotate(90deg) scale(0.5);
        opacity: 0.5;
      }
      @include lg {
        left: 0;
        top: -80px;
        transform: rotate(90deg) scale(0.5);
        opacity: 0.5;
      }
      @include md {
        left: 0;
        top: -80px;
        transform: rotate(90deg) scale(0.5);
        opacity: 0.5;
      }
      @include sm {
        left: 0;
        top: -80px;
        transform: rotate(90deg) scale(0.5);
        opacity: 0.5;
      }
    }

    &._matrix__left {
      background-image: url("../../assets/images/green-dots-lg.svg");
      width: 473px;
      height: 214px;
      right: 380px;
      top: 307px;
      @include md {
        background-image: url("../../assets/images/green-dots.svg");
        transform: rotate(90deg) scale(0.5);
        right: 50%;
        top: 100%;
        opacity: 0.5;
      }
      @include sm {
        background-image: url("../../assets/images/green-dots.svg");
        transform: rotate(90deg) scale(0.5);
        right: 50%;
        top: 100%;
        opacity: 0.5;
      }
    }
  }
}

.list-item {
  display: inline-block;
  margin-right: 10px;
}
.list-enter-active,
.list-leave-active {
  transition: all 1s ease;
}
.list-enter-from,
.list-leave-to {
  opacity: 0;
  transform: translateY(30px);
}
</style>
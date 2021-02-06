<template>
  <div class="vertical_card">
    <div class="__image">
      <slot name="image"></slot>
      <!-- <img :src="require(image)" alt="" > -->
    </div>
    <div class="__title">
      <slot name="title"></slot>
    </div>
    <div class="__desc">
      <slot name="desc"></slot>
    </div>
    <div class="__actions">
      <slot name="cta"></slot>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss">
.vertical_card {
  display: flex;
  flex-direction: column;
  width: 430px;
  margin-right: 70px;
  margin-top: 74px;

  &:first-child {
    margin-top: 0px;
  }
  &:last-child {
    margin-top: 148px;
    margin-right: 0;
  }

  .__image {
    width: 430px;
    height: 293px;
    box-shadow: 0px 18px 52.8537px rgba(215, 228, 249, 0.5);
    border-radius: 20px;
    margin-bottom: 40px;
    overflow: hidden;

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
  }

  .__actions {
  }
}
</style>
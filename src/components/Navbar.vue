<template>
  <header class="header">
    <div class="brand">
      <img src="../assets/icons/LOGO.svg" alt="commerce logo" />
    </div>
    <nav class="navbar">
      <ul class="navbar-nav">
        <li class="nav-item">Sell</li>
        <li class="nav-item">Marketplace</li>
        <li class="nav-item">Community</li>
        <li class="nav-item">Develop</li>
        <li class="nav-item">Resources</li>
        <li class="nav-item">Login</li>
      </ul>
    </nav>
    <div class="cta_group d_flex align_center">
        <button class="btn primary">Get Started</button>
        <button class="icon">
            <img src="../assets/icons/icon-search.svg" alt="search icon">
        </button>
    </div>
  </header>
</template>

<script>
export default {
  name: "navbar",
};
</script>

<style lang="scss">
.header {
  display: flex;
  align-items: center;
  z-index: 999;
//   background: yellow;
  padding: 37px 55px;
  padding-bottom: 0px;
  .brand {
    height: 16.78062629699707px;
    width: 108.17298889160156px;
    margin-right: 57px;
    cursor: pointer;
    img {
      height: 100%;
      width: 100%;
      object-fit: contain;
    }
  }

  .navbar {
    //    background: yellowgreen;
       width: 100%;
    .navbar-nav {
      display: flex;
      align-items: center;
      margin: 0;
      padding: 0;
      list-style: none;
      .nav-item {
        font-family: "Roboto", sans-serif;
        font-weight: 500;
        color: #272d4e;
        font-size: 18px;
        line-height: 21px;
        margin-right: 38px;
        cursor: pointer;
        transition: color 0.25s ease;

        &:hover{
            color: #7854f7;
        }

        &:last-child{
            margin-left: auto;
        }
      }
    }
  }
}
</style>
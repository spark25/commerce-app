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
      <button class="btn primary __nav-cta">Get Started</button>
      <button class="icon">
        <img src="../assets/icons/icon-search.svg" alt="search icon" />
      </button>
      <button class="icon __ham" @click="mobileNavOpen = !mobileNavOpen">
        <svg width="16" height="10" viewBox="0 0 16 10">
          <title>Open mobile navigation</title>
          <g fill="var(--knockoutColor)" fill-rule="evenodd">
            <rect y="8" width="16" height="2" rx="1"></rect>
            <rect y="4" width="16" height="2" rx="1"></rect>
            <rect width="16" height="2" rx="1"></rect>
          </g>
        </svg>
      </button>
    </div>

    <div class="mobile-nav" :class="{ __open: mobileNavOpen }">
      <button class="icon close-menu" @click="mobileNavOpen = false">
        <svg width="40" height="40" viewBox="0 0 40 40">
          <title>Close mobile navigation</title>
          <path
            d="M25.6 14.3a1 1 0 0 1 0 1.4l-4.24 4.25 4.25 4.24a1 1 0 1 1-1.42 1.42l-4.24-4.25-4.24 4.25a1 1 0 0 1-1.42-1.42l4.25-4.24-4.25-4.24a1 1 0 0 1 1.42-1.42l4.24 4.25 4.24-4.25a1 1 0 0 1 1.42 0z"
            fill="#8898AA"
            fill-rule="evenodd"
          ></path>
        </svg>
      </button>

      <nav class="mobile-navbar">
        <ul class="mobile-navbar-nav" :class="{ navOpen: mobileNavOpen }">
          <li class="nav-item">Sell</li>
          <li class="nav-item">Marketplace</li>
          <li class="nav-item">Community</li>
          <li class="nav-item">Develop</li>
          <li class="nav-item">Resources</li>
        </ul>
      </nav>

      <div class="d_flex align_center justify_space_between">
        <div class="btn __text">Login</div>
        <button class="btn primary __mobile-nav-cta">Get Started</button>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: "navbar",

  data() {
    return {
      mobileNavOpen: false,
    };
  },
};
</script>

<style lang="scss">
.header {
  display: flex;
  align-items: center;
  z-index: 999;
  padding: 37px 55px;
  padding-bottom: 0px;
  position: relative;
  .brand {
    min-height: 16.78062629699707px;
    min-width: 108.17298889160156px;
    margin-right: 57px;
    cursor: pointer;
    img {
      height: 100%;
      width: 100%;
      object-fit: contain;
    }
  }

  .navbar {
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

        &:hover {
          color: #7854f7;
        }

        &:last-child {
          margin-left: auto;
        }
      }
    }

    @include lg {
      display: none;
    }

    @include md {
      display: none;
    }
    @include sm {
      display: none;
    }
  }

  .__ham {
    height: 32px;
    width: 32px;
    align-items: center;
    justify-content: center;
    display: none;
  }

  .mobile-nav {
    position: absolute;
    width: 95%;
    padding: 4rem 2rem 2rem 2rem;
    border-radius: 20px;
    background: #fff;
    display: block;
    top: 10px;
    left: 50%;
    display: grid;
    justify-content: stretch;

    box-shadow: 0 50px 100px -20px rgba(50, 50, 93, 0.25),
      0 30px 60px -30px rgba(0, 0, 0, 0.3);
    transform: translateX(-50%) scale(0);
    opacity: 0;
    transition: opacity 0.5s ease, transform 0.2s ease;
    transform-origin: top right;

    .mobile-navbar {
      width: 100%;
      margin-bottom: 1rem;
      .mobile-navbar-nav {
        display: none;
        justify-content: stretch;
        margin: 0;
        padding: 0;
        list-style: none;
        opacity: 0;
        transition: all 0.5s ease-out;

        &.navOpen {
          display: grid;
          opacity: 1;
          animation: fadeInDown 1s;
        }
        .nav-item {
          height: 2rem;
          font-family: "Roboto", sans-serif;
          font-weight: 500;
          color: #272d4e;
          font-size: 14px;
          line-height: 21px;
          margin-bottom: 1rem;
          padding: 0px 1rem;
          cursor: pointer;
          transition: color 0.25s ease;
          display: flex;
          justify-content: center;
          align-items: center;

          &:hover {
            color: #7854f7;
          }
        }
      }
    }

    &.__open {
      transform: translateX(-50%) scale(1) !important;
      opacity: 1;
    }
    .__mobile-nav-cta {
      font-size: 14px;
      padding: 8px 16px;
    }

    .__text {
      font-size: 14px;
      padding: 8px 16px;
      color: #272d4e;
      line-height: 21px;
      cursor: pointer;
      transition: color 0.25s ease;
      text-align: center;

      &:hover {
        color: #7854f7;
      }
    }
    .icon.close-menu {
      position: absolute;
      right: 0;
      top: 0;
      height: 54px;
      width: 54px;
    }
  }

  @include lg {
    justify-content: space-between;
    height: 54px;
    padding: 37px 24px;
    .__nav-cta {
      display: none;
    }
    .__ham {
      display: block;
    }
  }
  @include md {
    justify-content: space-between;
    height: 54px;
    padding: 37px 16px;
    .__nav-cta {
      display: none;
    }
    .__ham {
      display: block;
    }
  }

  @include sm {
    justify-content: space-between;
    height: 54px;
    padding: 37px 16px;
    .__nav-cta {
      display: none;
    }
    .__ham {
      display: block;
    }
  }
}
</style>
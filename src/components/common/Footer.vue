<template>
  <div class="footer">
    <div class="footer_content container">
      <div class="about_safety d_flex align_center">
        <div class="d_flex align_center">
          <span class="__icon"
            ><img src="../../assets/icons/check_circle.svg" alt=""
          /></span>
          <span class="__title">30 day money back guarantee</span>
        </div>
        <div class="d_flex align_center">
          <span class="__icon"
            ><img src="../../assets/icons/support.svg" alt=""
          /></span>
          <span class="__title">Support teams across the world</span>
        </div>
        <div class="d_flex align_center">
          <span class="__icon"
            ><img src="../../assets/icons/safe.svg" alt=""
          /></span>
          <span class="__title">Safe &amp; Secure online payment</span>
        </div>
      </div>

      <div class="brand d_flex align_center justify_center">
        <img src="../../assets/icons/LOGOlight.svg" alt="Commerce Logo" />
      </div>

      <div class="__divider"></div>

      <div class="quick_links">
        <!-- About links  -->
        <div class="d-flex flex_column">
          <div class="__title">Who we Are</div>
          <ul class="__links">
            <li class="__link">About</li>
            <li class="__link">Team</li>
            <li class="__link">Work With Us</li>
          </ul>
        </div>

        <!-- site links  -->
        <div class="d-flex flex_column">
          <div class="__title">Commerce</div>
          <ul class="__links">
            <li class="__link">Features</li>
            <li class="__link">Payments</li>
            <li class="__link">Marketing</li>
            <li class="__link">Shipping</li>
            <li class="__link">Extension Store</li>
            <li class="__link">eCommerce blog</li>
            <li class="__link">Development blog</li>
            <li class="__link">Ideas board</li>
            <li class="__link">Mobile App</li>
            <li class="__link">Community</li>
            <li class="__link">Style Guide</li>
            <li class="__link">Email Newsletter</li>
          </ul>
        </div>

        <!-- other products  -->
        <div class="d-flex flex_column">
          <div class="__title">Other products</div>
          <ul class="__links">
            <li class="__link">Storefront</li>
            <li class="__link">Slider</li>
            <li class="__link">Majax</li>
            <li class="__link">Majax Extensions</li>
          </ul>
        </div>

        <!-- support links  -->
        <div class="d-flex flex_column">
          <div class="__title">Support</div>
          <ul class="__links">
            <li class="__link">Documentation</li>
            <li class="__link">Customizations</li>
            <li class="__link">Support Policy</li>
            <li class="__link">Contact</li>
            <li class="__link">COVID-19 Resources</li>
            <li class="__link">Privacy Notice for</li>
            <li class="__link">California Users</li>
          </ul>
        </div>

        <!-- Recommended links  -->
        <div class="d-flex flex_column">
          <div class="__title">We recommend</div>
          <ul class="__links">
            <li class="__link">Experts</li>
            <li class="__link">Hosting Solutions</li>
            <li class="__link">Pre-sales FAQ</li>
            <li class="__link">Success Stories</li>
            <li class="__link">Design Feedback Group</li>
          </ul>
        </div>
      </div>
    </div>
    <div class="social_links">
      <ul class="__social d-flex align-center justify_space_between">
        <li class="__link">
          <img src="../../assets/icons/twitter.svg" alt="twitter" />
        </li>
        <li class="__link">
          <img src="../../assets/icons/facebook.svg" alt="facebook" />
        </li>
        <li class="__link">
          <img src="../../assets/icons/feed.svg" alt="feed" />
        </li>
        <li class="__link">
          <img src="../../assets/icons/ig.svg" alt="instagram" />
        </li>
      </ul>
      <span class="__cp">
        COPYRIGHT COMMERCE 2020 - TERMS &amp; CONDITIONS PRIVACY POLICY
      </span>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss">
.footer {
  display: grid;
  flex-direction: column;
  background: #7854f7;

  .footer_content {
    width: 100%;
    .about_safety {
      justify-content: space-around;
      padding: 45px 0px;
      .__icon {
        width: 41px;
        height: 41px;
      }
      .__title {
        margin-left: 15px;
        font-family: "Roboto";
        font-style: normal;
        font-weight: normal;
        font-size: 20px;
        line-height: 52px;
        /* identical to box height, or 262% */

        color: #ffffff;
      }

      @include lg {
        display: grid;
        gap: 20px;
      }
      @include md {
        display: grid;
        gap: 20px;
      }
      @include sm {
        display: grid;
        gap: 20px;
      }
    }

    .brand {
      margin: 141px auto 68px auto;
    }

    .quick_links {
      display: grid;
      grid-template-columns: repeat(5, 1fr);
      justify-items: center;
      padding-bottom: 64px;

      .__title {
        font-family: "Roboto";
        font-style: normal;
        font-weight: bold;
        font-size: 14px;
        line-height: 52px;
        text-transform: uppercase;
        color: #ffffff;
      }

      .__links {
        margin: 0;
        padding: 0;
        list-style: none;

        .__link {
          font-family: "Roboto";
          font-style: normal;
          font-weight: normal;
          font-size: 12px;
          line-height: 22px;
          text-transform: capitalize;
          color: #ffffff;
          cursor: pointer;

          &:hover {
            color: #ffffffd8;
          }
        }
      }

      @include md {
        grid-template-columns: 1fr 1fr 1fr;
        row-gap: 2rem;
        .__title {
          font-size: 16px;
        }
        .__link {
          font-size: 14px !important;
          line-height: 32px;
          margin-bottom: 0.8rem;
        }
      }
      @include sm {
        grid-template-columns: 1fr 1fr;
        row-gap: 2rem;
        .__title {
          font-size: 16px;
        }
        .__link {
          font-size: 14px !important;
          line-height: 32px;
          margin-bottom: 0.8rem;
        }
      }
    }
  }

  .social_links {
    display: flex;
    align-items: center;
    justify-content: space-between;
    background: #fff;
    padding: 21px 220px;
    .__social {
      margin: 0;
      padding: 0;
      list-style: none;
      display: flex;
      .__link {
        margin-right: 54px;
        cursor: pointer;
        display: flex;
        align-items: center;
        justify-content: center;

        &:last-child {
          margin-right: 0;
        }
      }
    }
    .__cp {
      font-style: normal;
      font-weight: normal;
      font-size: 12px;
      line-height: 22px;
      text-align: center;
      color: #272d4e;
      cursor: unset;
    }
  }

  @include sm {
    display: grid;
    grid-template-columns: 1fr;
    .social_links {
      display: flex;
      align-items: center;
      justify-content: center;
      flex-direction: column;
      padding: 1rem;

      .__social {
        padding-bottom: 1rem;
      }
      .__cp {
        align-self: center;
      }
    }
  }
}
</style>
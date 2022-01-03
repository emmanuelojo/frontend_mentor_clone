<template>
  <section id="contact" class="footer">
    <div class="icons">
      <div class="logo">
        <SvgIcon name="logo" />
      </div>

      <div class="social-media">
        <SvgIcon name="facebook" />
        <SvgIcon name="youtube" />
        <SvgIcon name="twitter" />
        <SvgIcon name="pinterest" />
        <SvgIcon name="instagram" />
      </div>
    </div>

    <div class="connect">
      <div>
        <a href="#about">About Us</a>
        <a href="#contact">Contact</a>
        <a href="#blog">Blog</a>
      </div>

      <div>
        <a>Careers</a>
        <a>Support</a>
        <a>Privacy Policy</a>
      </div>
    </div>

    <div class="invite-holder">
      <div class="invite">
        <p>Request Invite</p>
      </div>

      <p>&copy; Easybank. All Rights Reserved</p>
    </div>
  </section>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import SvgIcon from "./SvgIcon.vue";

export default defineComponent({
  name: "Footer",
  components: { SvgIcon },
});
</script>

<style lang="scss">
.footer {
  display: grid;
  grid-template-columns: repeat(3, auto);
  gap: 5rem;
  background: hsl(233, 26%, 24%);
  padding: 5rem;

  .icons {
    display: grid;
    gap: 2rem;
    color: #fff;

    .logo {
      img {
        color: #fff;
      }
    }

    .social-media {
      display: flex;

      svg {
        margin: 0 0.5rem;

        &:hover {
          cursor: pointer;
        }
      }
    }
  }

  .connect {
    display: grid;
    grid-template-columns: repeat(2, auto);
    gap: 4rem;
    color: gray;
    text-align: left;

    > div {
      display: grid;

      a {
        text-decoration: none;
        color: gray;
      }
    }
  }

  .invite-holder {
    display: grid;
    justify-content: center;
    gap: 1rem;

    .invite {
      display: flex;
      justify-content: center;
      align-items: center;
      background-image: linear-gradient(
        to right,
        hsl(136, 65%, 51%),
        hsl(192, 70%, 51%)
      );
      border-radius: 1.5rem;
      height: 2.5rem;
      width: 10rem;

      p {
        color: #fff;
        padding: 0.25rem 1.5rem;
        font-weight: 500;

        &:hover {
          cursor: pointer;
        }
      }
    }

    p {
      color: gray;
    }
  }

  @media screen and (max-width: 62.25rem) {
    padding: 3rem 1.5rem;

    .invite-holder {
      p {
        font-size: 12px;
        text-align: left;
      }
    }
  }

  @media screen and (max-width: 31.25rem) {
    grid-template-columns: repeat(1, auto);
    justify-content: center;

    .connect {
      grid-template-columns: repeat(1, auto);
      gap: 0;

     a {
        text-align: center;
        line-height: 24px;
      }
    }

    .invite-holder {
      p {
        display: flex;
        font-size: 12px;
      }
    }
  }
}
</style>

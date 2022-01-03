<template>
  <section id="about" class="services">
    <div class="header">
      <h1>Why choose Easybank?</h1>
      <p>
        <span>
          We leverage Open Banking to turn your bank account into your financial
          hub.
        </span>
        <span> Control your finances like never before. </span>
      </p>
    </div>

    <div class="services-list">
      <!-- <div class="service" v-for="(service, index) in services" :key="index">
        <div class="image">
          <SvgIcon name="budget" />
          <SvgIcon :name="service.svgName"/>
        </div>

        <h3>{{ service.name }}</h3>

        <p>
          {{ service.text }}
        </p>
      </div> -->

      <div class="service">
        <div class="image">
          <SvgIcon name="online" />
        </div>

        <h3>Online Banking</h3>

        <p>
          Our modern web and mobile applications allow you to keep track of your
          finances wherever you are in the world.
        </p>
      </div>

      <div class="service">
        <div class="image">
          <SvgIcon name="budget" />
        </div>

        <h3>Simple Budgeting</h3>

        <p>
          See exactly where =your money goes each month. Receive notifications
          when you're close to hitting your limits.
        </p>
      </div>
      <div class="service">
        <div class="image">
          <SvgIcon name="onboarding" />
        </div>

        <h3>Fast Onboarding</h3>

        <p>
          We don't do branches. Open your account in minutes online and start
          taking control of your finances right away.
        </p>
      </div>
      <div class="service">
        <div class="image">
          <SvgIcon name="api" />
        </div>

        <h3>Open API</h3>

        <p>
          Manage your savings, investments, pension, and much more from one
          account. Tracking your money has never been easier.
        </p>
      </div>
    </div>
  </section>
</template>

<script lang="ts">
import { defineComponent, ref } from "vue";
import SvgIcon from "./SvgIcon.vue";
export default defineComponent({
  name: "Services",

  components: { SvgIcon },

  setup() {
    const services = [
      {
        name: "Online Banking",
        text: "Our modern web and mobile applications allow you to keep track of your finances wherever you are in the world.",
        svgName: "'budget'",
      },
      {
        name: "Simple Budgeting",
        text: "See exactly where =your money goes each month. Receive notifications when you're close to hitting your limits.",
        svgName: "'budget'",
      },
      {
        name: "Fast Onboarding",
        text: "We don't do branches. Open your account in minutes online and start taking control of your finances right away.",
        svgName: "'budget'",
      },
      {
        name: "Open API",
        text: "Manage your savings, investments, pension, and much more from one account. Tracking your money has never been easier.",
        svgName: "'budget'",
      },
    ];

    return {
      services,
    };
  },
});
</script>

<style lang="scss">
.services {
  text-align: left;
  padding: 5rem 3rem;

  .header {
    h1 {
      font-size: 50px;
    }

    p {
      color: gray;
      display: grid;
      text-align: left;
    }
  }

  &-list {
    display: grid;
    grid-template-columns: repeat(4, auto);
    gap: 1rem;
    margin-top: 4rem;

    .service {
      width: 300px;

      p {
        color: gray;
      }
    }
  }

  @media screen and (max-width: 64rem) {
    .header {
      h1 {
        font-size: 40px;
        display: flex;
        justify-content: center;
      }

      p {
        display: grid;
        justify-content: center;
      }
    }

    &-list {
      display: grid;
      grid-template-columns: repeat(2, auto);
      justify-content: center;
    }
  }

  @media screen and (max-width: 31.25rem) {
    .header {
      h1 {
        text-align: center;
        font-size: 35px;
      }

      p {
        text-align: left;
      }
    }

    &-list {
      display: grid;
      grid-template-columns: repeat(1, auto);
      gap: 1rem;
      justify-content: center;

      .service {
        display: flex;
        flex-direction: column;
        justify-content: center;
        margin: 0 auto;
        width: auto;

        .image {
          display: flex;
          justify-content: center;
          margin: 0 auto;
        }

        h3 {
          text-align: center;
        }

        p {
          text-align: left;
        }
      }
    }
  }
}
</style>

<template>
  <section id="home" class="hero">
    <div class="text">
      <h1>
        <span> Next generation </span>
        <span> digital banking</span>
      </h1>

      <p>
        <span> Take your financial life online. Your Easybank account </span>
        <span> will be a one-stop-shop for spending, saving, </span>
        <span> budgeting, investing, and much more. </span>
      </p>

      <div class="invite">
        <p>Request invite</p>
      </div>
    </div>

    <div class="images">
      <img src="../assets/images/image-mockups.png" alt="" />
    </div>
  </section>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "Hero",
});
</script>

<style lang="scss">
.hero {
  display: flex;
  justify-content: space-around;
  align-items: center;
  padding: 0 1.5rem;
  background: #f7f7f7;

  .text {
    text-align: left;

    h1 {
      display: grid;
      font-size: 50px;
      font-weight: 600;
    }

    p {
      display: grid;
      color: gray;
      line-height: 1.5rem;
    }

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
        padding: 0.25rem 1rem;
        font-weight: 600;

        &:hover {
          cursor: pointer;
        }
      }
    }
  }

  @media screen and (max-width: 64rem) {
    display: flex;
    justify-content: space-around;
    align-items: center;

    .text {
      text-align: left;

      h1 {
        font-size: 40px;
      }

      p{
        font-size: 12px;
      }
    }

    .images {
      width: 350px;
      max-width: 400px;

      img {
        width: 100%;
      }
    }
  }

  @media screen and (max-width: 31.25rem) {
    display: grid;
    padding-bottom: 2rem;

    .images {
      order: 1;
      width: 300px;

      img {
        width: 100%;
      }
    }
    .text {
      order: 2;
      display: flex;
      flex-direction: column;
      justify-content: center;

      h1 {
        span {
          text-align: center;
          font-size: 35px;
        }
      }

      p {
        display: grid;
        line-height: 20px;

        span {
          text-align: left;
          padding-left: 0.25rem;
          padding-right: 0.25rem;
        }
      }

      .invite {
        display: flex;
        justify-content: center;
        margin: 2rem auto;
      }
    }
  }
}
</style>

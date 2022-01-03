<template>
  <section id="blog" class="articles">
    <div class="header">
      <h1>Latest Articles</h1>
    </div>

    <div class="articles-list">
      <!-- <div class="article" v-for="(article, index) in articles" :key="index">
        <div class="image-holder">
          <img :src="article.image" alt="article-image" />
        </div>
        <div class="content">
          <div class="author">
            <p>By {{ article.author }}</p>
          </div>
          <h3>{{ article.title }}</h3>
          <p>{{ article.text }}</p>
        </div>
      </div> -->
      <div class="article">
        <div class="image-holder">
          <img src="../assets/images/image-currency.jpg" alt="article-image" />
        </div>
        <div class="content">
          <div class="author">
            <p>By Claire Robinson</p>
          </div>
          <h3>Receive money in any currency with no fees</h3>
          <p>
            The world is getting smaller and we're becoming more mobile. So why
            should you be forced to only receive money in a single
          </p>
        </div>
      </div>
      <div class="article">
        <div class="image-holder">
          <img
            src="../assets/images/image-restaurant.jpg"
            alt="article-image"
          />
        </div>
        <div class="content">
          <div class="author">
            <p>By Wilson Hutton</p>
          </div>
          <h3>Treat yourself without worrying about money</h3>
          <p>
            Our simple budgeting feature allows you to separate out your
            spending and set realistic limits each month. That means you
          </p>
        </div>
      </div>
      <div class="article">
        <div class="image-holder">
          <img src="../assets/images/image-plane.jpg" alt="article-image" />
        </div>
        <div class="content">
          <div class="author">
            <p>By Wilson Hutton</p>
          </div>
          <h3>Take your Easybank card wherever you go</h3>
          <p>
            We want you to enjoy your travels. This is why we don't charge any
            fees on purchases while you're abroad. We'll even show you
          </p>
        </div>
      </div>
      <div class="article">
        <div class="image-holder">
          <img src="../assets/images/image-confetti.jpg" alt="article-image" />
        </div>
        <div class="content">
          <div class="author">
            <p>By Claire Robinson</p>
          </div>
          <h3>Our invite-only Beta accounts are now live!</h3>
          <p>
            After a lot of hard work by the whole team, we're excited to launch
            our closed beta. It's easy to request an invite through the site
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "Articles",
  setup() {
    const articles = [
      {
        author: "Claire Robinson",
        title: "Receive money in any currency with no fees",
        text: "The world is getting smaller and we're becoming more mobile. So why should you be forced to only receive money in a single",
        image: "@/assets/images/image-currency.jpg",
      },
      {
        author: "Wilson Hutton",
        title: "Treat yourself without worrying about money",
        text: "Our simple budgeting feature allows you to separate out your spending and set realistic limits each month. That means you",
        image: "@/assets/images/image-restaurant.jpg",
      },
      {
        author: "Wilson Hutton",
        title: "Take your Easybank card wherever you go",
        text: "We want you to enjoy your travels. This is why we don't charge any fees on purchases while you're abroad. We'll even show you",
        image: "@/assets/images/image-plane.jpg",
      },
      {
        author: "Claire Robinson",
        title: " Our invite-only Beta accounts are now live!",
        text: "After a lot of hard work by the whole team, we're excited to launch our closed beta. It's easy to request an invite through the site",
        image: "@/assets/images/image-confetti.jpg",
      },
    ];

    return {
      articles,
    };
  },
});
</script>

<style lang="scss">
.articles {
  background: #f7f7f7;
  padding: 3rem 2rem 5rem 2rem;

  .header {
    h1 {
      text-align: left;
      font-weight: 600;
      font-size: 50px;
    }
  }

  &-list {
    display: grid;
    grid-template-columns: repeat(4, auto);
    gap: 1rem;

    .article {
      border-radius: 0.5rem;
      width: 300px;
      background: #ffff;
      box-shadow: 0px 1px 5px rgba(0, 0, 0, 0.1);

      .image-holder {
        height: 200px;
        width: 100%;
        border-radius: 0.5rem 0.5rem 0 0;

        img {
          width: 100%;
          height: 100%;
          border-radius: 0.5rem 0.5rem 0 0;
        }
      }

      .content {
        text-align: left;
        padding: 0.5rem 1.5rem;

        .author {
          p {
            font-size: 14px;
            color: gray;
            padding-bottom: 0;
          }
        }

        h3 {
          font-weight: 600;
          padding-bottom: 0;
        }

        p {
          padding: 0 0 1rem 0;
          color: gray;
          line-height: 22px;
        }
      }
    }
  }

  @media screen and (max-width: 64rem) {
    .header {
      h1 {
        font-size: 40px;
        text-align: center;
      }
    }
    
    &-list {
      display: grid;
      grid-template-columns: repeat(2, auto);
      gap: 2.5rem;
      justify-content: center;
    }
  }

  @media screen and (max-width: 31.25rem) {
    .header {
      h1 {
        font-size: 35px;
        text-align: center;
      }
    }
    &-list {
      display: grid;
      grid-template-columns: repeat(1, auto);
      gap: 2.5rem;
      justify-content: center;
    }
  }
}
</style>

<template>
  <div class="nav">
    <input type="checkbox" id="nav-check" />
    <div class="nav-header">
      <div class="logo">
        <SvgIcon name="logo" />
      </div>
    </div>
    <div class="nav-btn">
      <label for="nav-check">
        <span></span>
        <span></span>
        <span></span>
      </label>
    </div>

    <div class="nav-links">
      <ul>
        <li><a href="#home"> Home </a></li>
        <li><a href="#about"> About </a></li>
        <li><a href="#contact"> Contact </a></li>
        <li><a href="#blog"> Blog </a></li>
        <li><a> Careers </a></li>
      </ul>

      <div class="invite">
        <p>Request Invite</p>
      </div>
    </div>
  </div>

</template>

<script lang="ts">
import { defineComponent } from "vue";
import SvgIcon from "./SvgIcon.vue";
import SvgIcon1 from "./SvgIcon.vue";

export default defineComponent({
  name: "Navbar",
  components: { SvgIcon, SvgIcon1 },
});
</script>

<style lang="scss">
* {
  box-sizing: border-box;
}

body {
  margin: 0px;
  font-family: "segoe ui";
}

.nav {
  position: fixed;
  display: flex;
  justify-content: space-around;
  align-items: center;
  background-color: #ffff;
  height: 4.5rem;
  width: 100%;

  > .nav-btn {
    display: none;
  }

  > .nav-links {
    display: flex;
    justify-content: space-between;
    align-items: center;

    ul {
      display: flex;

      li {
        list-style: none;
        margin: 0 0.75rem;

        a {
          text-decoration: none;
          color: gray;

          &:hover {
            color: hsl(192, 70%, 51%);
          }

          &.active {
            color: hsl(192, 70%, 51%);
          }
        }
      }
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
      margin-left: 5rem;

      p {
        color: #fff;
        padding: 0.25rem 1.5rem;
        font-weight: 500;

        &:hover {
          cursor: pointer;
        }
      }
    }
  }

  > #nav-check {
    display: none;
  }
}

@media screen and (max-width: 62.25rem) {
  .nav {
    display: flex;
    justify-content: space-around;
    align-items: center;

    &-header {
      position: absolute;
      left: 0.5rem;
    }
  }
  .nav > .nav-btn {
    display: inline-block;
    position: absolute;
    right: 0px;
  }
  .nav > .nav-btn > label {
    display: inline-block;
    width: 50px;
    height: 50px;
    padding: 13px;
  }

  .nav > .nav-btn > label > span {
    display: block;
    width: 25px;
    height: 10px;
    border-top: 2px solid #eee;
  }
  .nav > .nav-links {
    position: absolute;
    display: grid;
    justify-content: center;
    width: 100%;
    height: 80vh;
    background-color: #fff;
    box-shadow: 0px 1px 5px rgba(0, 0, 0, 0.1);
    transition: all 0.3s ease-in;
    overflow-y: hidden;
    top: 70px;
    left: 0px;

    ul {
      display: grid;
      margin: 0 auto;
      padding-left: 0;

      li {
        list-style: none;
        margin: 0.75rem auto;

        a {
          text-decoration: none;
          color: gray;
          text-align: left;
        }
      }
    }

    .invite {
      display: flex;
      justify-content: center;
      align-items: center;
      margin-left: 0;
      margin-top: 0;
      padding-top: 0;
    }
  }
  .nav > .nav-links > a {
    display: block;
    width: 100%;
  }
  .nav > #nav-check:not(:checked) ~ .nav-links {
    height: 0px;
  }
  .nav > #nav-check:checked ~ .nav-links {
    height: calc(100vh - 50px);
    overflow-y: auto;
  }
}

</style>

<template>
  <header class="header">
    <img src="../assets/logo2.svg" alt="Alam Logo" />
    <label class="hamburger">
      <input type="checkbox" @click="toggleMenu" />
      <svg viewBox="0 0 32 32">
        <path
          class="line line-top-bottom"
          d="M27 10 13 10C10.8 10 9 8.2 9 6 9 3.5 10.8 2 13 2 15.2 2 17 3.8 17 6L17 26C17 28.2 18.8 30 21 30 23.2 30 25 28.2 25 26 25 23.8 23.2 22 21 22L7 22"
        ></path>
        <path class="line" d="M7 16 27 16"></path>
      </svg>
    </label>
    <div class="menu" :class="showMenu ? 'active' : 'close'">
      <div class="menu-content" :class="showMenu ? 'active' : 'close'">
        <div class="links">
          <ul>
            <li><a href="/my-work">My Work</a></li>
            <li>
              <a href="/my-resume">My Resume</a>
            </li>
            <li>
              <a href="/#contact-me">Contact Me</a>
            </li>
          </ul>
        </div>
        <div class="social">
          <img src="../assets/img/github.png" />
          <img src="../assets/img/insta.png" />
          <img src="../assets/img/linkedin.png" />
        </div>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: "VueHeader",
  data() {
    return {
      showMenu: false,
    };
  },
  methods: {
    toggleMenu() {
      this.showMenu = !this.showMenu;
    },
  },
};
</script>

<style scoped lang="scss">
.header {
  position: fixed;
  left: 0;
  right: 0;
  top: 0;
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 20px 40px;
}
.header img {
  width: 3.5%;
}

.menu {
  position: absolute;
  z-index: 100;
  opacity: 0;
  right: 1%;
  top: 10%;
  width: 200px;
  height: 280px;
  background: #ffffff;
  padding: 150px 40px;
  transition: width 0.4s, height 0.4s, opacity 0.4s;
  .menu-content {
    transition: opacity 0.4s;
    transition-delay: 350ms;
    opacity: 0;
    display: flex;
    flex-direction: column;
    z-index: 20;
    .links {
      ul {
        list-style: none;
        li {
          font-size: 30px;
          margin-bottom: 30px;
          font-weight: 400;
          color: #c8c8c8;
          cursor: pointer;
          &:hover {
            color: #262626;
          }
        }
      }
    }
    .social {
      margin-top: 65%;
      img {
        width: 10%;
        margin-right: 20px;
        cursor: pointer;
      }
    }
    .contact-me {
      font-size: 25px;
      text-transform: uppercase;
      margin-top: 55px;
      margin-bottom: 20px;
      color: #c1c1c1;
      font-family: Montserrat;
    }
    &.active {
      opacity: 1;
    }
    &.close {
      transition: opacity 0.2s;
      transition-delay: 0ms;
      opacity: 0;
    }
  }
  &.active {
    width: 500px;
    height: 700px;
    opacity: 1;
    box-shadow: -16px 15px 19px -3px rgba(0, 0, 0, 0.2);
  }
  &.close {
    transition: width 0.2s, height 0.2s, opacity 0.2s;
    width: 500px;
    height: 700px;
    opacity: 0;
    box-shadow: -16px 15px 19px -3px rgba(0, 0, 0, 0);
  }
}

.hamburger {
  cursor: pointer;
  padding-top: 10px;
  font-size: 70px;
  z-index: 110;
}
.hamburger input {
  display: none;
}
.hamburger svg {
  /* The size of the SVG defines the overall size */
  height: 0.9em;
  /* Define the transition for transforming the SVG */
  transition: transform 600ms cubic-bezier(0.4, 0, 0.2, 1);
}
.line {
  fill: none;
  stroke: #262626;
  stroke-linecap: round;
  stroke-linejoin: round;
  stroke-width: 1.5;
  /* Define the transition for transforming the Stroke */
  transition: stroke-dasharray 600ms cubic-bezier(0.4, 0, 0.2, 1),
    stroke-dashoffset 600ms cubic-bezier(0.4, 0, 0.2, 1);
}
.line-top-bottom {
  stroke-dasharray: 12 63;
}
.hamburger input:checked + svg {
  transform: rotate(-45deg);
}
.hamburger input:checked + svg .line-top-bottom {
  stroke-dasharray: 20 300;
  stroke-dashoffset: -32.42;
}
</style>

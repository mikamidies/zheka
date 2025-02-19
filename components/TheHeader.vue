<template>
  <div class="wrap" id="navbar">
    <div class="container">
      <div class="left">
        <button @click="scrollElement('hero')">
          <img class="brand" src="/public/assets/img/logo/brand.png" alt="" />
        </button>
      </div>
      <div class="mid">
        <button @click="scrollElement('about')">About</button>
        <button @click="scrollElement('services')">Services</button>
        <button @click="scrollElement('portfolio')">Portfolio</button>
        <button @click="scrollElement('contact')">Contact</button>
      </div>
      <div class="right">
        <button class="lang">
          Eng
          <Icon style="width: 32px; height: 32px" icon="twemoji:flag-for-flag-united-kingdom" />
        </button>
        <div class="batton">
          <button class="call" @click="scrollElement('contact')">
            Contact me
            <Icon icon="mdi:call" />
          </button>
          <img class="gif" src="/public/assets/img/square.gif" alt="" />
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { onMounted, onUnmounted } from "vue";

function scrollHeader() {
  const navbar = document.getElementById("navbar");
  if (window.scrollY >= 50) {
    navbar.classList.add("scroll");
  } else {
    navbar.classList.remove("scroll");
  }
}

onMounted(() => {
  window.addEventListener("scroll", scrollHeader);
});

onUnmounted(() => {
  window.removeEventListener("scroll", scrollHeader);
});

const scrollElement = (id) => {
  const element = document.getElementById(id);
  if (element) {
    element.scrollIntoView({ block: "start", behavior: "smooth" });
  }
  menuHandle.value = false;
};
</script>

<style scoped>
.wrap {
  padding: 10px;
  border-bottom: 1px solid #ebebeb;
  /* position: fixed; */
  top: 0;
  left: 0;
  width: 100%;
  background: white;
  z-index: 99;
  transition: 0.4s;
}

.brand {
  width: 90px;
  height: 70px;
  object-fit: cover;
}

.wrap.scroll {
  position: fixed;
  padding: 10px;
}

.container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
}

.mid {
  display: flex;
  justify-content: center;
  gap: 40px;
}

.left {
  display: flex;
  align-items: center;
}

.right {
  display: flex;
  justify-content: flex-end;
  gap: 40px;
  align-items: center;
}

.mid button {
  font-size: 18px;
  transition: 0.4s;
}

.mid button:hover {
  color: var(--blue);
}

.lang {
  display: flex;
  align-items: center;
  gap: 12px;
  font-size: 20px;
  font-family: var(--medium);
  display: none;
}

.batton {
  background: var(--blue);
  width: 180px;
  height: 50px;
  border-radius: 8px;
  position: relative;
  overflow: hidden;
  display: flex;
  justify-content: center;
  align-items: center;
}

.call {
  color: white;
  font-size: 18px;
  z-index: 2;
  position: relative;
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 12px;
  width: 100%;
  height: 100%;
}

.gif {
  z-index: 1;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  opacity: 0.2;
}

@media (max-width: 1023px) {
  .container {
    grid-template-columns: 1fr 2fr 1fr;
  }

  .mid {
    gap: 20px;
  }

  .right {
    gap: 20px;
  }

  .mid button {
    font-size: 16px;
  }

  .lang {
    font-size: 18px;
  }

  .call {
    min-width: 150px;
    height: 40px;
    font-size: 16px;
  }
}

@media (max-width: 767px) {
  .container {
    grid-template-columns: 1fr;
    gap: 16px;
  }

  .left {
    text-align: center;
  }

  .mid {
    flex-direction: column;
    gap: 12px;
  }

  .right {
    justify-content: center;
    gap: 16px;
  }

  .mid button {
    font-size: 14px;
  }

  .lang {
    font-size: 16px;
  }

  .call {
    min-width: 120px;
    height: 36px;
    font-size: 14px;
  }
}
</style>

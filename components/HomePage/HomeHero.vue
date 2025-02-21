<template>
  <div class="wrap">
    <div class="anchor" id="hero"></div>
    <div class="container">
      <div class="grid">
        <div class="left">
          <h4 class="title">
            Independent
            <br />
            <span>
              <AnimatedText />
            </span>
            developer
          </h4>

          <div class="text">
            <p class="txt">
              Turning bugs into features since 2021. <br />
              No <span>404</span>s here!
            </p>
          </div>

          <div
            class="batton fancy-button"
            ref="button"
            @mousemove="moveButton"
            @mouseleave="resetButton"
          >
            <button @click="scrollElement('contact')">Contact me</button>
            <img class="gif" src="/public/assets/img/square.gif" alt="" />
          </div>
        </div>
        <div class="right">
          <div class="round"></div>
          <div class="glass"></div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";
import { useNuxtApp } from "#app";

const button = ref(null);
const { $gsap } = useNuxtApp();

const moveButton = (event) => {
  const buttonElement = button.value;
  const rect = buttonElement.getBoundingClientRect();

  const mouseX = event.clientX - rect.left - rect.width / 2;
  const mouseY = event.clientY - rect.top - rect.height / 2;

  const distance = Math.sqrt(mouseX * mouseX + mouseY * mouseY);
  const maxDistance = 25;

  if (distance < maxDistance) {
    const moveX = (mouseX / distance) * maxDistance;
    const moveY = (mouseY / distance) * maxDistance;

    $gsap.to(buttonElement, {
      x: moveX,
      y: moveY,
      duration: 0.3,
      ease: "power2.out",
    });
  }
};

const resetButton = () => {
  const buttonElement = button.value;

  $gsap.to(buttonElement, {
    x: 0,
    y: 0,
    duration: 0.3,
    ease: "power2.out",
  });
};

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
  position: relative;
  height: 75vh;
}

.back {
  background: var(--blue);
  height: 340px;
  width: 540px;
  border-radius: 16px 0 0 16px;
  overflow: hidden;
}

.back img {
  width: 100%;
  height: 400px;
  object-fit: contain;
}

.container {
  height: 100%;
}

.grid {
  height: 100%;
  display: grid;
  grid-template-columns: 6fr 4fr;
  align-items: center;
  border-inline: 1px solid #ebebeb;
}

.title {
  font-size: 80px;
  font-style: normal;
  line-height: 72px;
  font-family: var(--bold);
}

.left {
  padding-left: 32px;
  display: flex;
  flex-direction: column;
  gap: 40px;
}

.left button {
  font-size: 20px;
  font-style: normal;
  font-weight: 500;
  line-height: 24px;
  width: 186px;
  height: 186px;
  border-radius: 50%;
  color: white;
  border: none;
  cursor: pointer;
  transition: transform 0.2s ease-out;
  position: relative;
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 2;
}

.batton {
  position: relative;
  overflow: hidden;
  display: inline-flex;
  width: 186px;
  height: 186px;
  border-radius: 50%;
  background: var(--blue);
}

.gif {
  position: absolute;
  top: 50%;
  left: 50% !important;
  transform: translate(-50%, -50%);
  width: 100%;
  left: 100%;
  z-index: 1;
  opacity: 0.2;
}

.text {
  display: flex;
  justify-content: center;
}

.txt {
  max-width: 500px;
  font-size: 20px;
  font-style: normal;
  font-weight: 400;
  line-height: 24px;
  /* 133.333% */
  letter-spacing: 0.72px;
  font-style: italic;
}

.txt span {
  color: var(--blue);
}

.glass {
  display: flex;
  justify-content: flex-end;
  position: relative;
  z-index: 2;
}

.glass img {
  height: 240px;
}

.right {
  position: relative;
  display: flex;
  justify-content: flex-end;
}

.round {
  position: absolute;
  z-index: 1;
  top: 50%;
  right: 5%;
  transform: translate(-50%, -50%);
  width: 370px;
  height: 370px;
  border-radius: 500px;
  background: linear-gradient(104deg, #e4f048 0%, #f3d112 100%);
  filter: blur(7px);
  animation: move 10s linear 4s infinite;
}

@keyframes move {
  0% {
    right: 5%;
  }

  25% {
    right: 15%;
  }

  50% {
    right: 5%;
  }

  75% {
    right: 15%;
  }

  100% {
    right: 5%;
  }
}

.fancy-button {
  cursor: pointer;
  transition: transform 0.2s ease-out;
  position: relative;
}

.glass {
  width: 448px;
  height: 220px;
  background: rgba(255, 255, 255, 0.2);
  backdrop-filter: blur(14px);
  border-radius: 12px 0 0 12px;
  box-shadow: -6px 0 6px rgba(0, 0, 0, 0.1), 0 4px 6px rgba(0, 0, 0, 0.1);
  mix-blend-mode: inherit;
}

@media (max-width: 1023px) {
  .wrap {
    height: 400px;
    border-bottom: 1px solid #ebebeb;
    margin-bottom: 32px;
  }
  .right {
    display: none;
  }
  .grid {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: flex-start;
    border: 0;
  }
  .title {
    font-size: 40px;
    line-height: 120%;
    text-align: center;
  }
  .title span {
    display: flex;
    justify-content: center;
  }
  .left {
    gap: 24px;
    padding: 0;
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
  }
  .txt {
    text-align: center;
    font-size: 14px;
  }
  .batton,
  .left button {
    width: 286px;
    height: 56px;
    border-radius: 12px;
    font-size: 18px;
  }
}
</style>

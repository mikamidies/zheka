<template>
  <div class="wrap">
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
              Turning bugs into features since 2020. <br />
              No <span>404</span>s here!
            </p>
          </div>

          <div
            class="batton fancy-button"
            ref="button"
            @mousemove="moveButton"
            @mouseleave="resetButton"
          >
            <button>Contact me</button>
            <img class="gif" src="/public/assets/img/square.gif" alt="" />
          </div>
        </div>
        <div class="right">
          <svg
            class="home__blob"
            viewBox="0 0 200 187"
            xmlns="http://www.w3.org/2000/svg"
            xmlns:xlink="http://www.w3.org/1999/xlink"
          >
            <mask id="mask0" mask-type="alpha">
              <path
                d="M190.312 36.4879C206.582 62.1187 201.309 102.826 182.328 134.186C163.346 165.547 
                                130.807 187.559 100.226 186.353C69.6454 185.297 41.0228 161.023 21.7403 129.362C2.45775 
                                97.8511 -7.48481 59.1033 6.67581 34.5279C20.9871 10.1032 59.7028 -0.149132 97.9666 
                                0.00163737C136.23 0.303176 174.193 10.857 190.312 36.4879Z"
              />
            </mask>
            <g mask="url(#mask0)">
              <path
                d="M190.312 36.4879C206.582 62.1187 201.309 102.826 182.328 134.186C163.346 
                                165.547 130.807 187.559 100.226 186.353C69.6454 185.297 41.0228 161.023 21.7403 
                                129.362C2.45775 97.8511 -7.48481 59.1033 6.67581 34.5279C20.9871 10.1032 59.7028 
                                -0.149132 97.9666 0.00163737C136.23 0.303176 174.193 10.857 190.312 36.4879Z"
              />
              <image
                class="home__blob-img"
                x="12"
                y="18"
                href="/public/assets/img/abbos.png"
              />
            </g>
          </svg>
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
</script>

<style scoped>
.home__blob {
  width: 400px;
  fill: var(--blue);
}

.home__blob-img {
  width: 170px;
}

.wrap {
  position: relative;
  height: 80vh;
}

.container {
  height: 100%;
}

.grid {
  height: 100%;
  display: grid;
  grid-template-columns: 5fr 5fr;
  align-items: center;
  border-inline: 1px solid #ebebeb;
}

.title {
  font-size: 68px;
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
  font-size: 18px;
  font-style: normal;
  font-weight: 500;
  line-height: 24px;
  width: 176px;
  height: 176px;
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
  width: 176px;
  height: 176px;
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
  justify-content: center;
}

.round {
  position: absolute;
  z-index: 1;
  top: 50%;
  left: 30%;
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
    left: 30%;
  }

  25% {
    left: 40%;
  }

  50% {
    left: 30%;
  }

  75% {
    left: 20%;
  }

  100% {
    left: 30%;
  }
}

.fancy-button {
  cursor: pointer;
  transition: transform 0.2s ease-out;
  position: relative;
}

@media (max-width: 1023px) {
  .grid {
    grid-template-columns: 1fr;
    gap: 40px;
    padding: 20px;
  }

  .left {
    padding-left: 0;
    align-items: center;
    text-align: center;
  }

  .title {
    font-size: 48px;
    line-height: 56px;
  }

  .txt {
    max-width: 100%;
  }

  .glass img {
    height: 180px;
  }

  .round {
    width: 280px;
    height: 280px;
  }
}

@media (max-width: 767px) {
  .grid {
    grid-template-columns: 1fr;
    gap: 20px;
    padding: 10px;
  }

  .title {
    font-size: 36px;
    line-height: 44px;
  }

  .left button {
    width: 140px;
    height: 140px;
    font-size: 16px;
  }

  .batton {
    width: 140px;
    height: 140px;
  }

  .txt {
    font-size: 16px;
    line-height: 20px;
  }

  .glass img {
    height: 120px;
  }

  .round {
    width: 200px;
    height: 200px;
  }
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
</style>

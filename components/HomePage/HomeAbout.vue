<template>
  <div class="wrap">
    <div class="anchor" id="about"></div>
    <div class="container">
      <div class="liner">
        <h4 class="section__title">About me</h4>
        <p class="txt">
          Hello! I’m a passionate Frontend Developer with over 3 years of
          experience, specializing in Vue.js and Nuxt.js. <br />
          Crafting seamless, pixel-perfect, and responsive web applications is
          not just my job—it's my art. Let’s build something amazing together!
        </p>

        <video
          muted
          loop
          playsinline
          autoplay
          src="/public/assets/img/video.mp4"
        ></video>

        <div class="items">
          <div class="item">
            <div class="item__logo">
              <Icon icon="material-symbols:close-fullscreen-rounded" />
            </div>
            <h4 class="item__title">Pixel Perfect</h4>
            <p class="item__txt">
              Delivering precise, high-quality designs that flawlessly match
              every detail of the original concept
            </p>
          </div>
          <div class="item">
            <div class="item__logo">
              <Icon
                icon="material-symbols:screenshot-monitor-outline-rounded"
              />
            </div>
            <h4 class="item__title">Responsive</h4>
            <p class="item__txt">
              Ensuring seamless functionality and a perfect user experience
              across all devices and screen sizes
            </p>
          </div>
          <div class="item">
            <div class="item__logo">
              <Icon icon="material-symbols:stack-star" />
            </div>
            <h4 class="item__title">Modern and Gorgeous</h4>
            <p class="item__txt">
              Crafting sleek, cutting-edge visuals that captivate and leave a
              lasting impression
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.txt {
  font-size: 18px;
  max-width: 90%;
  display: flex;
}

video {
  width: 100%;
  height: 440px;
  margin-top: 24px;
  object-fit: cover;
  border-radius: 12px;
}

.items {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 24px;
  margin-top: 24px;
}

.item svg {
  width: 64px;
  height: 64px;
}

.item svg :deep(path) {
  fill: var(--blue);
}

.item__title {
  font-size: 24px;
  margin: 12px 0;
  font-family: var(--bold);
}

.item__txt {
  font-size: 18px;
  max-width: 95%;
}
@media (max-width: 1023px) {
  .liner {
    padding: 0 12px 48px 12px;
  }
  .txt {
    font-size: 14px;
    max-width: 100%;
  }
  video {
    height: 220px;
  }
  .items {
    gap: 16px;
    grid-template-columns: repeat(1, 1fr);
  }
  .item svg {
    width: 32px;
    height: 32px;
  }
  .item__logo {
    display: flex;
    justify-content: center;
  }
  .item__title {
    text-align: center;
    margin: 0;
    font-size: 20px;
    line-height: 160%;
  }
  .item__txt {
    text-align: center;
    font-size: 14px;
    max-width: 90%;
    margin: 0 auto;
  }
}
</style>

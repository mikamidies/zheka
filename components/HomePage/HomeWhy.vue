<template>
  <div class="wrap">
    <div class="container">
      <div class="liner">
        <h4 class="section__title">Why me?</h4>

        <div class="cardo">
          <img class="gif" src="/public/assets/img/square.gif" alt="" />
          <div class="item">
            <p class="title">
              Fastest <Icon icon="material-symbols:rocket-launch" />
            </p>
            <p class="txt">
              Quick Turnarounds - I deliver fast, efficient solutions without
              cutting corners—because your time matters.
            </p>
          </div>
          <div class="item">
            <p class="title">
              Quality
              <Icon icon="material-symbols:award-star-rounded" />
            </p>
            <p class="txt">
              Top-Notch Work - Every detail is crafted with precision, ensuring
              high-quality results that exceed expectations.
            </p>
          </div>
          <div class="item">
            <p class="title">
              Reliability
              <Icon icon="material-symbols:approval-delegation" />
            </p>
            <p class="txt">
              Dependable Every Time - Consistent, clear, and committed. I’m here
              to deliver exactly what you need, when you need it.
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.wrap {
  overflow: hidden;
  padding-bottom: 32px;
}
.liner {
  border-bottom: 0;
}
.cardo {
  background: rgba(82, 114, 255, 0.7);
  padding: 32px;
  border-radius: 24px;
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 16px;
  position: relative;
}
.gif {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  object-fit: cover;
  z-index: 1;
  border-radius: 24px;
  opacity: 0.22;
  pointer-events: none;
}
.item {
  background: white;
  padding: 16px;
  border-radius: 12px;
  position: relative;
  z-index: 2;
}
.title {
  font-size: 30px;
  font-family: var(--bold);
  margin-bottom: 8px;
  display: flex;
  align-items: center;
  gap: 12px;
}
.title :deep(path) {
  fill: var(--blue);
}
.txt {
  font-size: 18px;
  max-width: 90%;
  opacity: 0.8;
}
.rocket {
  position: absolute;
  top: 25%;
  right: -80px;
  width: 320px;
  z-index: 3;
}
@media (max-width: 1023px) {
  .liner {
    padding: 32px 12px;
    border-top: 1px solid #ebebeb !important;
  }
  .cardo {
    grid-template-columns: repeat(1, 1fr);
    padding: 12px;
    border-radius: 16px;
  }
  .gif {
    border-radius: 16px;
  }
  .title {
    font-size: 24px;
  }
  .txt {
    font-size: 14px;
  }
}
</style>

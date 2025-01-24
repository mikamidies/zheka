<template>
  <div class="wrap">
    <div class="container">
      <div class="liner">
        <div class="cardo">
          <div class="left">
            <h4 class="text">
              Independent
              <span
                >Frontend,
                <br />
                Backend, Game, <br />
                Graphic design</span
              >
              master.
            </h4>
          </div>
          <div class="right">
            <div class="square">
              <img src="/public/assets/img/logo/brand.png" alt="" />
            </div>
          </div>
        </div>

        <div class="bottom">
          <div class="leftist">
            <div class="item">
              <p class="sup">Phone number</p>
              <p class="value">+998 90 140 00 00</p>
            </div>

            <div class="item">
              <p class="sup">Email</p>
              <p class="value">zhekadeveloper@gmail.com</p>
            </div>
          </div>
          <div class="rightist">
            <div class="item">
              <p class="sup">Socials</p>
              <div class="socs">
                <a href="https://instagram.com" target="_blank">
                  <Icon icon="simple-icons:instagram" />
                </a>
                <a href="https://telegram.org" target="_blank">
                  <Icon icon="simple-icons:telegram" />
                </a>
                <a href="https://github.com" target="_blank">
                  <Icon icon="simple-icons:github" />
                </a>
                <a href="https://linkedin.com" target="_blank">
                  <Icon icon="simple-icons:linkedin" />
                </a>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.cardo {
  background: var(--blue);
  border-radius: 32px 32px;
  padding: 48px;
  display: grid;
  grid-template-columns: 7fr 3fr;
  gap: 40px;
}
.liner {
  border-top: 0;
  padding: 32px 0 32px 32px;
}
.text {
  font-size: 78px;
  line-height: 100%;
  font-family: var(--bold);
  color: rgba(255, 255, 255, 0.4);
}
.left {
  display: flex;
  align-items: center;
}
.text span {
  color: white;
}
.square {
  width: 280px;
  height: 280px;
  background: white;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
}
.square img {
  width: 160px;
}
.right {
  display: flex;
  align-items: center;
  justify-content: center;
}
.bottom {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 32px 16px 0 0;
}
.leftist {
  display: flex;
  align-items: center;
  gap: 40px;
}
.sup {
  font-size: 16px;
  opacity: 0.6;
}
.value {
  font-size: 18px;
  font-family: var(--medium);
}
.item {
  display: flex;
  flex-direction: column;
  gap: 8px;
}
.rightist .item {
  display: flex;
  flex-direction: column;
  align-items: flex-end;
}
.socs {
  display: flex;
  align-items: center;
  gap: 16px;
}
.socs :deep(svg) {
  width: 24px;
  height: 24px;
}
.socs :deep(path) {
  fill: var(--blue);
}
</style>

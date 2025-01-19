<template>
  <div class="wrap">
    <div class="container">
      <div class="liner">
        <h4 class="section__title">Why me?</h4>

        <div class="cardo">
          <img class="gif" src="/public/assets/img/square.gif" alt="" />
          <div class="item">
            <p class="title">
              I'm the fastest <Icon icon="material-symbols:rocket-launch" />
            </p>
            <p class="txt">
              Lorem, ipsum dolor sit amet consectetur adipisicing elit. Nam nemo
              fugiat a quibusdam dignissimos inventore, repellat sapiente harum
              consequuntur sint.
            </p>
          </div>
          <div class="item">
            <p class="title">
              The best quality
              <Icon icon="material-symbols:award-star-rounded" />
            </p>
            <p class="txt">
              Lorem, ipsum dolor sit amet consectetur adipisicing elit. Nam nemo
              fugiat a quibusdam dignissimos inventore, repellat sapiente.
            </p>
          </div>
          <div class="item">
            <p class="title">
              Cheap prices
              <Icon icon="material-symbols:money-bag-rounded" />
            </p>
            <p class="txt">
              Lorem, ipsum dolor sit amet consectetur adipisicing elit. Nam nemo
              fugiat a quibusdam dignissimos inventore.
            </p>
          </div>

          <img class="rocket" src="/public/assets/img/rocket.gif" alt="" />
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
}
.item {
  background: white;
  padding: 16px;
  border-radius: 12px;
  position: relative;
  z-index: 2;
}
.title {
  font-size: 28px;
  font-family: var(--bold);
  margin-bottom: 8px;
  display: flex;
  align-items: center;
  gap: 8px;
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
</style>

<template>
  <div class="wrap">
    <div class="anchor" id="portfolio"></div>
    <div class="container">
      <div class="liner">
        <h4 class="section__title">My Portfolio</h4>

        <div class="items">
          <div class="item">
            <div class="image">
              <img src="/public/assets/img/port-1.jpg" alt="" class="pic" />
            </div>
            <div class="content">
              <div>
                <p class="name">Fintax</p>
                <p class="sub">Website for accountant company</p>
              </div>
              <div class="linker">
                <a href="#" target="_blank" class="link">
                  www.fintax.uz
                  <Icon icon="material-symbols:arrow-insert-rounded" />
                </a>
              </div>
            </div>
          </div>
          <div class="item">
            <div class="image">
              <img src="/public/assets/img/port-2.jpg" alt="" class="pic" />
            </div>
            <div class="content">
              <div>
                <p class="name">Hyper Power Server</p>
                <p class="sub">Web-server supply shop</p>
              </div>
              <div class="linker">
                <a href="#" target="_blank" class="link">
                  www.hpsuz.com
                  <Icon icon="material-symbols:arrow-insert-rounded" />
                </a>
              </div>
            </div>
          </div>
          <div class="item">
            <div class="image">
              <img src="/public/assets/img/port-3.jpg" alt="" class="pic" />
            </div>
            <div class="content">
              <div>
                <p class="name">Uzbekistan Airways Tech</p>
                <p class="sub">
                  The only aircraft repair center in central asia
                </p>
              </div>
              <div class="linker">
                <a href="#" target="_blank" class="link">
                  www.airtech.uz
                  <Icon icon="material-symbols:arrow-insert-rounded" />
                </a>
              </div>
            </div>
          </div>
          <div class="item">
            <div class="image">
              <img src="/public/assets/img/port-4.jpg" alt="" class="pic" />
            </div>
            <div class="content">
              <div>
                <p class="name">Polimer Group Asia</p>
                <p class="sub">Leading manufacturer of polymer pipes</p>
              </div>
              <div class="linker">
                <a href="#" target="_blank" class="link">
                  www.pga.uz
                  <Icon icon="material-symbols:arrow-insert-rounded" />
                </a>
              </div>
            </div>
          </div>
          <div class="item">
            <div class="image">
              <img src="/public/assets/img/port-5.jpg" alt="" class="pic" />
            </div>
            <div class="content">
              <div>
                <p class="name">Premium Pipe</p>
                <p class="sub">Leading manufacturer of polymer pipes</p>
              </div>
              <div class="linker">
                <a href="#" target="_blank" class="link">
                  www.premiumpipe.uz
                  <Icon icon="material-symbols:arrow-insert-rounded" />
                </a>
              </div>
            </div>
          </div>
          <div class="item">
            <div class="vinet">and 50+ more projects</div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style>
.items {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 24px;
  padding-top: 24px;
}

.image {
  width: 100%;
  height: 480px;
  border-radius: 12px;
  border: 1px solid #ebebeb;
  overflow: hidden;
}

.pic {
  width: 100%;
  height: 100%;
  object-fit: cover;
  transition: 0.4s;
}

.item:hover .pic {
  transform: scale(1.2);
}

.content {
  display: grid;
  grid-template-columns: 6fr 4fr;
  align-items: end;
  padding-top: 16px;
}

.name {
  font-family: var(--bold);
  font-size: 28px;
  margin-bottom: 4px;
}

.sub {
  font-size: 18px;
}

.linker {
  display: none;
  justify-content: flex-end;
  padding-right: 16px;
}

.link {
  font-size: 18px;
  font-style: italic;
  display: flex;
  align-items: center;
  gap: 8px;
  color: var(--blue);
}

.link svg {
  transform: rotate(90deg);
}

.vinet {
  width: 100%;
  height: 480px;
  background: var(--blue);
  border-radius: 12px;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 32px;
  color: white;
  font-family: var(--medium);
}
</style>

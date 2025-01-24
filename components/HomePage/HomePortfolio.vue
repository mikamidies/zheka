<template>
  <div class="wrap">
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
                <p class="name">Website name</p>
                <p class="sub">Website description, what the heck is this?!</p>
              </div>
              <div class="linker">
                <a href="#" target="_blank" class="link">
                  www.websitelink.com
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
                <p class="name">Website name</p>
                <p class="sub">Website description, what the heck is this?!</p>
              </div>
              <div class="linker">
                <a href="#" target="_blank" class="link">
                  www.websitelink.com
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
                <p class="name">Website name</p>
                <p class="sub">Website description, what the heck is this?!</p>
              </div>
              <div class="linker">
                <a href="#" target="_blank" class="link">
                  www.websitelink.com
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
                <p class="name">Website name</p>
                <p class="sub">Website description, what the heck is this?!</p>
              </div>
              <div class="linker">
                <a href="#" target="_blank" class="link">
                  www.websitelink.com
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
                <p class="name">Website name</p>
                <p class="sub">Website description, what the heck is this?!</p>
              </div>
              <div class="linker">
                <a href="#" target="_blank" class="link">
                  www.websitelink.com
                  <Icon icon="material-symbols:arrow-insert-rounded" />
                </a>
              </div>
            </div>
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
  height: 380px;
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
  display: flex;
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
</style>

<template>
  <div class="wrap">
    <div class="anchor" id="portfolio"></div>
    <div class="container">
      <div class="liner">
        <h4 class="section__title">My Portfolio</h4>

        <div class="items">
          <div class="item" v-for="item in port" :key="item.id">
            <div class="image">
              <img :src="item.img" alt="" class="pic" />
            </div>
            <div class="content">
              <div>
                <p class="name">{{ item.title }}</p>
                <p class="sub">{{ item.desc }}</p>
              </div>
              <div class="linker">
                <a :href="item.link" target="_blank" class="link">
                  {{ formatLink(item.link) }}
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

<script setup>
const port = [
  {
    title: "OKC",
    desc: "Original cosmetics from South Korea",
    img: "assets/img/okc.jpg",
    link: "https://okc.uz",
  },
  {
    title: "Savia",
    desc: "Manufacturer of Faucets and sanitary ware",
    img: "assets/img/savia.webp",
    link: "https://saviagroup.uz",
  },
  {
    title: "Jahon Invest Plast",
    desc: "Manufacturer of plastic consumer goods",
    img: "assets/img/jip.jpg",
    link: "https://jahoninvestplast.com",
  },
  {
    title: "Oson School",
    desc: "Online English Language School",
    img: "assets/img/oson.png",
    link: "https://osonschool.uz",
  },
  {
    title: "Hajtex",
    desc: "Website for the manufacturer of an international textile company",
    img: "assets/img/hajtex.jpg",
    link: "https://osonschool.uz",
  },
  {
    title: "Polimer Group Asia",
    desc: "Leading manufacturer of polymer pipes",
    img: "assets/img/port-4.jpg",
    link: "https://pga.uz",
  },
  {
    title: "Hyper Power Server",
    desc: "Web-server supply shop",
    img: "assets/img/port-2.jpg",
    link: "https://hpsuz.com",
  },
  {
    title: "Rehau Asia",
    desc: "Manufacturer of windows and doors made of Rehau profiles",
    img: "assets/img/rehau.jpg",
    link: "https://osonschool.uz",
  },
  {
    title: "Orzu Osh tuzi",
    desc: "Local manufacturer of iodized salt",
    img: "assets/img/orzu.webp",
    link: "https://osonschool.uz",
  },
  {
    title: "Fintax",
    desc: "Website for accountant company",
    img: "assets/img/port-1.jpg",
    link: "https://fintax.uz",
  },
  {
    title: "Uzbekistan Airways Tech",
    desc: "The only aircraft repair center in central asia",
    img: "assets/img/port-3.jpg",
    link: "https://airtech.uz",
  },
  {
    title: "Premium Pipe",
    desc: "Leading manufacturer of polymer pipes",
    img: "assets/img/port-5.jpg",
    link: "https://premiumpipe.com",
  },
  {
    title: "Home24",
    desc: "Online store for home supplies",
    img: "assets/img/home.jpg",
    link: "https://home24.uz",
  },
];

const formatLink = (url) => url.replace(/^https?:\/\//, "");
</script>

<style scoped>
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
@media (max-width: 1023px) {
  .liner {
    padding: 32px 12px;
    border-top: 1px solid #ebebeb !important;
  }
  .items {
    grid-template-columns: repeat(1, 1fr);
    padding-top: 0;
  }
  .image {
    height: 220px;
  }
  .content {
    grid-template-columns: repeat(1, 1fr);
    padding-top: 12px;
  }
  .name {
    font-size: 24px;
    line-height: 120%;
  }
  .sub {
    font-size: 14px;
  }
  .vinet {
    height: 64px;
    font-size: 20px;
  }
}
</style>

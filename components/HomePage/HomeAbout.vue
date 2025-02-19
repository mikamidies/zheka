<template>
  <div class="wrap">
    <div class="anchor" id="about"></div>
    <div class="container">
      <div class="liner">
        <h4 class="section__title">About me</h4>
        <p class="txt">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Assumenda
          fugit accusantium enim fugiat debitis necessitatibus inventore nulla
          neque possimus eos autem corrupti magni, odit hic. Laudantium
          temporibus facere quaerat, sit corrupti accusamus nihil, non adipisci,
          voluptatibus commodi molestias sunt sint?
        </p>

        <video muted loop playsinline autoplay src="/public/assets/img/video.mp4"></video>
      </div>
    </div>
  </div>
</template>

<style scoped>
.txt {
  font-size: 20px;
  max-width: 80%;
  display: flex;
}

video {
  width: 100%;
  height: 440px;
  margin-top: 24px;
  object-fit: cover;
  border-radius: 12px;
}
</style>

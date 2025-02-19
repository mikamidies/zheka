<template>
  <div class="wrap">
    <div class="anchor" id="contact"></div>
    <div class="container">
      <div class="liner">
        <h4 class="section__title">Contact me</h4>
        <p class="sub">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Libero,
          impedit sequi deserunt ullam magnam consectetur!
        </p>

        <form>
          <input type="text" placeholder="Your name" />
          <input type="text" placeholder="Your number" />

          <button type="submit">Submit</button>
        </form>
      </div>
    </div>
  </div>
</template>

<style scoped>
.liner {
  margin-top: -32px;
  padding-top: 0;
  border-block: 0;
}

.section__title {
  margin-bottom: 12px;
}

form {
  background: #ebebeb;
  display: inline-flex;
  gap: 24px;
  margin-top: 24px;
  padding: 20px 20px 20px 40px;
  border-radius: 32px;
}

input {
  background: transparent;
  border: 0;
  min-width: 300px;
  border-bottom: 1px solid #00000042;
  padding: 12px 0;
  font-size: 18px;
}

input:focus {
  outline: none;
}

button {
  width: 280px;
  background: white;
  border-radius: 18px;
  height: 58px;
  font-family: var(--medium);
  font-size: 20px;
}
</style>

<template>
  <div class="wrap">
    <div class="anchor" id="contact"></div>
    <div class="container">
      <div class="liner">
        <div class="div">
          <h4 class="section__title">Contact me</h4>
          <p class="sub">
            Describe your project or idea, and I'll get in touch soon!
          </p>

          <form>
            <div class="inputs">
              <input type="text" placeholder="Your name" required />
              <input type="text" placeholder="Your number" required />
            </div>
            <textarea placeholder="Message"></textarea>

            <div class="buttoner">
              <button type="submit">Submit</button>
            </div>
          </form>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.liner {
  margin-top: -32px;
}

.div {
  max-width: 1000px;
  margin: 0 auto;
}

.section__title {
  margin-bottom: 12px;
}

form {
  width: 100%;
  background: #ebebeb;
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 24px;
  margin-top: 48px;
  padding: 32px 32px 32px 40px;
  border-radius: 32px;
}

.inputs {
  display: flex;
  flex-direction: column;
  gap: 16px;
}

input,
textarea {
  background: transparent;
  border: 0;
  padding: 16px;
  font-size: 18px;
  background: white;
  border-radius: 16px;
  resize: none;
}

input:focus {
  outline: none;
}

button {
  height: 100%;
  width: 100%;
  background: var(--blue);
  border-radius: 16px;
  font-family: var(--medium);
  font-size: 24px;
  color: white;
}

.buttoner {
  display: flex;
  flex-direction: column;
}
</style>

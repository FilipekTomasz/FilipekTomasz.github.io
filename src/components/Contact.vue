<script setup lang="ts">

</script>
<template>
<section id="contact">
      <p class="text_1">Get in Touch</p>
      <h1 class="text_2">Contact Me</h1>
      <div class="contact-info-container">
        <div class="contact-info-box">
          <img
            src="../assets/email.png"
            alt="Email icon"
            class="icon contact-icon email-icon"
            href="mailto:filipektomasz03@gmail.com"
          />
          <a href="mailto:filipektomasz03@gmail.com">filipektomasz03@gmail.com</a>
        </div>
        <div class="contact-info-box">
          <img
            src="../assets/linkedin.png"
            alt="LinkedIn icon"
            class="icon contact-icon"
            href="https://www.linkedin.com/in/tomasz-filipek-143360221/"
          />
          <a href="https://www.linkedin.com/in/tomasz-filipek-143360221/">LinkedIn</a>
        </div>
      </div>
    </section>
</template>
<style scoped>

#contact {
  display: flex;
  flex-direction: column;
  height: 30vw;
  margin-top: 8vw;
}

.contact-info-container {
  display: flex;
  justify-content: center;
  border-radius: 2rem;
  border: rgb(53, 53, 53) 0.1rem solid;
  border-color: rgb(163, 163, 163);
  background: (250, 250, 250);
  margin: 2rem auto;
  padding: 0.5rem;
}

.contact-info-box {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 0.5rem;
  margin: 1rem;
  text-align: center;

}

.contact-info-container p {
  font-size: larger;
}

.contact-icon {
  cursor: default;
}

.email-icon {
  height: 2.5rem;
}
.icon {
  cursor: pointer;
  height: 2rem;
}

.text_1 {
  text-align: center;
  margin: 0;
}

.text_2 {
  font-size: 3rem;
  text-align: center;
}

a {
  color: black;
  text-decoration: none;
  text-decoration-color: white;
  align-self: center;
  transition: all 300ms ease;

}
@media screen and (max-width: 1400px) {
  #contact {
    height: fit-content;
  }
}

@media screen and (max-width: 600px) {
  .contact-info-container {
    flex-direction: column;
  }
  .contact-info-box{
    align-items: baseline;
    justify-content:start;
    text-align: left;
  }

}





</style>
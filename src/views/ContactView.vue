<template>
  <div class="flex-wrapper">
    <br />
    <h1 class="page-header">Contact</h1>
    <br />
    <div class="contact-wrapper">
      <div class="personal-contact">
        <h2>Caden Ellis</h2>
        <img src="../../public/img/caden.jpg" />
        <br />
        <br />
        <ul>
          <li><a href="caden.ellis77+website@gmail.com">Email</a></li>
          <li>
            <a href="https://www.facebook.com/caden.ellis.98">Facebook</a>
          </li>
          <li><a href="https://github.com/Caden-Ellis77">GitHub</a></li>
          <li>
            <a href="https://www.linkedin.com/in/caden-ellis/">LinkedIn</a>
          </li>
        </ul>
      </div>
      <br />
      <div class="personal-contact">
        <h2>Courtney Ellis</h2>
        <img src="../../public/img/courtney.jpg" />
        <br />
        <br />
        <ul>
          <li><a href="courtneycaloca@gmail+website.com">Email</a></li>
          <li>
            <a href="https://www.facebook.com/courtney.caloca/">Facebook</a>
          </li>
          <li><a href="https://github.com/courtneysellis">GitHub</a></li>
          <li>
            <a href="https://www.linkedin.com/in/courtneysellis/">LinkedIn</a>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ContactView",
};
</script>

<style scoped>
.contact-wrapper {
  display: flex;
  flex-direction: column;
  align-items: center;
}
.personal-contact {
  font-family: Helvetica, sans-serif, Arial;
  font-size: 30px;
  color: black;
}
.personal-contact img {
  width: 150px;
  border-radius: 50%;
}
.personal-contact ul {
  list-style-type: none;
  font-size: 22px;
}
/* Tablet Styles  */
@media only screen and (min-width: 450px) and (max-width: 991px) {
  .contact-wrapper {
    justify-content: space-evenly;
    flex-direction: row;
  }
}

/* Desktop Styles */
@media only screen and (min-width: 992px) {
  .contact-wrapper {
    justify-content: space-evenly;
    flex-direction: row;
  }
}
</style>

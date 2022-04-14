<template>
  <div id="app">
    <div class="spacer">
      <nav class="navbar fixed-top navbar-expand-lg navbar-dark bg-dark">
        <router-link class="navbar-brand" to="/">The Ellis'</router-link>
        <button
          class="navbar-toggler"
          type="button"
          data-toggle="collapse"
          data-target="#navbarNav"
          aria-controls="navbarNav"
          aria-expanded="false"
          aria-label="Toggle navigation"
        >
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarNav">
          <ul class="navbar-nav">
            <li>
              <router-link class="nav-link" to="/blog">Blog</router-link>
            </li>
            <li>
              <router-link class="nav-link" to="/contact">Contact</router-link>
            </li>
          </ul>
        </div>
      </nav>
      <router-view />
    </div>
    <div class="footer">
      <div class="footer-element">
        <span>&copy; 2022</span>
      </div>
      <div class="footer-element">
        <span>Caden and Courtney Ellis</span>
      </div>
      <div class="footer-element">
        <span
          ><a
            href="https://github.com/EllisFam/VueEllisBlog.git"
            target="_blank"
            >GitHub Link</a
          ></span
        >
      </div>
    </div>
  </div>
</template>

<style>
.spacer {
  min-height: 90vh;
}

.page {
  background-color: whitesmoke;
}
.page-header {
  text-align: center;
}
/* Navbar */
.navbar-brand {
  font-family: "Pacifico", cursive !important;
  color: #f5f5f5 !important;
  font-size: 30px !important;
}
.bg-dark {
  background-color: #222 !important;
}
.navbar-nav {
  display: flex !important;
  justify-content: space-evenly !important;
  overflow: hidden;
  flex-wrap: wrap;
  width: 100%;
  padding: 0px 0px 0px 0px;
}
.nav-item {
  display: flex !important;
  justify-content: space-evenly !important;
}
.nav-link {
  color: whitesmoke !important;
  font-family: Helvetica, Arial, sans-serif !important;
  overflow: hidden;
  font-size: 20px;
}
/* Footer */
.footer {
  display: flex;
  justify-content: space-evenly;
  background-color: #222;
  align-items: center;
  margin-top: auto;
  width: 100%;
}
.footer-element {
  display: flex;
  align-items: center;
}
.footer span {
  font-family: Helvetica, Arial, sans-serif !important;
  font-size: 10px;
  padding-top: 10px;
  padding-bottom: 10px;
  color: whitesmoke;
}
.footer span a {
  text-decoration: none;
  color: whitesmoke;
}
.footer span a:hover {
  text-decoration: none;
  color: whitesmoke;
}
/* Tablet Styles  */
@media only screen and (min-width: 450px) and (max-width: 991px) {
  .footer span {
    font-size: 15px;
  }
}

/* Desktop Styles */
@media only screen and (min-width: 992px) {
  .footer span {
    font-size: 17px;
  }
}
</style>

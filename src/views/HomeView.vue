<template>
  <div class="home">
    <div class="flex-wrapper">
      <div class="hero">
        <h1>The Ellis'</h1>
      </div>
      <div class="about">
        <h3>About Us</h3>
        <div class="container">
          <div class="row">
            <div class="col-md">
              <p>
                Hello! We are the Ellis Family. Caden grew up in Abilene, Texas
                and went on a mission to Buenos Aires, Argentina from 2016-2018.
                Courtney was raised in Pleasant Grove, Utah. We met each other
                at BYU in the fall of 2018 during both of our first semesters at
                BYU. Eventually we started dating in the spring of 2019. After a
                busy summer of traveling and getting to know each other more
                (mostly through long distance) we got engaged in August and
                married on November 23, 2019.
              </p>
            </div>
            <hr />
            <div class="col-md">
              <p>
                We love to play games and watch shows together! If you ever want
                to play games with us just ask! We also enjoy making good food
                together and going to Disneyland. We love both the Marvel and
                Star Wars universes. Caden has enjoyed introducing Courtney to
                these, and more, during their relationship.
              </p>
            </div>
          </div>
          <hr />
          <div class="row">
            <div class="col-md">
              <p>
                Caden studied Computer Engineering at BYU and loves to learn new
                things. He is currently working at SchedMD in Lehi, Utah
                developing the
                <a href="https://www.schedmd.com/">Slurm</a> workload manager.
              </p>
            </div>
            <div class="col-md">
              <p>
                Courtney is a fine specimen to behold. She is breath taking and
                frankly Caden is lucky she even gave him a chance. She
                <strong>loves</strong> ice cream. She is currently working at
                <a href="https://www.eidebailly.com/">Eide Bailly</a> as a
                Salesforce Developer and Consultant.
              </p>
            </div>
          </div>
        </div>
        <hr />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "HomeView",
};
</script>

<style scoped>
/* Home Page */
.hero {
  background-image: url(../../public/img/IMG_5287.jpg);
  background-size: cover;
  background-position: center;
  width: 100%;
  height: 740px;
}
h1 {
  font-family: "Pacifico", cursive !important;
}
.hero h1 {
  text-align: center;
  padding-top: 350px;
  font-size: 150px;
  color: rgba(255, 255, 255, 0.479);
}
.about {
  display: flex;
  justify-content: center;
  flex-direction: column;
}
.about h3 {
  text-align: center;
  padding: 18px 50px 10px 50px;
}
.about p {
  font-family: Arial, Helvetica, sans-serif;
  font-size: 15px;
  margin: 0px 50px 10px 50px;
}
.about p a {
  text-decoration: none;
  color: gray;
}
.about p a:hover {
  text-decoration: none;
  color: blue;
}
</style>

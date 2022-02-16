<template>
  <div id="nav">
    <img src="./assets/shared/logo.svg" alt="logo" class="nav__logo" />

    <hr class="line" />
    <div class="navbar">
      <router-link to="/"><strong>00</strong>Home</router-link>
      <router-link to="/Destination"
        ><strong>01</strong>Destination</router-link
      >
      <router-link to="/Crew"><strong>02</strong>Crew</router-link>
      <router-link to="/Technology"><strong>03</strong>Technology</router-link>
    </div>
    <input
      type="checkbox"
      id="mobile__bar"
      style="display: none"
      class="mobile__checkbox"
    />
    <div class="mobile__bar-cover animate__animated animate__fadeInRight">
      <label for="mobile__bar" class="mobile__bar"></label>
    </div>
    <div class="mobile__navbar">
      <div class="mobile__nav">
        <router-link to="/"><strong>00</strong>Home</router-link>
        <router-link to="/Destination"
          ><strong>01</strong>Destination</router-link
        >
        <router-link to="/Crew"><strong>02</strong>Crew</router-link>
        <router-link to="/Technology"
          ><strong>03</strong>Technology</router-link
        >
      </div>
    </div>
  </div>
  <router-view />
</template>

<style>
@import url("https://fonts.googleapis.com/css2?family=Bellefair&display=swap");

:root {
  --black-color: #0b0d17;
  --primary-color: #d0d6f9;
  --white-color: #fff;
  --ash-color: rgb(121, 121, 121);
}
*,
*::after,
*::before {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
body {
  position: relative;
}
html {
  font-size: 10px;
  font-family: "Bellefair", serif;
  font-weight: 400;
  margin: 0;
  color: var(--white-color);
  padding: 0;
}
h1,
h2,
h3,
h4,
h5,
h6 {
  font-weight: 400;
}
/* body{
  background-image:url("./assets/home/background-home-mobile.jpg");
} */
h1 {
  font-size: 10rem;
}
#nav {
  font-size: 2rem;
  color: var(--white-color);
  display: flex;
  justify-content: space-between;
  width: 90%;
  margin: 2.5rem;
  align-items: center;
  position: absolute;
  left: 4%;
}
.line {
  background-color: var(--white-color);
  height: 0.0001px;
  width: 70rem;
  opacity: 0.3;
  z-index: 2;
  margin-right: -15rem;
}
a {
  color: inherit;
  text-decoration: none;
}
.navbar {
  background-color: rgba(136, 136, 136, 0.171);
  padding: 2rem;
  padding-left: 25rem;
  height: 100%;
  backdrop-filter: blur(2rem);
  -webkit-backdrop-filter: blur(2rem);
  transition: all 0.5s ease-in-out;
}
.nav__logo {
  margin-right: 3rem;
}
.navbar > a {
  margin-right: 4rem;
  text-transform: uppercase;
  font-weight: 400;
  font-size: 1.8rem;
  transition: all 0.5s ease-in-out;
}
.mobile__nav > a {
  text-transform: uppercase;
  font-size: 2rem;
  margin-bottom: 5rem !important;
}
.navbar > a > strong,
.mobile__nav > a > strong {
  margin-right: 1rem;
  font-weight: 800;

  font-size: inherit;
}
.navbar > a:hover {
  border-bottom: 0.3rem solid rgba(224, 223, 223, 0.568);
  padding-bottom: 2rem;
}
.navbar > .router-link-exact-active {
  border-bottom: 0.3rem solid var(--white-color);
  padding-bottom: 2rem;
}
.mobile__navbar {
  width: 50%;
  position: absolute;
  right: 0%;
  top: 0%;
  z-index: 1000;
  display: none;
  transition: all 0.4s ease-in-out;
}
.mobile__bar-cover {
  position: absolute;
  right: 2%;
  top: 40%;
  width: 3.8rem;
  z-index: 1100;
  height: 3rem;
  display: none;
}
.mobile__bar,
.mobile__bar::before,
.mobile__bar::after {
  width: 100%;
  position: absolute;
  height: 0.5rem;
  background-color: var(--white-color);
  transition: all 0.2s ease-in;
}
.mobile__bar {
  top: 50%;
}
.mobile__bar::before {
  content: "";
  top: -250%;
}
.mobile__bar::after {
  content: "";
  top: 250%;
}
.mobile__nav {
  width: 100%;
  margin: 0;
  padding-left: 2rem;
  background: #55555541;
  z-index: 1000;
  backdrop-filter: blur(2rem);
  height: 100vh;
  display: absolute;
  top: 45%;
  padding-top: 20rem;
  display: flex;
  flex-direction: column;
  transition: all 0.4s ease-in-out;
}
.mobile__checkbox:checked ~ .mobile__navbar {
  display: block;
}
.mobile__checkbox:checked ~ .mobile__bar-cover > .mobile__bar::after {
  top: 50%;
  transform: rotate(85deg);
}
.mobile__checkbox:checked ~ .mobile__bar-cover > .mobile__bar::before {
  display: none;
}
.mobile__checkbox:checked ~ .mobile__bar-cover > .mobile__bar {
  top: 50%;
  transform: rotate(-45deg);
}
.mobile__checkbox:checked ~ .mobile__bar-cover {
  width: 5rem;
}
.mobile__nav > a {
  margin-bottom: 3rem;
}

@media only screen and (max-width: 82.25rem) {
  .line {
    width: 30rem;
    background-color: red;
    margin-right: -10rem;
  }
}
@media only screen and (max-width: 73.25rem) {
  .line {
    display: none;
  }
  html {
    font-size: 8px;
  }
}
/*TABLET*/
@media only screen and (max-width: 50.25rem) {
  #nav {
    margin: 0px;
    width: 96vw;
  }
  .navbar {
    padding-left: 8rem;
    padding-right: 0px;
    height: 8rem;
  }
  .navbar > a:hover {
    border-bottom: 0.3rem solid rgba(224, 223, 223, 0.568);
    padding-bottom: 4rem;
  }
  .navbar > .router-link-exact-active {
    border-bottom: 0.3rem solid var(--white-color);
    padding-bottom: 4rem;
  }
}
@media only screen and (max-width: 40rem) {
  .navbar {
    padding-left: 2rem;
  }
}
@media only screen and (max-width: 37.5rem) {
  .navbar {
    display: none;
  }
  #nav {
    align-items: start;
  }
  .nav__logo {
    margin-top: 3.2rem;
    width: 4rem;
  }
  .mobile__bar-cover {
    display: block;
  }
}

/**Moblie */
@media only screen and (max-width: 27rem) {
  html {
    font-size: 7px;
  }
}
@media only screen and (max-width: 20rem) {
  html {
    font-size: 6px;
  }
}
</style>

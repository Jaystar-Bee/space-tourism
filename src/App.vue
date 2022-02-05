<template>
  <div id="nav">
    
    <img src="./assets/shared/logo.svg" alt="logo" />
    <hr>
    <div class="navbar">
      <router-link to="/"><strong>00</strong>Home</router-link>
      <router-link to="/Destination"><strong>01</strong>Destination</router-link>
      <router-link to="/Crew"><strong>02</strong>Crew</router-link>
      <router-link to="/Technology"><strong>03</strong>Technology</router-link>
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
}
*,*::after,*::before {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
html {
  font-size: 10px;
  font-family: "Bellefair", serif;
  margin: 0;
  color: var(--white-color);
  padding: 0;
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
hr {
  background-color: var(--white-color);
  height: .0001px;
  width: 40rem;
  z-index: 2;
  margin-right: -20rem;
}
a {
  color: inherit;
  text-decoration: none;
}
.navbar{
  background-color: rgba(136, 136, 136, 0.171);
  padding: 2rem;
  padding-left: 25rem;
  height: 100%;
  backdrop-filter: blur(2rem);
  -webkit-backdrop-filter: blur(2rem);
    transition: all .5s ease-in-out;
}
.navbar > a{
  margin-right: 4rem;
  text-transform: uppercase;
  font-weight: 400;
  font-size: 1.4rem;
  transition: all .5s ease-in-out;
}
.navbar > a > strong {
  margin-right: 1rem;
  font-weight: 800;
  font-size: inherit;
}
.navbar > a:hover {
  border-bottom: .3rem solid rgba(224, 223, 223, 0.568);
  padding-bottom: 2rem;
}
.router-link-exact-active {
  border-bottom: .3rem solid var(--white-color);
  padding-bottom: 2rem;
}
</style>

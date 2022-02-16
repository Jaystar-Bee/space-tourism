<template>
  <div class="home">
    <div class="text__field">
      <div class="text animate__animated animate__backInLeft">
        <h4>So, You want to travel to</h4>
        <h1>Space</h1>
        <p>
          Let’s face it; if you want to go to space, you might as well genuinely
          go to outer space and not hover kind of on the edge of it. Well sit
          back, and relax because we’ll give you a truly out of this world
          experience!
        </p>
      </div>
      <div class="explore animate__animated animate__rollIn">
        <div class="circle"><h2>EXPLORE</h2></div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "homeBody",
  data() {
    return {};
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.home {
  background-image: url("./../../assets/home/background-home-desktop.jpg");
  background-size: cover;
  min-height: 100vh;
}
.text__field {
  margin: 20 auto;
  padding: 10rem;
  align-items: center;
  position: absolute;
  top: 25%;
  display: flex;
}
.text {
  width: 80%;
}
.text > h4 {
  font-size: 2rem;
  text-transform: uppercase;
  letter-spacing: 0.8rem;
}
.text > h1 {
  padding: 1.3rem 0;
  font-size: 18rem;
  text-transform: uppercase;
  font-weight: 400;
  font-family: inherit;
}
.text > p {
  font-size: 2rem;
  width: 80%;
  line-height: 2.8rem;
}
.circle {
  height: 30rem;
  width: 30rem;
  position: relative;
  background-color: var(--white-color);
  border-radius: 100%;
  color: var(--black-color);
  display: flex;
  z-index: 10;
  justify-content: center;
  align-items: center;
  cursor: pointer;
}
.circle::before {
  content: "";
  display: inline-block;
  height: 100%;
  width: 100%;
  border-radius: 100%;
  position: absolute;
  z-index: -1;
  left: 0;
  top: 0;
  background: var(--white-color);
  opacity: 0.5;
  transition: all 0.5s ease-out;
}
.circle:hover::before {
  transform: scale(1.3);
}
.circle > h2 {
  color: #000;
  font-weight: 400;
  font-size: 3rem;
}

@media only screen and (max-width: 56.25rem) {
  .home {
    background-image: url("./../../assets/home/background-home-tablet.jpg");
    height: 110rem;
  }
  .text__field {
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
    top: 15%;
  }
  .text {
    width: 100%;
  }
  .text > h1 {
    font-size: 13rem;
  }
  .text > p {
    width: 100%;
    margin-bottom: 8rem;
  }
  .circle:hover::before {
    transform: scale(1.2);
  }
}

@media only screen and (max-width: 34.4rem) {
  .text > h4 {
    font-size: 1.8rem;
  }
  .text__field {
    padding: 5rem;
  }
  .circle {
    height: 20rem;
    width: 20rem;
  }
}
@media only screen and (max-width: 28rem) {
  .text > h4 {
    font-size: 1.6rem;
  }
  .text__field {
    padding: 2rem;
  }
}
</style>

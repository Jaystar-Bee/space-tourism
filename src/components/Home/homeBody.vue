<template>
  <div class="home">
    <div class="text__field">
      <div class="text">
        <h4>SO, YOU WANT TO TRAVEL TO</h4>
        <h1>SPACE</h1>
        <p>Let’s face it; if you want to go to space, you might as well genuinely go to outer space and not hover kind of on the edge of it. Well sit back, and relax because we’ll give you a truly out of this world experience!</p>
      </div>
      <div class="explore">
        <div class="circle"><h2>EXPLORE</h2></div>
      </div>
    </div>
  </div>
</template>

<script>

export default {
  name: "homeBody",
  data() {
    return {

    }

  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.home{
  background-image: url('./../../assets/home/background-home-desktop.jpg');
  background-size: cover;
  min-height: 100vh;
}
.text__field{
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
}
.text > h1 {
  padding: 1.3rem 0;
}
.text > p {
  font-size: 2rem;
  width: 50%;
  line-height: 2rem;
}
.circle{
  height: 30rem;
  width: 30rem;
  position: relative;
  background-color: var(--white-color);
  border-radius: 100%;
  color: var(--black-color);
  display: inline-block;
  /* justify-content: center;
  align-items: center; */
  opacity: ;
  cursor: pointer;
}
.circle::before {
  content: "";
  display: inline-block;
  height: 100%;
  width: 100%;
  border-radius: 100%;
  z-index: -1 ;
  position: absolute;
  left: 0;
  top: 0;
  background: red;
  transition: all .5s ease-out;
  opacity: .5;
}
.circle:hover::before{
  transform: scale(1.5);
}
.circle >h2 {
  color: #000;
  font-weight: 400;
  font-size: 3rem;
}
</style>

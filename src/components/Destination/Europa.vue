<template>
  <div class="europa">
    <img src="./../../assets/destination/image-europa.png" alt="" />
    <div class="europa__contents">
      <h1>europa</h1>
      <p>
        The smallest of the four Galilean moons orbiting Jupiter, Europa is a
        winter lover’s dream. With an icy surface, it’s perfect for a bit of ice
        skating, curling, hockey, or simple relaxation in your snug wintery
        cabin.
      </p>
      <hr />
      <div class="europa__bottom">
        <div class="distance">
          <p class="distance__topic">AVG. DISTANCE</p>
          <p class="distance__amount">628 MIL. KM</p>
        </div>
        <div class="time">
          <p class="time__topic">EST. TRAVEL TIME</p>
          <p class="time__amount">3 YEARS</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Europa",
  data() {
    return {};
  },
};
</script>

<style scoped>
.europa {
  font-family: inherit;
  margin: 3rem;
  margin-bottom: 0;
  height: inherit;
  display: flex;
  justify-content: space-around;
}
.europa__contents {
  width: 29%;
}
.europa__contents > p {
  font-size: 2.2rem;
  color: rgb(164, 168, 190);
  margin-bottom: 7rem;
  margin-top: 1rem;
}
.europa__contents > h1 {
  margin-left: 1rem;
  text-transform: uppercase;
}
hr {
  width: 100%;
}
.europa__bottom {
  margin-top: 3rem;
  display: flex;
}
.distance {
  margin-right: 20rem;
}
.distance__topic,
.time__topic {
  font-size: 1.2rem;
  color: rgb(164, 168, 190);
  margin: 1rem 0;
}
.distance__amount,
.time__amount {
  font-size: 2.4rem;
}

/**Rsponsiveness */

@media only screen and (max-width: 94.4rem) {
  .distance {
    margin-right: 12rem;
  }
}

@media only screen and (max-width: 73.25rem) {
  .europa__contents {
    width: 33%;
  }
}

@media only screen and (max-width: 50rem) {
  .europa {
    flex-direction: column;
  }
  img {
    width: 70%;
    margin: 0 auto;
    margin-bottom: 4rem;
  }
  .europa__contents {
    margin: 20rem auto;
    text-align: center;
    width: 80%;
  }
  .europa__bottom {
    margin: 3rem auto;
    justify-content: center;
  }
  .distance {
    margin-right: 25rem;
  }
  .distance__amount,
  .time__amount {
    font-size: 2.8rem;
  }
  .europa__contents > p {
    font-size: 2.4rem;
  }
}

@media only screen and (max-width: 34.4rem) {
  .distance {
    margin-right: 16rem;
  }
}
@media only screen and (max-width: 31.4rem) {
  .europa__contents {
    width: 90%;
  }
  img {
    width: 80%;
  }
}
@media only screen and (max-width: 26.6rem) {
  .europa__bottom {
    flex-direction: column;
  }
  .distance {
    margin-right: 0;
    margin-bottom: 2rem;
  }
  .europa__contents {
    width: 95%;
  }
  hr {
    width: 90%;
    margin: 0 auto;
  }
}
</style>
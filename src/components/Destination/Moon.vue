<template>
  <div class="moon">
    <img
      src="./../../assets/destination/image-moon.png"
      alt=""
      class="animate__animated animate__rollIn"
    />
    <div class="moon__contents">
      <h1>Moon</h1>
      <p>
        See our planet as you’ve never seen it before. A perfect relaxing trip
        away to help regain perspective and come back refreshed. While you’re
        there, take in some history by visiting the Luna 2 and Apollo 11 landing
        sites.
      </p>
      <hr />
      <div class="moon__bottom">
        <div class="distance">
          <p class="distance__topic">AVG. DISTANCE</p>
          <p class="distance__amount">384,400 KM</p>
        </div>
        <div class="time">
          <p class="time__topic">EST. TRAVEL TIME</p>
          <p class="time__amount">3 DAYS</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Moon",
  data() {
    return {};
  },
};
</script>

<style scoped>
.moon {
  font-family: inherit;
  margin: 3rem;
  margin-bottom: 0;
  height: inherit;
  display: flex;
  justify-content: space-around;
}
.moon__contents {
  width: 29%;
}
.moon__contents > p {
  font-size: 2.2rem;
  color: rgb(164, 168, 190);
  margin-bottom: 7rem;
  margin-top: 1rem;
}
.moon__contents > h1 {
  margin-left: 1rem;
  text-transform: uppercase;
}
hr {
  width: 100%;
}
.moon__bottom {
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
  .moon__contents {
    width: 33%;
  }
}

@media only screen and (max-width: 50rem) {
  .moon {
    flex-direction: column;
  }
  img {
    width: 70%;
    margin: 0 auto;
    margin-bottom: 4rem;
  }
  .moon__contents {
    margin: 20rem auto;
    text-align: center;
    width: 80%;
  }
  .moon__bottom {
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
  .moon__contents > p {
    font-size: 2.4rem;
  }
}

@media only screen and (max-width: 34.4rem) {
  .distance {
    margin-right: 16rem;
  }
}
@media only screen and (max-width: 31.4rem) {
  .moon__contents {
    width: 90%;
  }
  img {
    width: 80%;
  }
}
@media only screen and (max-width: 26.6rem) {
  .moon__bottom {
    flex-direction: column;
  }
  .distance {
    margin-right: 0;
    margin-bottom: 2rem;
  }
  .moon__contents {
    width: 95%;
  }
  hr {
    width: 90%;
    margin: 0 auto;
  }
}
</style>
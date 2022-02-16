<template>
  <div class="titan">
    <img
      src="./../../assets/destination/image-titan.png"
      alt=""
      class="animate__animated animate__rollIn"
    />
    <div class="titan__contents">
      <h1>titan</h1>
      <p>
        The only moon known to have a dense atmosphere other than Earth, Titan
        is a home away from home (just a few hundred degrees colder!). As a
        bonus, you get striking views of the Rings of Saturn.
      </p>
      <hr />
      <div class="titan__bottom">
        <div class="distance">
          <p class="distance__topic">AVG. DISTANCE</p>
          <p class="distance__amount">1.6 BIL. KM</p>
        </div>
        <div class="time">
          <p class="time__topic">EST. TRAVEL TIME</p>
          <p class="time__amount">7 YEARS</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Titan",
  data() {
    return {};
  },
};
</script>

<style scoped>
.titan {
  font-family: inherit;
  margin: 3rem;
  margin-bottom: 0;
  height: inherit;
  display: flex;
  justify-content: space-around;
}
.titan__contents {
  width: 29%;
}
.titan__contents > p {
  font-size: 2.2rem;
  color: rgb(164, 168, 190);
  margin-bottom: 7rem;
  margin-top: 1rem;
}
.titan__contents > h1 {
  margin-left: 1rem;
  text-transform: uppercase;
}
hr {
  width: 100%;
}
.titan__bottom {
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
  .titan__contents {
    width: 33%;
  }
}

@media only screen and (max-width: 50rem) {
  .titan {
    flex-direction: column;
  }
  img {
    width: 70%;
    margin: 0 auto;
    margin-bottom: 4rem;
  }
  .titan__contents {
    margin: 20rem auto;
    text-align: center;
    width: 80%;
  }
  .titan__bottom {
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
  .titan__contents > p {
    font-size: 2.4rem;
  }
}

@media only screen and (max-width: 34.4rem) {
  .distance {
    margin-right: 16rem;
  }
}
@media only screen and (max-width: 31.4rem) {
  .titan__contents {
    width: 90%;
  }
  img {
    width: 80%;
  }
}
@media only screen and (max-width: 26.6rem) {
  .titan__bottom {
    flex-direction: column;
  }
  .distance {
    margin-right: 0;
    margin-bottom: 2rem;
  }
  .titan__contents {
    width: 95%;
  }
  hr {
    width: 90%;
    margin: 0 auto;
  }
}
</style>
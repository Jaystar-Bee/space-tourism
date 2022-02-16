<template>
  <div class="mars">
    <img
      src="./../../assets/destination/image-mars.png"
      alt=""
      class="animate__animated animate__rollIn"
    />
    <div class="mars__contents">
      <h1>mars</h1>
      <p>
        Don’t forget to pack your hiking boots. You’ll need them to tackle
        Olympus Mons, the tallest planetary mountain in our solar system. It’s
        two and a half times the size of Everest!
      </p>
      <hr />
      <div class="mars__bottom">
        <div class="distance">
          <p class="distance__topic">AVG. DISTANCE</p>
          <p class="distance__amount">225 MIL. KM</p>
        </div>
        <div class="time">
          <p class="time__topic">EST. TRAVEL TIME</p>
          <p class="time__amount">9 MONTHS</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Mars",
  data() {
    return {};
  },
};
</script>

<style scoped>
.mars {
  font-family: inherit;
  margin: 3rem;
  margin-bottom: 0;
  height: inherit;
  display: flex;
  justify-content: space-around;
}
.mars__contents {
  width: 29%;
}
.mars__contents > p {
  font-size: 2.2rem;
  color: rgb(164, 168, 190);
  margin-bottom: 7rem;
  margin-top: 1rem;
}
.mars__contents > h1 {
  margin-left: 1rem;
  text-transform: uppercase;
}
hr {
  width: 100%;
}
.mars__bottom {
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
  .mars__contents {
    width: 33%;
  }
}

@media only screen and (max-width: 50rem) {
  .mars {
    flex-direction: column;
  }
  img {
    width: 70%;
    margin: 0 auto;
    margin-bottom: 4rem;
  }
  .mars__contents {
    margin: 20rem auto;
    text-align: center;
    width: 80%;
  }
  .mars__bottom {
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
  .mars__contents > p {
    font-size: 2.4rem;
  }
}

@media only screen and (max-width: 34.4rem) {
  .distance {
    margin-right: 16rem;
  }
}
@media only screen and (max-width: 31.4rem) {
  .mars__contents {
    width: 90%;
  }
  img {
    width: 80%;
  }
}
@media only screen and (max-width: 26.6rem) {
  .mars__bottom {
    flex-direction: column;
  }
  .distance {
    margin-right: 0;
    margin-bottom: 2rem;
  }
  .mars__contents {
    width: 95%;
  }
  hr {
    width: 90%;
    margin: 0 auto;
  }
}
</style>
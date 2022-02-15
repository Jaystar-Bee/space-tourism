<template>
  <div class="flight">
    <div class="text">
      <h2 class="text__topic">flight engineer</h2>
      <h1 class="text__name">Anousheh Ansari</h1>
      <p class="text__body">
        Anousheh Ansari is an Iranian American engineer and co-founder of Prodea
        Systems. Ansari was the fourth self-funded space tourist, the first
        self-funded woman to fly to the ISS, and the first Iranian in space.
      </p>
    </div>
    <img
      src="./../../assets/crew/image-anousheh-ansari.png"
      alt="Anousheh Ansari"
    />
  </div>
</template>
<script>
export default {
  name: "flight",
};
</script>

<style scoped>
.flight {
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.text {
  width: 50%;
}
.text__topic,
.text__name {
  text-transform: uppercase;
}
.text__topic {
  color: var(--ash-color);
  font-size: 5rem;
  margin-bottom: 3rem;
}
.text__name {
  font-size: 6rem;
  font-weight: 400;
  margin-bottom: 2rem;
}
.text__body {
  font-size: 2.1rem;
  line-height: 3rem;
  color: rgb(164, 168, 190);
}

/**REsponsiveness */
@media only screen and (max-width: 79.35rem) {
  img {
    width: 45rem;
  }
  .text__name {
    font-size: 4.5rem;
  }
  .text__topic {
    font-size: 3.5rem;
  }
}
@media only screen and (max-width: 59.4rem) {
  img {
    width: 40rem;
    justify-self: end;
  }
}

/**Tablet */
@media only screen and (max-width: 50rem) {
  .flight {
    flex-direction: column;
    text-align: center;
    margin-top: 10rem;
  }
  .text {
    margin-bottom: 15rem;
    width: 70%;
  }
  img {
    margin-bottom: 10rem;
  }
}
@media only screen and (max-width: 40rem) {
  .text {
    width: 80%;
  }
}
@media only screen and (max-width: 31.5rem) {
  .text {
    width: 100%;
  }
  .text__topic {
    font-size: 3rem;
  }
  .text__name {
    font-size: 4rem;
  }
}

/**Mobile */
@media only screen and (max-width: 26.6rem) {
  .flight {
    flex-direction: column-reverse;
  }
  img {
    margin-bottom: 12rem;
  }
  .text {
    margin-bottom: 8rem;
  }
}

@media only screen and (max-width: 23.2rem) {
  .text {
    margin-bottom: 2rem;
  }
  img {
    margin-bottom: 15rem;
  }
}
</style>
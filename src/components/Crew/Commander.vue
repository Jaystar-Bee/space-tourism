<template>
  <div class="commander">
    <div class="text">
      <h2 class="text__topic">Commander</h2>
      <h1 class="text__name">douglas hurley</h1>
      <p class="text__body">
        Douglas Gerald Hurley is an American engineer, former Marine Corps pilot
        and former NASA astronaut. He launched into space for the third time as
        commander of Crew Dragon Demo-2.
      </p>
    </div>
    <img
      src="./../../assets/crew/image-douglas-hurley.png"
      alt="Douglas Hurley"
      class="animate__animated animate__fadeInDown"
    />
  </div>
</template>
<script>
export default {
  name: "Commander",
};
</script>

<style scoped>
.commander {
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
  .commander {
    flex-direction: column;
    text-align: center;
    margin-top: 10rem;
  }
  .text {
    margin-bottom: 15rem;
    width: 60%;
  }
  img {
    border-bottom: 1.8px solid var(--ash-color);
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
  .commander {
    flex-direction: column-reverse;
  }
  img {
    margin-bottom: 12rem;
  }
}
</style>
<template>
  <div class="pilot">
    <div class="text">
      <h2 class="text__topic">pilot</h2>
      <h1 class="text__name">victor glover</h1>
      <p class="text__body">
        Pilot on the first operational flight of the SpaceX Crew Dragon to the
        International Space Station. Glover is a commander in the U.S. Navy
        where he pilots an F/A-18.He was a crew member of Expedition 64, and
        served as a station systems flight engineer.
      </p>
    </div>
    <img
      src="./../../assets/crew/image-victor-glover.png"
      alt="Victor Glover"
      class="animate__animated animate__fadeInDown"
    />
  </div>
</template>
<script>
export default {
  name: "Pilot",
};
</script>

<style scoped>
.pilot {
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
  .pilot {
    flex-direction: column;
    text-align: center;
    margin-top: 10rem;
  }
  .text {
    margin-bottom: 25rem;
    width: 70%;
  }
  img {
    border-bottom: 1.8px solid var(--ash-color);
  }
}
@media only screen and (max-width: 40rem) {
  .text {
    width: 90%;
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
  .pilot {
    flex-direction: column-reverse;
  }
  img {
    margin-bottom: 12rem;
  }
  .text {
    margin-bottom: 5rem;
  }
}
</style>
<template>
  <div class="mission">
    <div class="text">
      <h2 class="text__topic">Mission Specialist</h2>
      <h1 class="text__name">Mark Shuttleworth</h1>
      <p class="text__body">
        Mark Richard Shuttleworth is the founder and CEO of Canonical, the
        company behind the Linux-based Ubuntu operating system. Shuttleworth
        became the first South African to travel to space as a space tourist.
      </p>
    </div>
    <img
      src="./../../assets/crew/image-mark-shuttleworth.png"
      alt="Mark Shuttleworth"
    />
  </div>
</template>
<script>
export default {
  name: "Mission",
};
</script>

<style scoped>
.mission {
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
  .mission {
    flex-direction: column;
    text-align: center;
    margin-top: 10rem;
  }
  .text {
    margin-bottom: 15rem;
    width: 60%;
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
  .mission {
    flex-direction: column-reverse;
  }
  img {
    margin-bottom: 12rem;
  }
  .text {
    margin-bottom: 18rem;
  }
}
@media only screen and (max-width: 24.6rem) {
  .text {
    margin-bottom: 10rem;
  }
}
@media only screen and (max-width: 22.6rem) {
  .text {
    margin-bottom: 8rem;
  }
}
</style>
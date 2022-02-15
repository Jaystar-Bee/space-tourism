<template>
  <div class="crew">
    <div class="crew__header">
      <h1><strong>02</strong>Meet your crew</h1>
    </div>
    <Commander />

    <div class="carousel__cover">
      <div
        class="carousel__button"
        :class="{ active: isActive('commander') }"
        @click="setActive('commander')"
      ></div>
      <div class="carousel__button"></div>
      <div class="carousel__button"></div>
      <div class="carousel__button"></div>
    </div>
  </div>
</template>

<script>
import Commander from "./../components/Crew/Commander.vue";
export default {
  name: "Crew",
  components: {
    Commander,
  },
  data() {
    return {
      activeTab: "commander",
    };
  },
  methods: {
    setActive(tab) {
      this.activeTab = tab;
    },
    isActive(tab) {
      return this.activeTab === tab;
    },
  },
};
</script>

<style scoped>
.crew {
  background-color: var(--black-color);
  background-image: url(./../assets/crew/background-crew-desktop.jpg);
  background-size: cover;
  min-height: 100vh;
  padding: 10rem;
  padding-left: 20rem;
  /* position: relative; */
}
.crew__header {
  text-transform: uppercase;
  font-size: 2.8rem;
  letter-spacing: 1rem;
  margin-top: 10rem;
}

.crew__header > h1 {
  font-size: inherit;
}
.crew__header > h1 > strong {
  margin-right: 2.4rem;
  color: rgb(121, 121, 121);
}
.carousel__cover {
  display: flex;
  position: absolute;
  top: 80%;
}
.carousel__button {
  background-color: rgb(92, 92, 92);
  width: 2rem;
  height: 2rem;
  border-radius: 100%;
  transition: all 0.4s ease-in-out;
}
.carousel__button:hover {
  background-color: var(--ash-color);
}
.carousel__button:not(:last-of-type) {
  margin-right: 2rem;
}
.active {
  background: var(--white-color);
}

/**Responsiveness */
@media only screen and (max-width: 90rem) {
  .crew {
    padding-left: 12rem;
  }
}
@media only screen and (max-width: 52.25rem) {
  .crew {
    padding: 6rem;
    padding-left: 8rem;
  }
}
@media only screen and (max-width: 52.25rem) {
  .crew {
    padding: 6rem;
  }
}
</style>
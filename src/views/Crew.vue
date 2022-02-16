<template>
  <div class="crew">
    <div class="crew__header">
      <h1><strong>02</strong>Meet your crew</h1>
    </div>
    <Commander v-if="isActive('commander')" />
    <Mission v-if="isActive('mission')" />
    <Pilot v-if="isActive('pilot')" />
    <Flight v-if="isActive('flight')" />

    <div class="carousel__cover">
      <div
        class="carousel__button"
        :class="{ active: isActive('commander') }"
        @click="setActive('commander')"
      ></div>
      <div
        class="carousel__button"
        :class="{ active: isActive('mission') }"
        @click="setActive('mission')"
      ></div>
      <div
        class="carousel__button"
        :class="{ active: isActive('pilot') }"
        @click="setActive('pilot')"
      ></div>
      <div
        class="carousel__button"
        :class="{ active: isActive('flight') }"
        @click="setActive('flight')"
      ></div>
    </div>
  </div>
</template>

<script>
import Commander from "./../components/Crew/Commander.vue";
import Mission from "./../components/Crew/Mission.vue";
import Pilot from "./../components/Crew/Pilot.vue";
import Flight from "./../components/Crew/Flight.vue";
export default {
  name: "Crew",
  components: {
    Commander,
    Mission,
    Pilot,
    Flight,
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
  letter-spacing: 0.8rem;
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
  background-color: var(--white-color);
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

/**Tablet */
@media only screen and (max-width: 50rem) {
  .crew {
    background-image: url(./../assets/crew/background-crew-tablet.jpg);
  }
  .carousel__cover {
    top: 45%;
    left: 50%;
    transform: translate(-45%, -50%);
  }
  .carousel__button:not(:last-of-type) {
    margin-right: 4.5rem;
  }
}

/**Mobile */
@media only screen and (max-width: 26.6rem) {
  .crew {
    background-image: url(./../assets/crew/background-crew-mobile.jpg);
  }
  .carousel__cover {
    top: 65%;
    left: 54%;
    transform: translate(-65%, -50%);
  }
  .carousel__button:not(:last-of-type) {
    margin-right: 2.5rem;
  }
  .crew__header {
    letter-spacing: 0.6rem;
    font-size: 2.4rem;
  }
}
</style>
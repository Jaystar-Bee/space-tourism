<template>
  <div class="technology">
    <div class="technology__heading animate__animated animate__rubberBand">
      <h1><strong>03</strong> space launch 101</h1>
    </div>
    <main class="technology__body">
      <div class="carousel__cover">
        <div
          class="carousel__button"
          @click="setActive('vehicle')"
          :class="{ active: isActive('vehicle') }"
        >
          1
        </div>
        <div
          class="carousel__button"
          @click="setActive('port')"
          :class="{ active: isActive('port') }"
        >
          2
        </div>
        <div
          class="carousel__button"
          @click="setActive('capsule')"
          :class="{ active: isActive('capsule') }"
        >
          3
        </div>
      </div>
      <Vehicle v-if="isActive('vehicle')" />
      <Port v-if="isActive('port')" />
      <Capsule v-if="isActive('capsule')" />
    </main>
  </div>
</template>

<script>
import Vehicle from "./../components/Technology/Vehicle.vue";
import Port from "./../components/Technology/Port.vue";
import Capsule from "./../components/Technology/Capsule.vue";
export default {
  name: "Technology",
  components: {
    Vehicle,
    Port,
    Capsule,
  },
  data() {
    return {
      activeTab: "vehicle",
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
.technology {
  padding: 10rem;
  padding-left: 20rem;
  min-height: 100vh;
  background-color: var(--black-color);
  background-image: url(./../assets/technology/background-technology-desktop.jpg);
  background-size: cover;
}
.technology__heading {
  font-size: 2.8rem;
  letter-spacing: 0.8rem;
  text-transform: uppercase;
  margin-top: 10rem;
}
.technology__heading > h1 {
  font-size: inherit;
}
.technology__heading > h1 > strong {
  color: var(--ash-color);
  font-weight: 900;
}
.technology__body {
  display: flex;
  margin-top: 5rem;
}
.carousel__cover {
  margin-right: 5rem;
}
.carousel__button {
  height: 7rem;
  width: 7rem;
  border: 2px solid rgb(90, 90, 90);
  border-radius: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 2rem;
  font-weight: 900;
  transition: all 0.4s ease-in-out;
}
.carousel__button:hover {
  border: 2px solid var(--ash-color);
}
.carousel__button:not(:last-of-type) {
  margin-bottom: 4rem;
}
.active {
  color: var(--black-color);
  background-color: var(--white-color);
  border: 2px solid var(--white-color);
}

/**Responsive */
@media only screen and (max-width: 81rem) {
  .technology {
    padding-left: 15rem;
  }
}
@media only screen and (max-width: 56.25rem) {
  .technology {
    padding: 7rem;
    padding-left: 10rem;
  }
}
@media only screen and (max-width: 52rem) {
  .carousel__cover {
    margin-right: 3rem;
  }
}
/**Tablet */
@media only screen and (max-width: 50rem) {
  .technology {
    background-image: url(./../assets/technology/background-technology-tablet.jpg);
    padding: 0;
  }
  .technology__heading {
    padding-top: 15rem;
    margin: 0;
  }
  .technology__heading > h1 {
    margin-left: 3rem;
  }
  .technology__body {
    flex-direction: column;
    text-align: center;
    position: relative;
  }
  .carousel__cover {
    position: absolute;
    display: flex;
    top: 65%;
    left: 50%;
    transform: translate(-50%, -65%);
    flex-direction: row;
  }
  .text {
    padding: 0 2rem;
  }
  .carousel__button {
    width: 5rem;
    height: 5rem;
  }
  .carousel__button:not(:last-of-type) {
    margin-right: 3rem;
  }
}
@media only screen and (max-width: 45.5rem) {
  .carousel__cover {
    top: 63%;
  }
}
@media only screen and (max-width: 41.9rem) {
  .carousel__cover {
    top: 61%;
  }
}
@media only screen and (max-width: 38.5rem) {
  .carousel__cover {
    top: 57%;
  }
}
@media only screen and (max-width: 36.5rem) {
  .carousel__cover {
    top: 55%;
  }
}
@media only screen and (max-width: 30rem) {
  .carousel__cover {
    top: 52%;
  }
}
/**Mobile */
@media only screen and (max-width: 26.6rem) {
  .technology {
    background-image: url(./../assets/technology/background-technology-mobile.jpg);
  }
  .carousel__cover {
    top: 50%;
  }
  .technology__heading > h1 {
    text-align: center;
    margin: 0;
    letter-spacing: 0.5rem;
    width: 100%;
  }
}
@media only screen and (max-width: 21.3rem) {
  .carousel__cover {
    top: 47%;
  }
}
</style>

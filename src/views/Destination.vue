<template>
  <div class="destination">
    <div class="destination__heading">
      <div class="pick animate__animated animate__rubberBand">
        <p><strong>01</strong>Pick your Destination</p>
      </div>
      <div class="destination__router">
        <p
          class="destination__link"
          @click="setActive('moon')"
          :class="{ active: isActive('moon') }"
        >
          Moon
        </p>
        <p
          class="destination__link"
          @click="setActive('mars')"
          :class="{ active: isActive('mars') }"
        >
          Mars
        </p>
        <p
          class="destination__link"
          @click="setActive('europa')"
          :class="{ active: isActive('europa') }"
        >
          Europa
        </p>
        <p
          class="destination__link"
          @click="setActive('titan')"
          :class="{ active: isActive('titan') }"
        >
          Titan
        </p>
      </div>
    </div>
    <div class="destination__view">
      <Moon v-if="isActive('moon')" />
      <Mars v-if="isActive('mars')" />
      <Europa v-if="isActive('europa')" />
      <Titan v-if="isActive('titan')" />
    </div>
  </div>
</template>

<script>
import Moon from "./../components/Destination/Moon.vue";
import Mars from "./../components/Destination/Mars.vue";
import Titan from "./../components/Destination/Titan.vue";
import Europa from "./../components/Destination/Europa.vue";
export default {
  name: "Destination",
  data() {
    return {
      activeTab: "moon",
    };
  },
  components: {
    Moon,
    Mars,
    Europa,
    Titan,
  },
  methods: {
    setActive(tab) {
      this.activeTab = tab;
    },
    isActive(tab) {
      return this.activeTab === tab;
    },
  },
  computed: {},
};
</script>

<style scoped>
.destination {
  background-color: var(--black-color);
  background-image: url(./../assets/destination/background-destination-desktop.jpg);
  background-size: cover;
  min-height: 100vh;
  padding-top: 20rem;
  font-size: inherit;
}
.destination__heading {
  display: flex;
  height: 10rem;
  font-size: 2.5rem;
  position: relative;
  justify-content: space-around;
}
.pick > p {
  letter-spacing: 0.7rem;
  text-transform: uppercase;
}
.pick > p > strong {
  color: rgb(121, 121, 121);
  margin-right: 2.5rem;
}
.destination__router {
  display: flex;
  align-self: end;
  font-size: 1.6rem;
  height: 2.5rem;
  width: 30%;
}
.destination__link {
  color: rgb(164, 168, 190);
  cursor: pointer;
  display: inline-block;
  text-transform: uppercase;
  backface-visibility: hidden;
  transition: all 0.3s ease-in-out;
}
.destination__link {
  margin-right: 1.5rem;
}
.destination__link:hover {
  border-bottom: 0.3rem solid rgb(160, 160, 160);
}
.active {
  color: var(--white-color);
  border-bottom: 0.3rem solid var(--white-color);
}

/**Rsponsiveness */

@media only screen and (max-width: 50rem) {
  .destination {
    background-image: url(./../assets/destination/background-destination-tablet.jpg);
  }
  .destination__router {
    position: absolute;
    top: 92vh;
    width: 100%;
    margin: 0 auto;
    justify-content: center;
  }
  .pick > p {
    margin-left: -25rem;
  }
}
@media only screen and (max-width: 45rem) {
  .destination__router {
    top: 85vh;
  }
}
@media only screen and (max-width: 41.3rem) {
  .destination__router {
    top: 82vh;
  }
  .pick > p {
    margin-left: -20rem;
  }
}
@media only screen and (max-width: 36.6rem) {
  .pick > p {
    margin-left: -15rem;
    font-size: 2.4rem;
    letter-spacing: 0.5rem;
  }
}
@media only screen and (max-width: 34.7rem) {
  .destination__router {
    top: 78vh;
  }
  .pick > p {
    margin-left: -12rem;
  }
}
@media only screen and (max-width: 31.25rem) {
  .destination {
    background-image: url(./../assets/destination/background-destination-mobile.jpg);
  }
  .destination__router {
    top: 70vh;
  }
  .pick > p {
    margin-left: -8rem;
  }
}
@media only screen and (max-width: 27.5rem) {
  .destination__router {
    top: 65vh;
  }
}
@media only screen and (max-width: 26.9rem) {
  .destination__link {
    font-size: 1.8rem;
  }
  .destination__router {
    top: 60vh;
  }
}
@media only screen and (max-width: 26.9rem) {
  .pick > p {
    margin-left: -10rem;
    letter-spacing: 0.3rem;
  }
}
@media only screen and (max-width: 22.5rem) {
  .destination__router {
    top: 55vh;
  }
  .pick > p {
    margin-left: -6rem;
    letter-spacing: 0.3rem;
  }
  .pick > p > strong {
    margin-right: 2rem;
  }
}
</style>
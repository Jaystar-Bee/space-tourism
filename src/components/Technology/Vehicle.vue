<template>
  <div class="vehicle">
    <div class="text">
      <div class="text__topic">The terminology ...</div>
      <h1 class="text__name">Launch vehicle</h1>
      <p class="text__body animate__animated animate__zoomIn">
        A launch vehicle or carrier rocket is a rocket-propelled vehicle used to
        carry a payload from Earth's surface to space, usually to Earth orbit or
        beyond. Our WEB-X carrier rocket is the most powerful in operation.
        Standing 150 metres tall, it's quite an awe-inspiring sight on the
        launch pad!
      </p>
    </div>
    <img
      src="./../../assets/technology/image-launch-vehicle-portrait.jpg"
      alt=" Portrait"
      class="portrait animate__animated animate__fadeIn"
    />
    <img
      src="./../../assets/technology/image-launch-vehicle-landscape.jpg"
      alt=" Landscape"
      class="landscape"
    />
  </div>
</template>
<style scoped>
.vehicle {
  display: flex;
  justify-content: space-between;
}
.text__topic,
.text__body {
  color: rgb(164, 168, 190);
  font-size: 2.1rem;
}
.text__topic,
.text__name {
  text-transform: uppercase;
}
.text__name {
  font-size: 8rem;
  margin: 2rem 0;
}
.text__body {
  line-height: 3rem;
  width: 65%;
}
.landscape {
  display: none;
}
/**Responsive */
@media only screen and (max-width: 102.5rem) {
  .text__name {
    font-size: 6rem;
  }
  .text__body {
    width: 75%;
  }
}
@media only screen and (max-width: 91.5rem) {
  .text__body {
    width: 80%;
  }
  .portrait {
    width: 40%;
  }
}
@media only screen and (max-width: 81.25rem) {
  .text__name {
    font-size: 5rem;
  }
}

/**Tablet */
@media only screen and (max-width: 50rem) {
  .vehicle {
    flex-direction: column-reverse;
    align-items: center;
  }
  .landscape {
    margin-bottom: 15rem;
    display: block;
    width: 100vw;
  }
  .text__name {
    font-size: 4rem;
  }
  .portrait {
    display: none;
  }
  .text__body {
    width: 70%;
    margin: 3rem auto;
  }
}
@media only screen and (max-width: 26.6rem) {
  .text__body {
    width: 80%;
  }
}
</style>
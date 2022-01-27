<template>
  <div
    v-for="place in places"
    :key="place.city"
  >
    <slot name="country" :place="place.country" id="1" :log="logPlaces"> </slot>
    <slot name="city" :place="place.city" id="2"> </slot>
  </div>
</template>

<script>
export default {
  name: "Places",
  setup() {
    const places = [
      { country: "GB", city: "London" },
      { country: "IT", city: "Rome" },
      { country: "USA", city: "New York" },
    ];

    const logPlaces = () => {
      console.log('places', places);
    }


    return {
      places,
      logPlaces
    };
  },
};
</script>
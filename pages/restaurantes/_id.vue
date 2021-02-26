<template>
  <div>
    <h1>{{ restaurant.name }}</h1>
    <img :src="restaurant.img" />
    <p>{{ restaurant.description }}</p>
  </div>
</template>

<script>
export default {
  async asyncData({ params, $axios }) {
    const restaurant = await $axios.$get(
      `http://localhost:3001/restaurants/${params.id}`
    );
    return { restaurant };
  }
};
</script>

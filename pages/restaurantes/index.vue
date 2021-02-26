<template>
  <div>
    <h1>Restaurantes</h1>
    <item-card
      v-for="(restaurant, key) in restaurants"
      :key="key"
      :name="restaurant.name"
      :description="restaurant.description"
      :img="restaurant.img"
      :id="restaurant.id"
    />
  </div>
</template>

<script>
export default {
  async asyncData({ $axios }) {
    const restaurants = await $axios.$get("http://localhost:3001/restaurants");
    return { restaurants };
  }
};
</script>

<template>
  <div>
    <h1>Pajarerías</h1>
    <item-card
      v-for="(pajareria, key) in pajarerias"
      :key="key"
      :name="pajareria.name"
      :description="pajareria.description"
      :img="pajareria.img"
    />
  </div>
</template>

<script>
export default {
  async asyncData({ params, $axios }) {
    const pajarerias = await $axios.$get("http://localhost:3001/birdShop");
    return { pajarerias };
  }
};
</script>

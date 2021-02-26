<template>
  <div>
    <b-card
      :title="name"
      :img-src="img"
      img-alt="Image"
      img-top
      tag="article"
      style="max-width: 20rem;"
      class="mb-2"
    >
      <b-card-text>
        {{ description }}
      </b-card-text>
      <b-button :to="'restaurantes/' + `${id}`" variant="primary">Ver</b-button>
    </b-card>
  </div>
</template>

<script>
export default {
  props: ["name", "description", "img", "id"]
};
</script>

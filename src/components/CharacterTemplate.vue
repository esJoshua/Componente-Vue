<template>
  <div class="container">
    <div class="row">
      <div
        class="col-12 d-flex flex-row align-items-center"
        v-for="(character, i) in dataCharacter"
        :key="i"
      >
        <img :src="character.src" :alt="character.nombre" />
        <p>{{ character.nombre }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "CharacterTemplate",
  props: {
    dataCharacter: {
      type: Array,
      default: () => {},
    },
  },
};
</script>

<style scoped lang="scss">
img {
  width: 200px;
  border-radius: 50%;
  padding: 2rem;
}
p {
  color: green;
  font-size: 2rem;
  font-style: italic;
}
</style>

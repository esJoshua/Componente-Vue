<template>
  <div class="container">
    <!-- METODO 1
      <div class="row">
      <div
        class="col-12 d-flex flex-row align-items-center"
        v-for="(character, i) in dataCharacter"
        :key="i"
      >
        <img :src="character.src" :alt="character.nombre" />
        <p>{{ character.nombre }}</p>
      </div>
    </div> -->
    <!-- METODO 2 -->
    <div class="col-12 d-flex flex-row align-items-center">
      <img :src="dataCharacter.src" :alt="dataCharacter.nombre" />
      <p>{{ dataCharacter.nombre }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "CharacterTemplate",
  props: {
    /*METODO 1
     dataCharacter: {
      type: Array,
      default: () => [],
    }, */
    /* METODO 2 */
    dataCharacter: {
      type: Object,
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

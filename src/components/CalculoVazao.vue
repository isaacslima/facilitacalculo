<template>
  <div class="hello">
    <h1>Calcula Vazão</h1>
    <p>
      Insira os dados para Calcular a vazão de água por tempo.
    </p>
    <input v-model="tempo" type="number"/> em segundos
    <br>
    <input v-model="quantidade" type="number"/> em ml
    <br>
    <button type="submit" @click="calcular()">Calcular</button>
    <br>
    <h3 v-if="show">
      Total de vazão: {{ total }} L/h (litros por hora)
    </h3>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'CalculoVazao',
  data() {
    return {
      tempo: 0,
      quantidade: 0,
      total: 0,
      show: false
    }
  },
  methods: {
    calcular(): void {
      console.log(this.quantidade)
      console.log(this.tempo)
      this.total = 3.6 * this.quantidade / this.tempo
      console.log(this.total)
      this.show = true
    }
  }
});
</script>
<style scoped lang="scss">

</style>

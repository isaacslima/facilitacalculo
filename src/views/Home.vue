<template>
  <div class="home">
    <CalculoVazao/>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import CalculoVazao from '@/components/CalculoVazao.vue'; // @ is an alias to /src

export default defineComponent({
  name: 'Home',
  components: {
    CalculoVazao,
  },
});
</script>

<template>
    <div class="dueños">
<formularioDueños/> 
<tablaDueños/>
    </div>
</template>

<script>
import formularioDueños from '@/components/formularioDueños.vue'
import tablaDueños from '@/components/tablaDueños.vue'

export default {
  name: 'Dueños',
  components: {
    formularioDueños,tablaDueños
  }
}

</script>

<style scoped>
.dueños{
    text-align: center;
}
</style>

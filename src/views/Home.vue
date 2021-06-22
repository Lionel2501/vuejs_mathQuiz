<template>
  <div class="home">
    <h1>Math Quizz App</h1>
    <OperatorQuizz v-if="operator" :operator="operator" @onBack="clearOperator"/>
    <OperatorSelector v-if="!operator" @selectOperator="selectOperator"/>
  </div>
</template>

<script>
import OperatorSelector from '@/components/OperatorSelector.vue'
import OperatorQuizz from '../components/OperatorQuizz.vue'

export default {
  name: 'Home',
  components:{OperatorSelector, OperatorQuizz},
  data(){
    return{
      operator:null
    }
  },
  methods:{
    selectOperator(operator){
      this.operator = operator
    },
    clearOperator(){
      this.operator = null
    }
  }
}
</script>


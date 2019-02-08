<template>
    <div style="position: relative;">
        <temp-var-chart v-bind:tempVar="tempVar"></temp-var-chart>
        <highlights v-bind:highlights="highlights"></highlights>
    </div>
</template>

<script>
import TempVarChart from './TempVarChart.vue'
import Highlights from './Highlights.vue'

export default {
    props: ['highlights', 'tempVar'],
    components:{
        'temp-var-chart':TempVarChart,
        'highlights':Highlights
    },
    data() {
        return {
            tempVar:this.highlights,
            highlights:this.tempVar
        }
    },
    methods: {
        
    },
    computed: {
        
    },
}
</script>
<style>
#pagecontent {
  border: 1px solid black;
  padding: 2px;
}
</style>
<template>
    <div>
        <div id="LinedPart">
            <button @click="addNewLined">+</button>
            <div>
                <LinedUnit v-for="n in linedUnitCount" :key="n" :id="n" @addNextUnit="addNewLined"
                           @removeLinedUnit="removeLined"/>
            </div>
        </div>
        <div id="UnitContentPart">

        </div>
        <div id="UnitsPart">

        </div>
    </div>
</template>

<script>
  import LinedUnit from '@/components/PipelineComponents/LinedUnit'

  export default {
    name: 'Pipeline',
    components: {
      LinedUnit
    },
    data () {
      return {
        linedUnitCount: 0,
      }
    },
    methods: {
      addNewLined () {
        this.linedUnitCount += 1
      },
      removeLined (index) {
        this.linedUnitCount -= 1
        console.log('移除第'+index+'个元素')
      }
    }
  }
</script>

<style scoped>
#LinedPart {
    float: left;
    width: 25%;
    height: 700px;
    background: #42b983;
    text-align: center;
}

#UnitContentPart {
    float: left;
    width: 50%;
    height: 700px;
    background: antiquewhite;
}

#UnitsPart {
    float: left;
    width: 25%;
    height: 700px;
    background: cornflowerblue;
}
</style>
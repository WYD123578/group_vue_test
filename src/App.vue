<template>
    <div id="app">
        <pipeline/>
    </div>
</template>

<script>
  import Pipeline from '@/components/PipelineComponents/Pipeline'

  let curLinedUnitCount = 10

  export default {
    name: 'App',
    data () {
      return {
        count: curLinedUnitCount
      }
    },
    components: {
      Pipeline
    },
    methods: {

    }
  }
</script>

<style>
#app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
}
</style>

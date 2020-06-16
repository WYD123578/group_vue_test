<template>
    <div id="LinedButton">
        <button>组件{{id}}</button>
        <div>
            <button @click="addNextUnit">+</button>
            <button @click.once="removeSelf">-</button>
        </div>
    </div>
</template>

<script>
  export default {
    name: 'LinedUnit',
    props: {
      id: {
        type: Number,
        required: true
      }
    },
    data () {
      return {
        nextUnitIds: [],
        versionName: '',
      }
    },
    methods: {
      addNextUnit () {
        console.log('子组件添加新元素')
        this.$emit('addNextUnit')
      },
      removeSelf () {
        this.$emit('removeLinedUnit', this.id)
      }
    }
  }
</script>

<style scoped>
#LinedButton{
    width: 80px;
    height: 80px;
    background: #2c3e50;
    margin: 10px;
    float: left;
}
</style>
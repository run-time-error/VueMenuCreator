<template>
  <li v-if="children.length>0">
    <span>{{name}}</span>
    <ul>
      <ListItem
        v-for="item in children"
        :key="item.title"
        :name="item.title"
        :children="item.children"
      />
    </ul>
  </li>
  <li v-else>{{name}}</li>
</template>

<script>
export default {
  name: "ListItem",
  props: {
    name: String,
    children: Array
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>

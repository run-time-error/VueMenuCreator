<template>
  <li v-if="children.length>0">
    <span>{{name}}</span>
    <button v-if="edit">Insert Here</button>
    <ul>
      <ListItem
        v-for="item in children"
        :key="item.title"
        :name="item.title"
        :edit="edit"
        :children="item.children"
      />
    </ul>
  </li>
  <li v-else>
    <span>{{name}}</span>
    <button v-if="edit">Insert Here</button>
  </li>
</template>

<script>
export default {
  name: "ListItem",
  props: {
    name: String,
    children: Array,
    edit: Boolean
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>

<template>
  <div>
    <ul>
      <ListItem
        v-for="item in menus"
        :name="item.title"
        :children="item.children"
        :edit="edit"
        :key="item.title"
      />
    </ul>
  </div>
</template>

<script>
import ListItem from "./ListItem";
export default {
  name: "Menu",
  props: {
    edit: Boolean
  },
  components: {
    ListItem
  },
  data() {
    return {
      menus: [
        {
          title: "LLI",
          children: [
            {
              title: "Client",
              children: [
                {
                  title: "Add",
                  children: []
                },
                {
                  title: "Search",
                  children: []
                }
              ]
            }
          ]
        },
        {
          title: "VPN",
          children: [
            {
              title: "Client",
              children: [
                {
                  title: "Add",
                  children: []
                },
                {
                  title: "Search",
                  children: []
                }
              ]
            }
          ]
        }
      ]
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>

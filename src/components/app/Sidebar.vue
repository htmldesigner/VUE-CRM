<template>
  <ul class="sidenav app-sidenav" v-bind:class="{open: value}">
    <router-link v-for="link in links" v-bind:key="link.url" tag="li" v-bind:exact="link.exect" active-class="active" v-bind:to="link.url" >
      <a  href="#" class="waves-effect waves-orange pointer">{{link.title}}</a>
    </router-link>
  </ul>
</template>

<script>
export default {
  props: ['value'],
  name: 'Sidebar',
  data: () => ({
    links: [
      { title: 'Счет', url: '/', exact: true },
      { title: 'История', url: '/history' },
      { title: 'Планирование', url: '/planning' },
      { title: 'Новая', url: '/record' },
      { title: 'Категории', url: '/categories' }
    ]
  })
}
</script>

<style scoped>

</style>

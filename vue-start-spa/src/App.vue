<template>
  <navbar></navbar>

  <router-view></router-view>

  <!--<page-viewer 
    v-if="pages.length > 0"
    :page="pages[activePage]"
    ></page-viewer> 

  <create-page
    @page-created="pageCreated"
    ></create-page> -->
</template>

<script>
  import Navbar from './components/Navbar.vue'

  export default {
    components: {
      PageViewer,
      Navbar,
      CreatePage
    },
    methods: {
      pageCreated(pageObj) {
        this.pages.push(pageObj);
      }
    }
  }
</script>

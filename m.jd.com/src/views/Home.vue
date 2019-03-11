<template>
  <div class="home">
   <search-bar></search-bar>
  </div>
</template>

<script>
	
import SearchBar from "@/components/SearchBar.vue";

export default {
  name: 'home',
  components: {
  	SearchBar:SearchBar
  }
}
</script>

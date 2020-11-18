<template>
  <div id="app">
   <button @click="openSafari">Open Safari</button>
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: 'Home',
  components: {
  },
  methods:{
    openSafari(){
      console.log("clicked Open safari")
      window.location='googlechrome-x-callback://x-callback-url/open/?url='+encodeURIComponent(location.href)+'&x-source=Safari&x-success='+encodeURIComponent(location.href);
    }
  }
}
</script>

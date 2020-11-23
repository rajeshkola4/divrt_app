<template>
  <div id="app">
    <button @click="copyToClipboard">Copy To ClipBoard</button>
    <button @click="openSafari">Open Safari</button>
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: "Home",
  components: {},
  methods: {
    openSafari() {
      location.href = "x-web-search://";
    },
    copyToClipboard() {
      const el = document.createElement("textarea");
      el.value = "https://gmail.com";
      el.setAttribute("readonly", "");
      document.body.appendChild(el);
      el.select();
      document.execCommand("copy");
      document.body.removeChild(el);
    }
  }
};
</script>
<template>
  <h1>{{ title }}</h1>
</template>


<script>
export default {
  name: 'Developers',
  data() {
    return {
      title: 'Developers',
      msg: ''
    }
  },
  mounted() {
    fetch("/developers")
      .then((response) => response.text())
      .then((data) => {
          this.msg = JSON.parse(data);
      });
  }
}
</script>
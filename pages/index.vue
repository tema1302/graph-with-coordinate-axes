<template lang="pug">
.container-fluid.px-10.mx-auto
  .min-h-screen.flex.items-start.justify-center
    User(v-for="(id, name, idx) in users" :playerId="id" :playerName="name" :key="idx")
</template>

<script>
import User from '~/components/User.vue'
export default {
  name: 'IndexPage',
  components: { User },
  data() {
    return {
      users: {
        'TS': 33541,
      },
    }
  },
}
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Montserrat&family=Tenor+Sans&family=Open+Sans+Condensed:wght@300&display=swap');

.container-fluid {
  // background-image: url('./static/123.jpg');
  background-repeat: no-repeat;
  background-size: 100%;
  background-position: 47% 100%;
  font-family: 'Tenor Sans', sans-serif;

  &::before {
    content: '';
    top: 0;
    left: 0;
    bottom: 0;
    right: 0;
    z-index: 0;
    background: rgba($color: #222, $alpha: 0.5);
    // backdrop-filter: blur(1px);
    position: fixed;
  }
}
</style>

<template>
  <div class="notFound">
    <v-container class="mycontainer">
        <div class="textWrapper">
            <div class="mainText">404</div>
        <div class="secondaryText">{{getRoute()}} doesn't exist.</div>
        </div>
    </v-container>
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: "notFound",
  methods: {
      getRoute () {
          return this.$route.path
      }
  }
};
</script>
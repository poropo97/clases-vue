<template>
  <div class="d-flex">
    <h5>{{user.nom}}</h5>
    <img width="50" :src="user.img" class="img img-thumbnail" alt="">
  </div>
</template>

<script>
export  default {

  props: {
    user: {

    }
  }
}

</script>

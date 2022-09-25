
<template>
  <div class="card">
    <div class="card-header">
      {{titol}}
    </div>
    <div  class="card-body">
      {{cos}}
    </div>
    <div class="card-footer" v-if="peu !== false">
      {{peu}}
    </div>
  </div>
</template>

<script>
export  default {

  props: {
    titol: {},
    cos: {},
    peu: {
      default: false
    }
  }
}

</script>


<template>
  <div class="card">
    <div class="card-header">
      <Profile :user="info.user" />
    </div>
    <div  class="card-body">
      <p>
        {{info.cos}}
      </p>
      <img width="400" :src="info.imatge" class="img-thumbnail" alt="">
    </div>
    <div class="card-footer" >
      <svg v-if="info.is_likeable" xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-heart-fill m-3" viewBox="0 0 16 16">
        <path fill-rule="evenodd" d="M8 1.314C12.438-3.248 23.534 4.735 8 15-7.534 4.736 3.562-3.248 8 1.314z"/>
      </svg>

      <button @click="openComent()" v-if="info.is_comentable" type="button" class="btn btn-primary" name="button">Comentar</button>
      <Comentari  v-if="showComent" />
    </div>
  </div>
</template>

<script>
import Profile from "@/components/Profile.vue"
import Comentari from "@/components/Comentari.vue"

export  default {
  data(){
    return {
      showComent: false
    }
  },

  components: {
    Profile,
    Comentari
  },
  props: {
    info: {
      titol:{},
      cos: {},
      imatge:{},

    },

  },
  methods: {
    openComent() {
      this.showComent = !this.showComent
    }
  }
}

</script>

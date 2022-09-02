<template>
  <div class="row">
    <div class="col-md-12">
      <h1>Últimas Noticias</h1>
    </div>
    <div class="col-md-12">
      <Articulo
        class="mt-3"
        v-for="articulo in articles"  :key="articulo"
        :info="articulo" />
    </div>
  </div>

</template>


<script>
import Articulo from '@/components/Articulo.vue'


export default {
  data(){
    return {
      articles: [
        {
          titol: "Nuevo planeta descubierto",
          cos: "Se ha descubierto un nuevo planeta en el exterior del sistema solar",
          imatge: "https://wp.es.aleteia.org/wp-content/uploads/sites/7/2017/05/web3-planet-earth-space-nasa-space-stars-sun-shutterstock_526255060-shutterstock.jpg",
          is_likeable:true,
          is_comentable: true,
          user: {
            nom: "Joan Capdevila",
            img: "https://img.blogs.es/anexom/wp-content/uploads/2021/12/perfil-1024x754.jpg"
          }
        },
        {
          is_likeable: true,
          is_comentable: false,
          titol: "Nueva fábrica abierta en Badalona",
          cos: "El ayuntamiento ha abierto una fábrica nueva, la polémica está servida",
          imatge: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSnP9xe30kyIsVXcEsbwwrurZDYavRWN0yOHQ6VDxVImRmBP3H_tHiqNKTgsylp_stObjw&usqp=CAU",
          user: {
            nom: "Pau Alsina",
            img: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcS_3FlCnFuOd9nXxC6_oWIjF1-PqTiILFS9Ig&usqp=CAU"
          }
        }
      ]
    }
  },
  components: {
    Articulo
  }

}

</script>

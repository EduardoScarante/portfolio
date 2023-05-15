<script>

import blogCard from '../components/blogCard.vue'
import aylaPhoto from '/src/img/a1.jpeg'
import negoPhoto from '/src/img/n2.jpeg'
import isaPhoto from '/src/img/isa.jpeg'
import eduPhoto from '/src/img/edu.png'


export default {
  components: {
    blogCard
  },
  data() {
    return {
      infos: [
        {
          id: 0,
          nome: "Ayla",
          profissao: "Farrejadora de petisco",
          data: "Preguiçosa, antipática e carente!",
          path: aylaPhoto
        },
        {
          id: 1,
          nome: "Nego",
          profissao: "Aquecedor de cadeira",
          data: "Brincalhão, cheio de energia e carinhoso!",
          path: negoPhoto
        },
        {
          id: 2,
          nome: "Isa",
          profissao: "Técnica em Enfermagem",
          data: "Carinhosa, dorminhoca e otimista!",
          path: isaPhoto
        },
        {
          id: 3,
          nome: "Eduardo",
          profissao: "Quiçá um desenvolvedor e quase Eng. Elétrico",
          data: "Barrigudo, criativo e sonhador!",
          path: eduPhoto
        }
      ]
    }
  }/* ,
  mounted(){
    console.log('montou')
    fetch("")
    // const res = fetch()
    // this.infos = res.data
  },
  unmounted(){
    console.log('desmontou')
    // const res = fetch()
    // this.infos = res.data
  } */
}

</script>
<template>
  <div class="about">

    <div v-for="x in infos">
      <blogCard 
      :nome="infos[x.id].nome" 
      :profissao="infos[x.id].profissao" 
      :data="infos[x.id].data"
      :path="infos[x.id].path" />
    </div>

    <div class="iframe">
      <iframe src="https://giphy.com/embed/yPRo73ILrGjny" width="200" frameBorder="0" class="giphy-embed">
      </iframe>

      <iframe src="https://giphy.com/embed/ySpxjJmsq9gsw" width="200" frameborder="0" class="giphy-embed">
      </iframe>
    </div>

  </div>
</template>

<style scoped>
.about {
  margin: 50px;
  justify-content: center;

  display: flex;
  flex-wrap: wrap;
  align-items: center;
}
.iframe{
  width: 450px;

  display: flex;
  justify-content: space-around;
  
}

</style>

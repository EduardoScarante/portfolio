<script>

export default {
  data() {
    return {
      index: 0,

      empresaArray: [
        {
          empresa: "JMalucelli",
          funções: "Estagiário",
          description: "Primeiro contato com a programação, C++, Python e VBA para desenvolvimento de scripts e análises de dados.",
          tempo: "1 ano e 4 meses"
        },
        {
          empresa: "Copel",
          funções: "Estágio",
          description: "Primeiros códigos em PHP, Xampp e MySQL",
          tempo: "3 meses"
        },
        {
          empresa: "Just in Time Engenharia",
          funções: "Estágio 'Chefe'",
          description: "Desenvolvimento mobile com React Native e Ionic, Python para script e VBA para automatizações.",
          tempo: "2 anos e 2 meses",

        },
        {
          empresa: "Elco Engenharia",
          funções: "Estágio",
          description: "SQL para Oracle no ERP Mega, desenvolvimento de relatórios em Power BI, scripts Python para automatização de tarefas e análises de dados.",
          tempo: "1 ano",

        },
        {
          empresa: "4network",
          funções: "Desenvolvedor",
          description: "Contato maior com Java Script (Realidade aumentada), uso de PHP para manutenção nos sistemas legados e novos scripts, análises de dados para dashboards no Qlik Sense e Power BI vindo do banco de dados Postgress, treinamento em Vue.JS para FrontEnd e em Java para BackEnd",
          tempo: "6 meses"
        }
      ]
    }
  },
  methods: {
    indexCardMenos() {
      this.index == 0 ? this.index = 0 : this.index--
    },
    indexCardMais() {
      this.index == 4 ? this.index = 4 : this.index++
    }
  },
  computed: {
    infoEmpresa() {
      return this.empresaArray[this.index]
    }
  }
}
</script>


<template>
  <div class="work">

    <div class="cards">
      <button @click="indexCardMenos">&lt</button>
      <div class="card">
        <h1>{{ infoEmpresa.empresa }}</h1><br>
        <h2>{{ infoEmpresa.funções }}</h2><br>
        <h3>{{ infoEmpresa.description }}</h3><br>
        <h4>{{ infoEmpresa.tempo }} meses</h4>
      </div>
      <button @click="indexCardMais">></button>
    </div>

  </div>
</template>

<style scoped>
.work {
  display: flex;
  justify-content: center;
}

.title {
  text-align: center;
}

.cards {
  max-width: 800px;
  padding-top: 80px;

  flex-wrap: wrap;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.cards button {
  background-color: black;
  color: white;
  font-weight: 800;
  width: 30px;
  height: 30px;
  border-radius: 10px;
  border: none;
  text-decoration: none;
  transition: 0.6s ease-in-out;
}

.cards button:hover {
  background-color: red;
}

.card {
  display: flex;
  flex-direction: column;
  justify-content: center;


  height: 300px;
  width: 400px;

  margin: 10px;
  padding: 25px;

  box-shadow: 3px 3px 3px rgb(7, 7, 7);
  border-radius: 20px;
  background-color: rgba(0, 0, 0, 0.2);
  transition: 0.6s ease-in-out;
}

.card:hover {
  box-shadow: 0px 0px 3px rgb(253, 253, 253);
}

h1 {
  font-size: 24px;
  font-weight: 400;

}

h2 {
  font-size: 20px;
  font-weight: 200;

}

h3 {
  font-size: 16px;
  font-weight: 200;

}

h4 {
  font-size: 12px;
  font-weight: 200;
}
</style>

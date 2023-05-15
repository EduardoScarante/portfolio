<script>

export default {
  data() {
    return {
      res:
        []
    }
  },
  mounted() {
    fetch("http://127.0.0.1:8000/api/users/",
      {
        method: "GET",
      }
    ).then(res => {
      return res.json()
    }).then(res => {
      this.res = res
    }).catch(err => {
      alert("Algo deu errado, tente mais tarde")
    })
  },
  /*   unmounted() {
      console.log("desmontou");
    }, */
  methods: {
    click() {
      console.log("fetch Post fictício");
    }
  }
}

</script>

<template>
  <body>
    <table>
      <tr>
        <td class="c">Nome</td>
        <td class="c">Cor Favorita</td>
        <td class="c">Endereço</td>
        <td class="c">Email</td>
        <td class="c">Nome do Pet</td>
      </tr>

      <tr v-for='x in res'>
        <td>{{ x.name }}</td>
        <td>{{ x.favorite_color }}</td>
        <td>{{ x.address }}</td>
        <td>{{ x.email }}</td>
        <td>{{ x.pet_name }}</td>
      </tr>

    </table>

    <!--     <button @click="click">POST</button>
 -->
  </body>
</template>

<style scoped>
body {
  display: flex;
  flex-direction: column;
  height: 80vh;
  justify-content: center;
  text-align: center;
  align-items: center;
}

td {
  font-weight: 400;
  width: 150px;
  text-align: left;

}

table{
  border: 1px solid gray;
}

.c {
  text-align: center;
  font-weight: 800;
  border-bottom: 1px solid gray;
}
</style>

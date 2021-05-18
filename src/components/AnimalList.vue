
<template>
  <div>
      <h3>{{ msg }}</h3>
      <v-if="animal.date">
      <v-else>Nepoznat</v-else>
      <ul>
        <li v-for-key="animal in animals">{{ animal.id+' '+ animal.ime + animal.date}}</li>
      </ul>
        <form @submit.prevent="addAnimal">
        <input v-model="animal.ime" />
        <input v-model="animal.age" />
        <input v-model="animal.date"/>
        <button type="submit" v-on="toTop">Add Animal</button>
    </form>
  </div>
</template>

<script>

export default {
    name: 'AnimalList',
    props: {
        msg:String
    },
    data () {
        return {
            animals: [
                {id:1, vrsta:'domaca', ime: 'Konj', date: new Date(2018, 12, 24) },
                {id:2, vrsta:'domaca', ime: 'Svinja', date: new Date(2017, 1, 14) },
                {id:3, vrsta: 'divlja', ime: 'Lav', date: new Date(2012, 11, 20) },
                {id:4, vrsta: 'divlja', ime: 'Slon', date: new Date(2012, 11, 20) }
            ]
            animal:[
                {id:0,vrsta:'',ime:'',date:new Date()}
            ]
        }
    },
    methods: {
        addAnimal() {
        this.animals.push({ name: this.animal.name, age: this.animal.age }); 
        animals.unshift(animals.splice(index, 1)[0]);
        },
        removeAnimal() {
        
        }
    }
}
</script>
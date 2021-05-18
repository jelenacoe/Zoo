
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
        <button @mouseover="submit">Add Animal</button>
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
                {id:1, vrsta:0, ime: 'Konj', date: new Date(2018, 12, 24) },
                {id:2, vrsta:0, ime: 'Svinja', date: new Date(2017, 1, 14) },
                {id:3, vrsta: 1, ime: 'Lav', date: new Date(2012, 11, 20) }
            ]
        }
    },
    methods: {
        addAnimal() {
        this.animals.push({ name: this.animal.name, age: this.animal.age }); 
        },
        removeAnimal() {
        
        }
    }
}
</script>
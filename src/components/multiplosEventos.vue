<template>
    <div>
        <button @click="primeiro($event),segundo($event)">Ativar Multiplos Eventos</button>
        <p>{{multiplos_eventos}}</p>
    </div>
    
</template>
<script>
export default {
    name:'multiplosEventos',
    data(){
       return{
         multiplos_eventos:""
    }
},

methods: {
    primeiro(e) {
        e.preventDefault(),
        this.multiplos_eventos = "Primeiro Evento Ativado!"
    },
    segundo(e){
        e.preventDefault(),
        setTimeout(()=> this.multiplos_eventos = "Segundo Evento",500)
    }
}
}
</script>
<style scoped>
   div{
     margin:100px;
   }
</style>
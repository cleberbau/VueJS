<template>
    <h1> meu Nome é: {{ nome}}</h1>
</template>
<script>
export default{
    name: 'LifeCycle',
    data(){
        return{
            nome: 'Segundo Componente'

        }
    },
    created(){
        setTimeout(()=>{this.nome = 'Carol e Davi'},2000);
        this.LifeCycle()
        
    },
    mounted(){
        setTimeout(()=>{this.nome = 'Cleber'},4000);
        this.LifeCycle()
       
    },
    methods:{
        LifeCycle(){
            console.log('Execultou');
        }
    }
}
</script>
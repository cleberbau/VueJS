<template>
    <img :src="avatar" :alt="descricao" >
</template>
<script>
export default {
    name:'Picture',
    data(){
        return{
            avatar:'./img/avatar.png',
            descricao: 'Avatar Mateus Batisti',
            title: 'Avatar Mateus Batisti'
        }
    }
    
}
</script>
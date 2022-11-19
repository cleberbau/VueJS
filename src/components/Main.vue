<template>
    <div>
           <form action="">
           <div><input type="text" name="" id=""></div> 
           <div> <input type="text" name="" id=""></div>
           <div> <input type="submit" value=""></div>
        </form>
    </div>
    <button @click="showEmail">{{TextoBotao}}</button>
    <div>
       
        <p v-show="mostra_email">'Você Receber uma mensagem no Email {{email}} de confirmação'</p>
        <p>Para Acessar meu Protifolio  <a v-bind:href="meu_link" target="_blank"> Basta Clicar</a></p>
        <Picture />
    </div>
</template>
<script>

import Picture from './Picture.vue';
export default {
    name: 'Main',
    components: {
        Picture
    },
    data(){
        return{
            
            email: "cps89.dev@gmail.com",
            mostra_email: false,
            meu_link: 'http://www.google.com',
            TextoBotao: 'Mostrar Email'
            
            }
        },
        methods:{
            showEmail(){
                this.mostra_email = !this.mostra_email
                if(!this.mostra_email){
                    this.TextoBotao = 'Mostrar Email'
                }else{
                    this.TextoBotao = 'Ocultar Email'
                }
            }
        }

    
   
        
    }

</script>
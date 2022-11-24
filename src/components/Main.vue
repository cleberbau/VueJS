<template>
    <div>
           <form action="">
           <div><input type="text" v-model="name"></div> 
           <div> <input type="text" v-model="email"></div>
           <div> <input type="submit" value="" @submit="enviarFormulario($event)"></div>
        </form>

        <div>
            <p>Tecnologias Back End Utilizadas:</p>
            <ul >
                <li v-for="(tecnology,index) in backend_technologies" v-bind:key="index">{{tecnology}}</li>
                
            </ul>
            <p>Tecnologias front End Utilizadas:</p>
            <ul >
                <li v-for= "technology in frontend_techologies" :key="technology.id">
                    {{technology.language}}
                </li>
                
            </ul>
        </div>
    </div>
    <button @click="showEmail">{{TextoBotao}}></button>
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
            
            name:"",
            email: "",
            mostra_email: false,
            meu_link: 'http://www.google.com',
            TextoBotao: 'Mostrar Email',
            backend_technologies:['Flutter','GO','Java','Estou conseguindo'],
            frontend_techologies:[
                {id: 1, language: 'HTML'},
                {id: 1, language: 'CSS'},
                {id: 1, language: 'JAVASCRIPT'},
            ]
            
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
            },
            enviarFormulario(e){
                e.preventDefault();
                const name = this.name;
                const email = this.email;

                console.log('Formulario Enviado!');
                console.log('O nome é :' + name);
                console.log("O Email é:" + email);
            }

            
        }

    
   
        
    }

</script>
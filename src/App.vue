<template>
<Header />
<LifeCycle />
<Main />

</template>
<script>
import LifeCycle from './components/LifeCycle.vue'
import Header from './components/Header.vue'
import Main from './components/Main.vue'

export default {
  name: 'App',
  components:{ 
    LifeCycle,
    Header,
    Main
    
    
  }
}
</script>
<style>
  body{
    background: gray;
    color: white;
    
  }

img{
  max-width: 200px;
}
</style>


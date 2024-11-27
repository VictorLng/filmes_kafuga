<template>
    <div class="main">
       <a v-for="item in headers"
            class="links-header ma-2"
            :key="item.title"
            :href="item.href"
            :title="item.title"
            :style="{ 
                '--link-color': item.color,
                '--icon-color': item.color
            }"
            >
            <v-icon
            >
              {{ item.icon }} 
            </v-icon>
            <span class="title">{{ item.title }}</span>
        </a>
    </div>
</template>

<script setup>
 const headers= [
    {
        title:'Filmes',
        href: '/filmes',
        icon:'mdi-video-vintage',
        color:'#67A3D9',
        background:'#B7D4F3'
    },
    {
        title:'Series',
        href: '/series',
        icon:'mdi-video-wireless',
        color:'#D9281E',
        background:'#EB343D'
    },
    {
        title:'Games',
        href: '/games',
        icon:'mdi-controller',
        color:'#65DB81',
        background:'#97C4F3'
    }
 ]

</script>
<style scoped lang="scss">
    .main {
      display: flex;
      justify-content: space-around; 
      align-items: center; 
      padding-top: 30vh; 
    }
    .links-header {
      text-decoration: none;
      transition: .2s ease-in-out;
      display: flex;
      flex-direction: column; 
      align-items: center;
      font-size: 1.2rem; 
      padding: 200px;
      color: var(--link-color);
  
      &:hover {
        color: rgb(4, 4, 4);
        opacity: 0.8; 
        transform: scale(1.05);  
        background-color: var(--icon-color) ;
      }
    }
    .icon {
      font-size: 2rem; 
      margin-bottom: 5px;   
      color: var(--icon-color);
      transition: .2s ease-in-out;
      &:hover {
        
        opacity: 0.8; 
        transform: scale(1.05);  
      }
    }

    .title {
      font-size: 1.1rem; 
    }
    
</style>





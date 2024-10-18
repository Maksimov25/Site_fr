<template>
    <header
        class="header"
    >
        
        <ProfileIcon/> 
        <NotificationsIcon/>
        <SearchContainer/>
         

            <nav>
                <ul>
                    <li><router-link to="/create">Создать форум</router-link></li>
                    <li><router-link to="/about">О нас</router-link></li>
                    <li><router-link to="/contact">Поддержка</router-link></li>
                </ul>
            </nav> 

    </header>
  </template>
  
  <script>
  import ProfileIcon from '@/components/header/profile-icon.vue';
  import NotificationsIcon from '@/components/header/notifications-icon.vue';
  import SearchContainer from '@/components/header/search-container.vue';

  export default {
    name: 'Header',

    components: {
        ProfileIcon,
        NotificationsIcon,
        SearchContainer

    }

  };


  </script>
  
  <style scoped>
  
  header {
    display: flex;
    align-items: center;
    padding: 15;
    background-color: #f8f9fa;
  }


  nav ul {
    list-style: none;
    justify-content: space-between;
    /* display: flex; */
    gap: 20;
    margin: auto;
  }

.circle {
  width: 30px;
  height: 30px;
  border-radius: 50%;
  background-color: #00ffd5; 
  color: rgba(255, 255, 255, 0.771); 
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 17px; 
}

  </style>
  
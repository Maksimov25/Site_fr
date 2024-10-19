<template>
    <header
        class="header"
    >
        
        <ProfileIcon/>
        <SearchContainer/>
            <nav>
                <ul>
                    <li><router-link to="/contact">Поддержка</router-link></li>
                </ul>
            </nav> 

    </header>
  </template>
  
  <script>
  import ProfileIcon from '@/components/header/profile-icon.vue';
  import SearchContainer from '@/components/header/search-container.vue';
  


  export default {
    name: 'Header',

    components: {
        ProfileIcon,
        // NotificationsIcon,
        SearchContainer
    }

  };


  </script>
  

  <style scoped>
header {
  display: flex;
  align-items: center;
  padding: 15px;
  background-color: #333;
  justify-content: space-between;
}

/* .nav-left, .nav-right {
    display: flex;
    align-items: center; /* Центрируем по вертикали */
 

    nav ul {
    list-style: none; /* Убираем маркеры списка */
    display: flex; /* Используем flex для горизонтального расположения элементов */
    margin: 0; /* Убираем внешние отступы */
    padding: 0; /* Убираем внутренние отступы */
    color: #faf8f8; /* Цвет текста */
}

nav ul li {
    margin-right: 20px; /* Отступ между элементами списка */
}


.circle {
  width: 30px;
  height: 30px;
  border-radius: 50%;
  background-color: #eef4f3; 
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 17px; 
}
</style>

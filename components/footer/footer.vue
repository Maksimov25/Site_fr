<template>
    <footer class="footer">
        <div class="footer__copyright copyrightText">{{ copyrightText }}</div>
        <nav class='footer_nav'>  
            <ul> 
                <li><a href="#privacy">Политика конфиденциальности</a></li>
                <li><a href="#terms">Условия использования</a></li>
            </ul>
        </nav>
        <div class="footer_social-links">
            <a href="https://vk.com/maksimov_89" target="_blank">VK</a>
            <a href="https://vk.com/maksimov_89" target="_blank">Instagram</a>
        </div>
    </footer>
</template>

<script>
export default {
    computed: {
        copyrightText() {
            const currentYear = new Date().getFullYear();
            return `2023-${currentYear}, Форум`;
        }
    }
}
</script>

<style lang="scss">

// body {
//     background: linear-gradient(to bottom, #87CEEB, #00008B); // светло-синий к темно-синему
//     margin: 0; 
//     height: 100vh; 
// }

.footer {
    background: linear-gradient(#909, #000);
    text-align: center;
    padding: 20px;
}

.copyrightText {
    color: #999;
}

.footer_nav ul {
    list-style-type: none;
    padding: 0;
}

.footer_nav ul li {
    display: inline;
    margin: 0 15px;
    color: #999;
}

.footer_social-links {
    margin-top: 10px;
    
}

.footer_social-links a {
    margin: 0 10px;
    text-decoration: none;
    color: #999;
}

.footer_social-links a:hover {
    text-decoration: underline;
}

</style>
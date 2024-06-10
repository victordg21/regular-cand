<script>

export default {
    data() {
        return {
            header: ['Início', 'Sobre Nós', 'Artigos', 'Localização', 'Contato'],
            menuAberto: false
        };
    },
    methods:{
        toggleMenu() {
            this.menuAberto = !this.menuAberto;
        }
    }
};
</script>

<template>
    <header class="container-header justify-between flex py-2"><!--HEADER-->
        <img class="h-16" src="../assets/RegularCand.jpeg" alt="">
        <div class="flex justify-center items-center pr-5">
            <svg @click="toggleMenu" xmlns="http://www.w3.org/2000/svg" width="40" height="40" fill="#000" class="bi bi-list xl:hidden" viewBox="0 0 16 16">
                <path fill-rule="evenodd" d="M2.5 12a.5.5 0 0 1 .5-.5h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1-.5-.5m0-4a.5.5 0 0 1 .5-.5h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1-.5-.5m0-4a.5.5 0 0 1 .5-.5h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1-.5-.5"/>
            </svg>
        </div>
        <ul class="text-xl flex gap-x-24 items-center hidden xl:flex">
            <li v-for="(item, index) in header" :key="index">
                <a class="borders" :href="'#' + item">{{ item }}</a>
            </li>
        </ul>
    </header>
    <nav v-if="menuAberto" class="menu">
        <ul class="text-xl text-right w-full gap-x-24 items-center block">
            <li class="no-underline border-b border-black" v-for="(item, index) in header" :key="index">
                <a class="border-opacity-50" :href="'#' + item">{{ item }}</a>
            </li>
        </ul>
    </nav>
</template>

<style scoped>

.borders{
    border-bottom: 2px solid white;
}

.borders:hover{
    border-color: #CBAF6E;
}

.menu {
    background-color: #BE9C4B; 
    padding: 10px; 
    display: flex; 
    justify-content: space-around; 
    overflow: hidden;
}

.container-header{
    width: 90%; /* Define a largura do container como 80% */
    margin-left: 5%; /* Define a margem esquerda como metade da largura restante (10% de 20%) */
    margin-right: 5%; /* Define a margem direita como metade da largura restante (10% de 20%) */
}



</style>
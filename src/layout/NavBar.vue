<script setup>
    import Menu from '../components/Menu.vue';
    import Logo from '../components/Logo.vue';
</script>

<template> 
    <div  class="w-full flex flex-row justify-between ">
        <Logo />
        <ul class="flex flex-row">
            <Menu menu="Home" url="#home"/>
            <Menu menu="About" url=""/>
            <Menu menu="Project" url="#home"/>

        </ul>
    </div>
</template>
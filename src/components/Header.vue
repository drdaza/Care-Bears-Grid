<script setup>

</script>
<template>
    <header>
        <img src="../assets/logo.svg" alt="logo Vue">
        <nav>
            <RouterLink to="/">Care Bears</RouterLink>
            <RouterLink to="/about">about</RouterLink>
        </nav>
    </header>
</template>
<style lang="scss" scoped>
    header{
        width: 100%;
        display: flex;
        flex-direction: column;
        align-items: center;
        img{
            width: 15%;
            margin: 1em;
        }
        nav{
            width: 100%;
            display: flex;
            flex-direction: row;
            justify-content: center;
            a{
                margin: 0 1% 0 1%;
            }
            a:hover{
                color: darkblue;
            }
        }
    }
</style>
<template>
    <div class="myhead">
    <div>
        Home
    </div>
    <div>
        Events
    </div>
    <div>
        About
    </div>
    <div>
        Join Us
    </div>
    </div>
</template>

<script>
export default {
    name:'Menu',
}
</script>

<style scoped>
.myhead {
    display: flex;
    justify-content: space-around;
    align-items: center;
}

div{
    background-color: rgb(213, 213, 213);
}
</style>
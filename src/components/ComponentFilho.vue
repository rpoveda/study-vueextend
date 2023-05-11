<template>
    <div>
        <h1>{{ texto }}</h1>
        <img v-if="showImage" src="https://www.codemotion.com/magazine/wp-content/uploads/2022/08/VueJS-e1659695444607.jpg" style="witdh:250px; height:250px" />
    </div>
</template>

<script>
export default {
    props: {
        texto: {
            type: String,
            default: () => null
        },
        showImage: {
            type: Boolean,
            default: () => true
        }
    }    
}
</script>

<style>
h1 {
    color: red;
}
</style>
<template>
    <div>

    </div>
</template>

<script>
export default {
    name: 'SeccionApi',
    data(){
        return{
            movies:null
        }
    },
    mounted(){
        fetch('https://www.omdbapi.com/?s=harry+potter&type=movie&apikey=23daade9',{method:'GET'})
        .then(response => (this.movies = response))
    }    
}
</script>

<style scoped>

</style>
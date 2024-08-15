<template>
    <div>
        <h2>
            {{ foodName }}
            <img v-show="foodIsFavorite" src="https://icons.iconarchive.com/icons/hopstarter/soft-scraps/256/Button-Favorite-icon.png">
        </h2>
        <p>{{ foodDesc }}</p>
        <button @:click="toggleFavorite">Favorite</button>
    </div>
</template>

<script>
export default {
    props: ['foodName', 'foodDesc', 'isFavorite'],
    data() {
        return {
            foodIsFavorite: this.isFavorite
        }
    },
    methods:{
        toggleFavorite(){
            this.foodIsFavorite = !this.foodIsFavorite
        }
    }
}
</script>

<style>
    img {
        height: 1.5em;
        float: right;
    }
</style>
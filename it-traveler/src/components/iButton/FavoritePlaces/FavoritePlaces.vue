<script setup>
    import FavoritePlace from '../FavoritePlace/FavoritePlace.vue';
    import iButton from '../iButton/iButton.vue';
</script>

<template>
    <div class="px-6 mb-4">
        <div class="text-gray">Додані маркери</div>

<FavoritePlace v-for="n in 4" :key="n"/>

    </div>
    <iButton class="w-full mt-10">Додати маркер</iButton>
</template>
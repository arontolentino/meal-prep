<template>
    <span>
        <HomeHero></HomeHero>
        <HomeDetails></HomeDetails>
    </span>
</template>

<script>
import HomeHero from '@/components/HomeHero';
import HomeDetails from '@/components/HomeDetails';

export default {
    name: 'Home',
    components: {
        HomeHero,
        HomeDetails
    }
};
</script>

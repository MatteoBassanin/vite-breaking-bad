<template>
    <div class="loading" v-if="store.loading">
        <h1>Sta tranquillo stamo a caricà</h1>
    </div>
</template>


<script>
import { store } from '../store';


export default {
    name: 'MyLoading',
    data() {
        return {
            store
        }
    }
}
</script>


<style scoped>
h1 {
    font-size: 100px;
    color: red;
}
</style>
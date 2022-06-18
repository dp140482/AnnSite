<template>
    <div class="middle-container">
        <div class="container">
            <Lessons />
        </div>
    </div>
</template>

<script>
import Lessons from './Lessons.vue'

export default {
    name: 'Main',
    components: { Lessons },
}
</script>

<style>
.middle-container {
    position: relative;
    display: flex;
    justify-content: center;
    padding: 15px 0;
}
.container {
    max-width: 1100px;
    min-width: 450px;
    width: 80%;
}
</style>
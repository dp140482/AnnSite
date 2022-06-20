<template>
    <div class="middle-container">
        <div class="container">
            <Modules v-show="showModules" @update="toLessons" />
            <Lessons v-show="!showModules" />
        </div>
    </div>
</template>

<script>
import Lessons from './Lessons.vue'
import Modules from './Modules.vue'
import { EventBus } from '@/eventbus.js'

export default {
    name: 'Main',
    components: { Lessons, Modules },
    data: () => ({
        showModules: true,
    }),
    methods: {
        toLessons() {
            this.showModules = false
            EventBus.$emit('changeToLessons')
        },
    },
    created() {
        EventBus.$on('changeToModules', () => {
            this.showModules = true
        })
    }
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
    max-width: 500px;
    min-width: 350px;
    width: 80%;
    position: relative;
}
.ontop {
    position: absolute;
    left: 217px;
    top: -94px;
}
</style>
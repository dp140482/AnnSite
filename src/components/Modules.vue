<template>
    <div class="modules">
        <button 
            v-for="(item, index) in modulesList"
            class="module lesson_active lesson-link"
            @click="onClick(item)"
        >
                <span class="number">{{ index + 1 }}</span>
                {{ item.title }}
        </button>
    </div>
</template>

<script>
export default {
    name: 'Modules',
    data: () => ({
        isModulesVisible: true,
        modulesList: [
            { title: 'Пчела' },
            { title: 'Обзор инструментов' },
            { title: 'Обзор материалов' }, 
            { title: 'Жучки' },
            { title: 'Клевер' },
            { title: 'Кленовый лист' },
            { title: 'Перо' },
            { title: 'Птица' },
            { title: 'Бонусный урок' },
        ],
    }),
    methods: {
        onClick(item) {
            if (item.title === 'Пчела') this.$emit('update')
        },
    },
}
</script>

<style>
.module {
    display: block;
    width: 100%;
    text-align: left;
    font-family: inherit;
    font-size: inherit;
    border: 1px solid gainsboro;
    padding: 20px;
    background-color: lavenderblush;
    margin-bottom: 10px;
    box-shadow: 2px 5px 5px darkred;
    color: #33241b;
    cursor: pointer;
}
.module::before {
    content: 'Модуль ';
}
.module:first-of-type {
    border-top-left-radius: 20px;
    border-top-right-radius: 20px;
}
.module:last-of-type {
    border-bottom-left-radius: 20px;
    border-bottom-right-radius: 20px;
    margin-bottom: 0;
}
</style>
<template>
    <div class="lessons">
        <div v-for="(item, index) in lessonsList" class="lesson lesson_active">
            <span class="number">{{ index + 1 }}</span>
            {{ item }}
        </div>
    </div>
</template>

<script>
export default {
    name: 'Lessons',
    data: () => ({
        lessonsList: [
            'Обзор инструментов',
            'Обзор материалов',
            'Жучки',
            'Клевер',
            'Кленовый лист',
            'Перо',
            'Птица',
            'Бонусный урок',
        ]
    }),
}
</script>

<style>
.lesson {
    border: 1px solid gainsboro;
    padding: 20px;
    background-color:lavenderblush;
    margin-bottom: 10px;
    box-shadow: 2px 5px 5px darkred;
    color: #33241b;
}
.lesson::before {
    content: 'Модуль ';
}
.lesson:first-of-type {
    border-top-left-radius: 20px;
    border-top-right-radius: 20px;
}
.lesson:last-of-type {
    border-bottom-left-radius: 20px;
    border-bottom-right-radius: 20px;
    margin-bottom: 0;
}
.lesson_active {
    transition: 0.1s all ease-in;
}
.lesson_active:hover {
    transform: scale(1.01);
}
.number {
    border: 1px solid gainsboro;
    background-color: gainsboro;
    color: black;
    padding: 0 3px;
    font-size: 12pt;
}
</style>
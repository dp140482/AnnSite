<template>
    <div class="lessons">
        <a 
            v-for="(item, index) in lessonsList"
            :href="item.video"
            class="lesson lesson_active lesson-link"
        >
                <span class="number">{{ index + 1 }}</span>
                {{ item.title }}
        </a>
    </div>
</template>

<script>
export default {
    name: 'Lessons',
    data: () => ({
        lessonsList: [
            { title: 'Создание контура', video: 'https://disk.yandex.ru/i/PdeNe0VGAYZ5xA' },
            { title: 'Вышивка тела', video: 'https://disk.yandex.ru/i/1r6swyfKrbcCQA' },
            { title: 'Вышивка крыльев', video: 'https://disk.yandex.ru/i/e_nYtKl6IKDv8w' },
            { title: 'Изнаночная сторона', video: 'https://disk.yandex.ru/i/ZFpwHSUyfLGKGg' },
            { title: 'Монтирование лапок', video: 'https://disk.yandex.ru/i/DJexjMMJBZ6RFA' },
            { title: 'Приклеивание', video: 'https://disk.yandex.ru/i/hY5HEkIuIMn9RQ' },
            { title: 'Обшивка края', video: 'https://disk.yandex.ru/i/HQHjhqIh3TpWbA' }
        ],
    }),
}
</script>

<style>
.lesson {
    display: block;
    border: 1px solid gainsboro;
    padding: 20px;
    background-color: lavenderblush;
    margin-bottom: 10px;
    box-shadow: 2px 5px 5px darkred;
    color: #33241b;
    cursor: pointer;
}
.lesson::before {
    content: 'Урок ';
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
    transform: scale(1.05);
}
.number {
    border: 1px solid gainsboro;
    background-color: gainsboro;
    color: black;
    padding: 0 3px;
    font-size: 12pt;
}
.lesson-link {
    text-decoration: none;
}
</style>
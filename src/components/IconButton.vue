<template>
    <p>
        <a
            :href="link"
            target="_blank"
            rel="noopener noreferrer"
        >
            <img 
                :src="icon"
                :alt="buttonName"
                :title="buttonName"
                width="30"
                height="30"
                class="iconbtn"
            />
        </a>
    </p>
</template>

<script>
export default {
    name: 'IconButton',
    props: {
        link: '',
        icon: '',
        buttonName: '',
    },
}
</script>

<style>
.iconbtn {
    transition: 0.1s all ease-in;
}
.iconbtn:hover {
    transform: scale(1.2);
}
</style>
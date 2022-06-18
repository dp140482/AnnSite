<template>
    <footer class="footer">
        <div class="iconline">
            <IconButton
                link = "https://instagram.com/anka.bijou?utm_medium=copy_link"
                :icon = "InstagramImage"
                buttonName = "Instagram"
            />
            <IconButton
                link = "https://vm.tiktok.com/ZSJGRJ4SL/"
                :icon = "TikTokImage"
                buttonName = "TikTok"
            />
            <IconButton
                link = "https://vk.com/anka.bijou"
                :icon = "VKImage"
                buttonName = "VK"
            />
            <IconButton
                link = "https://wa.me/79111333099"
                :icon = "WhatsAppImage"
                buttonName = "WhiatsApp"
            />
            <IconButton
                link = "https://zen.yandex.ru/id/61e88f160141a70c4a179306"
                :icon = "ZenImage"
                buttonName = "Яндекс.дзен"
            />
            <IconButton
                link = "tg://resolve?domain=ankabijou"
                :icon = "TelegramImage"
                buttonName = "Telegram"
            />
            <IconButton
                link = "viber://chat?number=+79111333099"
                :icon = "ViberImage"
                buttonName = "Viber"
            />
        </div>
        <div class="credits">
            &copy; Anka.Bijou 2022. Некоторые иконки с сайта <a href="http://www.onlinewebfonts.com/icon">Icon Fonts</a> лицензированы CC BY 3.0
        </div>
    </footer>
</template>

<script>
import IconButton from './IconButton.vue'
import InstagramImage from '../assets/instagram.svg'
import TikTokImage from '../assets/tiktok.svg'
import VKImage from '../assets/vk.svg'
import WhatsAppImage from '../assets/whatsapp.svg'
import ZenImage from '../assets/zen-new-icon.svg'
import TelegramImage from '../assets/telegram.svg'
import ViberImage from '../assets/viber.svg'

export default {
    name: 'Footer',
    data: () => ({
        InstagramImage,
        TikTokImage,
        VKImage,
        WhatsAppImage,
        ZenImage,
        TelegramImage,
        ViberImage,
    }),
  components: { IconButton },
}
</script>

<style>
.footer {
    padding: 15px 0;
    background: linear-gradient(90deg,rgba(255,255,255,0) 20%, rgba(255,255,255,1) 30%, rgba(255,255,255,1) 70%, rgba(255,255,255,0) 80%);
}
.footer p {
    margin: 0 20px;
}
.iconline {
    display: flex;
    justify-content: center;
}
.credits {
    font-size: 10pt;
    color: darkgray;
    margin: 0 20px;
    text-align: center;
}
.credits a {
    color: darkgray;
    text-decoration: none;
}
.credits a:hover {
    color: darkred;
}
</style>
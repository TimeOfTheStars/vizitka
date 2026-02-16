<template>
    <video class="hero__video" autoplay muted loop playsinline>
        <source src="/IMG_5223.mp4" type="video/mp4" />
        Ваш браузер не поддерживает видео
    </video>
    <section class="hero">

        <div class="hero__inner container">
            <h1 class="hero__title">Стань частью нашей команды!</h1>
        </div>
    </section>
</template>

<script setup lang="ts"></script>

<style scoped>
.hero {
    position: relative;
    padding: 4rem 0;
    text-align: center;
    overflow: hidden;
    min-height: 700px;
    display: flex;
    align-items: center;
    justify-content: center;
    margin-top: 70px;
}

.hero__video {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    object-fit: cover;
    z-index: 1;
}

.hero__overlay {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: rgba(0, 0, 0, 0.4);
    z-index: 2;
}

.hero__inner {
    max-width: 600px;
    position: relative;
    z-index: 3;
}

.hero__title {
    font-size: 2.5rem;
    margin: 0;
    line-height: 1.2;
    color: white;
    text-shadow: 2px 2px 8px rgba(0, 0, 0, 0.6);
}

@media (max-width: 600px) {
    .hero__title {
        font-size: 1.75rem;
    }

    .hero {
        min-height: 350px;
    }
}
</style>

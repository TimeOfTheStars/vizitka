<template>
    <video class="hero__video" autoplay muted loop playsinline>
        <source src="/IMG_5223.mp4" type="video/mp4" />
        Ваш браузер не поддерживает видео
    </video>
    <div class="hero__overlay" aria-hidden="true"></div>
    <section class="hero">

        <div class="hero__inner container">
            <h1 class="hero__title">Стань частью нашей команды!</h1>
            <img
                src="/logo-star-kids.webp"
                alt=""
                class="hero__league-icon"
            />
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
    inset: 0;
    z-index: 2;
    pointer-events: none;
    background-color: rgba(0, 25, 80, 0.6);
    background-image: radial-gradient(
        circle at center,
        rgba(255, 255, 255, 0.35) 1px,
        transparent 1px
    );
    background-size: 12px 12px;
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

.hero__league-icon {
    display: none;
}

@media (max-width: 600px) {
    .hero__inner {
        display: flex;
        flex-direction: column;
        align-items: center;
    }

    .hero__league-icon {
        display: block;
        order: -1;
        width: 200px;
        height: auto;
        margin: 0 auto 1.25rem;
    }

    .hero__title {
        font-size: 1.75rem;
    }

    .hero {
        min-height: 350px;
    }
}
</style>

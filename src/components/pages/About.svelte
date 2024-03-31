<script>
    import TextMedia from "../layout/TextMedia.svelte";
    import Banner from "../layout/Banner.svelte";
</script>

<div class="about">
    <div class="about__content">
        <TextMedia />
    </div>

    <Banner />
</div>

<style lang="scss">
    .about {
        &__content {
            height: 100vh;
        }
    }
</style>
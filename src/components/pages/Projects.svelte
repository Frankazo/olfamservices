<script>
    import Banner from '../layout/Banner.svelte';
</script>

<div class="projects">
    <div class="projects__content">
        <h2>Coming Soon</h2>
    </div>
    <Banner />
</div>

<style lang="scss">
    .projects {
        &__content {
            height: 100vh;
            padding: 100px 0;
            display: flex;
            justify-content: center;
            align-items: center;
            color: #000;
        }
    }
</style>
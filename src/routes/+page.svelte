<script lang="ts">
    import Decorations from "../components/Decorations.svelte";

</script>

<Decorations />
<main style:height="90dvh">
    <div class="paint-tools-bar">
        toolbar
    </div>
    <div class="main-region">
        <div class="paint-region">
            canvas
        </div>
        <div class="properties-bar">
            properties
        </div>
    </div>
</main>

<style lang="sass">

    main
        width: 90%
        margin: 0 auto

        display: flex
        flex-direction: column

        gap: 10px

    .main-region
        display: grid
        grid-template-columns: 2fr 1fr
        gap: 10px
        height: 70dvh

    .paint-tools-bar, .paint-region, .properties-bar
        background-color: #fff
        border-radius: 10px

    .paint-tools-bar
        height: 100px

</style>

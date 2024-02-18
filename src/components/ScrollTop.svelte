<script>
    const handleClick = () => document.body.scrollIntoView({ behavior: "smooth"});
    export let scroll;
</script>

<!--scroll to top-->
<button class="scroll-top" class:active={scroll >= 600} on:click={handleClick}>
    <i class="fa fa-angle-up" aria-hidden="true"></i>
</button>

<style lang="scss">
    .scroll-top {
        display: flex;
        justify-content: center;
        align-items: center;
        bottom: 20px;
        font-size: 20px;
        height: 40px;
        position: fixed;
        text-align: center;
        width: 40px;
        z-index: 10;
        cursor: pointer;
        transition: .3s;
        border-radius: 50%;
        line-height: 40px;
        right: -100px;
        color: #ffffff;
        background-color: rgba(29, 233, 182, 0.5); 

        &:hover {
            background-color: #1de9b6;
            transition: all .4s ease-in-out; 
        }

        &.active {
            right: 20px; 
        }
    }
</style>
<script>
	import XIcon from './../../assets/XIcon.svelte';
	import {fade} from 'svelte/transition'
    import { clickOutside } from '../../constants/clickOutside';
    export let currentService;
	let showing = false;
    let selectedImg = '';


</script>


<div class="grid">
    {#each currentService.images as img}
        <button class="grid__item" on:click={() => {selectedImg = img; showing = true;}}>
            <img src="{img}" alt="">
        </button>
    {/each}
</div>

{#if showing}
    <div class="imageModal" transition:fade={{duration: 100}}>
        <div class="imageModal__content" use:clickOutside on:click_outside={() => showing = false}>
            <button class="imageModal__close" on:click={()=>{showing = false}}><XIcon /></button>
            <img src="{selectedImg}" alt="">
        </div>
    </div>
{/if}

<style lang="scss">
	.grid {
        max-width: 1600px;
		display: grid;
		grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
		grid-gap: 0.8rem;
	}

    .imageModal {
        display: flex;
        justify-content: center;
        align-items: center;
        overflow-y:scroll;
        overflow-x:hidden;
        position:fixed;
        top: 0;
        left: 0;
        z-index: 100;
        padding:1rem;
        width:100%;
        height:100%;
        background-color: rgba(0,0,0,0.8);

        &__content {
            img {
                height: 90vh;
            }
        }
        
        &__close {
            color: #fff;
            position: absolute;
            top: -20px;
            right: -40px;
            width: 40px;
            height: 40px;
        }
    }

    button {
        background-color: transparent;
        cursor: pointer;
        &:focus {
            outline:0;
        }
    }

    @media only screen and (max-width: 767px) {
	    .grid {
            padding: 0 20px;
            grid-template-columns: repeat(auto-fit, minmax(100%, 1fr));
        }

        .imageModal {
            padding: 0 20px;
            &__close {
                top: -40px;
                right: -10px;
            }
        }
    }
</style>
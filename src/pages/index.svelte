<script>
    import Card from './component/_card.svelte'
    import {tab} from '../store.js'
</script>
<div class="wildcard">
    {#if $tab == 'recent-activities'}
        recent-activities
    {/if}
    {#if $tab == 'projects'}
        projects
    {/if}
    {#if $tab == 'tech'}
        tech
    {/if}
    {#if $tab == 'misc'}
        misc
    {/if}
    
</div>
<style>
    .wildcard{
        display: flex;
        justify-content: center;
        align-items: center;
        height: 100%;
        width: 100%;
        background: rgb(255, 255, 255);
    }
</style>
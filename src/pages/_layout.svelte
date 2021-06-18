<script>
    import Profile from './_profile.svelte'
    import {tab} from '../store.js'

</script>

<div id="logical-body">
    <div id="profile">
        <Profile />
    </div>
    
    <div id="nav">
        <div id="slot">
            <slot />
        </div>
        <div id="navbar">
            <button style={$tab == 'recent-activities'? "background:white; color:black" : ""} on:click={()=>{$tab = 'recent-activities'; }}><b>Recent Activities</b></button>
            <button style={$tab == 'projects'? "background:white; color:black" : ""} on:click={()=>{$tab = 'projects'}}><b>Projects</b></button>
            <button style={$tab == 'tech'? "background:white; color:black" : ""} on:click={()=>{$tab = 'tech'}}><b>Tech</b></button>
            <button style={$tab == 'misc'? "background:white; color:black" : ""} on:click={()=>{$tab = 'misc'}}><b>Misc</b></button>
        </div>
    </div>
</div>

<style>
    #profile{
        background: rgb(255, 255, 255);
        margin: 10px;
        width: 24vw;
        height: 86vh;
        border: 2px solid black;
        box-shadow: 4px 4px;
        border-radius: 3px;
    }
    #nav{
        background: rgb(255, 255, 255);
        margin: 10px;
        width: 72vw;
        height: 86vh;
        display: flex;
        flex-direction: column;
        border: 2px solid black;
        box-shadow: 4px 4px;
    }
    #slot{
        width: 100%;
        height: 90%;
        background: rgb(255, 255, 255);
    }

    #navbar{
        width: 100%;
        height: 10%;
        display: flex;
    }

    #logical-body{
        height: 100vh;
        width: 100vw;
        display: flex;
        justify-content: center;
        align-items: center;
    }
    button{
        width: 100%;
        border: none;
        color: orangered;
        background: rgb(25, 3, 36);
        font-size: large;
        outline: none;
    }
    button:hover{
        color: black;
        background: rgb(255, 255, 255);
        transition: all 0.2s ease-in-out;
    }
</style>
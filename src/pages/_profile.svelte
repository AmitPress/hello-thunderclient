<script>
    import Upperbody from './_upperbody.svelte'
    import Middlebody from './_middlebody.svelte'
    import Button from './component/_button.svelte'
</script>

<div id="profile">
    <div id="upper">
        <Upperbody />
    </div>
    <div id="middle">
        <Middlebody />
    </div>
    <div id="lower">
        <Button btnName="Contact Me" />
    </div>

</div>

<style>
    #profile{
        background: pink;
        width: 100%;
        height: 100%;
        display: flex;
        flex-direction: column;
    }

    #upper{
        background-image: url('./probg.jpg');
        flex: 2;
        display: flex;
        justify-content: center;
        align-items: center;
        border: 2px solid rgb(255, 255, 255);
    }
    #lower{
        padding: 5px;
    }
    #middle{
        background: rgb(255, 255, 255);
        flex: 3;
        display: flex;
        justify-content: center;
        align-items: center;
        
    }


</style>
<script>
    export let title = 'default'
    export let tags = []
</script>

<div class="card">
    <div class="title">
        {title}
    </div>
    <ul class="tags">
        Tags:
        {#each tags as tag}
            <li>
                {tag}
            </li>
        {/each}
    </ul>
</div>

<style>
    .card{
        position: relative;
        padding: 20px;
        color: white;
        background: linear-gradient(to right top, #833ab4, #b221a3, #d6008b, #ee006d, #fb004c, #ff2a3c, #ff4229, #fe570f, #fe7218, #fd8926, #fc9d37, #fcb04b);
        width: 60%;
        height: 21%;
        border: 2px solid black;
        transition: all .2s ease-in-out;
    }
    .card:hover{
        transform: scale(1.02);
    }
    .tags{
        position: absolute;
        bottom: 20px;
        list-style-type: none;
    }
    li{
        margin: 5px;
        padding: 2px;
        border-radius: 3px;
        display: inline-block;
        color: rgb(255, 255, 255);
        background: rgb(56, 16, 56);
    }
</style>
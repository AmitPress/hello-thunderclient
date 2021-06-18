<script>

	import {onMount} from 'svelte';
    export let btnName = "click"
	let btn;
	onMount(()=>{
		btn = document.getElementById('btn')
		btn.addEventListener('click',(e)=>{
			let circle = document.createElement('span');
			const d = Math.max(e.target.clientWidth, e.target.clientHeight);
			circle.style.width = circle.style.height = d + "px";
			circle.style.left = e.layerX - d / 2 + "px";
			circle.style.top = e.layerY - d / 2 + "px";
			circle.classList.add("ripple");
			e.target.appendChild(circle);
		})
	})
	
</script>


<div id="btn">
	{btnName}
</div>


<style>

	#btn{
		position: relative;
		display: flex;
		justify-content: center;
		align-items: center;
		cursor: pointer;
		width: 100%;
		height: 80px;
		background: rgb(18, 32, 233);
		text-transform: uppercase;
		color: white;
		overflow: hidden;
	}
    #btn:hover{
        background: rgb(0, 0, 165);
        transition: ease-out 0.5s;
    }
	
    :global(.ripple) {
  width: 50px;
  height: 50px;
  border-radius: 50%;
  background-color: rgba(255, 255, 255, 1);
  position: absolute;
  transform: scale(0);
  animation: ripple 0.7s linear;
  pointer-events: none;
	}
	@keyframes ripple {
		to {
			transform: scale(2.5);
			opacity: 0;
		}
	}

</style>


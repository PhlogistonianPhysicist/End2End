<!-- TODO have constants defined for arena height and width -->
<script>
	import { onMount } from 'svelte';
	let canvas;
	onMount(() => {
        const x_circle_center = 
		const ctx = canvas.getContext('2d');
		ctx.fillStyle = 'red';
		ctx.fillRect(0, 0, 150, 75);
	});
</script>

<p>This is where the canvas is</p>
<canvas
	bind:this={canvas}
	id="curlingSheet"
	height="300"
	width="660"
	style="border:1px solid black;"
></canvas>

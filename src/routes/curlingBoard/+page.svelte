<script>
	const c_height = 122.5;
	const c_width = 245;
	const y_circle_center = c_height / 2;
	const x_circle_center = (c_width * 6) / 27;

	import { onMount } from 'svelte';
	let canvas;
	onMount(() => {
		const ctx = canvas.getContext('2d');
		ctx.beginPath();
		ctx.arc(x_circle_center, y_circle_center, (6 / 33) * c_width, 0, 2 * Math.PI, false);

		ctx.fillStyle = 'blue';
		ctx.fill();
		ctx.beginPath();

		ctx.arc(x_circle_center, y_circle_center, (4 / 33) * c_width, 0, 2 * Math.PI, false);
		ctx.fillStyle = 'white';
		ctx.fill();
		ctx.beginPath();

		ctx.arc(x_circle_center, y_circle_center, (2 / 33) * c_width, 0, 2 * Math.PI, false);
		ctx.fillStyle = 'red';
		ctx.fill();
		ctx.beginPath();

		ctx.arc(x_circle_center, y_circle_center, (0.5 / 33) * c_width, 0, 2 * Math.PI, false);
		ctx.fillStyle = 'yellow';
		ctx.fill();
		ctx.beginPath();
	});
</script>

<p>This is where the canvas is</p>
<canvas
	bind:this={canvas}
	id="curlingSheet"
	height={c_height}
	width={c_width}
	style="border:1px solid black;"
></canvas>

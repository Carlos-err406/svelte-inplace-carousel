<script lang="ts">
	import * as Carousel from '$lib/index.js';
</script>

<div class="h-[354px]">
	<Carousel.Root interval={30000}>
		<svelte:fragment let:builder slot="prev">
			<button {...builder} type="button" class="scale-150">◀️</button>
		</svelte:fragment>
		<svelte:fragment let:builder slot="next">
			<button {...builder} type="button" class="scale-150">▶️</button>
		</svelte:fragment>
		<Carousel.Item>
			<div class="size-60 flex items-center justify-center bg-red-500">A</div>
			<svelte:fragment slot="footer">
				<div class="flex flex-col gap-2">
					<span> Hello this is the footer for A </span>
					<span> Hello this is the footer for A </span>
				</div>
			</svelte:fragment>
		</Carousel.Item>
		<Carousel.Item>
			<div class="size-60 flex items-center justify-center bg-blue-500">B</div>
			<svelte:fragment slot="footer">Hello this is the footer for B</svelte:fragment>
		</Carousel.Item>
		<Carousel.Item>
			<div class="size-60 flex items-center justify-center bg-yellow-500">C</div>
		</Carousel.Item>
		<Carousel.Item>
			<div class="size-60 flex items-center justify-center bg-pink-500">D</div>
		</Carousel.Item>
		<Carousel.Item>
			<div class="size-60 flex items-center justify-center bg-green-500">E</div>
		</Carousel.Item>
	</Carousel.Root>
</div>
<div>something outside the carousel</div>

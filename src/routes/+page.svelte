<script lang="ts">
	import BentoGrid from '../components/bento/grid/index.svelte';
	import BentoCard from '../components/bento/card/index.svelte';

	let selected = 0;

	async function flip(id: number) {
		selected = id;
	}

</script>

<div class="flex-1 flex flex-col justify-center">
	<BentoGrid>
    {#each Array.from({ length: 8 }) as _, i}
      {@const details = selected === i}
      {@const number = i + 1}
		<BentoCard active={details} on:click={() => flip(i)}>
		</BentoCard>
  {/each}
</BentoGrid>
</div>

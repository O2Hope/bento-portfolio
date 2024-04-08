<script lang="ts">
	import { Card } from 'flowbite-svelte';

  interface $$Props {
    class?: string;
    active?: boolean;
  }

  export let active: $$Props["active"] = false;
</script>

<Card padding="none" class={`min-h-[280px] max-w-full ${active ? "row-span-2 md:col-span-2" : ""}`}>
	<slot />
</Card>


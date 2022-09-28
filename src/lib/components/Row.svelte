<script type="ts">
	import Stack from './Stack.svelte';

	export let breakpoint: 'small' | 'medium' | undefined = undefined;
	export let gap: 'small' | 'medium' | 'large' | 'none' | number = 'medium';
	export let align: 'flex-start' | 'flex-end' | 'center' | 'baseline' | 'stretch' = 'center';
	export let justify:
		| 'flex-start'
		| 'flex-end'
		| 'center'
		| 'space-between'
		| 'space-around'
		| 'space-evenly' = 'center';
</script>

<Stack direction="row" {breakpoint} {gap} {align} {justify}>
	<slot />
</Stack>

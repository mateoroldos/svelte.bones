<script type="ts">
	export let padding: 'small' | 'medium' | 'large' = 'medium';
</script>

<div class={padding}>
	<slot />
</div>

<style>
	.small {
		padding-block: var(--card-padding-s, 2rem);
	}
	.medium {
		padding-block: var(--section-padding-m, 4rem);
	}
	.large {
		padding-block: var(--section-padding-l, 6rem);
	}
</style>

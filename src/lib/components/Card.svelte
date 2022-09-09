<script type="ts">
	export let padding: 'small' | 'medium' | 'large' = 'medium';
</script>

<div class={padding}>
	<slot />
</div>

<style>
	.small {
		padding-block: var(--bones-card-padding-s, 2rem);
	}
	.medium {
		padding-block: var(--bones-card-padding-m, 4rem);
	}
	.large {
		padding-block: var(--bones-card-padding-l, 6rem);
	}
</style>

<script>
	export let title;
</script>

<header class="header">
	<h2 class="header__title">{title}</h2>
</header>

<style>
	.header {
		padding: 3rem 0 2rem 0;
		border-top: 2px solid var(--neutral-three);
	}

	.header__title {
		color: var(--neutral-seven);
		font-size: 0.875rem;
		line-height: 1.25rem;
		letter-spacing: 0.1em;
		text-transform: uppercase;
		font-weight: 400;
	}
</style>

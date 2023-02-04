<script>
	export let name;
	export let description;
	export let contacts;
</script>

<div class="contact">
	<div class="contact__container">
		<header class="contact__header">
			<h1 class="contact__name">{name}</h1>
			<p class="contact__description">{description}</p>
		</header>
		<div class="contact__contacts">
			{#each contacts as { id, href, text } (id)}
				<p><a class="contact__link" {href}>{text}</a></p>
			{/each}
		</div>
	</div>
</div>

<style>
	.contact {
		padding: 5rem 2rem 1.5rem 2rem;
	}

	.contact__container {
		display: flex;
		gap: 2rem;
		justify-content: space-between;
		align-items: flex-end;
		max-width: 67rem;
		margin: 0 auto;
	}

	.contact__header {
		max-width: 32.5rem;
	}

	.contact__name {
		color: var(--neutral-ten);
		font-size: 3rem;
		line-height: 1;
		font-weight: 700;
	}

	.contact__description {
		color: var(--neutral-eight);
		margin-top: 1rem;
		font-size: 1rem;
		line-height: 1.5rem;
		font-weight: 400;
	}

	.contact__contacts > :not(:first-child) {
		margin-top: 0.25rem;
	}

	.contact__link {
		text-decoration: none;
		color: var(--neutral-eight);
		font-size: 1rem;
		line-height: 1.5rem;
		font-weight: 400;
	}

	.contact__link:hover,
	.contact__link:focus-visible {
		color: var(--brand-one);
	}

	.contact__link:focus-visible {
		text-decoration: underline;
	}

	@media (max-width: 640px) {
		.contact {
			padding-left: 1rem;
			padding-right: 1rem;
		}

		.contact__container {
			flex-direction: column;
			justify-content: flex-start;
			align-items: flex-start;
			gap: 1rem;
		}

		.contact__name {
			font-size: 2.25rem;
			line-height: 2.5rem;
		}

		.contact__description {
			font-size: 0.875rem;
			line-height: 1.25rem;
			margin-top: 0.75rem;
		}

		.contact__link {
			font-size: 0.875rem;
			line-height: 1.25rem;
		}
	}
</style>

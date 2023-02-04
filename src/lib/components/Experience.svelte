<script>
	export let experience;

	let { position, company, date, location, description, bullets } = experience;
</script>

<div class={$$props.class}>
	<div class="experience__trim">
		<div class="experience__marker">
			<div class="experience__dot" />
		</div>
		<div class="experience__border" />
	</div>
	<div class="experience__details">
		<header class="experience__role">
			<h3 class="experience__position">{position}</h3>
			<p class="experience__company">{company}</p>
		</header>
		<div class="experience__period">
			<p class="experience__date">{date}</p>
			<p class="experience__location">{location}</p>
		</div>
		<p class="experience__description">{description}</p>
		<ul class="experience__bullets">
			{#each bullets as bullet}
				<li class="experience__bullet">{bullet}</li>
			{/each}
		</ul>
	</div>
</div>

<style>
	.experience__item {
		max-width: 49rem;
		display: flex;
		gap: 2rem;
	}

	.experience__trim {
		display: flex;
		flex-direction: column;
		align-items: center;
		gap: 1rem;
		flex: none;
		padding-top: 0.25rem;
	}

	.experience__marker {
		width: 1.5rem;
		height: 1.5rem;
		border-radius: 9999px;
		background-color: var(--neutral-three);
		display: flex;
		align-items: center;
		justify-content: center;
		flex: none;
	}

	.experience__dot {
		width: 0.5rem;
		height: 0.5rem;
		border-radius: 9999px;
		background-color: var(--neutral-ten);
	}

	.experience__border {
		flex: 1 1 0%;
		width: 2px;
		background-color: var(--neutral-three);
	}

	.experience__details {
		flex: 1 1 0%;
	}

	.experience__position {
		display: inline-block;
		color: var(--neutral-ten);
		font-size: 1.5rem;
		line-height: 2rem;
		font-weight: 600;
	}

	.experience__company {
		display: inline-block;
		color: var(--neutral-six);
		margin-left: 0.75rem;
		font-size: 1.5rem;
		line-height: 2rem;
		font-weight: 400;
	}

	.experience__period {
		margin-top: 0.75rem;
	}

	.experience__date {
		display: inline-block;
		color: var(--neutral-eight);
		font-size: 0.875rem;
		line-height: 1.25rem;
		font-weight: 600;
	}

	.experience__location {
		display: inline;
		color: var(--neutral-six);
		margin-left: 1rem;
		font-size: 0.875rem;
		line-height: 1.25rem;
		font-weight: 500;
	}

	.experience__description {
		margin-top: 1rem;
		color: var(--neutral-eight);
		font-size: 1rem;
		line-height: 1.5rem;
		font-weight: 400;
	}

	.experience__bullets {
		margin-top: 1rem;
		list-style: disc;
		padding-left: 2.5rem;
	}

	.experience__bullets > :not(:first-child) {
		margin-top: 0.75rem;
	}

	.experience__bullet {
		color: var(--neutral-eight);
		font-size: 1rem;
		line-height: 1.5rem;
		font-weight: 400;
	}

	@media (max-width: 640px) {
		.experience__position {
			display: block;
			font-size: 1.25rem;
			line-height: 1.75rem;
		}

		.experience__company {
			display: block;
			font-size: 1.25rem;
			line-height: 1.75rem;
			margin-left: 0;
			margin-top: 0.125rem;
		}

		.experience__description {
			margin-top: 0.75rem;
			font-size: 0.875rem;
			line-height: 1.5rem;
		}

		.experience__bullets {
			margin-top: 0.75rem;
			padding-left: 1.875rem;
		}

		.experience__bullets > :not(:first-child) {
			margin-top: 0.5rem;
		}

		.experience__bullet {
			font-size: 0.875rem;
			line-height: 1.5rem;
		}
	}
</style>

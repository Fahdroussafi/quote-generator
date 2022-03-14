<template>
	<section class="quote">
		<div class="quote-content">
			{{ quote.content }}
		</div>
		<div class="quote-info">
			<div class="quote-info-anime">
				{{ quote.anime }}
			</div>
			<div class="quote-info-author">
				{{ quote.character }}
			</div>
		</div>
	</section>
</template>

<script>
export default {
	props: ['quote']
}
</script>

<style lang="scss" scoped>
.quote {
	position: relative;
	padding: 32px;
	margin: 0 auto;
	max-width: 720px;

	&-content {
		position: relative;
		font-size: 1.5em;
		font-weight: 700;
		background-color: var(--dark);
		color: var(--light);
		padding: 48px 32px;
		border-radius: 16px;

		&:before, 
		&:after {
			content: "\"";
			color: var(--grey);
			margin: 0 2px;
		}
	}

	&-info {
		position: absolute;
		top: 0;
		left: 0;
		right: 0;
		bottom: 0;
		padding: 32px;

		&-author, &-anime {
			position: absolute;

			padding: 12px 16px;
			font-size: 1.2em;
			font-weight: 400;
			border-radius: 99px;
			color: var(--light);
			text-align: center;
		}

		&-author {
			top: calc(100% - 32px);
			right: 0px;
			transform: translateY(-50%);
			background-color: var(--secondary);
		}

		&-anime {
			top: 0px;
			left: 0px;
			background-color: var(--tertiary);
			color: var(--dark);
		}
	}
}
</style>
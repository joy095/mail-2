<script>
	import Icon from '@iconify/svelte';
</script>

<div class="bar">
	<div class="location">
		<p>Location</p>
		<input type="text" placeholder="Where are you going?" />
	</div>
	<div class="check-in">
		<p>Check in</p>
		<input type="text" placeholder="Add dates" />
	</div>
	<div class="check-out">
		<p>Check out</p>
		<input type="text" placeholder="Add dates" />
	</div>
	<div class="guests">
		<p>Guests</p>
		<input type="text" placeholder="Add guests" />
		<span>
			<Icon icon="material-symbols-light:search" width="24" height="24" />
		</span>
	</div>
</div>

<style>
	.bar {
		width: 650px;
		background: white;
		box-shadow: 0 0 5px hsl(0 0% 78%);
		height: 55px;
		border-radius: 100vw;
		display: flex;
		justify-content: center;
		font-size: 0.6rem;
		border: 1px solid hsl(0 0% 94%);
	}

	.bar div {
		border-radius: inherit;
		padding: 0.8rem 1.5rem;
		transition: background 250ms ease;
	}

	.bar div:hover {
		background: hsl(0 0% 94%);
	}

	.location {
		width: 34%;
	}
	.check-in,
	.check-out,
	.guests {
		width: 22%;
	}

	input {
		color: black;
	}

	p {
		color: black;
	}

	input[type='text'] {
		background: none;
		border: none;
		padding: 0.2rem 0 0 0;
	}

	input[type='text']:focus {
		outline: none;
	}

	::placeholder {
		font-size: 0.75rem;
	}

	.guests {
		position: relative;
	}
	.guests span {
		position: absolute;
		top: 50%;
		right: 10px;
		transform: translateY(-50%);
		background: #ff385c;
		color: white;
		font-size: 0.8rem;
		padding: 0.7rem;
		border-radius: 50%;
	}

	.bar > div {
		position: relative;
	}

	.bar > div::before {
		position: absolute;
		content: '';
		left: 0;
		top: 50%;
		transform: translateY(-50%);
		width: 1px;
		height: 55%;
		background: hsl(0 0% 90%);
	}

	.bar > div:nth-of-type(1)::before {
		background: transparent;
	}

	.bar > div:hover::before {
		background: transparent;
	}
</style>

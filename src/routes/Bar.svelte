<script>
	export let activeId = '0';
	export let single = false;

	const nav = ['Банки', 'Промышленость', 'IT компании', 'Ритейл', 'Банки2', 'Промышленость2'];
	let animation = 'left';
	let a = 0;
	let id = a;

	/**
	 * @param {number} a
	 */
	function numberCheck(a) {
		a = a % 6;
		if (a < 0) a = 6 + a;
		return a;
	}

	/**
	 * @param {{ target: any; }} event
	 */
	function handleClick(event) {
		if (event.target.id == 'left') {
			animation = 'left';
			a = a - 1;
			id = numberCheck(a);

			if (single) activeId = id.toString();
			return;
		}
		if (event.target.id == 'right') {
			animation = 'right';
			a = a + 1;
			id = numberCheck(a);

			if (single) activeId = id.toString();
			return;
		}
		activeId = event.target.id;
	}
</script>

<ul style:grid-template-columns={single ? '46px 1fr 46px' : '46px 1fr 1fr 1fr 1fr 46px'}>
	<!-- svelte-ignore a11y-click-events-have-key-events -->
	<li><a id="left" on:click={handleClick}>&lt;</a></li>
	{#if single}
		<!-- svelte-ignore a11y-missing-attribute -->
		<li><a>{nav[+activeId]}</a></li>
	{:else}
		{#each Array.from({ length: 4 }, (_, i) => i) as i}
			{@const checked = numberCheck(id + i).toString()}
			<li>
				{#key a}
					<!-- svelte-ignore a11y-click-events-have-key-events -->
					<a
						id={checked}
						class={animation}
						class:active={activeId === checked}
						on:click={handleClick}
					>
						{nav[+checked]}
					</a>
				{/key}
			</li>
		{/each}
	{/if}

	<!-- svelte-ignore a11y-click-events-have-key-events -->
	<li><a id="right" on:click={handleClick}>&gt;</a></li>
</ul>

<style>
	ul {
		list-style-type: none;
		margin: 0;
		padding: 0;
		user-select: none;
		max-width: 1000px;
		left: 50%;
		position: relative;
		transform: translateX(-50%);
		overflow: hidden;
		padding: 1rem;
		display: grid;
		gap: 1rem;
		justify-self: center;
	}

	#left,
	#right {
		transition: transform 0.3s;
		position: relative;
		max-width: 46px;
		flex-grow: 0;
		box-shadow: 0 0 8px rgba(0, 0, 0, 0.3);
		background-color: white;
		border-radius: 100%;
		z-index: 10;
		cursor: pointer;
	}

	#left:hover,
	#right:hover {
		transform: scale(0.95);
		color: #635ef6;
	}

	li {
		float: left;
	}

	li a {
		display: block;
		color: black;
		text-align: center;
		padding: 14px 16px;
		text-decoration: none;
		border-radius: 0.5rem;
		cursor: pointer;
		box-shadow: 0 1px 2px rgba(0, 0, 0, 0.2);
	}

	li a:hover:not(.active) {
		background-color: #817ec7;
		color: white;
	}

	.active {
		background-color: #635ef6;
		color: white;
	}

	.left {
		z-index: 10;
		animation: left 0.3s 1;
	}
	.right {
		z-index: 10;
		animation: right 0.3s 1;
	}

	@keyframes right {
		0% {
			transform: translateX(100%);
		}
		100% {
			transform: translateX(0%);
		}
	}
	@keyframes left {
		0% {
			transform: translateX(-100%);
		}
		100% {
			transform: translateX(0%);
		}
	}
</style>

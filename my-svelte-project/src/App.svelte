<script>
	export let count;
	$: doubled = count * 2;

	$: if (count >= 10) {
		alert("Count access the limit!");
		count = 9;
	}

	function handleClick() {
		count++;
	}
</script>

<button on:click={handleClick}>
	Clicked
	{count}
	{count === 1 ? 'time' : 'times'}
</button>

<p>{count} doubled is {doubled}</p>

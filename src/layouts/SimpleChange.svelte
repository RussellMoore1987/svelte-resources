<script>
    let count = 0;
	$: doubled = count * 2;

	$: console.log(`the count is ${count}`);
	$: {
		console.log(`the count is ${count}`);
		console.log(`I SAID THE COUNT IS ${count}`);
	}
	$: if (count >= 10) {
		console.log(`count is dangerously high!`);
		count = 9;
	}

  	function incrementCount() {
		count += 1;
	}
</script>

<p>{count} doubled is {doubled}</p>
<button on:click={incrementCount}>
	Clicked {count} {count === 1 ? 'time' : 'times'}
</button>
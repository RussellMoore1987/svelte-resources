<script>
    let name = "Max";
	let age = 30;

    // let uppercaseName; not required!

	$: uppercaseName = name.toUpperCase();

    $: console.log(name);

    // this particular set of code runs when name changes
    $: if (name === 'Maximilian') {
        console.log('It runs!');
        age = 31;
    }

    // this particular set of code runs when either name or age changes
    // $: if (name === 'Maximilian' && age > 50) {
    // 	console.log('It runs!');
    // 	age = 31;
    // }

    function incrementAge() {
		age += 1;
	}

	function changeName() {
		name = 'Maximilian';
	}

	function changeName2() {
		name = 'Max';
	}

	function nameInput(event) {
		const enteredValue = event.target.value;
		name = enteredValue;
	}
</script>


<h1>Welcome to SvelteKit dsfgdgvs {name}</h1>
<input type="text" bind:value="{name}" />
<p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>
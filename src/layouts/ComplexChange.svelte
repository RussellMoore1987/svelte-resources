<script>
    // ? https://svelte.dev/tutorial/updating-arrays-and-objects
    let numbers = [1, 2, 3, 4];
    const character = {
        name: 'Thorgrim',
        characterType: 'Viking'
    };

	$: sum = numbers.reduce((t, n) => t + n, 0);

    function addNumber() {
        numbers = [...numbers, numbers.length + 1];
    }

    function changeCharacter() {
        if (character.name === 'Thorgrim') {
            character.name = 'Thorgrim Jr.';
            character.characterType = 'Dentist';
            return;
        }
        // another way
        character.name = 'Thorgrim';
        character.characterType = 'Viking';
    }
</script>

<p>{numbers.join(' + ')} = {sum}</p>

<button on:click={addNumber}>
	Add a number
</button>

<p>Character Name: {character.name}</p>
<p>Character Type: {character.characterType}</p>
<button on:click={changeCharacter}>
	Change Character
</button>
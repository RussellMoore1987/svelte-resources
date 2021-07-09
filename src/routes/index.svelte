<script>
	import Card from '../layouts/card.svelte'
	import Card2 from '../layouts/card2.svelte'
	import MaxSection from '../layouts/max_section.svelte'
	import Img from '../layouts/img.svelte'
	import ComplexChange from '../layouts/ComplexChange.svelte'
	import SimpleChange from '../layouts/SimpleChange.svelte'

	let string = `this string contains some <strong>HTML!!!</strong>`;
</script>

<h2>Two way binding and inputs</h2>
<hr>
<MaxSection/>
<br><br><br><br>

<h2>Working with images special syntax</h2>
<hr>
<Img/>
<br><br><br><br>

<h2>Card component</h2>
<hr>
<Card></Card>
<Card/>
<br><br><br><br>

<!-- need to make shure it is clean, no mulishis code -->
<h2>Things to work with special HTML characters</h2>
<hr>
{@html string}
<br>
{string}
<br><br><br><br>

<h2>Changing simple variables</h2>
<hr>
<SimpleChange/>
<br><br><br><br>

<h2>Changing arrays and objects</h2>
<hr>
<ComplexChange/>
<br><br><br><br>

<h2>Passing props</h2>
<hr>
<!-- <Card2/>  --> <!-- not working -->
<Card2 answer="42"/>
<Card2 answer={31}/>
<Card2 answer={36}>
	<Card/>
</Card2>
<Card2 answer={22}>
	<Card/>
</Card2>
<Card2 answer={999}>
	<Img/>
</Card2>

<br><br><br><br>

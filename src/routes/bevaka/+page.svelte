<script>
	let availableCourses = ['Ängen', 'Queens'];
	let courses = [];

	$: console.log(courses);

</script>



<h1>
	Bevaka
</h1>

<form method="POST">

	<label>
		Datum
		<input name="date" type="date">
	</label>
	<label>
		Från klockan
		<input name="fromTime" type="time">
	</label>
	<label>
		Till klockan
		<input name="toTime" type="time">
	</label>
	<label>
		Antal spelare
		<input name="players" type="number">
	</label>
	<label>
		Bana/Banor

		{#each availableCourses as courseOption}
			<label>
				<input type="checkbox" bind:group={courses} value={courseOption} />
				{courseOption}
			</label>
		{/each}

	</label>
	<label>
		Email
		<input name="email" type="email">
	</label>
	<button>Starta bevakning</button>
</form>

<style>
	h1 {
		text-align: center;
	}
	form {
		display: flex;
		flex-direction: column;
		align-items: center;
	}
	label {
		display: flex;
		flex-direction: column;
		margin: 10px;
	}
	input {
		margin-top: 5px;
	}
</style>
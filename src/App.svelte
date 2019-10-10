<script>
	import "@ui5/webcomponents/dist/Table";
	import "@ui5/webcomponents/dist/TableColumn";
	import "@ui5/webcomponents/dist/TableRow";
	import "@ui5/webcomponents/dist/TableCell";

	let users = [];

	setImmediate(function () {
		users = [{ name: "John", username: "john1995", email: "john@example.com"},
			{name: "Carl",username: "cookie123",email: "carl.smith@example.com"}];
	});

</script>

<h1>UI5 1.0.0-rc.3 table problems with Svelte</h1>

<h2>Normal Table</h2>
<table>
	<tr>
		<th>Name</th>
		<th>Username</th>
		<th>Email</th>
	</tr>
	{#each users as user}
		<tr>
			<td>{user.name}</td>
			<td>{user.username}</td>
			<td>{user.email}</td>
		</tr>
	{/each}
</table>
<hr>
<h2>UI5-Table</h2>
<ui5-table>
	<ui5-table-column slot="columns">Name</ui5-table-column>
	<ui5-table-column slot="columns">Username</ui5-table-column>
	<ui5-table-column slot="columns">Email</ui5-table-column>
	{#each users as user}
		<ui5-table-row>
			<ui5-table-cell>{user.name}</ui5-table-cell>
			<ui5-table-cell>{user.username}</ui5-table-cell>
			<ui5-table-cell>{user.email}</ui5-table-cell>
		</ui5-table-row>
	{/each}
</ui5-table>
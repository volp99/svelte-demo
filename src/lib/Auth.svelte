<script lang="ts">
	let user = {loggedIn: false};

	function handleToggle() {
		user.loggedIn = !user.loggedIn;
	}
</script>

{#if user.loggedIn}
    <button on:click={handleToggle}>Logout</button>
{:else}
    <button on:click={handleToggle}>Login</button>
{/if}

<style>
	button {
		background: #ff3e00;
		color: white;
		padding: 10px;
		border: none;
		border-radius: 5px;
		cursor: pointer;
		width: 100px;
	}

	button:hover {
		background: #e8683f;
	}
</style>
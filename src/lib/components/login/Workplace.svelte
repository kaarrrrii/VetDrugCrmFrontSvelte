<script lang="ts">
	import TextInput from '$lib/components/login/TextInput.svelte';
	import SignInBtn from '$lib/components/login/SignInBtn.svelte';
</script>

<section class="workplace">
	<p class="title">Вход</p>
		<section class="input">
			<TextInput
				title="Почта"
			/>
			<TextInput
				title="Пароль"
			/>
		</section>
	<SignInBtn />
</section>

<style>
	* {
		margin: 0;
		padding: 0;
	}

	@import url('https://fonts.googleapis.com/css2?family=Montserrat:ital,wght@0,100..900;1,100..900&display=swap');

	.workplace {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		width: 62.5vw;
		aspect-ratio: 12/7;
		background-color: rgb(255, 255, 255);
		border-radius: 1.5vw;
		border: 1px solid #E3E3E3;
		box-shadow: -0.5px 4px 6px rgba(107, 107, 107, 0.25);
	}

	.title {
		font-family: "Montserrat", sans-serif;
		font-weight: 750;
		font-size: 3.5vw;
	}
</style>
<script lang="ts">
	import MenuButtonSidebar from '$lib/components/workspace/MenuButtonSidebar.svelte';
	import MenuButtonHeader from '$lib/components/workspace//MenuButtonHeader.svelte';
	import Search from '$lib/components/workspace/Search.svelte';
	import LogoutButton from '$lib/components/workspace/LogoutButton.svelte';
	import UserAvatar from '$lib/components/workspace/UserAvatar.svelte';

	type Props = {
		icon_notif?:string;
	}

	let {
		icon_notif ="src/lib/assets/Property 1=Variant2.svg",
	}: Props = $props();
</script>

<section class="workspace">
	<header class="workspace__header">
		<section class="header__content">
			<section class="header__menu">
				<MenuButtonHeader 
					title="Главная"
				/>
				<MenuButtonHeader 
					title="Пользователи"
				/>
				<MenuButtonHeader 
					title="Уведомления"
				/>
				<MenuButtonHeader 
					title="Журнал действий"
				/>
				<MenuButtonHeader 
					title="Отчёты"
				/>
				<section class="user__side">
					<img src={icon_notif} alt="" class="notifications">
					<Search/>
					<UserAvatar />
				</section>
			</section>
		</section>
	</header>
	<section class="workspace__content">
		<aside class="workspace__sidebar">
			<section class="sidebar__menu">
				<MenuButtonSidebar
					title="Главная"
					icon="src/lib/assets/Home.svg" 
				/>
				<MenuButtonSidebar
					title="Пользователи"
					icon="src/lib/assets/users.svg"
				/>
				<MenuButtonSidebar
					title="Уведомления"
					icon="src/lib/assets/Property 1=Default.svg"
				/>
				<MenuButtonSidebar
					title="Журнал действий"
					icon="src/lib/assets/журнал_действий.svg"
				/>
				<MenuButtonSidebar
					title="Отчёты"
					icon="src/lib/assets/отчеты_ocin.svg"
				/>
			</section>
			<LogoutButton />
		</aside>
		<main class="workspace__main"></main>
	</section>
	<footer class="workspace__footer"></footer>
</section>

<style>
	* {
		margin: 0;
		padding: 0;
	}
	.workspace {
		margin-top: 10vh;
		margin-left: 2.5vw;
		display: flex;
		flex-direction: column;
		align-items: center;
	}
	.workspace__header {
		width: 90vw;
		height: 10vh;
		background-color: white;
		border-radius: 10px 10px 0px 0px;
		box-shadow: 0px 4px 10px rgb(69 76 104/0.23);
		display: flex;
		align-items: center;
	}
	.workspace__content {
		display: flex;
		width: 90vw;
	}
	.workspace__main {
		width: 75vw;
		height: 60vh;
		background-color: #FBFBFB;
		box-shadow: inset 0 0 0 1px rgb(157 161 173/0.2);
		}
	.workspace__sidebar {
		width: 15vw;
		height: 60vh;
		background-color: white;
		box-shadow: 
				inset 0 0 0 1px rgb(157 161 173/0.20),
				0px 4px 10px 2px rgb(38 42 51 /0.05);
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: space-between;
	}
	.workspace__footer {
		width: 90vw;
		height: 10vh;
		background-color: white;
		border-radius: 0px 0px 10px 10px;
		box-shadow: 0px 2px 10px rgb(69 76 104/0.1);
	}

	.sidebar__menu {
		display: flex;
		flex-direction: column;
		justify-content: space-between;
	}

	.header__content {
		padding-left: 6.5vw;
	}
	
	.header__menu {
		display: flex;
		align-items: center;
		justify-content: space-between;
		gap: 0.1vw
	}

	.user__side {
		display: flex;
		align-items: center;
		gap: 2vw;
	}

	.notifications {
		width: 2.5vw;
		height: 2.5vw;
		margin-left: 1vw;
	}

	.notifications:hover {
		cursor: pointer;
		background-color: rgba(151, 151, 151, 0.1);
		border-radius: 10px;
	}

</style>
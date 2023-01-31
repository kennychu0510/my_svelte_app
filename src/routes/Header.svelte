<script>
	import moment from 'moment'
	const HEADER_LEFT_ITEMS = ['Home', 'File', 'Edit', 'View', 'Go', 'Window', 'Help'];
	const date = moment().format('ddd D MMM')
	let time = moment().format('H:mm A')
	setInterval(() => {
		time = moment().format('H:mm A')
	}, 1000)
</script>

<header>
	<div class="group">
		<svg role="img" id="apple-logo" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"
			><title>Apple</title><path
				d="M12.152 6.896c-.948 0-2.415-1.078-3.96-1.04-2.04.027-3.91 1.183-4.961 3.014-2.117 3.675-.546 9.103 1.519 12.09 1.013 1.454 2.208 3.09 3.792 3.039 1.52-.065 2.09-.987 3.935-.987 1.831 0 2.35.987 3.96.948 1.637-.026 2.676-1.48 3.676-2.948 1.156-1.688 1.636-3.325 1.662-3.415-.039-.013-3.182-1.221-3.22-4.857-.026-3.04 2.48-4.494 2.597-4.559-1.429-2.09-3.623-2.324-4.39-2.376-2-.156-3.675 1.09-4.61 1.09zM15.53 3.83c.843-1.012 1.4-2.427 1.245-3.83-1.207.052-2.662.805-3.532 1.818-.78.896-1.454 2.338-1.273 3.714 1.338.104 2.715-.688 3.559-1.701" /></svg>

		{#each HEADER_LEFT_ITEMS as item, i}
			{#if i === 0}
				<span class="header-text bold">{item}</span>
			{:else}
				<span class="header-text left">{item}</span>
			{/if}
		{/each}
	</div>
	<div class="group">
		<svg height="16px" width="16px" id="wifi" style="enable-background:new 0 0 512 512;" version="1.1" viewBox="0 0 512 512"  xml:space="preserve" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink"><g><path d="M256.1,96L256.1,96c-79.9,0-155.7,29.9-213.9,84.1L32,189.6l9.9,9.8l32.3,32l9.3,9.2l9.6-8.8   c44.5-40.9,102.3-63.5,162.8-63.5c60.5,0,118.4,22.6,162.8,63.5l9.6,8.8l9.3-9.2l32.3-32l9.9-9.8l-10.2-9.5   C411.6,125.9,335.7,96,256.1,96z"/><path d="M397.4,256.4c-38.8-35.1-88.9-54.4-141.1-54.4h-0.1h-0.3h-8.5l-0.1,0.2c-49.2,2-96,21.1-132.6,54.2l-10.5,9.5l10.1,10   l32.7,32.4l9.1,9l9.6-8.4c25.3-22.2,57.4-34.5,90.3-34.5c33.1,0,65.2,12.3,90.5,34.5l9.6,8.4l9.1-9l32.7-32.4l10.1-10L397.4,256.4z   "/><path d="M256.2,416l9.6-9.5l52.8-52.2l10.6-10.5l-11.6-9.5c-15.4-11.4-32.4-20-61.5-20c-29,0-44.9,9.4-61.5,20l-11.5,9.5l10.6,10.5   l52.8,52.2L256.2,416z"/></g></svg>
		<span class="header-text right">{date}</span>
		<span class="header-text right">{time}</span>
	</div>
</header>

<style>
	header {
		height: 22px;
		background-color: rgba(0, 0, 0, 0.4);
		display: flex;
		align-items: center;
		padding: 0 15px;
		justify-content: space-between;
	}
	.group {
		display: flex;
		align-items: center;
	}
	#apple-logo {
		fill: white;
		height: 14px;
		margin-right: 10px;
	}
	.header-text {
		color: white;
		font-size: smaller;
	}
	.left{
		margin: 0 10px;

	}
	.right {
		margin: 0 5px;
	}
	.bold {
		font-weight: bold;
		margin: 0 13px;
	}
	#wifi {
		fill: white;
		margin: 0 5px;
	}
</style>

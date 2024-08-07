<script>
	import { Listgroup } from 'flowbite-svelte';

	let links = [
		{ name: '账本', href: '/account-book', current: true },
		{ name: '待定', href: '/table-content' }
	];
</script>

<Listgroup active items={links} let:item class="w-96 mx-auto">
	{item.name}
</Listgroup>

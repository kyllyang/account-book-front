<script>
	import { page } from '$app/stores';
	import { Breadcrumb, BreadcrumbItem, Sidebar, SidebarGroup, SidebarItem, SidebarWrapper } from 'flowbite-svelte';
	import { ChartMixedDollarOutline, EditOutline, RectangleListOutline } from 'flowbite-svelte-icons';

	$: activeUrl = $page.url.pathname;
	let activeClass = 'flex items-center p-2 text-base font-normal text-primary-900 bg-primary-200 dark:bg-primary-700 rounded-lg dark:text-white hover:bg-primary-100 dark:hover:bg-gray-700';
	let nonActiveClass = 'flex items-center p-2 text-base font-normal text-green-900 rounded-lg dark:text-white hover:bg-green-100 dark:hover:bg-green-700';
</script>

<Breadcrumb solid>
	<BreadcrumbItem href="/" home>首页</BreadcrumbItem>
	<BreadcrumbItem href="/table-content">应用</BreadcrumbItem>
	<BreadcrumbItem href="/account-book">账本</BreadcrumbItem>
</Breadcrumb>

<br/>
<Sidebar {activeUrl} {activeClass} {nonActiveClass} asideClass="fixed w-64 h-screen transition-transform -translate-x-full sm:translate-x-0">
	<SidebarWrapper>
		<SidebarGroup>
			<SidebarItem label="录入" href="/account-book/input">
				<svelte:fragment slot="icon">
					<EditOutline class="w-6 h-6" />
				</svelte:fragment>
			</SidebarItem>
			<SidebarItem label="数据" href="/account-book/data">
				<svelte:fragment slot="icon">
					<RectangleListOutline class="w-6 h-6" />
				</svelte:fragment>
			</SidebarItem>
			<SidebarItem label="统计" href="/account-book/stat">
				<svelte:fragment slot="icon">
					<ChartMixedDollarOutline class="w-6 h-6" />
				</svelte:fragment>
			</SidebarItem>
		</SidebarGroup>
	</SidebarWrapper>
</Sidebar>
<div class="p-4 sm:ml-64">
	<slot></slot>
</div>
<br/>

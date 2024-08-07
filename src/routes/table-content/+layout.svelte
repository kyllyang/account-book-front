<script>
	import { Breadcrumb, BreadcrumbItem} from 'flowbite-svelte';
</script>

<Breadcrumb solid>
	<BreadcrumbItem href="/" home>首页</BreadcrumbItem>
	<BreadcrumbItem href="/table-content">应用</BreadcrumbItem>
</Breadcrumb>

<br/>
<slot></slot>
<br/>

<script>
	import { Breadcrumb, BreadcrumbItem} from 'flowbite-svelte';
</script>

<Breadcrumb solid>
	<BreadcrumbItem href="/" home>首页</BreadcrumbItem>
	<BreadcrumbItem href="/login">登录</BreadcrumbItem>
</Breadcrumb>

<br/>
<slot></slot>
<br/>

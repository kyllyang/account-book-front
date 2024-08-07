<script>
	import '../app.css';
	import { Navbar, NavBrand, NavLi, NavUl, NavHamburger, BreadcrumbItem, Breadcrumb } from 'flowbite-svelte';
	import { Footer, FooterCopyright, FooterLinkGroup, FooterBrand, FooterLink } from 'flowbite-svelte';
</script>

<Navbar class="w-full">
	<NavBrand href="/">
		<img src="/images/ks-evo-logo.png" class="me-3 h-6 sm:h-9" alt="KS-EVO Logo" />
		<span class="self-center whitespace-nowrap text-xl font-semibold dark:text-white">KS-EVO</span>
	</NavBrand>
	<NavHamburger />
	<NavUl>
		<NavLi href="/" active={true}>首页</NavLi>
		<NavLi href="/login">登录</NavLi>
	</NavUl>
</Navbar>

<slot></slot>

<Footer>
	<div class="sm:flex sm:items-center sm:justify-between">
		<div/>
		<FooterLinkGroup ulClass="flex flex-wrap items-center mb-6 text-sm text-gray-500 sm:mb-0 dark:text-gray-400">
			<FooterLink href="/about">关于</FooterLink>
			<FooterLink href="/privacy-policy">隐私政策</FooterLink>
			<FooterLink href="/licensing">版权</FooterLink>
			<FooterLink href="/contact">联系</FooterLink>
		</FooterLinkGroup>
	</div>
	<hr class="my-2 border-gray-200 sm:mx-auto dark:border-gray-700" />
	<FooterCopyright href="/" by="KS-EVO"/>
</Footer>

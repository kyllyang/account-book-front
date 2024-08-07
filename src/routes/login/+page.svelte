<script>
	import { Card, Button, Label, Input, Checkbox } from 'flowbite-svelte';
</script>

<Card class="mx-auto">
	<form class="flex flex-col space-y-6" action="/table-content">
		<Label class="space-y-2">
			<span>用户</span>
			<Input type="text" name="email" placeholder="name@company.com" required />
		</Label>
		<Label class="space-y-2">
			<span>密码</span>
			<Input type="password" name="password" placeholder="•••••" required />
		</Label>
		<div class="flex items-start">
			<Checkbox checked>Remember me</Checkbox>
		</div>
		<Button type="submit" class="w-full">登录</Button>
	</form>
</Card>

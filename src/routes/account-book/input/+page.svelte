<script>
	import { Label, Select, Datepicker, NumberInput, Input, Checkbox, Button} from 'flowbite-svelte';

	let selected = 'cmb';
	let channels = [
		{ value: 'cmb', name: '招商银行卡' },
		{ value: 'citicib', name: '中信银行卡' },
		{ value: 'icbc', name: '工商银行卡' },
		{ value: 'jd', name: '京东金融' },
		{ value: 'allipay', name: '支付宝借呗' }
	];

	let now = new Date(new Date().getTime() - (new Date().getTimezoneOffset() * 60000 )).toISOString().split("T")[0];
</script>

<form>
	<div class="grid gap-6 mb-6 md:grid-cols-1">
		<div>
			<Label for="channel" class="mb-2">渠道</Label>
			<Select id="channel" items={channels} bind:value={selected} required />
		</div>
		<div>
			<Label for="date" class="mb-2">日期</Label>
			<Datepicker id="date" datepickerButtons datepickerFormat="yyyy-mm-dd" value={now}/>
		</div>
		<div>
			<Label for="amount" class="mb-2">金额</Label>
			<NumberInput id="amount" required />
		</div>
		<div>
			<Label for="remark" class="mb-2">备注</Label>
			<Input type="text" id="remark"/>
		</div>
		<div>
			<Label for="tags" class="mb-2">标签</Label>
			<div class="flex gap-4">
				<Checkbox checked color="yellow">每日花销</Checkbox>
				<Checkbox color="yellow">交通</Checkbox>
				<Checkbox color="yellow">餐饮</Checkbox>
				<Checkbox color="yellow">公共</Checkbox>
			</div>
			<div class="flex gap-4">
				<Checkbox color="green">高德打车</Checkbox>
				<Checkbox color="green">出租车</Checkbox>
				<Checkbox color="green">公交卡</Checkbox>
			</div>
			<div class="flex gap-4">
				<Checkbox color="red">早餐</Checkbox>
				<Checkbox color="red">午餐</Checkbox>
				<Checkbox color="red">晚餐</Checkbox>
				<Checkbox color="red">饮料</Checkbox>
				<Checkbox color="red">彩票</Checkbox>
				<Checkbox color="red">啤酒</Checkbox>
				<Checkbox color="red">鸭货</Checkbox>
				<Checkbox color="red">游玩</Checkbox>
			</div>
			<div class="flex gap-4">
				<Checkbox color="teal">超市</Checkbox>
				<Checkbox color="teal">饭店</Checkbox>
				<Checkbox color="teal">水产</Checkbox>
				<Checkbox color="teal">麦德龙</Checkbox>
				<Checkbox color="teal">欧亚</Checkbox>
				<Checkbox color="teal">天乐</Checkbox>
				<Checkbox color="teal">梓宁</Checkbox>
				<Checkbox color="teal">博瑞生鲜</Checkbox>
				<Checkbox color="teal">果语堂</Checkbox>
				<Checkbox color="teal">果婆婆</Checkbox>
				<Checkbox color="teal">明宇食堂</Checkbox>
				<Checkbox color="teal">杭州小笼包</Checkbox>
				<Checkbox color="teal">豆腐脑</Checkbox>
				<Checkbox color="teal">李先生牛肉面</Checkbox>
				<Checkbox color="teal">川小调</Checkbox>
				<Checkbox color="teal">佳兰雅序</Checkbox>
				<Checkbox color="teal">柴大叔</Checkbox>
				<Checkbox color="teal">福奈特洗衣</Checkbox>
				<Checkbox color="teal">京东</Checkbox>
				<Checkbox color="teal">淘宝</Checkbox>
				<Checkbox color="teal">Steam</Checkbox>
				<Checkbox color="teal">WeMod</Checkbox>
			</div>
			<div class="flex gap-4">
				<Checkbox color="purple">电话费</Checkbox>
				<Checkbox color="purple">网费</Checkbox>
				<Checkbox color="purple">燃气费</Checkbox>
				<Checkbox color="purple">水费</Checkbox>
				<Checkbox color="purple">电费</Checkbox>
				<Checkbox color="purple">物业费</Checkbox>
				<Checkbox color="purple">车辆管理费</Checkbox>
				<Checkbox color="purple">会员费</Checkbox>
				<Checkbox color="purple">幼儿园</Checkbox>
				<Checkbox color="purple">课后班</Checkbox>
				<Checkbox color="purple">舞蹈班</Checkbox>
				<Checkbox color="purple">保险</Checkbox>
				<Checkbox color="purple">医药</Checkbox>
			</div>
			<div class="flex gap-4">
				<Checkbox color="orange">杨磊</Checkbox>
				<Checkbox color="orange">琛琛</Checkbox>
				<Checkbox color="orange">蓁蓁</Checkbox>
				<Checkbox color="orange">妈妈</Checkbox>
			</div>
		</div>
	</div>
	<Button type="submit">Submit</Button>
</form>

<script>
	import { Chart, Card, A, Button, Dropdown, DropdownItem } from 'flowbite-svelte';
	import { UsersGroupOutline, ArrowUpOutline, ChevronDownOutline, ChevronRightOutline } from 'flowbite-svelte-icons';

	const options = {
		colors: ['#1A56DB', '#FDBA8C'],
		series: [
			{
				name: 'Organic',
				color: '#1A56DB',
				data: [
					{ x: 'Mon', y: 231 },
					{ x: 'Tue', y: 122 },
					{ x: 'Wed', y: 63 },
					{ x: 'Thu', y: 421 },
					{ x: 'Fri', y: 122 },
					{ x: 'Sat', y: 323 },
					{ x: 'Sun', y: 111 }
				]
			},
			{
				name: 'Social media',
				color: '#FDBA8C',
				data: [
					{ x: 'Mon', y: 232 },
					{ x: 'Tue', y: 113 },
					{ x: 'Wed', y: 341 },
					{ x: 'Thu', y: 224 },
					{ x: 'Fri', y: 522 },
					{ x: 'Sat', y: 411 },
					{ x: 'Sun', y: 243 }
				]
			}
		],
		chart: {
			type: 'bar',
			height: '320px',
			fontFamily: 'Inter, sans-serif',
			toolbar: {
				show: false
			}
		},
		plotOptions: {
			bar: {
				horizontal: false,
				columnWidth: '70%',
				borderRadiusApplication: 'end',
				borderRadius: 8
			}
		},
		tooltip: {
			shared: true,
			intersect: false,
			style: {
				fontFamily: 'Inter, sans-serif'
			}
		},
		states: {
			hover: {
				filter: {
					type: 'darken',
					value: 1
				}
			}
		},
		stroke: {
			show: true,
			width: 0,
			colors: ['transparent']
		},
		grid: {
			show: false,
			strokeDashArray: 4,
			padding: {
				left: 2,
				right: 2,
				top: -14
			}
		},
		dataLabels: {
			enabled: false
		},
		legend: {
			show: false
		},
		xaxis: {
			floating: false,
			labels: {
				show: true,
				style: {
					fontFamily: 'Inter, sans-serif',
					cssClass: 'text-xs font-normal fill-gray-500 dark:fill-gray-400'
				}
			},
			axisBorder: {
				show: false
			},
			axisTicks: {
				show: false
			}
		},
		yaxis: {
			show: false
		},
		fill: {
			opacity: 1
		}
	};
</script>

<Card>
	<div class="flex justify-between pb-4 mb-4 border-b border-gray-200 dark:border-gray-700">
		<div class="flex items-center">
			<div class="w-12 h-12 rounded-lg bg-gray-100 dark:bg-gray-700 flex items-center justify-center me-3">
				<UsersGroupOutline class="w-6 h-6 text-gray-500 dark:text-gray-400" />
			</div>
			<div>
				<h5 class="leading-none text-2xl font-bold text-gray-900 dark:text-white pb-1">3.4k</h5>
				<p class="text-sm font-normal text-gray-500 dark:text-gray-400">Leads generated per week</p>
			</div>
		</div>
		<div>
      <span class="bg-green-100 text-green-800 text-xs font-medium inline-flex items-center px-2.5 py-1 rounded-md dark:bg-green-900 dark:text-green-300">
        <ArrowUpOutline class="w-2.5 h-2.5 me-1.5" />
        42.5%
      </span>
		</div>
	</div>
	<div class="grid grid-cols-2">
		<dl class="flex items-center">
			<dt class="text-gray-500 dark:text-gray-400 text-sm font-normal me-1">Money spent:</dt>
			<dd class="text-gray-900 text-sm dark:text-white font-semibold">$3,232</dd>
		</dl>
		<dl class="flex items-center justify-end">
			<dt class="text-gray-500 dark:text-gray-400 text-sm font-normal me-1">Conversion rate:</dt>
			<dd class="text-gray-900 text-sm dark:text-white font-semibold">1.2%</dd>
		</dl>
	</div>
	<Chart {options} />
	<div class="grid grid-cols-1 items-center border-gray-200 border-t dark:border-gray-700 justify-between">
		<div class="flex justify-between items-center pt-5">
			<Button class="text-sm font-medium text-gray-500 dark:text-gray-400 hover:text-gray-900 text-center inline-flex items-center dark:hover:text-white bg-transparent hover:bg-transparent dark:bg-transparent dark:hover:bg-transparent focus:ring-transparent dark:focus:ring-transparent py-0">Last 7 days<ChevronDownOutline class="w-2.5 m-2.5 ms-1.5" /></Button>
			<Dropdown class="w-40" offset="-6">
				<DropdownItem>Yesterday</DropdownItem>
				<DropdownItem>Today</DropdownItem>
				<DropdownItem>Last 7 days</DropdownItem>
				<DropdownItem>Last 30 days</DropdownItem>
				<DropdownItem>Last 90 days</DropdownItem>
			</Dropdown>
			<A href="/" class="uppercase text-sm font-semibold hover:text-primary-700 dark:hover:text-primary-500 rounded-lg hover:bg-gray-100 dark:hover:bg-gray-700 dark:focus:ring-gray-700 dark:border-gray-700 px-3 py-2 hover:no-underline">
				Leads Report
				<ChevronRightOutline class="w-2.5 h-2.5 ms-1.5" />
			</A>
		</div>
	</div>
</Card>

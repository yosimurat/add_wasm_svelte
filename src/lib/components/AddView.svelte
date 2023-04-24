<script lang="ts">
	import wasm from '@yosimurat/add_wasm';

	export let a: number;
	export let b: number;

	let value: number = 0;

	(wasm as any)({}).then(({ instance }: any) => {
		value = instance.exports.add(a, b);
	});
</script>

<div>
	{value}
</div>

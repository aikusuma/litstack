<template>
	<lit-col :width="width">
		<component :is="heading" v-html="title" v-if="title != ''" />
		<p
			:key="key"
			v-for="(info, key) in text"
			v-html="info"
			class="text-secondary"
		/>
	</lit-col>
</template>

<script>
export default {
	name: 'Info',
	props: {
		width: {
			type: Number,
			required: true,
		},
		title: {
			type: String,
			required: true,
		},
		text: {
			type: Array,
			required: true,
		},
		heading: {
			type: String,
			required: true,
		},
		model: {},
		config: {},
	},
};
</script>

<template>
	<div :class="classNames">
		<slot></slot>
	</div>
</template>

<script>
import gridMethods from './methods.js';

export default {
	name: 'column',
	props: {
		small: {
			type: String,
			default: null
		},
		medium: {
			type: String,
			default: null
		},
		large: {
			type: String,
			default: null
		},
		xlarge: {
			type: String,
			default: null
		},
		xxlarge: {
			type: String,
			default: null
		},
		backgroundColor: {
			type: String,
			default: null
		},
		textColor: {
			type: String,
			default: null
		}
	},
	data() {
		return {
			classNames: ['column']
		};
	},
	methods: gridMethods.methods,
	created() {
		if (this.$props.small == undefined) {
			this.classNames.push('small-full');
		}
		this.classNames.push(this.setClasses(this.$props, this));
		this.classNames.push(this.setWidth(this.$props, this));
	}
};
</script>

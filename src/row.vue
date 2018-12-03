<template>
  <div :class="classNames">
    <slot></slot>
  </div>
</template>

<script>
import gridMethods from './methods.js';

export default {
	name: 'row',
	props: {
		center: {
			type: String,
			default: null
		},
		left: {
			type: String,
			default: null
		},
		right: {
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
			classNames: ['row']
		};
	},
	methods: gridMethods.methods,
	created() {
		this.classNames.push(this.setClasses(this.$props, this));
		this.classNames.push(this.setWidth(this.$props, this));
	}
};
</script>

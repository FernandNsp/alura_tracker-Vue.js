<template>
	<button class="button" @click="evento" :disabled="cronometroRodando">
		<span class="icon">
			<i :class="icone"></i>
		</span>
		<span>{{ texto }}</span>
	</button>
</template>

<script lang="ts">
	import { defineComponent } from 'vue'

	export default defineComponent({
		name: "Botao",
		emits: ['evento'],
		props: {
			disabled: Boolean,
			icone: {
				type: String,
				required: true
			},
			texto: {
				type: String,
				required: true
			},
		},
		methods: {
			evento() : void {
				this.$emit('evento')
			}
		}
	})
</script>

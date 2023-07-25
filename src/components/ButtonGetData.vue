<template>
	<div class="ButtonGetData">
		<button class="ButtonGetData__Button" @click="getData">Получить данные</button>
	</div>
</template>

<script>


export default {
	name: 'ButtonGetData',
  methods: {
    async getData() {
      this.$emit('get-data');
    }
  }
};
</script>

<style lang="scss">
	.ButtonGetData {
		&__Button {
			padding: 10px 20px;
			font-size: 16px;
			background-color: #007bff;
			color: #fff;
			border: none;
			cursor: pointer;
			border-radius: 4px;
			transition: background-color 0.3s ease;

			&:hover {
				background-color: #0056b3;
			}
		}
	}
</style>
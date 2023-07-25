<template>
	<div class="ItemFromList">
		<ul class="ItemFromList__List">
			<li class="ItemFromList__List-Item">{{ item.userId }}</li>
			<li class="ItemFromList__List-Item">{{ item.id }}</li>
			<li class="ItemFromList__List-Item">{{ item.title }}</li>
			<li class="ItemFromList__List-Item">{{ item.completed ? 'Завершено' : 'Не завершено' }}</li>
		</ul>
	</div>
</template>

<script>


export default {
	name: 'ItemFromList',
	props: {
    item: {
      type: Object,
      required: true
    }
  }
}
</script>

<style lang="scss">
	.ItemFromList{
		&__List {
			list-style: none;
			padding: 10px 0px;
			display: flex;
			justify-content: space-between;
			border-bottom: 1px solid #000000;
		}

		&__List-Item {
			display: flex;
			align-items: center;
			justify-content: center;
			width: 300px;
		}
	}
</style>
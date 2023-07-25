<template>
	<div class="ListOfItems">
		<ul class="ListOfItems__List">
			<itemFromList v-for="item in dataList" :key="item.id" :item="item" />
		</ul>
	</div>
</template>	

<script>

import itemFromList from '@/components/ItemFromList'

export default {
	name: 'ListOfItems',
	components: {
		itemFromList,
	},
	props: {
    dataList: {
      type: Array,
      default: () => []
    }
  },
}
</script>

<style lang="scss">
	.ListOfItems{
		&__List {
			list-style: none;
			padding: 0;
			display: flex;
			flex-direction: column;
			row-gap: 20px;
		}
	}
</style>
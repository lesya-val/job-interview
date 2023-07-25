<template>
	<div class="ListPage">
		<buttonGetData @get-data="getData"/>
		<listOfItems :dataList="dataList"/>
	</div>
</template>

<script>

import buttonGetData from '@/components/ButtonGetData'
import listOfItems from '@/components/ListOfItems'

export default {
	name: 'ListPage',
	components: {
		buttonGetData,
		listOfItems
	},
	data() {
    return {
      dataList: []
    };
  },
  methods: {
    async getData() {
      try {
        const response = await fetch('https://jsonplaceholder.typicode.com/todos');
        const data = await response.json();
        this.dataList = data;
      } catch (error) {
        console.error('Ошибка при получении данных:', error);
      }
    }
	}
}
</script>

<style lang="scss">
	.ListPage {
		padding: 20px;
	}
</style>
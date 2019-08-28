<template>
	<div>
		<app-stock
			v-for="stock in stocks"
			:stock="stock"
		></app-stock>
	</div>
</template>

<style scoped>
.danger {
	border: 1px solid red;
}
</style>

<script>
import { mapGetters } from "vuex";
import Stock from "./Stock.vue";
export default {
	components: {
		appStock: Stock
	},
	computed: {
		...mapGetters({
			stocks: "stockPortfolio"
		})
	}
};
</script>

<template>
	<div class="w-card-container">
		<v-card
			class="w-card-content"
			v-for="item in service"
			:key="item.typeService"
		>
			<p>{{ item.name }}</p>
			<p>{{  item.typeService}}</p>
			<p>{{ item.date }}</p>
			<p>{{  item.value}}</p>
		</v-card>
	</div>
</template>

<script>
	export default {
		name: 'HistoryComponent',
		data() {
			return {
				service: [
					{ name: 'Inf. Pessoais', typeService: 'PerfilComponent' , date: '12/12/2020',value: 'R$4,99'},
					{ name: 'Histórico', typeService: 'HistoryComponent' , date: '12/12/2020',value: 'R$4,99'},
					{ name: 'Carteira', typeService: 'WalletComponent', date: '12/12/2020',value: 'R$4,99' }
				]
			}
		}
	}
</script>


<style lang="scss">
.w-card-container {
	display: flex;
	flex-direction: column;
	justify-content: center;
	width: 100%;

	.w-card-content {
		margin: 10px;
		max-width: 80%;
	}
}

</style>
<template>
	<div class="w-card-container">
		<v-card class="w-card-content" v-for="item in service" :key="item.typeService" >
			<div style="display: flex; margin-top: 15px ; margin-left:15px; margin-bottom: 15px;  width: 10px; text-align:left;  justify-content: space-between; align-items: flex-start ">
				<img src="../assets/asseio.png" width="45" height="45"/>
				<div style="margin-left: 15px; text-align: left;">
					<p style="font-size: 15px;">{{ item.name }}</p>
					<p style="font-size: 20px;">{{  item.typeService}}</p>
					<p style="font-size: 11px;">{{ item.date }}</p>
					<p style="font-size: 20px;">{{  item.value}}</p>
				</div>	
			</div>	
		</v-card>
	</div>
</template>

<script>
	export default {
		name: 'HistoryComponent',
		data() {
			return {
				service: [
					{ name: 'Serviço', typeService: 'Banho e Tosa' , date: '12/12/2020',value: 'R$80,00'},
					{ name: 'Serviço', typeService: 'Banho e Tosa' , date: '05/11/2020',value: 'R$80,00'},
					{ name: 'Serviço', typeService: 'Aparar Garras', date: '01/01/2020',value: 'R$35,00'}
				]
			}
		}
	}
</script>


<style lang="scss">
.w-card-container {
	
	background-color: #E0F3F0;
	display: flex;
	
	flex-direction: column;
	//justify-content:baseline ;
	//width: 100%;
	padding: 10%;

	.w-card-content {
		margin: 10px;
		max-width: auto;
		
	}
}



</style>
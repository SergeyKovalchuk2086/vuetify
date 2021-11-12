<template>
	<v-row>
		<v-col class="cafe__component">
			<h1 class="py-4 text-center">Lists of cafes</h1>
			<v-row class="cafe__list mx-2">
				<v-col
					v-for="cafe in cafes"
					:key="cafe.id"
					md="4"
					class="d-flex justify-center"
				>
					<v-card class="cafe__card text-center" width="300">
						<v-img height="150" :src="cafe.img"></v-img>
						<v-card-title class="d-block">
							<router-link to="/cafe/view">{{
								cafe.name
							}}</router-link></v-card-title
						>
						<v-card-text>
							<p>{{ cafe.description }}</p>
							<p>Rating : {{ cafe.rating }} of 5</p>
						</v-card-text>
					</v-card>
				</v-col>
			</v-row>
		</v-col>
	</v-row>
</template>

<script>
export default {
	name: "Cafe",
	data() {
		return {
			cafes: [
				{
					id: 0,
					name: "A-FOOD",
					description: "Here we can cook nice korean food",
					img: "https://static-sl.insales.ru/files/1/7017/14924649/original/menu-restaurant-vintage-table.jpg",
					tags: ["asian"],
					rating: 5,
				},
				{
					id: 1,
					name: "K-FOOD",
					description: "Here we can cook nice korean food",
					img: "https://media.istockphoto.com/photos/cafe-le-bon-georges-paris-france-picture-id1044154134?k=20&m=1044154134&s=612x612&w=0&h=IvdIPX9Lusn4bGLn1UyYjXVh6-YQYPhr1Zmst0Ypz28=",
					tags: ["korean"],
					rating: 3,
				},
				{
					id: 2,
					name: "R-FOOD",
					description: "Here we can cook nice korean food",
					img: "https://images.unsplash.com/photo-1495474472287-4d71bcdd2085?ixid=MnwxMjA3fDB8MHxzZWFyY2h8OHx8Y2FmZXxlbnwwfHwwfHw%3D&ixlib=rb-1.2.1&w=1000&q=80",
					tags: ["russian"],
					rating: 4,
				},
				{
					id: 3,
					name: "R-FOOD",
					description: "Here we can cook nice korean food",
					img: "http://retail-loyalty.org/upload/iblock/98a/telegraf_main_1_734x410_.jpg",
					tags: ["russian"],
					rating: 4,
				},
				{
					id: 4,
					name: "R-FOOD",
					description: "Here we can cook nice korean food",
					img: "https://a-a-ah-ru.s3.amazonaws.com/uploads/items/137865/282134/medium_VdcxmvmWRMY.jpg",
					tags: ["russian"],
					rating: 2,
				},
				{
					id: 5,
					name: "R-FOOD",
					description: "Here we can cook nice korean food",
					img: "https://cdnn21.img.ria.ru/images/07e4/03/04/1568146427_0:274:3068:2000_600x0_80_0_0_7571167de75b2b4f03d2f4adc918366b.jpg",
					tags: ["russian"],
					rating: 1,
				},
			],
		};
	},
};
</script>

<style scoped></style>

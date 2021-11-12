<template>
	<div>
		<v-row>
			<v-col>
				<v-breadcrumbs :items="breadCrumbs_items"></v-breadcrumbs>
			</v-col>
		</v-row>
		<v-row>
			<v-col md="5"
				><v-card
					><v-img
						height="350"
						src="https://static-sl.insales.ru/files/1/7017/14924649/original/menu-restaurant-vintage-table.jpg"
						class="d-flex align-end"
					>
						<v-card-title
							><h2 class="text-h2 white--text">K-FOOD</h2></v-card-title
						></v-img
					></v-card
				></v-col
			>
			<v-col md="7"
				><v-card class="h-100">
					<v-card-text>
						<h4 class="text-h5 mb-4">
							Come here if you wanna to taste cool ramen
						</h4>
						<v-divider></v-divider>
						<p class="mt-4 text-body-1 mr-5">
							Lorem ipsum dolor sit amet, consectetur adipisicing elit.
							Placeat explicabo possimus temporibus quasi dolores animi,
							soluta odio eum iste officia natus fuga quia corporis
							eveniet? Ipsum eum aut mollitia perferendis.
						</p>
					</v-card-text>
				</v-card></v-col
			></v-row
		>
		<v-row class="cafe__menu">
			<v-col md="6"
				><v-card>
					<v-img
						class="flex align-end"
						height="450"
						src="https://st.depositphotos.com/1007309/1634/i/950/depositphotos_16349865-stock-photo-romantic-entrance-to-old-restaurant.jpg"
						><v-card-title>
							<h2 class="text-h2 white--text">MENU</h2></v-card-title
						></v-img
					>
				</v-card></v-col
			>
			<v-col md="6"
				><v-card>
					<v-card-text>
						<v-list-item-group>
							<v-list-item v-for="item in menu__items" :key="item.id">
								<v-list-item-avatar>
									<v-img :src="item.img"></v-img>
								</v-list-item-avatar>
								<v-list-item-content>
									<v-list-item-title class="text-subtitle-1">{{
										item.title
									}}</v-list-item-title>
									<v-list-item-subtitle class="text-body-1">
										{{ item.price }}
									</v-list-item-subtitle>
								</v-list-item-content>
								<v-list-item-action>
									<v-btn icon>
										<v-icon>&#10004;</v-icon>
									</v-btn>
								</v-list-item-action>
							</v-list-item>
						</v-list-item-group>
					</v-card-text>
				</v-card></v-col
			>
		</v-row>
		<CafeComment />
	</div>
</template>

<script>
import CafeComment from "@/components/CafeComment";

export default {
	name: "CafeView",
	components: {
		CafeComment,
	},
	data() {
		return {
			menu__items: [
				{
					id: 0,
					title: "Soup",
					img: "https://hips.hearstapps.com/hmg-prod.s3.amazonaws.com/images/homemade-pumpkin-soup-royalty-free-image-1571855802.jpg?crop=0.667xw:1.00xh;0.333xw,0&resize=480:*",
					price: 55.75,
				},
				{
					id: 1,
					title: "Burger",
					img: "https://seafood-shop.storage.yandexcloud.net/iblock/e2e/e2e670a253d1991e6b19dee542b168a7.jpg",
					price: 35.55,
				},
				{
					id: 2,
					title: "Pasta",
					img: "https://img.delo-vcusa.ru/2019/11/Pasta-po-toskanski.jpg",
					price: 60.2,
				},
			],

			breadCrumbs_items: [
				{
					text: "Home",
					disabled: false,
					href: "/",
				},
				{
					text: "K-FOOD",
					disabled: true,
					href: "/cafe/view",
				},
			],
		};
	},
};
</script>

<style>
.h-100 {
	height: 100%;
}
</style>

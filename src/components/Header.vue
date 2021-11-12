<template>
	<div>
		<v-app-bar color="teal lighten-2" app>
			<v-row class="font-weight-bold white--text d-flex">
				<v-app-bar-nav-icon
					@click.stop="drawer = !drawer"
				></v-app-bar-nav-icon>
				<v-app-bar-title class="d-flex align-center">Food</v-app-bar-title>
			</v-row>
		</v-app-bar>
		<v-navigation-drawer
			v-model="drawer"
			absolute
			left
			temporary
			height="400"
		>
			<v-list nav dense>
				<v-list-item-group v-model="group" active-class="text--acent-4">
					<v-list-item class="text-center">
						<v-list-item-title>
							<router-link to="/">List of Cafes</router-link>
						</v-list-item-title>
					</v-list-item>
					<v-list-item class="text-center">
						<v-list-item-title>About</v-list-item-title>
					</v-list-item>
					<v-list-item class="text-center">
						<v-list-item-title>Contact</v-list-item-title>
					</v-list-item>
				</v-list-item-group>
			</v-list>
		</v-navigation-drawer>
	</div>
</template>

<script>
export default {
	name: "Header",
	data() {
		return {
			drawer: false,
			group: null,
		};
	},
};
</script>

<style></style>

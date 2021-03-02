<template>
	<div>
		<v-hover v-slot="{ hover }">
			<v-card
				:elevation="hover ? 10 : 2" 
				class="card"
				color="grey lighten-5"
			>
			<v-btn 
				absolute 
				style="z-index:2001;" 
				icon 
				class="ma-1"
			>
				<v-icon color="error">mdi-heart-outline</v-icon>
			</v-btn>
				<v-img src="../assets/photo1.jpg" height="230">
					<div class="discount"><center>New</center></div>
				<v-expand-transition>
                <div
                  v-if="hover"
                  class="d-flex transition-fast-in-fast-out orange display-1 darken-1 v-card--reveal white--text"
                  style="height: 100%;"
                >
                  $349<sup><small>.99</small></sup>
                </div>
              </v-expand-transition>
        </v-img>
				<div style="position:relative;">
				<v-card-title class=" font-weight-light orange--text">Lorem ipsum dolor</v-card-title>
				<v-card-text>
					<v-btn
						absolute
						fab 
						color="orange"
						class="white--text"
						right
						top
						dark
						elevation="0"
					>	
						<v-icon>mdi-cart-plus</v-icon>			
					</v-btn>
					<del>490</del><span style="font-size:20px; color:#B71C1C; margin-left:10px;">$349</span>
				</v-card-text>
				</div>
			</v-card>
		</v-hover>
	</div>
</template>


<script>
	export default{
		data(){
			return{

			}
		}
	};
</script>

<style>
	*{
		font-family: Lato;
	}

	@media all and (min-width: 960px){	
		.card{
			width: 24%;
			height: 330px;
			margin: .5%;
			float:left;
		}
		.move{
			margin-left:15%;
		}

		.discount{
		font-weight: bold;
		color: white;
		display:block;
		background-image: -webkit-linear-gradient(top, #53d343, #32812a);
		transform: rotate(45deg);
		margin-right: -140px;
		margin-left: -30px; 
		padding: .5px 0 .5px 37%;
	}
	}	

	@media all and (max-width:650px){
		.card{
			width: 49%;
			height: 330px;
			margin: .5%;
			float:left;
		}

		.discount{
		font-weight: bold;
		color: white;
		display:block;
		background-image: -webkit-linear-gradient(top, #53d343, #32812a);
		transform: rotate(45deg);
		margin-right: -140px;
		margin-left: -30px; 
		padding: .5px 0 .5px 30%;
	}
	}

	@media all and (min-width: 650px) and (max-width: 960px){
		.card{
			width: 32%;
			height: 330px;
			margin: .6%;
			float:left;
		}

		.discount{
		font-weight: bold;
		color: white;
		display:block;
		background-image: -webkit-linear-gradient(top, #53d343, #32812a);
		transform: rotate(45deg);
		margin-right: -140px;
		margin-left: -30px; 
		padding: .5px 0 .5px 35%;
	}
	}

	
</style>
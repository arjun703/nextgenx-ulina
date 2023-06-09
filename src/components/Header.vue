<template>
	
	<div id="header" class="sticky-top pb-2 pt-2" style="background-color: var(--bgColor)">


	<nav class="navbar navbar-expand-lg navbar-light" >
			
			<a class="navbar-brand" href="#">
				<img src="/src/assets/images/logo2.png">
			</a>


			<ul class="navbar-nav align-items-center d-none d-lg-flex  leftMenuOptions">
				<li class="nav-item dropdown active">
					<a class="nav-link dropdown-toggle" href="#" id="navbarDropdownMenuLink" role="button" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
						Home
					</a>
					<div class="dropdown-menu" aria-labelledby="navbarDropdownMenuLink">
						<a class="dropdown-item" href="#">Action</a>
						<a class="dropdown-item" href="#">Another action</a>
						<a class="dropdown-item" href="#">Something else here</a>
					</div>
				</li>

				<li class="nav-item dropdown">
					<a class="nav-link dropdown-toggle" href="#" id="navbarDropdownMenuLink" role="button" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
						Categories
					</a>
					<div class="dropdown-menu" aria-labelledby="navbarDropdownMenuLink">
						<a class="dropdown-item" href="#">Action</a>
						<a class="dropdown-item" href="#">Another action</a>
						<a class="dropdown-item" href="#">Something else here</a>
					</div>
				</li>

				<li class="nav-item">
					<a class="nav-link" href="#">Shop</a>
				</li>
				
				<li class="nav-item dropdown">
					<a class="nav-link dropdown-toggle" href="#" id="navbarDropdownMenuLink" role="button" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
						Pages
					</a>
					<div class="dropdown-menu" aria-labelledby="navbarDropdownMenuLink">
						<a class="dropdown-item" href="#">Action</a>
						<a class="dropdown-item" href="#">Another action</a>
						<a class="dropdown-item" href="#">Something else here</a>
					</div>
				</li>

				<li class="nav-item">
					<a class="nav-link" href="#">Blogs</a>
				</li>

				<li class="nav-item">
					<a class="nav-link" href="#">Contact</a>
				</li>				
			
			</ul>


		
			<!-- end of left aligned section !-->
			<!-- Right-aligned section -->
			<ul class="navbar-nav d-flex ml-auto  align-items-center ">


				<ul class="d-flex" style="list-style: none;">

					<li class="nav-item d-flex  social-icons align-items-center">
						<a class="nav-link" href="#"><i class="fa fa-search"></i></a>
						<a class="nav-link" href="#"><i class="fa fa-user"></i></a>
						<a class="nav-link position-relative" href="#">
							<span class="position-relative">
								<i class="fa fa-shopping-cart"></i>
								<span class="badge badge-pill badge-danger position-absolute top-0" style="width: 15px; height: 15px; font-size: 10px">3</span>
							</span>
						</a>
					</li>

				<li class="nav-item d-none ml-2 d-lg-block">
					<a class="nav-link" href="#"><i>|</i></a>
				</li>

					<!-- Social media icons -->
					<li class="nav-item social-icons d-none ml-4 ml-lg-0 d-md-flex align-items-center">
						<a class="nav-link" href="#"><i class="fab fa-facebook-f"></i></a>
						<a class="nav-link" href="#"><i class="fab fa-twitter"></i></a>
						<a class="nav-link" href="#"><i class="fab fa-instagram"></i></a>
						<a class="nav-link" href="#"><i class="fab fa-linkedin-in"></i></a>
					</li>


				</ul>
			

				<li class="nav-item d-none d-lg-block" >
					<a class="nav-link" href="#"><i>|</i></a>
				</li>


				<li class=" nav-item dropdown d-none d-lg-flex">
					<a class=" faded nav-link dropdown-toggle" href="#" id="navbarDropdownMenuLink" role="button" style="font-size: 12px" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
						EN
					</a>
					<div class="dropdown-menu" aria-labelledby="navbarDropdownMenuLink">
						<a class="dropdown-item" href="#">Action</a>
						<a class="dropdown-item" href="#">Another action</a>
						<a class="dropdown-item" href="#">Something else here</a>
					</div>
				</li>

				<li class="nav-item dropdown d-none d-lg-flex">
					<a class=" faded nav-link dropdown-toggle" href="#" id="navbarDropdownMenuLink" role="button" style="font-size: 12px" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
						USD
					</a>
					<div class="dropdown-menu" aria-labelledby="navbarDropdownMenuLink">
						<a class="dropdown-item" href="#">Action</a>
						<a class="dropdown-item" href="#">Another action</a>
						<a class="dropdown-item" href="#">Something else here</a>
					</div>
				</li>

				<li class="nav-item d-none d-lg-flex">
					<a class="nav-link" href="#"><i>|</i></a>
				</li>

				<li class="nav-item d-none d-lg-block">
					<a class="nav-link" style="font-size: 25px;" href="#"><i class="fa fa-phone"></i></a>
				</li>

				<li class="nav-item d-none d-lg-block" style="font-size: 12px; font-weight: bold;margin-left: -10px">
					<a class="nav-link" href="#"><span>Helpline</span><br><span>+ 123 - 456 - 7890</span></a>
				</li>


			</ul>

			
		</nav>

	</div>

</template>


<style>
	
	@media (max-width: 991px) {
		.navbar-nav .social-icons .nav-link {
		padding: 0.5rem;
		}
	}

	.leftMenuOptions li{
		margin-left: 10px;
		font-weight: bold;
		
		font-size: 13px;
	}



:root{
	--bgColor: rgb(236,245,244);
	--topCarouselColor: rgb(88,145,149);
	}

	body{
		overflow-x: hidden!important;
	}

	.signatureColor{
	color: var(--topCarouselColor);
	}

	.faded{
	opacity: 0.7
	}

	.controlIcon{
	height: 40px;
	width: 40px;
	font-size: 18px;
	border-radius: 50%;
	margin-left: 5px;
	border: 1px solid rgba(0, 0, 0, 0.5);
	background: white;
	}


	.horizontallyCentered{
	left: 50%;
	transform: translateX(-50%);
	}

	.verticallyCentered{
	top: 50%;
	transform: translateY(-50%);
	}

	.fullyCentered{
	left: 50%;
	top: 50%;
	transform: translate(-50%, -50%);
	}

	.horizontalCenterAlternate{
	margin-left: 50%;
	transform: translateX(-50%);
	}












</style>
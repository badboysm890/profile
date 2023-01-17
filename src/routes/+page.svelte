<script lang="ts">
	import {
		Collapse,
		Navbar,
		NavbarToggler,
		NavbarBrand,
		Nav,
		NavItem,
		NavLink,
		Progress
	} from 'sveltestrap';
	import Icon from '../assets/logo.png';
	let isOpen = false;
	const toggle = () => (isOpen = !isOpen);
</script>

<svelte:head>
	<link
		rel="stylesheet"
		href="https://cdn.jsdelivr.net/npm/bootstrap@5.2.1/dist/css/bootstrap.min.css"
	/>
	<link
		rel="stylesheet"
		href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.9.1/font/bootstrap-icons.css"
	/>
</svelte:head>

<Navbar>
	<NavbarBrand href="/" class="me-auto">
		<img src={Icon} alt="logo" width="150" class="d-inline-block align-text-top" />
	</NavbarBrand>
	<NavbarToggler on:click={toggle} class="me-2" />
</Navbar>

<body class="bg-dark">
	<!-- tabs with stat, inv, data, map and radio -->
	<div class="my-5">
		<nav>
			<div class="nav nav-tabs" id="nav-tab" role="tablist">
				<a
					class="nav-item nav-link active"
					id="nav-stat-tab"
					data-toggle="tab"
					href="#nav-stat"
					role="tab"
					aria-controls="nav-stat"
					aria-selected="true">Player Stat</a
				>
			</div>
		</nav>
		<div class="tab-content mx-5 my-5" id="nav-tabContent">
			<div
				class="tab-pane fade show active"
				id="nav-stat"
				role="tabpanel"
				aria-labelledby="nav-stat-tab"
			>
				<div class="row">
					<div class="col-md-12  text-center my-3">Devops (AWS,GCP,CICD,Cloud Architect)</div>
				</div>
				<div class="row">
					<div class="col-md-4  col-sm-12 text-end my-auto">Golang (Primary Weapon)</div>
					<div class="col-md-4  text-center">
						<img
							class="pip-boy-img"
							src="https://gifimage.net/wp-content/uploads/2018/04/pip-boy-gif-11.gif"
							alt="pip-boy"
						/>
					</div>
					<div class="col-md-4 col-sm-12  text-start my-auto">Mongo,MySQL,Redis (DB)</div>
				</div>
				<div class="row">
					<div class="col-md-4  text-end my-3 mx-auto">
						Javascript (<small>Peer Pressure</small>)
					</div>
					<div class="col-md-4  text-center my-3 mx-auto" />
					<div class="col-md-4  text-start my-3 mx-auto">Python (My Swiss knife)</div>
				</div>
				<div class="row">
					<div class="col-md-12 text-center my-3 mx-auto">Frontend (Any)</div>
				</div>

				<!-- border -->
				<div class="row align-items-end my-5 border border-5 border-success">
					<div class="col-md-4">
						<div class="col-md-12 text-center my-3 mx-auto">Player Name: Praveen</div>
					</div>
                    <div class="col-md-4">
                        <!-- calculated automatically in years from 2019 -->
                        <div class="col-md-12 text-center my-3 mx-auto">Player Exp: <span class="exp">3.5</span></div>
                    </div>
                    <div class="col-md-4">
                        <div class="col-md-12 text-center my-3 mx-auto">Player Health: 
                            <!-- progressbar -->
                            <span class="progress">
                                <span
                                    class="progress-bar progress-bar-striped progress-bar-animated"
                                    role="progressbar"
                                    style="width: 75%"
                                ></span>
                            </span>
                        </div>
                    </div>
				</div>
			</div>
			<div class="tab-pane fade" id="nav-inv" role="tabpanel" aria-labelledby="nav-inv-tab">
				Inv Content
			</div>
			<div class="tab-pane fade" id="nav-data" role="tabpanel" aria-labelledby="nav-data-tab">
				Data Content
			</div>
			<div class="tab-pane fade" id="nav-map" role="tabpanel" aria-labelledby="nav-map-tab">
				Map Content
			</div>
			<div class="tab-pane fade" id="nav-radio" role="tabpanel" aria-labelledby="nav-radio-tab">
				Radio Content
			</div>
		</div>
	</div>
</body>

<!-- body -->
<style>
	/* nav nav-tabs is equally spread with auto text size */
	/* use Microgramma for every text */

	* {
		/* monospace */
		font-family: 'Microgramma', monospace;
		color: #00ff00 !important;
		font-size: 1.8rem;
		font-weight: 900;
	}

	.nav-tabs .nav-item.show .nav-link,
	.nav-tabs .nav-link.active {
		border: 3px solid #00ff00;
		border-bottom: none;
		margin-bottom: -3px;
		border-top: none;
	}

	.nav-tabs {
		border-bottom: 3px solid #00ff00;
	}

	.nav-tabs .nav-item.show .nav-link,
	.nav-tabs .nav-link.active {
		background-color: black;
		width: 25%;
		text-align: center;
	}

	.nav-tabs {
		display: flex;
		flex-direction: row;
		justify-content: space-around;
		font-size: 1.5rem;
	}

	.pip-boy-img {
		/* css filter to match the bg-dark */
		filter: brightness(2);
	}

	.bg-dark {
		--bs-bg-opacity: 1;
		/* background-color: rgba(var(--bs-dark-rgb),var(--bs-bg-opacity))!important; */
		background-color: black !important;
	}

	/* hide pip-boy-img in mobile */
	@media (max-width: 768px) {
		.pip-boy-img {
			display: none;
		}
	}

	.progress-bar {
		background-color: #00ff00 !important;
        
	}
</style>

<template>
	<nav id="my-navbar">
		<div class="my-logo-row">
			<div class="my-navbar-logo">
				<a href="/" class="my-navbar-item"><img class="my-navbar-logo" src="/images/alibre-logo.png"></a>
			</div>
			<div class="my-navbar-mobile"
				 v-show="showMenu == false">
				<i class="fa fa-bars" aria-hidden="true"
				   v-on:click="showMenu = true"></i>
			</div>
		</div>
		<div class="my-navbar-items"
			 v-bind:class="{'showMenu': showMenu}">
			<a href="#" class="my-navbar-item"
						v-on:mouseover="showFunctions = true"
						v-on:mouseleave="showFunctions = false">Funkcje <i class="fa fa-caret-down" aria-hidden="true"></i>
				<transition name="rolldown">
				<div class="my-nabar-submenu"
					 v-show="showFunctions">
					<a href="/porownanie-wersji" class="my-navbar-item my-submenu-item">Porównanie wersji</a>
					<a href="/modelowanie-3d" class="my-navbar-item my-submenu-item">Modelowanie 3D</a>
					<a href="#" class="my-navbar-item my-submenu-item">Dokumentacja 2D</a>
					<a href="#" class="my-navbar-item my-submenu-item">Moduł blach</a>
					<a href="#" class="my-navbar-item my-submenu-item">Fotorealistyczny rendering</a>
					<a href="#" class="my-navbar-item my-submenu-item">Chmura punktów</a>
					<a href="#" class="my-navbar-item my-submenu-item">Wymiana danych CAD</a>
				</div>
				</transition>
			</a>
			<a href="#" class="my-navbar-item"
						v-on:mouseover="showSupport = true"
						v-on:mouseleave="showSupport = false">Wsparcie <i class="fa fa-caret-down" aria-hidden="true"></i>
				<transition name="rolldown">
				<div class="my-nabar-submenu"
					 v-show="showSupport">
					<a href="/wymagania-sprzetowe" class="my-navbar-item my-submenu-item">Wymagania sprzętowe</a>
					<a href="/pobieranie" class="my-navbar-item my-submenu-item">Pobieranie</a>
				</div>
				</transition>
			</a>
			<a href="#" class="my-navbar-item">Aktualnosci</a>
			<a href="/cennik" class="my-navbar-item">Cennik</a>
			<a href="/kontakt" class="my-navbar-item">Kontakt</a>
			<div class="my-navbar-item my-navbar-hide"
				 v-show="showMenu == true">
				 	<i class="fa fa-eject" aria-hidden="true"
				 	   v-on:click="showMenu = false"></i>
			</div>
		</div>
	</nav>
</template>

<script>
	export default{
		data: function () {
			return {
				showFunctions: false,
				showSupport: false,
				showMenu: false
			}
		}
	}

</script>


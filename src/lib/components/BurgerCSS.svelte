<!-- 
	Burgermenu, reacting to screen size.
	Check out a trick with the input element for pure css hamburger menus.
-->
<button class="menu-button" aria-label="Menu">
	<span class="menu-icon" />
</button>

<style>
	.menu-button {
		position: relative;
		padding: 0;
		display: inline-block;
		width: 24px;
		height: 24px;
		margin: 0 0 0 5px;
		border: none;
		background: none;
		padding: 7px;
		cursor: pointer;
	}

	.menu-button .menu-icon {
		background: #333;
		display: block;
		height: 2px;
		position: absolute;
		top: 50%;
		left: 50%;
		-webkit-transform: translate(-50%, -50%);
		transform: translate(-50%, -50%);
		transition: background 0.2s ease-out;
		width: 18px;
	}

	.menu-button .menu-icon::before,
	.menu-button .menu-icon::after {
		background: #333;
		content: '';
		display: block;
		height: 100%;
		position: absolute;
		width: 100%;
		transition: all 0.2s ease-out;
	}

	.menu-button .menu-icon::before {
		transform: translateY(6px);
	}

	.menu-button .menu-icon::after {
		transform: translateY(-6px);
	}

	/* Animations on Focus/Active state */

	.menu-button:active .menu-icon,
	.menu-button:focus .menu-icon {
		background: transparent;
	}

	.menu-button:active .menu-icon::before,
	.menu-button:focus .menu-icon::before {
		transform: rotate(-45deg) translateY(0px);
	}

	.menu-button:active .menu-icon::after,
	.menu-button:focus .menu-icon::after {
		transform: rotate(45deg) translateY(0px);
	}

	/* If screen bigger than 768px -> Burgermenu hidden */
	@media (min-width: 768px) {
		.menu-button {
			display: none;
		}
	}
</style>

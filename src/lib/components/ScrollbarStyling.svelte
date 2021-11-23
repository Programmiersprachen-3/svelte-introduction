<div class="scrollbar" id="customized">
	<div class="force-overflow" />
</div>

<!-- 
  Customized scrollbars. BEWARE: Not supported in every browser (firefox), non-standard feature!!
  Here to show browser cross compatibility. 
  More infos:
  - https://developer.mozilla.org/en-US/docs/Web/CSS/::-webkit-scrollbar
  
  Check if you can use a feature:
  - https://caniuse.com/

  Or implement it in your development process:
  - https://github.com/browserslist/browserslist
  - https://github.com/browserslist/caniuse-lite

  Hide scrollbars, but still be able to scroll:
  - https://www.w3schools.com/howto/howto_css_hide_scrollbars.asp
  
-->
<style>
	.scrollbar {
		margin-left: 30px;
		float: left;
		height: 300px;
		width: 65px;
		background: #f5f5f5;
		overflow-y: scroll;
		margin-bottom: 25px;
	}

	.force-overflow {
		min-height: 450px;
	}

	/*
 *  Customization. More examples at https://codepen.io/GhostRider/pen/GHaFw
 */

	#customized::-webkit-scrollbar-track {
		-webkit-box-shadow: inset 0 0 6px rgba(0, 0, 0, 0.3);
		background-color: #f5f5f5;
	}

	#customized::-webkit-scrollbar {
		width: 10px;
		background-color: #f5f5f5;
	}

	#customized::-webkit-scrollbar-thumb {
		background-color: #0ae;

		background-image: -webkit-gradient(
			linear,
			0 0,
			0 100%,
			color-stop(0.5, rgba(255, 255, 255, 0.2)),
			color-stop(0.5, transparent),
			to(transparent)
		);
	}
</style>

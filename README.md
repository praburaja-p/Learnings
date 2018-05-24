Angular 2 vs. Angular 1
------------------------
* Angular 2 is quite different from its predecessor. It is component-based, and the use of controllers and scope has been deprecated. Syntax and structure have also changed.
* It is faster than its predecessor. As said in ng-conf it is 2 to 5 times better than Angular 1.
* It took a mobile-first approach.
* Changed structure and syntax. It is simpler in structure. The component structure makes it easy to use.
* Changed dependency injection.
* More Language choices, i.e you can use Typescript, Dart, or JavaScript for your implementation.
* Difficult to set up. In Angular, you just have to add the reference of the library but in Angular 2 you have to set different node modules to make it work.
<style>
		body{ margin:0;}
		.grid-payemnt{  height: 100vh; min-width:768px; min-height: 620px; display: flex;}
		.grid-payLeft{ flex:1; max-width:40%; background: #f7f7f7; padding: 4px 2px; display: flex; flex-direction: column; }
		.grid-payRight{ flex:1; background: lightgreen;  padding: 15px; display: flex; flex-direction: column; }
		
		.grid-payTable{ max-height:45%; min-height: 45%; background: #fff; overflow-y:auto; }
		.grid-grid-payFinal{ max-height:55%; min-height: 55%; overflow-y:auto; }
		.payBtnPanelTop{ min-height:50px; background: #ddd; display: flex;}
		.payBtnPanelTop .btn{flex:1;}
		.payRightCalcPanel{ min-height: 50%; margin:5% 0 10%; padding: 10px; display: flex; justify-content: center; }
		.payBtnPanelBottom{ display: flex; flex-wrap: wrap; margin-bottom:20px;}
		.payBtnPanelBottom .btn{ height: 50px; width:25%;}
		.payCalcContent{ width:50%; margin-right: 20px; background: #ccc; }
		.payCalcCurrency{ width:10%; background: #bbb; }
		.payBtnPanelExta{display: flex; justify-content: center;}
		.payBtnPanelExta .btn{ height: 50px;}
	</style>
   
	<div class="grid-payemnt">
		<section class="grid-payLeft">
			<div class="grid-payTable">
				
			</div>
			<div class="grid-payFinal">
				
			</div>
		</section>
		<section class="grid-payRight">
			<section class="payBtnPanelTop">
				<button type="button" class="btn">1</button>
				<button type="button" class="btn">2</button>
				<button type="button" class="btn">3</button>
				<button type="button" class="btn">4</button>
			</section>
			<section class="payRightCalcPanel">
				<div class="payCalcContent"></div>
				<div class="payCalcCurrency"></div>
			</section>
			<section class="payBtnPanelBottom">
				<button type="button" class="btn">1</button>
				<button type="button" class="btn">2</button>
				<button type="button" class="btn">3</button>
				<button type="button" class="btn">4</button>
				<button type="button" class="btn">5</button>
				<button type="button" class="btn">6</button>
				<button type="button" class="btn">7</button>
				<button type="button" class="btn">8</button>
				<button type="button" class="btn">5</button>
				<button type="button" class="btn">6</button>
				<button type="button" class="btn">7</button>
				<button type="button" class="btn">8</button>
			</section>
			<section class="payBtnPanelExta">
				<button type="button" class="btn">Ok</button>
				<button type="button" class="btn">Cancel</button>
			</div>
		</section>
	</div>

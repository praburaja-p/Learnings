Angular 2 vs. Angular 1
------------------------
* Angular 2 is quite different from its predecessor. It is component-based, and the use of controllers and scope has been deprecated. Syntax and structure have also changed.
* It is faster than its predecessor. As said in ng-conf it is 2 to 5 times better than Angular 1.
* It took a mobile-first approach.
* Changed structure and syntax. It is simpler in structure. The component structure makes it easy to use.
* Changed dependency injection.
* More Language choices, i.e you can use Typescript, Dart, or JavaScript for your implementation.
* Difficult to set up. In Angular, you just have to add the reference of the library but in Angular 2 you have to set different node modules to make it work.
http://tobiasahlin.com/blog/how-to-animate-box-shadow/

<style>
		* { margin: 0; padding: 0; box-sizing: border-box; }
		.mainTableBox{ width: 100%; height: calc(100vh - 10px); background: #f2f2f2; display: flex; /* justify-content: space-between; align-items: center;*/}
		.left-panel-box{ background: #ffebee; width: 40%; border: 1px solid #ef9a9a;display: flex; flex-direction: column; }
		.right-panel-box{ background: #f9fbe7; width: 60%; border: 1px solid #ce93d8;display: flex;flex-direction: column; }
		
		.lp-header{ height: 6%; background: #fff; padding: 4px; border-bottom: 2px solid #ef9a9a;}
		.lp-user-info{ height: 10%; background: #e1f5fe; padding: 4px; border-bottom: 2px solid #ef9a9a; color: #000; }
		.lp-table{ height: 74%; padding: 4px; border-bottom: 2px solid #ef9a9a; color: #000; }
		.lp-footer{ height: 10%; background: #81d4fa; padding: 4px; color: #000; }
		
		.rp-header{ height: 6%; background: #fff; padding: 4px; border-bottom: 2px solid #ce93d8;}
		.rp-menulist{ height: 15%; padding: 4px; background: #f3e5f5;  display: flex; padding:4px 0 0 4px;flex-wrap: wrap;}
		.rp-submenulist{ height: 45%; background: #e3f2fd; border-bottom: 2px solid #8e24aa;display: flex; padding:4px 0 0 4px;flex-wrap: wrap;}
		.btnPurble{ border:0; min-width:60px; max-width: 11.92%; height: 50%; margin:0 4px 4px 0; background:linear-gradient(to bottom, #2196f3, #1565c0); color: #fff; font-weight: bold; cursor: pointer;}
		.btnPurble:active{background:linear-gradient(to bottom, #1565c0, #2196f3);}
		.btnOrange{ border:0; min-width:60px; max-width: 11.92%; padding: 5px; height: 16.5%; margin:0 4px 4px 0; background:linear-gradient(to bottom, #ff9800 , #ef6c00); color: #fff; font-weight: bold; cursor: pointer;}
		.btnOrange:active{background:linear-gradient(to bottom, #ef6c00 , #ff9800);}
		.rp-footerbtns table{ border-collapse: separate; border-spacing: 3px;}
		.fixedBtn{ border:0; padding: 5px; font-weight: bold; font-size: 10px; height:62px; text-align: center; cursor:pointer; background:linear-gradient(to bottom, #ccff90 , #76ff03);}
		.fixedBtn img{ max-width:24px; max-height:24px;}
		.fixedBtn span{ height:32px; display: block; text-align: center;}
		.fixedSubTotalBtn{background:linear-gradient(to bottom, #ff8a80, #ff1744); width:100px; color: yellow; text-transform: uppercase; font-size:20px; height:127px;}
		.fixedSubTotalBtn img{ max-width:32px; max-height:32px;}
		.fixedSubTotalBtn span{ height:44px;}
		
		.btnClrGreen{background:linear-gradient(to bottom, #b9f6ca , #00e676) !important;}
		.btnClrLime{background:linear-gradient(to bottom, #e6ee9c , #d4e157) !important;}
		.btnClrPink{background:linear-gradient(to bottom, #f8bbd0 , #f06292) !important;}
		
		.fixedNumBtn{ border:0; padding: 5px; font-weight: bold; font-size: 22px; height:40px; width:40px; text-align: center; cursor:pointer; margin:0 3px 3px 0; background:linear-gradient(to bottom, #b2dfdb , #4db6ac); float: left;}
		.clearLeft{ clear:left;}
		.mr-bottom-0{ margin-bottom:0 !important;}
		.fixedInputBlk{ background: #004d40; color: #ffd180; text-align: right; font-size:20px; font-weight:bold;}
		.fixedInputBlk input{ background: #004d40; color: #ffd180; text-align: right; border:0; width:90px; margin-left:-3px; display: block; height:40px; font-size: 20px; font-weight:bold;}
		.w-100{ width:100% !important;}
	</style>
	
    <main class="mainTableBox">
		<div class="left-panel-box">
			<!-- <section class="lp-header">Header</section>
			<section class="lp-user-info">User details</section>
			<section class="lp-table">table data</section>
			<section class="lp-footer">Footer data</section> -->
		</div>
		<div class="right-panel-box">
			<section class="rp-header">Header</section>
			<section class="rp-menulist">
				<!-- <button type="button" class="btnPurble">Meals</button>
				<button type="button" class="btnPurble">Meals updates shows here</button>
				<button type="button" class="btnPurble">04</button>
				<button type="button" class="btnPurble">05</button>
				<button type="button" class="btnPurble">02</button>
				<button type="button" class="btnPurble">02</button>
				<button type="button" class="btnPurble">02</button>
				<button type="button" class="btnPurble">02</button>
				<button type="button" class="btnPurble">07</button> -->
			</section>
			<section class="rp-submenulist">
				<!-- <button type="button" class="btnOrange">01</button>
				<button type="button" class="btnOrange">02</button>
				<button type="button" class="btnOrange">04</button> -->
			</section>
			<section class="rp-footerbtns">
				<table>
					<tr>
						<td><button type="button" class="fixedBtn"><span><img src="sam.png"></span> New Bill</button></td>
						<td><button type="button" class="fixedBtn btnClrGreen"><span><img src="sam.png"></span> Hold Bill</button></td>
						<td><button type="button" class="fixedBtn btnClrLime"><span><img src="sam.png"></span> View Bill</button></td>
						<td rowspan="2">
							<button type="button" class="fixedBtn fixedSubTotalBtn"><span><img src="dollar.png"></span> Sub Total</button></button>
						</td>					
						<td rowspan="2">
							<button type="button" class="fixedNumBtn">7</button>
							<button type="button" class="fixedNumBtn">8</button>
							<button type="button" class="fixedNumBtn">9</button>
							<button type="button" class="fixedNumBtn clearLeft">4</button>
							<button type="button" class="fixedNumBtn">5</button>
							<button type="button" class="fixedNumBtn">6</button>
							<button type="button" class="fixedNumBtn clearLeft mr-bottom-0">3</button>
							<button type="button" class="fixedNumBtn mr-bottom-0">2</button>
							<button type="button" class="fixedNumBtn mr-bottom-0">1</button>
						</td>						
					</tr>
					<tr>
						<td><button type="button" class="fixedBtn"><span><img src="sam.png"></span> New Bill</button></td>
						<td><button type="button" class="fixedBtn btnClrGreen"><span><img src="sam.png"></span> Hold Bill</button></td>
						<td><button type="button" class="fixedBtn btnClrLime"><span><img src="sam.png"></span> View Bill</button></td>
					</tr>
					<tr>
						<td class="fixedInputBlk">X</td>
						<td colspan="2" class="fixedInputBlk">
							<input type="text">
						</td>
						<td class=""><button type="button" class="fixedNumBtn mr-bottom-0 w-100">PLU</button></td>
						<td>
							<button type="button" class="fixedNumBtn mr-bottom-0">0</button>
							<button type="button" class="fixedNumBtn mr-bottom-0">.</button>
							<button type="button" class="fixedNumBtn mr-bottom-0 btnClrGreen">C</button>
						</td>
					</tr>
				</table>
			</section>
		</div>
	</main>

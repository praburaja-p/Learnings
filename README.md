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
<p>
		<button onclick="jsKeyboard.write(49)">1</button>
		<button onclick="jsKeyboard.write(50)">2</button>
		<button onclick="jsKeyboard.write(51)">3</button>
		<button onclick="jsKeyboard.del()">Del</button>
		<button onclick="jsKeyboard.appendChar('.')">.</button>
		<button onclick="jsKeyboard.appendChar('-')">-</button>
	</p>
<script>
	
	//https://www.sitepoint.com/demos/onscreenkeyboard/		
	var jsKeyboard = {
		currentElement: null,
		init: function(){
			$('input').not('[type="reset"]').not('[type="submit"]').on('focus, click', function(e){
            jsKeyboard.currentElement = $(this);
            jsKeyboard.currentElementCursorPosition = $(this).getCursorPosition();
            console.log('keyboard is now focused on '+jsKeyboard.currentElement.attr('name')+' at pos('+jsKeyboard.currentElementCursorPosition+')');
         });
		},
		updateCursor: function(){
			jsKeyboard.currentElement.setCursorPosition(jsKeyboard.currentElementCursorPosition);
		},
		write: function(m){
			if(jsKeyboard.currentElement){
				var a = jsKeyboard.currentElement.val(),
					b = String.fromCharCode(m),
					pos = jsKeyboard.currentElementCursorPosition,
					output = [a.slice(0, pos), b, a.slice(pos)].join('');
				jsKeyboard.currentElement.val(output);
				jsKeyboard.currentElementCursorPosition++; //+1 cursor
				jsKeyboard.updateCursor();
			}
		},
		appendChar: function(m){
			if(jsKeyboard.currentElement){
				var a = jsKeyboard.currentElement.val(),
					pos = jsKeyboard.currentElementCursorPosition,
					output = [a.slice(0, pos), m, a.slice(pos)].join('');
				jsKeyboard.currentElement.val(output);
				jsKeyboard.currentElementCursorPosition++; //+1 cursor
				jsKeyboard.updateCursor();
			}
		},
		del: function() {
			if(jsKeyboard.currentElement){
				var a = jsKeyboard.currentElement.val(),
					pos = jsKeyboard.currentElementCursorPosition,
					output = [a.slice(0, pos-1), a.slice(pos)].join('');
				jsKeyboard.currentElement.val(output);
				jsKeyboard.currentElementCursorPosition--; //-1 cursor
				jsKeyboard.updateCursor();
			}
		},
	}
	// GET CURSOR POSITION
	jQuery.fn.getCursorPosition = function(){
		if(this.lengh == 0) return -1;
		return $(this).getSelectionStart();
	}
	jQuery.fn.getSelectionStart = function(){
		if(this.lengh == 0) return -1;
		input = this[0];
		var pos = input.value.length;

		if (input.createTextRange) {
			var r = document.selection.createRange().duplicate();
			r.moveEnd('character', input.value.length);
			if (r.text == '')
				pos = input.value.length;
				pos = input.value.lastIndexOf(r.text);
		} else if(typeof(input.selectionStart)!="undefined")
		pos = input.selectionStart;
		return pos;
	}

	//SET CURSOR POSITION
	jQuery.fn.setCursorPosition = function(pos) {
		this.each(function(index, elem) {
			if (elem.setSelectionRange) {
				elem.setSelectionRange(pos, pos);
			} else if (elem.createTextRange) {
				var range = elem.createTextRange();
				range.collapse(true);
				range.moveEnd('character', pos);
				range.moveStart('character', pos);
				range.select();
			}
		});
		return this;
	};
	$(function(){
		jsKeyboard.init();
	});
</script>

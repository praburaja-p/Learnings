Angular 2 vs. Angular 1
------------------------
* Angular 2 is quite different from its predecessor. It is component-based, and the use of controllers and scope has been deprecated. Syntax and structure have also changed.
* It is faster than its predecessor. As said in ng-conf it is 2 to 5 times better than Angular 1.
* It took a mobile-first approach.
* Changed structure and syntax. It is simpler in structure. The component structure makes it easy to use.
* Changed dependency injection.
* More Language choices, i.e you can use Typescript, Dart, or JavaScript for your implementation.
* Difficult to set up. In Angular, you just have to add the reference of the library but in Angular 2 you have to set different node modules to make it work.
<script>
$('.add').on('click',function(){
	$('#list').append('<li><input class="field"> &nbsp;&nbsp;&nbsp; <input class="phone"></li>').attachAutocomplete();;
});
$.fn.attachAutocomplete = function() {
	$(this).find(".field").autocomplete({
	  source: [ "c++", "java", "php", "coldfusion", "javascript", "asp", "ruby" ],
	  classes: { "ui-autocomplete": "so_cute"},
	  select: function( event, ui ) {
		$(this).parent().find(".phone").val(ui.item.label);
	  }
  });
}
</script>

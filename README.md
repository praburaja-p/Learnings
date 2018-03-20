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

.spTabs{ background: #fff; list-style: none;padding:0; margin:0; border-bottom:3px solid #ddd;}
.spTabs li{ display: inline-block; padding-right:20px;}
.spTabs a{ text-decoration: none; display: block; text-align: center; padding: 10px; cursor: default;}
.spTabs a span{ width: 28px; line-height:28px; color: #999; font-weight: bold; height:28px; border-radius:20px; background: #ddd; display: inline-block; margin-bottom:5px;}
.spTabs a span u{ text-decoration: none;}
.spTabs a span .fa{ display: none;}
.spTabs a b{ color: #999;}
.spTabs .current a span{ color: #fff; background: lightgreen;}
.spTabs .current a b{ color: #111;}
.spTabs .completed a span{ color: #fff; background: lightgreen;}
.spTabs .completed a b{ color: #111;}
.spTabs .completed a span .fa{ display: inline;}
.spTabs .completed a span u{ display: none;}

.spTabBody{ clear:both; padding: 15px; display: none;}
.spTabBody.current{ display: block;}

<!Doctype html>

    
    <div class="container">
    <ul class="spTabs">
      <li class="current">
      <a href="#">
        <span><u>1</u><i class="fa fa-check"></i></span><br />
        <b>Entry details</b>
      </a>
      </li>
       <li>
      <a href="#">
        <span><u>2</u><i class="fa fa-check"></i></span><br />
        <b>Module data</b>
      </a>
      </li>
      <li>
      <a href="#">
        <span><u>3</u><i class="fa fa-check"></i></span><br />
        <b>Final review</b>
      </a>
      </li>
    </ul>
    <div class="spContent">
      <section id="spTab1" class="spTabBody current">
        <div class="form-horizontal">
  <div class="form-group">
    <label class="col-sm-2 control-label">Email</label>
    <div class="col-sm-10">
      <input type="email" class="form-control" id="">
    </div>
  </div>
  <div class="form-group">
    <div class="col-sm-offset-2 col-sm-10">
      <button type="submit" class="btn btn-warning" onClick="nextStep(2)">Next</button>
    </div>
  </div>
  </div>  
      </section>
      
      <section id="spTab2" class="spTabBody">
        <div class="form-horizontal">
  <div class="form-group">
    <label class="col-sm-2 control-label">Modular field</label>
    <div class="col-sm-10">
      <input type="email" class="form-control" id="">
    </div>
  </div>
  <div class="form-group">
    <div class="col-sm-offset-2 col-sm-10">
     <button type="button" class="btn btn-info" onClick="prevStep(1)">Back</button>
      <button type="button" class="btn btn-warning" onClick="nextStep(3)">Next</button>
    </div>
  </div>
  </div>  
      </section>
      
       <section id="spTab3" class="spTabBody">
        <div class="form-horizontal">
  <div class="form-group">
    <label class="col-sm-2 control-label">Final review</label>
    <div class="col-sm-10">
      <input type="email" class="form-control" id="">
    </div>
  </div>
  <div class="form-group">
    <div class="col-sm-offset-2 col-sm-10">
     <button type="button" class="btn btn-info" onClick="prevStep(2)">Back</button>
      <button type="button" class="btn btn-warning" onClick="">Submit</button>
    </div>
  </div>
  </div>  
      </section>
      
    </div>
    </div>

function nextStep(id){
	 $('.spTabs li.current').addClass('completed');
	 $('.spTabs li, .spTabBody').removeClass('current'); 
  $('.spTabs li').eq(id-1).addClass('current');
  $('#spTab'+id).addClass('current');
}
function prevStep(id){
	$('.spTabs li.current').removeClass('current');
  $('.spTabs li').eq(id-1).addClass('current').removeClass('completed');
  $('.spTabBody').removeClass('current'); 
  $('#spTab'+id).addClass('current');
}

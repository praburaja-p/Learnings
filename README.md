Angular 2 vs. Angular 1
------------------------
* Angular 2 is quite different from its predecessor. It is component-based, and the use of controllers and scope has been deprecated. Syntax and structure have also changed.
* It is faster than its predecessor. As said in ng-conf it is 2 to 5 times better than Angular 1.
* It took a mobile-first approach.
* Changed structure and syntax. It is simpler in structure. The component structure makes it easy to use.
* Changed dependency injection.
* More Language choices, i.e you can use Typescript, Dart, or JavaScript for your implementation.
* Difficult to set up. In Angular, you just have to add the reference of the library but in Angular 2 you have to set different node modules to make it work.
.page-header, .page-header-space {height: 80px; }
.page-footer, .page-footer-space { height: 30px; }
.page-footer { background: lightgreen; position: fixed; bottom: 0; width: 100%; }
.page-header { background: lightblue; position: fixed; top: 0mm; width: 100%; }
@media print {
.thead {display: table-header-group;} 
.tfoot {display: table-footer-group;}
}
.table{width:100%;}
.table thead{display: table-header-group;}
.table th{border: 1px solid #000; border-left:0; padding: 5px 10px;}
.table td{border-bottom:1px solid #000; border-right: 1px solid #000; padding: 30px 10px;}
.table tr{ page-break-inside:avoid; page-break-after:auto }
.table tr td:first-child, .table tr th:first-child{ border-left:1px solid #000; }
<div class="page-header"></div><div class="page-footer"></div><table width="100%"><thead class="thead"><tr><td><div class="page-header-space"></div></td></tr></thead><tbody><tr><td><table width="100%"><tr><td><table class="table" border="0"><thead class="thead"><tr><th></th><th></th><th></th></tr></thead><tbody><tr><td></td><td></td><td></td></tr></tbody></table></td></tr></table></td></tr></tbody><tfoot class="tfoot"><tr><td><div class="page-footer-space"></div></td></tr></tfoot></table>

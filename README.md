angular-draganddrop
===================

AngularJS drag&amp;drop module. The dragged element is rendered with a dedicated AngularJS controller. This controller and the associated view is fully customizable.

This modules contains 
- 2 directives: `drag` and `drop`
- 1 service: `dragAndDrop`
- 2 controllers: `DragAndDropController` and `DragAndDropItemController`


[You could find here a sample](http://plnkr.co/edit/o2YCbCDS6ZXfykSGAkL4?p=preview)

## Directives

### `drag` directive

`drag` enable drag support on an element

`drop-callback` callback called after drop occurs. Especialy uselfull to do post drop action (eg. delete dragged element). Evaluated as an expression. If the expression evalutes as a function, it will be called with `dragData` as argument

`drag-include` template included for rendering the dragged element. Evaluated as an expression.

`drag-data` data transfered from drag element to drop element. This module does not clone the data. It is the reponsability of user to clone data. Evaluated as an expression.

```html
<li ng-repeat="book in books" drag drop-callback="endDrag($index)" drag-include="'dragItemTemplate'" drag-data="book">
</li>

```


### `drop` directive

`drop` enable drop support on an element

`drop-callback` callback called then drop occurs. Evaluated as an expression. If the expression evalutes as a function, it will be called with `dragData` as argument



```html
<section drop drop-callback="endDrop">
</section>
```


## `dragAndDrop` Service

This service stores transfered data. 
Why a `map`? I have planned to add support for multi touch.

## Controllers

Controllers handles dragged item rendering. 
Why a `ngRepeat`  I have planned to add support for multi touch.







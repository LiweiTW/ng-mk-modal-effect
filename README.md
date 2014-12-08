# Custom effect modals

### Demo

[Simple](http://malikid.github.io/ng-mk-modal-effect/example/simpleExample.html)  
[Complete](http://malikid.github.io/ng-mk-modal-effect/example/)  



### Bower Package

Name: **ng-mk-modal-effect**  



### Environment

angular: ~1.2.18  
jquery: ~2.1.1



### Usage

##### In Angular Controller
```
$scope.data =
  modalData:
    // mkmd-effect-[effectType]. Effect types are listed below.
    effect: "mkmd-effect-so"
    // Actually, only height, width, top and left can be set.
    // If none is set there are default values.
    style:
      height: "auto"
      width: "70%"
```

##### In Template

- jade
```
button#modalTriggerBtn Open Modal

mk-modal(trigger-element-id="modalTriggerBtn", close-element-id="modalCloseBtn", data="data.modalData")
  div
   span Content to show, Angular binding with your controller still works here.
   button#modalCloseBtn Close Modal!
```
  

- html
```
<button id="modalTriggerBtn">
  Open Modal
</button>

<mk-modal trigger-element-id="modalTriggerBtn", close-element-id="modalCloseBtn", data="data.modalData">
  <div>
    <span>
      Content to show in modal, angular binding with your controller still works here.
    </span>
    <button id="modalCloseBtn">
      Close Modal!
    </button>
  </div>
</mk-modal>
```

##### Tag

> ####### mk-modal

##### Attributes

> ###### trigger-element-id

>> *REQUIRED!* Id of the element on original page to trigger modal open event.

> ###### close-element-id

>> *OPTIONAL.* Id of the element in modal to trigger modal close event.

> ###### data

>> *REQUIRED!* Data of this modal.



### Effect Types

| Effect Type                  | Value | Effect Type            |  Value |
|------------------------------|:-----:|------------------------|:------:|
| Fade In and Scale Up         |   fi  | Stand Out              |   so   |
| Slide from the Right         |   sl  | Super Scaled           |   ss   |
| Slide from the Bottom        |   su  | Just Me                |   jm   |
| Slide Down and Stick At Top  | sdsat | 3D Flip Horizontal     |  3dfh  |
| Slide Up and Stick At Bottom | susab | 3D Flip Vertical       |  3dfv  |
| Newspaper                    |   n   | 3D Sign                | 3dsign |
| Fall                         |   f   | 3D Slit                | 3dslit |
| Side Fall                    |   sf  | 3D Rotate from Bottom  |  3dru  |
|                              |       | 3D Rotate In from Left |  3drr  |

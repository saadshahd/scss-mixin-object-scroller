### SCSS Object Scroller

It takes a set of [parameters](#parameters) and generates a singletone **object** class.

The object class terminology comes from [cssguidelin.es](https://cssguidelin.es/)

#### Install
  1. `npm i -S scss-mixin-object-scroller`
  1. Import it into your SCSS code:
      ```scss
      @import "~scss-mixin-object-scroller";
      ```

#### Usage

##### Parameters
  - **$size:** `(unit) default: 6px`
  - **$bg:** `(color) default: #eee`
  - **$fg**. `(color) default: #333`
  - **$radius**. `(unit) default: $size`

##### Examples

  - Use it once to generate your singletone scroller object:
    ```scss
    @include scroller();
    ```

    It will generate:
    ```css
    .scroller { overflow: auto; }
    .scroller::-webkit-scrollbar { width: 6px; height: 6px; }
    .scroller::-webkit-scrollbar-track-piece { background-color: #eee; }
    .scroller::-webkit-scrollbar-thumb:horizontal,
    .scroller::-webkit-scrollbar-thumb:vertical { border-radius: 6px; background-color: #333; }
    ```

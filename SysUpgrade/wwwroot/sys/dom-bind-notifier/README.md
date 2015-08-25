# &lt;dom-bind-notifier&gt;

> Adds good old Object.observe to Polymer 1.0 template binding (dom-bind)

So you no longer have to worry about notifying your elements.
With single element, you get real TWO-way data-binding for HTML Templates.
DOM stays in sync with any JS object you provide.


## Demo

[Check it live!](http://Juicy.github.io/dom-bind-notifier)

## Install

Install the component using [Bower](http://bower.io/):

```sh
$ bower install dom-bind-notifier --save
```

Or [download as ZIP](https://github.com/Juicy/dom-bind-notifier/archive/master.zip).

## Usage

1. Import Web Components' polyfill, if needed:

    ```html
    <script src="bower_components/webcomponentsjs/webcomponents.js"></script>
    ```

2. Import Custom Element:

    ```html
    <link rel="import" href="bower_components/dom-bind-notifier/dom-bind-notifier.html">
    ```

3. Start using it!

    ```html
    <template is="dom-bind" id="tId">
      <dom-bind-notifier ref="tId" observed-object="{{myObj}}" path="myObj" deep></dom-bind-notifier>
      <!-- your magic goes here -->
    </template>
    ```
## Object.observe

Please note, that we use [`Object.observe` & `Array.observe`](http://wiki.ecmascript.org/doku.php?id=harmony:observe), so if your environment does not support it, you will need a shim.

## Options

Attribute         | Options   | Default | Description
---               | ---       | ---     | ---
`observed-object` | *Object*  |         | Object to bind to
`ref`             | *String*  |         | Id of `dom-bind` element to notify.
`path`            | *String*  |         | Path of observed object in scope of `ref`erenced `dom-bind`
`deep`            | *Boolean* | `false` | Should we observe objects deeply

## Events

Event    | Details                                       | Description
---      | ---                                           | ---
`change` | *Array* of changes in `Object.observe` format | Triggers when `dom-bind` gets notified with some changes

## Contributing

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -m 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request :D

## History

For detailed changelog, check [Releases](https://github.com/Juicy/dom-bind-notifier/releases).

## License

[MIT License](http://opensource.org/licenses/MIT)

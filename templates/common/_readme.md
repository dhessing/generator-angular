# <%= appname %>

## Quickstart

Run `grunt serve` for development.


**Note: If the above command fails, you've probably just cloned this repository and need to install some dependencies using `npm install` and `bower install`.
Run these commands form the root of your project.**

### Generators

Assuming you've included angular-resource.js during app generation (it was selected by default), let's add a new route to our project:

```bash
yo angular:route myroute
```

This generates a controller and view, and configures a route in `app/scripts/app.js` connecting them.
The terminal will show the files affected by this command.

Go to [http://127.0.0.1:9000/#/myroute](http://127.0.0.1:9000/#/myroute) to see your newly created route.
It will contain some dummy content.

To edit this route:

* Add your own content in `app/views/myroute.html`
* Add your own behaviour in `app/scripts/controllers/myroute.js`
* Add tests in `test/spec/controllers/myroute.js`

For more info about available generators, see the [generator documentation](https://github.com/yeoman/generator-angular/blob/master/readme.md#generators).

### Third-Party Dependencies

*(HTML/CSS/JS/Images/etc)*

Third-party dependencies are managed with [bower-install](https://github.com/stephenplusplus/grunt-bower-install). Add new dependencies using **Bower** and then run the **Grunt** task to load them:

```bash
  bower install --save jquery
  grunt bowerInstall
```

This works if the package author has followed the [Bower spec](https://github.com/bower/bower.json-spec). If the files are not automatically added to your index.html, check with the package's repo for support and/or file an issue with them to have it updated.

To manually add dependencies, `bower install depName --save` to get the files, then add a `script` or `style` tag to your `index.html` or an other appropriate place.

The components are installed in the root of the project at `/bower_components`. To reference them from the `grunt serve` web app `index.html` file, use `src="bower_components"` or `src="/bower_components"`. Treat the references as if they were a sibling to `index.html`.

*Testing Note*: a project checked into source control and later checked out, needs to have `bower install` run from the `test` folder as well as from project root.

### Building

Run `grunt` for building your project. It generates an optimized version of your application in the `dist` directory.

For deployment, see the [Yeoman deployment documentation](http://yeoman.io/deployment.html)


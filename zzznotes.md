# weird thing about getting started

create index.html in dist folder manually, like a peasant
will learn later how to do it the proper way though

# asset management

it just is what it says, some modules and loaders to add to webpack.config.js and also the node_modules to automatically create static assets that are usable in dist

# output management

ugh, kinda boring, but it is having 2 functions
or like two script .js in the src, and you want to import them twice in the html, and set the output to be the name of the file, or the name of the file and the bundle of the javascript for that file

then, the htmlwebpack plugin, outputting a html (plugins, new htmlwebpackplugin, title: output management)

then, cleaning the dist folder (output, clean:true)

# development

sourcemaps, just use (devtool: 'inline-source-map'), it helps

then, watch mode, add a script webpack --watch

then, webpack-dev-server

# code splitting

the split chunks plugin

wow so it adds a new modules thing

# caching

kind of important this part, dont reload vendor much

# libraries

library: "webpackNumbers",

    <script src="https://example.org/webpack-numbers.js"></script>
    <script>
        window.webpackNumbers.wordToNum('Five');
    </script>

    library: {
        name: 'webpackNumbers',
        type: 'umd',
    },

peer dependency

    externals: {
        lodash: {
        commonjs: 'lodash',
        commonjs2: 'lodash',
        amd: 'lodash',
        root: '_',
        },
    },

im not really sure what this peer dependency thing is

# environment variables

this is weird, passing in a single variable into module.exports as a function

# tree shaking

wow this is really weird
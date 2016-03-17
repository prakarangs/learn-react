## Documentation

### Webpack - Module loader(bundle)

1. To install webpack we need to also have node.js and start with package.json file.

		npm init
    

2. After package.json are created, let's install webpack and add that in your dependencies.

		npm -S install webpack
		
3. Also install webpack globally so you can always run webpack command

		npm install -g webpack
		
4. Create webpack.config.js file to tell webpack where to look and how to act.
Sample config code -> https://gist.github.com/learncodeacademy/25092d8f1daf5e4a6fd3



#### How to use webpack

Basically, we want to work with Javascript like the way we work with CSS via Sass.
We want to be able to work on different modules while load them into one single file which will help us perform better on browsers as we will be doing less http requests.

		// Example directory
		
			- project_folder
				- htdocs
					- js
						module1.js
						module2.js
						main.js
				- node_modules
				package.json
				webpack.config.js

As you see you have different module[i] files while you only have one main.js file. This is where we will import different module into one single file.

The configuration of path and filenames or tasks shall then be set in your `webpack.config.js` file. (Pretty much like Gulp and Grunt)

#### Run webpack and minify for Production

Run webpack (build your main.js file) in debug mode
		
		$ webpack
		
Minify your main.js in NODE_ENV=production

		$ NODE_ENV=production webpack

		
You can also install jQuery via `npm` and require to use jQuery in different module file.
However, jQuery won't be in global scope at all because webpack will use jQuery in module that it needs jQuery only.

More awesome introduction: http://blog.madewithlove.be/post/webpack-your-bags/


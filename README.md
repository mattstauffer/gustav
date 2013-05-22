Gustav
======

An opinionated, backend-agnostic, front-end development stack inspired by the Rails asset pipeline.

Features
--------
* Separation of source and deliverable assets
* [Sass](http://sass-lang.com/) & [Compass](http://compass-style.org/) for pre-compiled CSS
* Gemfile to allow use of [Bundler](http://gembundler.com/v1.3/gemfile.html) to manage Gems
* Guardfile to use [Guard](https://github.com/guard/guard) for livereload-style watching
* Jammit for simple, YAML-based asset management

Getting Started
---------------
1. Make sure you have Ruby installed. We recommend [RVM](http://net.tutsplus.com/tutorials/ruby/how-to-install-ruby-on-a-mac/).
2. Clone the git repository  
  `$ git checkout git://github.com/mattstauffer/gustav.git`

3. *(optional)* Delete the git repository so you just have the clean files  
   `$ cd gustav`  
   `$ rm -rf .git`

4. Customize the files to your liking. 
  * Add in any third-party javascripts into `source/vendors/js` and add any third-party css into `source/vendors/css`
    * **Note:** Any vendor images for JS or CSS should go in `source/vendors/img`, and you'll need to update the files to refer to them from within the vendor source files as `../img`. Vendor JS will end up in `assets/js`; vendor CSS will end up in `assets/css`; and vendor images will end up in `vendor/img`.
  * Add any custom javascript libraries to `source/js/libs`
  * *(optional)* Update the file structure of source/sass to your preferred Sass structure. The provided structure and partials are just a suggestion.
  * *(optional)* If you want to change the layout or names of any of the generated files, or the source directory structure, edit `config/assets.yml` and `config/compass.rb`.

5. *(optional)* Set up a [livereload extension](http://feedback.livereload.com/knowledgebase/articles/86242-how-do-i-install-and-use-the-browser-extensions-) in your browser.

6. Run guard, and it's now watching your source directories, outputting new files into your assets directories, and pinging your livereload browser extension with each change.  
  `$ bundle exec guard`

7. Link your files in your frontend view files (HTML). By default, these are the files you'll be referencing:
  * `assets/css/vendor.css`
  * `assets/css/style.css`
  * `assets/js/vendor.min.js`
  * `assets/js/main.min.js`

8. That's it!

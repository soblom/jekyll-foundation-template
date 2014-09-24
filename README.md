# Jekyll - Foundation 5 Template

To have an easy start for my standard static website setup (Jekyll and Foundation), I created this template. Maybe it is useful for anyone else.

The project is ready to use as-is. If you want to update the components involved, follow the steps in the "Setup" section first. If you (or I) ever wondered, which steps where involved to get to the initial project state from scratch, checkout "How to re-create this template"

## Setup

All my standard setup steps are collected in the `Rakelfile`. So just do

```
$:> rake setup
```

## How to recreate this template

Steps involved (in principle), to re-create the initial state of this template.

  1. Install jekyll-gem manually: `gem install jekyll`
  2. Initialize project `jekyll new jekyll-foundation-template`
  3. Install npm with homebrew: `brew install npm`
  4. create `bower.json` with
      ```javascript
      {
        "name": "foundation-compass-app",
        "version": "0.0.1",
        "private": "true",
        "dependencies": {
          "foundation": "zurb/bower-foundation"
        }
      }
      ```
  5. Run `bower install`
  6. Create `config.rb` with
      ```ruby
      # Require any additional compass plugins here.
      add_import_path "bower_components/foundation/scss"

      http_path = "/"
      css_dir = "stylesheets"
      sass_dir = "_scss"
      images_dir = "img"
      javascripts_dir = "js"
      ```

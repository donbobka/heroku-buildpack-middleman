# Middleman Build Pack

This is a build pack for [Middleman](http://middlemanapp.com) that will
create your static site.

It is cleaner than most Middleman build packs out there because it
takes advantage of [Heroku Multiple Buildpacks](https://devcenter.heroku.com/articles/using-multiple-buildpacks-for-an-app) to separate out the Ruby, Middleman and Web server specific components.

## Usage

This build pack is meant to be used with the
[Heroku Multiple Buildpacks](https://devcenter.heroku.com/articles/using-multiple-buildpacks-for-an-app).

```shell
heroku buildpacks:add --index 1 heroku/ruby
heroku buildpacks:add --index 2 https://github.com/donbobka/heroku-buildpack-middleman
heroku buildpacks:add --index 3 https://github.com/heroku/heroku-buildpack-static
```

Then just push!

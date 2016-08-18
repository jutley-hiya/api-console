# For when following the given steps isn't enough

Shoddy documentation, but should be better than nothing.

### Node

First off, I had to make sure my versions of `node` and `npm` were correct. Here are my versions that are working correctly.

```
➜  npm -v
2.15.8
➜  node -v
v4.4.7
```
To get here, I ran:
```
➜  brew tap homebrew/versions
➜  brew install homebrew/versions/node4-lts
```

### Karma

If you're seeing something like this:

```
Loading "grunt-karma.js" tasks...ERROR
>> Error: Cannot find module 'karma'

Running "concat:index" (concat) task
File dist/index.html created.

Done, without errors.
```

Try installing the specific karma version.

```npm install karma@~0.12.0```

### Sass

If you're seeing something like this

```
Running "ngtemplates:ramlConsole" (ngtemplates) task
File .tmp/templates/app.js created.

Running "concat:app" (concat) task
File dist/scripts/api-console.js created.

Done, without errors.
    Warning: Running "sass:build" (sass) task
Warning:
You need to have Ruby and Sass installed and in your PATH for this task to work.
More info: https://github.com/gruntjs/grunt-contrib-sass
 Use --force to continue.

Aborted due to warnings. Use --force to continue.

    Aborted due to warnings.
```

Try running

```gem install --user-install sass```

And then add the right path to your $PATH. For me, this looked like

```export PATH=$PATH:/Users/jutley/.gem/ruby/2.0.0/bin```

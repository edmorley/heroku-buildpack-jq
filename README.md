A Heroku buildpack to add [`jq`](https://github.com/stedolan/jq) support to any build or Dyno.

### Usage
``` bash
$ heroku buildpacks:add --index 1 https://github.com/szgupta/heroku-buildpack-jq.git --app <APP_NAME>
```
Note that you'll want to add the `jq` buildpack *before* any buildpack that relies on `libjq` (e.g. [`ruby-jq`](https://github.com/winebarrel/ruby-jq)). Supplying `--index 1` as an option will guarantee this.

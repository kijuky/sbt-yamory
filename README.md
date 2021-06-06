# yamory-sbt-plugin

[yamory](https://yamory.io/) for sbt

## Usage

This plugin requires sbt 1.4+

build.sbt:

```sbt
yamoryProjectGroupKey := "PUT PROJECT_GROUP_KEY"
yamoryApiKey := sys.env("YAMORY_API_KEY")
yamoryScriptUrl := "PUT https://yamory/script/..."
```

```.envrc:shell
export YAMORY_API_KEY="PUT YOUR YAMORY_API_KEY"
```

and run

```shell
sbt yamory
```

then scan results are recorded in yamory.

### Testing

Run `test` for regular unit tests.

Run `scripted` for [sbt script tests](http://www.scala-sbt.org/1.x/docs/Testing-sbt-plugins.html).

### Publishing

1. publish your source to GitHub
2. [create a bintray account](https://bintray.com/signup/index) and [set up bintray credentials](https://github.com/sbt/sbt-bintray#publishing)
3. create a bintray repository `sbt-plugins` 
4. update your bintray publishing settings in `build.sbt`
5. `sbt publish`
6. [request inclusion in sbt-plugin-releases](https://bintray.com/sbt/sbt-plugin-releases)
7. [Add your plugin to the community plugins list](https://github.com/sbt/website#attention-plugin-authors)
8. [Claim your project an Scaladex](https://github.com/scalacenter/scaladex-contrib#claim-your-project)

ScalaJs.io Core Utilities
=========================

### Description

Core utilities for the ScalaJs.io platform.

### Build Dependencies

* [SBT v0.13.13](http://www.scala-sbt.org/download.html)

### Build/publish the SDK locally

```bash
 $ sbt clean publish-local
```

### Running the tests

Before running the tests the first time, you must ensure the npm packages are installed:

```bash
$ npm install
```

Then you can run the tests:

```bash
$ sbt test
```

### Examples

```scala
import io.scalajs.JSON
import scalajs.js

val result = JSON.parseAs[js.Object]("""{"x":5}""", { (key: js.Any, value: js.Any) => value }: js.Function)
println(JSON.stringify(result)) // {"x":5}
```

### Artifacts and Resolvers

To add the `Core` binding to your project, add the following to your build.sbt:  

```sbt
libraryDependencies += "io.scalajs" %%% "core" % "0.3.0.5"
```

Optionally, you may add the Sonatype Repository resolver:

```sbt   
resolvers += Resolver.sonatypeRepo("releases") 
```

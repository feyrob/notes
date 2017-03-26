# Eclipse + Scala + Artifact Repo Dependencies + Debugging
```
mkdir myproject
cd myproject
sbt new sbt/scala-seed.g8
	enter name of project when asked
cd myproject
create the file
	project/plugins.sbt
with the content:
	addSbtPlugin("com.typesafe.sbteclipse" % "sbteclipse-plugin" % "5.1.0")
edit the file
	build.sbt
set scala version like this:
	lazy val root = (project in file(".")).
		settings(
			inThisBuild(List(
				organization := "com.example",
				scalaVersion := "2.11.8",

sbt
	eclipse

start eclipse
	import the project in eclipse
# fix debugging
in Eclipse in "Package Explorer" right click "myproject" -> "properties" -> "Java Build Path"
		find "Scala Library container [ ... ]", select it, and press "Up" until it is on top

# adding a library available on an artifact repository
- edit build.sbt
sbt
	eclipse
in Eclipse in "Package Explorer" ctrl+click myproject until it is _not_ selected
hit f5
```

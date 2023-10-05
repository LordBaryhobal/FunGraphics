# FunGraphics

A library used for teaching computer science in the [ISC](https://www.hevs.ch/isc) degree programme, notably for the course 101.1.
The documentation is available [here](https://isc-hei.github.io/FunGraphics/). It is automatically built and published each time a new version tag is added to the repo.

## Origin

This library has been developed for the [`PImp`](https://isc.hevs.ch/learn/courses/101-1) and the [`inf1`](https://inf1.begincoding.net) courses at the [HES-SO Valais//Wallis](https://www.hevs.ch).

## Compiling

* UNIX-like (Linux, MacOS X, ...) : ```./gradlew build```
* Windows : ```gradlew.bat build```

results :

| File                                 | Description                                                         |
|--------------------------------------|---------------------------------------------------------------------|
| `build/fungraphics-dev.jar`          | The latest build of the library, constant name, useful for testing. |
| `build/libs/fungraphics-VERSION.jar` | The same file with a [versioned](#Version) name.                    |

## Version

The version number used in the file name and available using `FunGraphics.version()` is
generated by inspecting the git state (see [com.palantir.git-version](https://github.com/palantir/gradle-git-version)
for details).

Here is an example : 1.5.7-3-g2aabbbf.dirty

* 1.5.7 is the last tag
* -3- we are 3 commits after the tag
* g2aabbbf : git short hash
* .dirty : some changes are not committed

## How to release (and have a nice version number)

1. git commit
1. git tag -a MAJOR.MINOR.SUB -m "tag vMAJOR.MINOR.SUB"
1. git push origin MAJOR.MINOR.SUB
1. [compile](#Compiling)

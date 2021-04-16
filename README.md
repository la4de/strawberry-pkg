# strawberry-pkg

The purpose of this repo is to demonstrate how easy it is to extend strawberry package with namespace packages.

Another goal is to show that developing the namespace repo is challenging.

## Content

Repo has two packages. `strawberry.pkg` and `testproject`. Tests are there to demonstrate the challenge.

## The challenge

The challenge here is that local development is difficult because you cannot import `strawberry.pkg`
from the local code. You can see that by running the tests. Tests under `strawberry.pkg are failing.

However package is working if you install that into another project. Testproject demonstrates that. Tests are passing there.

I also noticed that `pip install -e ...` does not work as usually with namespace package. You
can install the package but you have the same import problem. `import strawberry.pkg` raises `ModuleNotFoundError`

## Links
* https://packaging.python.org/guides/packaging-namespace-packages/
* https://stackoverflow.com/questions/11237685/developing-with-python-namespaced-packages

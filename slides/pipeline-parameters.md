### &hellip;And So much more!

* <!-- .element: class="fragment" --> `image`
* <!-- .element: class="fragment" --> `only` + `except`
* <!-- .element: class="fragment" --> `dependencies`

<!-- .element: class="fragment" --> [docs.gitlab.com/ee/ci/yaml](https://docs.gitlab.com/ee/ci/yaml/)

Note:

There are a ton of different parameters available to streamline your build.

`image` lets us use pre-built Docker images, so you can build exactly what you need to test.

`only` and `except` let us control the creation of jobs, making sure we're not wasting time and resources. Example: only run E2E tests on master.

`dependencies` lets us say "this job depends on that one passing" to help order things and prevent duplication.

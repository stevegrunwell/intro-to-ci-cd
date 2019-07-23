### GitLab CI/CD Tools

* <!-- .element: class="fragment" --> Define multiple **stages** (build, test, deploy, etc.)
* <!-- .element: class="fragment" --> Each stage has one or more **jobs**
* <!-- .element: class="fragment" --> Multiple runners == run jobs in parallel!

Note:

Some terminology: GitLab lets us define one or more *stages* in our pipelines. Typically, these will be something like: "install dependencies and build the app", "run our tests", then "deploy to target servers" (totally flexible)

Each stage is comprised of one or more "jobs" (e.g. "run unit tests")

Jobs are carried out by runners, and we can run multiple jobs in the same stage in parallel if we have multiple runners, which speeds up the pipeline.

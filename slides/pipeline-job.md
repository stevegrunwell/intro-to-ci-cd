### A simple job

<pre class="hljs yaml"><code>Install npm dependencies:</code><code class="fragment">    stage: build</code><code class="fragment">    script:
        - npm install --no-progress
        - npm run prod</code><code class="fragment">    artifacts:
        paths:
            - public</code><code class="fragment">    cache:
        key: ${CI_COMMIT_REF_SLUG}-npm
        paths:
            - node_modules</code></pre>

Note:

A common task: installing dependencies. This will typically fall under the "build" stage.

We'll install the dependencies, then run an npm script that calls webpack to build everything, just as we would locally.

We're telling GitLab that we want to hold onto what's generated into the public/ directory, since Webpack just built all of it.

We can also cache node_modules with the current commit, so if we need to re-run this it'll go faster for us.

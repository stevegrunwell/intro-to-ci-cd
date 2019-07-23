### Building a Docker Image

* <!-- .element: class="fragment" --> Final product: a Docker image of your app
* <!-- .element: class="fragment" --> Great for Docker-powered production clusters!

Note:

If you're using something like Docker Swarm or Kubernetes, you could also use the CI pipeline to literally build a Docker image of your app.

Also makes it easier to do "canary" releases, where maybe only 20% of traffic gets sent to the latest version of the app.

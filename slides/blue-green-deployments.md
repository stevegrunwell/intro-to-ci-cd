### Blue-Green Deployments

* <!-- .element: class="fragment" --> Run multiple production environments/servers
    - Some active (blue), some idle (green)
* <!-- .element: class="fragment" --> Deploy to green
* <!-- .element: class="fragment" --> Once ready, route traffic to green
    - Blue becomes idle
* <!-- .element: class="fragment" --> In case of issues, re-route to blue

Note:

This is a more advanced deployment scheme, wherein we have multiple production environments.

Simple example: two servers (blue and green) and a load balancer.
- All traffic is currently going to blue.
- Deploy + test in green environment.
- When ready, route traffic to green.
- Next deployment works the same, but goes to blue instead.
- If something went wrong, re-route from green to blue.

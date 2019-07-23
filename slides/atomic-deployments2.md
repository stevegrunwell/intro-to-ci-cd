### Atomic Deployments

```sh
# /var/www
releases/
  + 1563759801/ # Oldest
  + 1563759802/
  + 1563759803/ # Newest
shared/
  + logs/
  - config.json
```

<pre class="fragment-replacement fragment hljs" data-fragment-index="0"><div class="fragment fade-out" data-fragment-index="1"><code class="fragment" data-fragment-index="0">current => /var/www/releases/1563759803 # Point to the latest</code></div><code class="fragment fade-in" data-fragment-index="1">current => /var/www/releases/1563759802 # Point to the previous</code></pre>

Note:

For atomic deployments, our setup will look something like this: we have the last few releases stored in the `releases` directory, and anything that's shared is in `shared`.

We symlink the logs directory and config.json to each release as it's made, so they're all talking to a single copy of each file.

Then we update the `current` symlink to point to the release we want to make current. Our web root within nginx would be `/var/www/current`. If we needed to roll-back, we could update this symlink and be back to a previous release.

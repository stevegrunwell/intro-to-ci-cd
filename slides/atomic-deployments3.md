### Atomic Deployments

```yml
ship_to_production:
    stage: deploy
    script:
        # 1. Create + scp tarball
        # 2. Extract to /var/www/releases/{TIMESTAMP}
        # 3. Symlink shared assets
        # 4. Update the `current` symlink
        # 5. Reload the web server
        # 6. (Optional) Roll off older releases
```

<!-- .element: class="fragment" style="font-size: .86em;" --> [stevegrunwell.com/blog/atomic-deployments-from-scratch](https://stevegrunwell.com/blog/atomic-deployments-from-scratch/)

Note:

Deployment script is more complicated, probably a good idea to break it into a separate shell script in the repo.

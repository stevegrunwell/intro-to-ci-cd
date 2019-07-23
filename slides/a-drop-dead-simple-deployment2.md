### A drop-dead simple deployment:

```yml
ship_to_production:
    stage: deploy
    script:
        - tar -czf release.tgz dist/*
        - scp release.tgz "${SSH_USER}@${PRODUCTION_ADDR}:/tmp"
        - ssh "${SSH_USER}@${PRODUCTION_ADDR}" "cd /tmp \
          && tar -xzf release.tgz \
          && rsync release/ /var/www/html/ \
          "
```

### Environment Variables

![The "Environment Variables" configuration for GitLab's CI/CD pipelines](resources/environment-variables.png)

Note:

Storing pipeline configs in repo is great, but we don't want our secrets exposed there.

Instead, store them as environment variables for the CI/CD pipeline within GitLab.

Could include: API + deployment keys, SSH credentials, etc.

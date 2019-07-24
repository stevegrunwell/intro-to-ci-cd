### Environment Variables

![The "Environment Variables" configuration for GitLab's CI/CD pipelines](resources/environment-variables.png)

Note:

Storing pipeline configs in repo is great, but we don't want our secrets (API keys, database passwords, SSH keys, etc.) exposed there.

Instead, store them as environment variables for the CI/CD pipeline within GitLab.

Can also mask keys to keep them out of logs and/or only make them available to protected branches (e.g. master)

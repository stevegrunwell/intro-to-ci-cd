<!-- .slide: data-background-color="#fafafa" -->

### A Typical Pipeline

![A GitLab pipeline, describing 8 jobs across three stages (build, test, and deploy)](resources/pipeline.png)

Note:

Pretty typical pipeline for a Laravel app:

- Build stage where we install npm and composer dependencies
- Test stage: check coding standards, Jest for JS tests, PHPUnit for PHP unit and integration tests, and static code analysis via PHPStan
- Deploy stage: continuous deployment for staging, continuous delivery for production

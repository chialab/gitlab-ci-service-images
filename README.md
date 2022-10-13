<p align="center">
  <strong>Service Images for GitLab CI</strong>
</p>

<p align="center">
    <a href="https://github.com/chialab/gitlab-ci-service-images/actions/workflows/main.yml"><img alt="Build status" src="https://github.com/chialab/gitlab-ci-service-images/actions/workflows/main.yml/badge.svg"></a>
    <a href="https://www.chialab.it"><img alt="Authors link" src="https://img.shields.io/badge/Authors-Chialab-lightgrey.svg?style=flat-square"></a>
    <a href="https://github.com/chialab/gitlab-ci-service-images/blob/main/LICENSE"><img alt="License" src="https://img.shields.io/github/license/chialab/gitlab-ci-service-images.svg?style=flat-square"></a>
</p>

---

This repository stores commonly used Docker images, fixed for working within GitLab CI.

GitLab CI/CD pipelines fail to healthcheck service containers that expose more than one port,
like DinD and others (see [related](https://gitlab.com/gitlab-org/gitlab-runner/-/issues/4143) [issues](https://gitlab.com/gitlab-org/gitlab-runner/-/issues/3984)).

We fix that by building from `scratch` to remove exposed ports in upstream images,
and exposing only one port.

To copy original image's metadata (`ENV`, `ENTRYPOINT` and others) use `docker inspect`.

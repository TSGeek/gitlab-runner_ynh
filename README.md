<!--
N.B.: This README was automatically generated by https://github.com/YunoHost/apps/tree/master/tools/README-generator
It shall NOT be edited by hand.
-->

# GitLab Runner for YunoHost

[![Integration level](https://dash.yunohost.org/integration/gitlab-runner.svg)](https://dash.yunohost.org/appci/app/gitlab-runner) ![Working status](https://ci-apps.yunohost.org/ci/badges/gitlab-runner.status.svg) ![Maintenance status](https://ci-apps.yunohost.org/ci/badges/gitlab-runner.maintain.svg)  
[![Install GitLab Runner with YunoHost](https://install-app.yunohost.org/install-with-yunohost.svg)](https://install-app.yunohost.org/?app=gitlab-runner)

*[Lire ce readme en français.](./README_fr.md)*

> *This package allows you to install GitLab Runner quickly and simply on a YunoHost server.
If you don't have YunoHost, please consult [the guide](https://yunohost.org/#/install) to learn how to install it.*

## Overview

GitLab Runner is a continuous integration tool to use with a GitLab instance (YNH or not).


**Shipped version:** 15.6.0~ynh1

## Screenshots

![Screenshot of GitLab Runner](./doc/screenshots/ci-cd-test-deploy-illustration_2x.png)

## Disclaimers / important information

## Configuration

How to configure this app: by the admin panel of GitLab or the settings "CI/CD" of your project.

### System configuration

Running a Gitlab Runner mandates to choose [an executor](https://docs.gitlab.com/runner/executors/) at registeration time (when the Gitlab Runner instance registers to a Gitlab instance). For now this YunoHost application only supports the `docker` executor.

## Additional information

* To retrieve the information to be provided to the installation such as the `token` or the `gitlab's url` you must go here: `Settings->CI/CD->Runners->"Set up a specific Runner manually"` in the project or admin section of the GitLab instance to link to this runner.
* If you get this message during a job: `Could not resolve host: you.domain.tld`, you can add `dns_search = [“you.domain.tld”]` in the section `[[runners]]` section.

## Documentation and resources

* Official app website: <https://gitlab.com/gitlab-org/gitlab-runner>
* Official admin documentation: <https://docs.gitlab.com/runner/>
* Upstream app code repository: <https://gitlab.com/gitlab-org/gitlab-runner>
* YunoHost documentation for this app: <https://yunohost.org/app_gitlab-runner>
* Report a bug: <https://github.com/YunoHost-Apps/gitlab-runner_ynh/issues>

## Developer info

Please send your pull request to the [testing branch](https://github.com/YunoHost-Apps/gitlab-runner_ynh/tree/testing).

To try the testing branch, please proceed like that.

``` bash
sudo yunohost app install https://github.com/YunoHost-Apps/gitlab-runner_ynh/tree/testing --debug
or
sudo yunohost app upgrade gitlab-runner -u https://github.com/YunoHost-Apps/gitlab-runner_ynh/tree/testing --debug
```

**More info regarding app packaging:** <https://yunohost.org/packaging_apps>

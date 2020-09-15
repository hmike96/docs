---
title: Armory Cloud Compatability Matrix
linkTitle: Cloud Compatibility 
description: "Information about what Armory Cloud supports."
---

During the Early Access phase, Armory Cloud supports a subset of capabilities that the Armory Platform supports. New capability gets added as Armory iterates on Armory Cloud with design partners.

<!-- If you don't want to make markdown tables manually, use something like https://www.tablesgenerator.com/markdown_tables# 
Or you can write raw HTML :shrug: You might want to do that if you need to do bulleted lists etc inside of the table
Or a mixture of html + markdown. ## Deployment targets has an example of what this might look like
-->

## Legend
<!-- Copy and paste the below badges that apply to your area -->
<!-- Removing until we're out of MVP 
**Feature status** 

Armory releases software describes what state the feature is in and where you should install it. For more information, see [Release Definitions]({{< ref "release-definitions" >}}). You can also click the feature status badge directly.

[![Generally available](/images/ga.svg)]({{< ref "release-definitions#ga" >}}) The feature as a whole is generally available. There may be newer extended capability that is in a different state.

[![Early Access](/images/ea.svg)]({{< ref "release-definitions#early-release">}}) The feature is in Early Access.

[![Experiment](/images/exp.svg)]({{< ref "release-definitions#experiment">}}) The feature is an Experiment. -->

![new](/images/new-feature.svg) The feature is new. It either is available for the first time or underwent updates within the last 30 days.

**Versions**

For third-party software, **All supported versions** refers to any version of that software still actively supported by the vendor.

## Artifacts

Artifacts are  deployable resources.

### Stores

Armory supports the following artifact stores:

| Provider                                                           | Notes                                                               |
|--------------------------------------------------------------------|---------------------------------------------------------------------|
| [Bitbucket](https://spinnaker.io/setup/artifacts/bitbucket/)       |                                                                     |
| [GitHub](https://spinnaker.io/setup/artifacts/github/)             |                                                                     |
| [GitLab](https://spinnaker.io/setup/artifacts/gitlab/)             |                                                                     |
| [Git Repo](https://spinnaker.io/setup/artifacts/gitrepo/)          | GitHub or Bitbucket. Supports using the entire repo as an artifact. |
| [Google Cloud Storage](https://spinnaker.io/setup/artifacts/gcs/)  |                                                                     |
| [HTTP](https://spinnaker.io/setup/artifacts/http)                  |                                                                     |
| [Maven](https://spinnaker.io/setup/artifacts/maven/)               |                                                                     |
| [Oracle Object](https://spinnaker.io/setup/artifacts/oracle)       |                                                                     |
| [S3](https://spinnaker.io/setup/artifacts/s3/)                     |                                                                     |

### Types

Armory supports the following artifact types:

| Type                                                                                                              | Notes                                     |
|-------------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| [Bitbucket file](https://www.spinnaker.io/reference/artifacts-with-artifactsrewrite/types/bitbucket-file/)        |                                           |
| [Docker Image](https://spinnaker.io/reference/artifacts-with-artifactsrewrite/types/docker-image/)                | Can be hosted on DockerHub, GCR, ECR, etc |
| [Embedded Base64](https://spinnaker.io/reference/artifacts-with-artifactsrewrite/types/embedded-base64/)          |                                           |
| [GCS Object](https://www.spinnaker.io/reference/artifacts-with-artifactsrewrite/types/gcs-object/)                |                                           |
| [Git Repo](https://www.spinnaker.io/reference/artifacts-with-artifactsrewrite/types/git-repo/)                    |                                           |
| [GitHub file](https://www.spinnaker.io/reference/artifacts-with-artifactsrewrite/types/github-file/)              |                                           |
| [GitLab file](https://www.spinnaker.io/reference/artifacts-with-artifactsrewrite/types/gitlab-file/)              |                                           |
| [HTTP file](https://www.spinnaker.io/reference/artifacts-with-artifactsrewrite/types/http-file/)                  |                                           |
| [Kubernetes object](https://www.spinnaker.io/reference/artifacts-with-artifactsrewrite/types/kubernetes-object/)  |                                           |
| [Maven artifact](https://www.spinnaker.io/reference/artifacts-with-artifactsrewrite/types/maven-artifact/)        |                                           |
| [Oracle Object](https://www.spinnaker.io/reference/artifacts-with-artifactsrewrite/types/oracle-object/)          |                                           |
| [S3 object](https://www.spinnaker.io/reference/artifacts-with-artifactsrewrite/types/s3-object/)                  |                                           |

## Authentication

**Armory Cloud Console**

The following table lists the authentication protocols that Armory Cloud Console supports:

| Identity provider | Note |
|-------------------|------|
| Username/password |      |

**Spinnaker** 

The following table lists the authentication protocols that Spinnaker supports:

| Identity provider     | Note                                                                  |
|-----------------------|-----------------------------------------------------------------------|
| SAML                  |                                                                       |
| OAuth 2.0/OIDC        | Can use Auth0, Azure, GitHub, Google, Okta, OneLogin, or Oracle Cloud |
| LDAP/Active Directory |                                                                       |
| x509                  |                                                                       |

## Authorization

**Armory Cloud Console**

The following table lists the authorization protocols that Armory Cloud Console supports:

| Identity provider | Note |
|-------------------|------|
| Username/password |      |

**Spinnaker** 

The following table lists the authorization methods that Spinnaker supports:

| Provider              | Note                                                                            |
|------------------------|---------------------------------------------------------------------------------|
| GitHub Teams           | Roles from GitHub are mapped to the Teams under a specific GitHub organization. |
| Google Groups          |                                                                                 |
| LDAP/Active Directory  |                                                                                 |
| OAuth 2.0/OIDC         |                                                                                 |
| SAML                   |                                                                                 |

## Baking images

[![Generally available](/images/ga.svg)]({{< ref "release-definitions#ga" >}}) 

The following table lists the supported image bakeries:

| Provider  | Notes |
|-----------|-------|
| AWS       |       |
| GCE       |       |
| OCI       |       |
| Packer | Default image bakery for Spinnaker |


## Browsers

**Armory Cloud Console**

Armory Cloud Console works with most modern browsers.

**Spinnaker**

Spinnaker's UI (Deck) works with most modern browsers.

## Build (CI) systems

[![Generally available](/images/ga.svg)]({{< ref "release-definitions#ga" >}}) 

Connect your build system to Armory Cloud using the Armory Cloud Console. The following table lists supported build systems:

| Provider           | Version                 | Note                |
|--------------------|-------------------------|---------------------|
| AWS CodeBuild      | n/a                     |                     |
| GitHub Actions     | n/a                     | Webhook integration |
| Google Cloud Build | n/a                     |                     |
| Jenkins            | All supported versions  |                     |
| Travis             | All supported versions  |                     |
| Wercker            | All supported versions  |                     |

## Deployment targets

Connect your deployment targets to Armory Cloud using the Armory Cloud Console. The following table lists supported deployment targets.

| Provider   | Deployment target                                               | Deployment strategies | Notes                                               |
|------------|-----------------------------------------------------------------|-----------------------|-----------------------------------------------------|
| AWS        | ECS, EKS, S3, Cloudfront                                        |                       | EKS API must be accessible by public IPs for EKS deployments    |
| Kubernetes | Manifest-based deployments <ul><li>Versions A.B - X.Y</li></ul> |                       | Must be hosted on EC2 and accessible by public IPs |

## Manifest templating

The following table lists the supported manifest templating engines:

| Provider  | Notes                                |
|-----------|--------------------------------------|
| Helm 2    |                                      |
| Helm 3    |                                      |
| Kustomize | Kustomize version installed is 3.3.0 |

## Notifications

[![Generally available](/images/ga.svg)]({{< ref "release-definitions#ga" >}}) 

The following table lists the supported notification systems:

| Provider    | Notes |
|-------------|-------|
| Slack       |       |
| PagerDuty   |       |
| GitHub      |       |
| Jira        |       |
| BearyChat   |       |
| Email       |       |
| GoogleChat  |       |
| Twilio      |       |

## Pipeline triggers

[![Generally available](/images/ga.svg)]({{< ref "release-definitions#ga" >}}) 

The following table lists the supported pipeline triggers:

| Provider            | Notes |
|---------------------|-------|
| Artifactory         |       |
| AWS CodeBuild       |       |
| AWS Pub/Sub         |       |
| Cron                |       |
| Docker              |       |
| Git                 |       |
| GitHub Webhook      |       |
| Google Cloud Build  |       |
| Google Pub/Sub      |       |
| Jenkins Job         |       |
| Webhook             |       |
| Manual              |       |
| TravisCI Job        |       |
| Wercker             |       |
| Quay                |       |
| Nexus               |       |
| GitLab              |       |
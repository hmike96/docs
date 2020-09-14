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
**Feature status** 

Armory releases software describes what state the feature is in and where you should install it. For more information, see [Release Definitions]({{< ref "release-definitions" >}}). You can also click the feature status badge directly.

[![Generally available](/images/ga.svg)]({{< ref "release-definitions#ga" >}}) The feature as a whole is generally available. There may be newer extended capability that is in a different state.

[![Early Access](/images/ea.svg)]({{< ref "release-definitions#early-release">}}) The feature is in Early Access.

[![Experiment](/images/exp.svg)]({{< ref "release-definitions#experiment">}}) The feature is an Experiment.

![new](/images/new-feature.svg) The feature is new. It either is available for the first time or underwent updates within the last 30 days.

**Versions**

**All supported versions** for Armory refers to the current minor release and the two previous minor releases. For example, if the current Armory version is 2.21.x, all supported versions include 2.19.x, 2.20.x, and 2.21.x. For third-party software, **All supported versions** refers to any version of that software still actively supported by the vendor.

## Application metrics for Canary Analysis

[![Generally available](/images/ga.svg)]({{< ref "release-definitions#ga" >}}) 

Application metrics can be ingested by Kayenta to perform Canary Analysis or Automated Canary Analysis (ACA). The following table lists application metrics providers that Armory supports for metrics.

| Provider    | Version                | ACA | Note |
|-------------|------------------------|-----|------|
| Graphite    | All supported versions | Yes |      |
| New Relic   | All supported versions | Yes |      |
| Prometheus  | All supported versions | Yes |      |
| SignalFx    | All supported versions | Yes |      |
| Stackdriver | All supported versions | Yes |      |

## Artifacts

Artifacts are  deployable resources.

### Stores

[![Generally available](/images/ga.svg)]({{< ref "release-definitions#ga" >}})  

Armory supports the following artifact stores:

| Provider                                                          | Armory                 | Notes                                                               |
|-------------------------------------------------------------------|------------------------|---------------------------------------------------------------------|
| [Bitbucket](https://spinnaker.io/setup/artifacts/bitbucket/)      | All supported versions |                                                                     |
| [GitHub](https://spinnaker.io/setup/artifacts/github/)            | All supported versions |                                                                     |
| [GitLab](https://spinnaker.io/setup/artifacts/gitlab/)            | All supported versions |                                                                     |
| [Git Repo](https://spinnaker.io/setup/artifacts/gitrepo/)         | All supported versions | GitHub or Bitbucket. Supports using the entire repo as an artifact. |
| [Google Cloud Storage](https://spinnaker.io/setup/artifacts/gcs/) | All supported versions |                                                                     |
| [HTTP](https://spinnaker.io/setup/artifacts/http)                 | All supported versions |                                                                     |
| [Maven](https://spinnaker.io/setup/artifacts/maven/)              | All supported versions |                                                                     |
| [Oracle Object](https://spinnaker.io/setup/artifacts/oracle)      | All supported versions |                                                                     |
| [S3](https://spinnaker.io/setup/artifacts/s3/)                    | All supported versions |                                                                     |

### Types

Armory supports the following artifact types:

| Type                                                                                                             | Armory                 | Notes                                     |
|------------------------------------------------------------------------------------------------------------------|------------------------|-------------------------------------------|
| [Bitbucket file](https://www.spinnaker.io/reference/artifacts-with-artifactsrewrite/types/bitbucket-file/)       | All supported versions |                                           |
| [Docker Image](https://spinnaker.io/reference/artifacts-with-artifactsrewrite/types/docker-image/)               | All supported versions | Can be hosted on DockerHub, GCR, ECR, etc |
| [Embedded Base64](https://spinnaker.io/reference/artifacts-with-artifactsrewrite/types/embedded-base64/)         | All supported versions |                                           |
| [GCS Object](https://www.spinnaker.io/reference/artifacts-with-artifactsrewrite/types/gcs-object/)               | All supported versions |                                           |
| [Git Repo](https://www.spinnaker.io/reference/artifacts-with-artifactsrewrite/types/git-repo/)                   | All supported versions |                                           |
| [GitHub file](https://www.spinnaker.io/reference/artifacts-with-artifactsrewrite/types/github-file/)             | All supported versions |                                           |
| [GitLab file](https://www.spinnaker.io/reference/artifacts-with-artifactsrewrite/types/gitlab-file/)             | All supported versions |                                           |
| [HTTP file](https://www.spinnaker.io/reference/artifacts-with-artifactsrewrite/types/http-file/)                 | All supported versions |                                           |
| [Kubernetes object](https://www.spinnaker.io/reference/artifacts-with-artifactsrewrite/types/kubernetes-object/) | All supported versions |                                           |
| [Maven artifact](https://www.spinnaker.io/reference/artifacts-with-artifactsrewrite/types/maven-artifact/)       | All supported versions |                                           |
| [Oracle Object](https://www.spinnaker.io/reference/artifacts-with-artifactsrewrite/types/oracle-object/)         | All supported versions |                                           |
| [S3 object](https://www.spinnaker.io/reference/artifacts-with-artifactsrewrite/types/s3-object/)                 | All supported versions |                                           |

## As code solutions

### Pipelines as Code

[![Generally available](/images/ga.svg)]({{< ref "release-definitions#ga" >}}) 

[Pipelines as Code]({{< ref "install-dinghy" >}}) gives you the ability to manage your pipelines and their templates in source control.

**Supported version control systems**

| Feature          | Version                      | Notes                     |
|------------------|------------------------------|---------------------------|
| BitBucket Cloud  |                              |                           |
| BitBucket Server | Previous two major versions  |                           |
| GitHub           |                              | Enterprise and GitHub.com |
| GitLab           |                              |                           |

**Features**

| Feature                                                                           | Notes                                                                 |
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| Modules                                                                           | Templatize and re-use pipeline snippets across applications and teams |
| Slack notifications                                                               |                                                                       |
| Fiat service account integration                                                  |                                                                       |
| Webhook secret validation                                                         |                                                                       |
| Local modules for development                                                     |                                                                       |
| [Pull Request Validation]({{< ref "install-dinghy#pull-request-validations" >}})  |                                                                       |

### Pipelines as CRD

[![Experiment](/images/exp.svg)]({{< ref "release-definitions#experiment">}}) 

[PaCRD]({{< ref "pacrd" >}}) gives you the ability to manage your pipelines as
Kubernetes custom resources.

| Feature                                              | Notes                                                      |
|------------------------------------------------------|------------------------------------------------------------|
| Create, modify, and delete pipeline manifests        | Working within the same cluster Spinnaker is installed in. |
| Create, modify, and delete application manifests     | Working within the same cluster Spinnaker is installed in. |
| Define all stages supported by Spinnaker and Armory  | Validation support does not exist for all stages.          |

### Terraform Integration

[![Generally available](/images/ga.svg)]({{< ref "release-definitions#ga" >}}) 

The Terraform Integration gives you the ability to use Terraform within your Spinnaker pipelines to create your infrastructure as part of your software delivery pipeline.

**Supported Terraform versions**

| Terraform Versions    | Note                                                                  |
|-----------------------|------------------------|-----------------------------------------------------------------------|
| 0.11.10 - 0.11.14     |                                                                        |
| 0.12.0 - 0.12.24      |                                                                        |
  
**Features**

| Feature                                                                                         | Notes |
|-------------------------------------------------------------------------------------------------|-------|
| [Base Terraform Integration]({{< ref "terraform-enable-integration" >}})                        |       |
| [Named Profiles with authorization]({{< ref "terraform-enable-integration#named-profiles" >}})  |       |

## Authentication

**Armory Cloud Console**

[![Early Access](/images/ea.svg)]({{< ref "release-definitions#early-release">}}) The feature is in Early Access.

The following table lists the authentication protocols that the Armory Cloud Console supports:

| Identity provider | Note |
|-------------------|------|
| Username/password |      |

**Spinnaker** 

[![Generally available](/images/ga.svg)]({{< ref "release-definitions#ga" >}}) 

The following table lists the authentication protocols that Spinnaker supports:

| Identity provider     | Note                                                                  |
|-----------------------|-----------------------------------------------------------------------|
| SAML                  |                                                                       |
| OAuth 2.0/OIDC        | Can use Auth0, Azure, GitHub, Google, Okta, OneLogin, or Oracle Cloud |
| LDAP/Active Directory |                                                                       |
| x509                  |                                                                       |

## Authorization

[![Generally available](/images/ga.svg)]({{< ref "release-definitions#ga" >}}) 

The following table lists the authorization methods that Armory supports:

| Provider              | Note                                                                            |
|------------------------|---------------------------------------------------------------------------------|
| GitHub Teams           | Roles from GitHub are mapped to the Teams under a specific GitHub organization. |
| Google Groups          |                                                                                 |
| LDAP/Active Directory  |                                                                                 |
| OAuth 2.0/OIDC         |                                                                                 |
| SAML                   |                                                                                 |

## Baking images

[![Generally available](/images/ga.svg)]({{< ref "release-definitions#ga" >}}) 

Armory supports baking images in multiple providers

| Provider  | Notes |
|-----------|-------|
| AWS       |       |
| GCE       |       |
| OCI       |       |


## Browsers

**Armory Cloud Console**

Armory Cloud Console works with most modern browsers.

**Spinnaker**

Spinnaker's UI (Deck) works with most modern browsers.

## Build systems

[![Generally available](/images/ga.svg)]({{< ref "release-definitions#ga" >}}) 

The following table lists the CI systems that Armory supports:

| Provider           | Version                 | Note                |
|--------------------|-------------------------|---------------------|
| AWS CodeBuild      | n/a                     |                     |
| GitHub Actions     | n/a                     | Webhook integration |
| Google Cloud Build | n/a                     |                     |
| Jenkins            | All supported versions  |                     |
| Travis             | All supported versions  |                     |
| Wercker            | All supported versions  |                     |

## Deployment targets

[![Early Access](/images/ea.svg)]({{< ref "release-definitions#early-release">}}) 

Armory Cloud supports the following deployment targets:

| Provider   | Deployment target                                               | Deployment strategies | Notes                                               |
|------------|-----------------------------------------------------------------|-----------------------|-----------------------------------------------------|
| AWS        | ECS, EKS, S3, Cloudfront                                        |                       | EKS API must be accessible by public IPs for EKS deployments    |
| Kubernetes | Manifest-based deployments <ul><li>Versions A.B - X.Y</li></ul> |                       | Must be hosted on EC2 and accesssible by public IPs |

## Notifications

[![Generally available](/images/ga.svg)]({{< ref "release-definitions#ga" >}}) 

The following table lists the notification systems that Armory supports:

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

Armory supports using the following methods to trigger Spinnaker pipelines:

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

## Secret stores

[![Generally available](/images/ga.svg)]({{< ref "release-definitions#ga" >}}) 

{{% alert title="Note" %}} This section applies to secrets in configuration files, not ap- secrets. {{% /alert %}}

The following table lists the secret stores that Armory supports for referencing secrets in config files securely:

| Provider                                               | Notes |
|--------------------------------------------------------|-------|
| [AWS Secrets Manager]({{< ref "secrets-aws-sm" >}})    |       |
| [Encrypted GCS Bucket]({{< ref "secrets-gcs" >}})      |       |
| [Encrypted S3 Bucket]({{< ref "secrets-s3" >}})        |       |
| [Kubernetes secrets]({{< ref "secrets-kubernetes" >}}) |       |
| [Vault]({{< ref "secrets-vault" >}})                   |       |

## Templating manifests

[![Generally available](/images/ga.svg)]({{< ref "release-definitions#ga" >}}) 

Armory supporting Templating Manifests

| Provider  | Notes                                |
|-----------|--------------------------------------|
| Helm 2    |                                      |
| Helm 3    |                                      |
| Kustomize | Kustomize version installed is 3.3.0 |

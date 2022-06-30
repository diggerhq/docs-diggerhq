# Frequently Asked Questions



#### General

* What can I deploy with digger?
  * You can deploy any containerized applications using digger - all you need is a Dockerfile. We are also working on support for web apps, lambda functions and other popular frameworks. If you need help deploying your favorite language you can ask on our [slack channel](https://join.slack.com/t/diggertalk/shared\_invite/zt-yx6rua03-6z\~g\~\_RF3y5LTAK2Bu\_yOA).
* Is digger secure?
  * We take security very seriously.
  * If you discover any vulnerabilities in digger please email security@digger.dev
  * **Do not report vulnerabilities using public GitHub issues**
  * If you discover any vulnerabilities in digger please email security@digger.dev
* How do you import existing resources from AWS to digger?
  * Currently, we do not support importing existing resources from AWS to Digger by using the self-service platform
  * If you need help, contact our team and we will do our best to help you move over to our platform. You can drop us questions on [slack](https://join.slack.com/t/diggertalk/shared\_invite/zt-yx6rua03-6z\~g\~\_RF3y5LTAK2Bu\_yOA).

#### Security

* How will my secrets be stored?
  * We try to store as fewer secrets as possible every step of the way. For the actual storage we use highly secure AWS managed service (AWS Systems Manager Parameter Store). When you use application secrets they are stored on your account and they are never accessible from digger.
* What is the difference between secrets and env vars?
  * Secrets contain sensitive information, like passwords, that cannot be accessed easily and usually require infrastructure to read, store and manage them.
  * Environment variables are values that processes like containers, web service, scripts etc. access to control their own behaviour. They are accessible to anyone and anything that also have access to those processes, meaning that they aren’t secure. Don’t pass sensitive information via environment variables, use secrets instead.
*

#### Pricing

* How much will digger cost me ?
  * Digger changes a fixed price based on user count.
  * The other costs for running your infrastructure will be charged directly by AWS and can be covered by free credits provided by AWS.
  * We do our best to deploy the cheapest infrastructure to meet your need, so you never need to worry about ballooning costs.

#### Support

* **Do you offer support?**
  * Absolutely - you can drop us questions on [slack](https://join.slack.com/t/diggertalk/shared\_invite/zt-yx6rua03-6z\~g\~\_RF3y5LTAK2Bu\_yOA).
* I want to use digger for my business how do I get in touch for a demo?
  * Excellent! You are joining hundreds of happy companies using digger. Please email sales@digger.dev to request a demo. Or you can drop us questions on [slack](https://join.slack.com/t/diggertalk/shared\_invite/zt-yx6rua03-6z\~g\~\_RF3y5LTAK2Bu\_yOA).

#### Tech

* Can we do multiple account connection with digger?
  * Yes, you can create as many account connections as you wish.
* What is the difference between 2 ways of connection AWS account?
  * Our default option for connecting your AWS account to our platform is to use the keyless connection which will allow us to deploy resources on your AWS account without handling any sensitive data related to your account.
  * The option to connect using AWS keys is our legacy option. It allows you to connect your AWS account using using keys, which are later stored as secrets on your account. Since this option is legacy at this point, we cannot guarantee for how long we will support this option
* Do you support Pulumi or CDK or cloudformation?
  * Only terraform is supported currently. We do have plans to support other IaC tools in future. If you have a specific use-case you can tell us about it on [slack](https://join.slack.com/t/diggertalk/shared\_invite/zt-yx6rua03-6z\~g\~\_RF3y5LTAK2Bu\_yOA).
* Do you also support GCP, Azure or Digital Ocean?
  * We do have plans to support other cloud providers in the near future.
* What regions does digger support?
  * Digger supports all regions which AWS supports.

#### Misc

* Do I need to know docker to use digger?
  * Basic knowledge of docker is needed to deploy containers using Digger
* Do I need to know AWS to use digger?
  * Only enough to register an account on AWS
  * We do our best that you never need to return to AWS console after that.
* I got an error what do I do ?
  * For most cases, you individual step logs are available on the activity screen, that would help you to get to the bottom of the issue.
  * In case the logs are now available, contact our team, we will assist you with resolving the error.
* Is Digger production ready?
  * We run production infrastructure for a number of companies.

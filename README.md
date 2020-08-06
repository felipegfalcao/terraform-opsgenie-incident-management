# terraform-opsgenie-incident-management

 [![Latest Release](https://img.shields.io/github/release/cloudposse/terraform-opsgenie-incident-management.svg)](https://github.com/cloudposse/terraform-opsgenie-incident-management/releases/latest) [![Slack Community](https://slack.cloudposse.com/badge.svg)](https://slack.cloudposse.com) [![Discourse Forum](https://img.shields.io/discourse/https/ask.sweetops.com/posts.svg)](https://ask.sweetops.com/)

[![README Header][readme_header_img]][readme_header_link]

[![Cloud Posse][logo]](https://cpco.io/homepage)

<!--




  ** DO NOT EDIT THIS FILE
  **
  ** This file was automatically generated by the `build-harness`.
  ** 1) Make all changes to `README.yaml`
  ** 2) Run `make init` (you only need to do this once)
  ** 3) Run`make readme` to rebuild this file.
  **
  ** (We maintain HUNDREDS of open source projects. This is how we maintain our sanity.)
  **





-->

Terraform module to provision Opsgenie resources using the Opsgenie provider. The provider needs to be configured with the proper credentials before it can be used.
It consist of root module which is only here as an example. Mainly this repository should be used as a set of terraform submodules which can be combined in more complex modules.


---

This project is part of our comprehensive ["SweetOps"](https://cpco.io/sweetops) approach towards DevOps.
[<img align="right" title="Share via Email" src="https://docs.cloudposse.com/images/ionicons/ios-email-outline-2.0.1-16x16-999999.svg"/>][share_email]
[<img align="right" title="Share on Google+" src="https://docs.cloudposse.com/images/ionicons/social-googleplus-outline-2.0.1-16x16-999999.svg" />][share_googleplus]
[<img align="right" title="Share on Facebook" src="https://docs.cloudposse.com/images/ionicons/social-facebook-outline-2.0.1-16x16-999999.svg" />][share_facebook]
[<img align="right" title="Share on Reddit" src="https://docs.cloudposse.com/images/ionicons/social-reddit-outline-2.0.1-16x16-999999.svg" />][share_reddit]
[<img align="right" title="Share on LinkedIn" src="https://docs.cloudposse.com/images/ionicons/social-linkedin-outline-2.0.1-16x16-999999.svg" />][share_linkedin]
[<img align="right" title="Share on Twitter" src="https://docs.cloudposse.com/images/ionicons/social-twitter-outline-2.0.1-16x16-999999.svg" />][share_twitter]


[![Terraform Open Source Modules](https://docs.cloudposse.com/images/terraform-open-source-modules.svg)][terraform_modules]



It's 100% Open Source and licensed under the [APACHE2](LICENSE).







We literally have [*hundreds of terraform modules*][terraform_modules] that are Open Source and well-maintained. Check them out!






## Introduction

Available modules:
- [Alert Policy](modules/alert_policy)
- [API Integration](modules/api_integration)
- [Escalation](modules/escalation)
- [Notification Policy](modules/notification_policy)
- [Team](modules/team)
- [Team Routing Rule](modules/team_routing_rule)

**Note:** Root module is just an example that uses all of submodules.

## Usage


**IMPORTANT:** The `master` branch is used in `source` just as an example. In your code, do not pin to `master` because there may be breaking changes between releases.
Instead pin to the release tag (e.g. `?ref=tags/x.y.z`) of one of our [latest releases](https://github.com/cloudposse/terraform-opsgenie-incident-management/releases).


Here's how to invoke `team` module in your projects

```hcl
module "team-name" {
  source = "git::https://github.com/cloudposse/terraform-opsgenie-incident-management.git//modules/team?ref=master"

  provider_api_key = var.opsgenie_provider_api_key

  team = {
    name        = "team-name"
    description = "team-description"
  }

}
```




## Examples

Here is an example of using all submodules:
- [`examples/complete`](https://github.com/cloudposse/terraform-opsgenie-incident-management/examples/complete) - complete example of using this module

Submodules examples:
- [`alert_policy`](https://github.com/cloudposse/terraform-opsgenie-incident-management/examples/alert_policy)
- [`api_integration`](https://github.com/cloudposse/terraform-opsgenie-incident-management/examples/api_integration)
- [`escalation`](https://github.com/cloudposse/terraform-opsgenie-incident-management/examples/escalation)
- [`notification_policy`](https://github.com/cloudposse/terraform-opsgenie-incident-management/examples/notification_policy)
- [`team`](https://github.com/cloudposse/terraform-opsgenie-incident-management/examples/team)
- [`team_routing_rule`](https://github.com/cloudposse/terraform-opsgenie-incident-management/examples/team_routing_rule)



<!-- markdownlint-disable -->
## Makefile Targets
```text
Available targets:

  help                                Help screen
  help/all                            Display help for all targets
  help/short                          This help short screen
  lint                                Lint terraform code

```
<!-- markdownlint-restore -->
## Requirements

| Name | Version |
|------|---------|
| terraform | >= 0.12.0, < 0.14.0 |
| opsgenie | ~> 0.4 |

## Providers

No provider.

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| alert\_policy | This variable is used to configure Opsgenie Alert Policy. | `map` | `{}` | no |
| api\_integration | This variable is used to configure Opsgenie API Integration. | `map` | `{}` | no |
| attributes | Additional attributes (\_e.g.\_ "1") | `list(string)` | `[]` | no |
| delimiter | Delimiter between `namespace`, `stage`, `name` and `attributes` | `string` | `"-"` | no |
| enabled | Set to false to prevent the module from creating any resources | `bool` | `true` | no |
| escalation | This variable is used to configure Opsgenie Escalation. | `map` | `{}` | no |
| name | Name of the application | `string` | n/a | yes |
| namespace | Namespace (e.g. `eg` or `cp`) | `string` | `""` | no |
| notification\_policy | This variable is used to configure Opsgenie Notification Policy. | `map` | `{}` | no |
| opsgenie\_provider\_api\_key | The API Key for the Opsgenie Integration. If omitted, the OPSGENIE\_API\_KEY environment variable is used. | `string` | `""` | no |
| region | AWS region | `string` | n/a | yes |
| stage | Stage (e.g. `prod`, `dev`, `staging`) | `string` | `""` | no |
| tags | Additional tags (\_e.g.\_ { BusinessUnit : ABC }) | `map(string)` | `{}` | no |
| team | This variable is used to configure Opsgenie Team. | `map` | `{}` | no |
| team\_routing\_rule | This variable is used to configure Opsgenie Team Routing Rule. | `map` | `{}` | no |

## Outputs

No output.




## Share the Love

Like this project? Please give it a ★ on [our GitHub](https://github.com/cloudposse/terraform-opsgenie-incident-management)! (it helps us **a lot**)

Are you using this project or any of our other projects? Consider [leaving a testimonial][testimonial]. =)


## Related Projects

Check out these related projects.

- [terraform-datadog-monitor](https://github.com/cloudposse/terraform-datadog-monitor) - Terraform module to provision Standard System Monitors (cpu, memory, swap, io, etc) in Datadog




## References

For additional context, refer to some of these links.

- [Opsgenie API Overview](https://docs.opsgenie.com/docs/api-overview) - Opsgenie APIs give you interconnectivity to process your requests and access data. View our individual documentation for our APIs to see the methods used to process relevant requests. Action-specific instructions are included to help you complete requests, along with sample requests and responses for added guidance. Additionally, view our Rate Limiting section for specific details and configurations.
- [Terraform Registry Opsgenie Provider documentation](https://registry.terraform.io/providers/opsgenie/opsgenie/latest/docs) - The Opsgenie provider is used to interact with the many resources supported by Opsgenie. The provider needs to be configured with the proper credentials before it can be used.
- [Github Terraform OpsGenie provider repository](https://github.com/opsgenie/terraform-provider-opsgenie/) - The Opsgenie provider is used to interact with the many resources supported by Opsgenie. The provider needs to be configured with the proper credentials before it can be used.


## Help

**Got a question?** We got answers.

File a GitHub [issue](https://github.com/cloudposse/terraform-opsgenie-incident-management/issues), send us an [email][email] or join our [Slack Community][slack].

[![README Commercial Support][readme_commercial_support_img]][readme_commercial_support_link]

## DevOps Accelerator for Startups


We are a [**DevOps Accelerator**][commercial_support]. We'll help you build your cloud infrastructure from the ground up so you can own it. Then we'll show you how to operate it and stick around for as long as you need us.

[![Learn More](https://img.shields.io/badge/learn%20more-success.svg?style=for-the-badge)][commercial_support]

Work directly with our team of DevOps experts via email, slack, and video conferencing.

We deliver 10x the value for a fraction of the cost of a full-time engineer. Our track record is not even funny. If you want things done right and you need it done FAST, then we're your best bet.

- **Reference Architecture.** You'll get everything you need from the ground up built using 100% infrastructure as code.
- **Release Engineering.** You'll have end-to-end CI/CD with unlimited staging environments.
- **Site Reliability Engineering.** You'll have total visibility into your apps and microservices.
- **Security Baseline.** You'll have built-in governance with accountability and audit logs for all changes.
- **GitOps.** You'll be able to operate your infrastructure via Pull Requests.
- **Training.** You'll receive hands-on training so your team can operate what we build.
- **Questions.** You'll have a direct line of communication between our teams via a Shared Slack channel.
- **Troubleshooting.** You'll get help to triage when things aren't working.
- **Code Reviews.** You'll receive constructive feedback on Pull Requests.
- **Bug Fixes.** We'll rapidly work with you to fix any bugs in our projects.

## Slack Community

Join our [Open Source Community][slack] on Slack. It's **FREE** for everyone! Our "SweetOps" community is where you get to talk with others who share a similar vision for how to rollout and manage infrastructure. This is the best place to talk shop, ask questions, solicit feedback, and work together as a community to build totally *sweet* infrastructure.

## Discourse Forums

Participate in our [Discourse Forums][discourse]. Here you'll find answers to commonly asked questions. Most questions will be related to the enormous number of projects we support on our GitHub. Come here to collaborate on answers, find solutions, and get ideas about the products and services we value. It only takes a minute to get started! Just sign in with SSO using your GitHub account.

## Newsletter

Sign up for [our newsletter][newsletter] that covers everything on our technology radar.  Receive updates on what we're up to on GitHub as well as awesome new projects we discover.

## Office Hours

[Join us every Wednesday via Zoom][office_hours] for our weekly "Lunch & Learn" sessions. It's **FREE** for everyone!

[![zoom](https://img.cloudposse.com/fit-in/200x200/https://cloudposse.com/wp-content/uploads/2019/08/Powered-by-Zoom.png")][office_hours]

## Contributing

### Bug Reports & Feature Requests

Please use the [issue tracker](https://github.com/cloudposse/terraform-opsgenie-incident-management/issues) to report any bugs or file feature requests.

### Developing

If you are interested in being a contributor and want to get involved in developing this project or [help out](https://cpco.io/help-out) with our other projects, we would love to hear from you! Shoot us an [email][email].

In general, PRs are welcome. We follow the typical "fork-and-pull" Git workflow.

 1. **Fork** the repo on GitHub
 2. **Clone** the project to your own machine
 3. **Commit** changes to your own branch
 4. **Push** your work back up to your fork
 5. Submit a **Pull Request** so that we can review your changes

**NOTE:** Be sure to merge the latest changes from "upstream" before making a pull request!



## Copyrights

Copyright © 2020-2020 [Cloud Posse, LLC](https://cloudposse.com)





## License

[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)

See [LICENSE](LICENSE) for full details.

```text
Licensed to the Apache Software Foundation (ASF) under one
or more contributor license agreements.  See the NOTICE file
distributed with this work for additional information
regarding copyright ownership.  The ASF licenses this file
to you under the Apache License, Version 2.0 (the
"License"); you may not use this file except in compliance
with the License.  You may obtain a copy of the License at

  https://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing,
software distributed under the License is distributed on an
"AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY
KIND, either express or implied.  See the License for the
specific language governing permissions and limitations
under the License.
```









## Trademarks

All other trademarks referenced herein are the property of their respective owners.

## About

This project is maintained and funded by [Cloud Posse, LLC][website]. Like it? Please let us know by [leaving a testimonial][testimonial]!

[![Cloud Posse][logo]][website]

We're a [DevOps Professional Services][hire] company based in Los Angeles, CA. We ❤️  [Open Source Software][we_love_open_source].

We offer [paid support][commercial_support] on all of our projects.

Check out [our other projects][github], [follow us on twitter][twitter], [apply for a job][jobs], or [hire us][hire] to help with your cloud strategy and implementation.



### Contributors

|  [![Marcin Brański][3h4x_avatar]][3h4x_homepage]<br/>[Marcin Brański][3h4x_homepage] |
|---|

  [3h4x_homepage]: https://github.com/3h4x
  [3h4x_avatar]: https://img.cloudposse.com/150x150/https://github.com/3h4x.png

[![README Footer][readme_footer_img]][readme_footer_link]
[![Beacon][beacon]][website]

  [logo]: https://cloudposse.com/logo-300x69.svg
  [docs]: https://cpco.io/docs?utm_source=github&utm_medium=readme&utm_campaign=cloudposse/terraform-opsgenie-incident-management&utm_content=docs
  [website]: https://cpco.io/homepage?utm_source=github&utm_medium=readme&utm_campaign=cloudposse/terraform-opsgenie-incident-management&utm_content=website
  [github]: https://cpco.io/github?utm_source=github&utm_medium=readme&utm_campaign=cloudposse/terraform-opsgenie-incident-management&utm_content=github
  [jobs]: https://cpco.io/jobs?utm_source=github&utm_medium=readme&utm_campaign=cloudposse/terraform-opsgenie-incident-management&utm_content=jobs
  [hire]: https://cpco.io/hire?utm_source=github&utm_medium=readme&utm_campaign=cloudposse/terraform-opsgenie-incident-management&utm_content=hire
  [slack]: https://cpco.io/slack?utm_source=github&utm_medium=readme&utm_campaign=cloudposse/terraform-opsgenie-incident-management&utm_content=slack
  [linkedin]: https://cpco.io/linkedin?utm_source=github&utm_medium=readme&utm_campaign=cloudposse/terraform-opsgenie-incident-management&utm_content=linkedin
  [twitter]: https://cpco.io/twitter?utm_source=github&utm_medium=readme&utm_campaign=cloudposse/terraform-opsgenie-incident-management&utm_content=twitter
  [testimonial]: https://cpco.io/leave-testimonial?utm_source=github&utm_medium=readme&utm_campaign=cloudposse/terraform-opsgenie-incident-management&utm_content=testimonial
  [office_hours]: https://cloudposse.com/office-hours?utm_source=github&utm_medium=readme&utm_campaign=cloudposse/terraform-opsgenie-incident-management&utm_content=office_hours
  [newsletter]: https://cpco.io/newsletter?utm_source=github&utm_medium=readme&utm_campaign=cloudposse/terraform-opsgenie-incident-management&utm_content=newsletter
  [discourse]: https://ask.sweetops.com/?utm_source=github&utm_medium=readme&utm_campaign=cloudposse/terraform-opsgenie-incident-management&utm_content=discourse
  [email]: https://cpco.io/email?utm_source=github&utm_medium=readme&utm_campaign=cloudposse/terraform-opsgenie-incident-management&utm_content=email
  [commercial_support]: https://cpco.io/commercial-support?utm_source=github&utm_medium=readme&utm_campaign=cloudposse/terraform-opsgenie-incident-management&utm_content=commercial_support
  [we_love_open_source]: https://cpco.io/we-love-open-source?utm_source=github&utm_medium=readme&utm_campaign=cloudposse/terraform-opsgenie-incident-management&utm_content=we_love_open_source
  [terraform_modules]: https://cpco.io/terraform-modules?utm_source=github&utm_medium=readme&utm_campaign=cloudposse/terraform-opsgenie-incident-management&utm_content=terraform_modules
  [readme_header_img]: https://cloudposse.com/readme/header/img
  [readme_header_link]: https://cloudposse.com/readme/header/link?utm_source=github&utm_medium=readme&utm_campaign=cloudposse/terraform-opsgenie-incident-management&utm_content=readme_header_link
  [readme_footer_img]: https://cloudposse.com/readme/footer/img
  [readme_footer_link]: https://cloudposse.com/readme/footer/link?utm_source=github&utm_medium=readme&utm_campaign=cloudposse/terraform-opsgenie-incident-management&utm_content=readme_footer_link
  [readme_commercial_support_img]: https://cloudposse.com/readme/commercial-support/img
  [readme_commercial_support_link]: https://cloudposse.com/readme/commercial-support/link?utm_source=github&utm_medium=readme&utm_campaign=cloudposse/terraform-opsgenie-incident-management&utm_content=readme_commercial_support_link
  [share_twitter]: https://twitter.com/intent/tweet/?text=terraform-opsgenie-incident-management&url=https://github.com/cloudposse/terraform-opsgenie-incident-management
  [share_linkedin]: https://www.linkedin.com/shareArticle?mini=true&title=terraform-opsgenie-incident-management&url=https://github.com/cloudposse/terraform-opsgenie-incident-management
  [share_reddit]: https://reddit.com/submit/?url=https://github.com/cloudposse/terraform-opsgenie-incident-management
  [share_facebook]: https://facebook.com/sharer/sharer.php?u=https://github.com/cloudposse/terraform-opsgenie-incident-management
  [share_googleplus]: https://plus.google.com/share?url=https://github.com/cloudposse/terraform-opsgenie-incident-management
  [share_email]: mailto:?subject=terraform-opsgenie-incident-management&body=https://github.com/cloudposse/terraform-opsgenie-incident-management
  [beacon]: https://ga-beacon.cloudposse.com/UA-76589703-4/cloudposse/terraform-opsgenie-incident-management?pixel&cs=github&cm=readme&an=terraform-opsgenie-incident-management

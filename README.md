# Awesome-Continuous-Integration-Deployment-CI-CD

# Awesome-Continuous-Integration-Deployment-CI-CD

**Top Continuous Integration Deployment CI CD (Opensource) 🌟 Star if you like it! 🌟**



**Curated List of SaaS Products & Open-Source GitHub Projects**

*Focused on Pipeline Orchestration, GitOps Delivery, Self-Hosted Runners & Container-Native Builds*

**Last updated: November 2026**



This repository tracks notable **SaaS platforms** and **open-source projects** for **Continuous Integration & Deployment (CI/CD)**. These tools enable teams to automate building, testing, and deploying software—from fully managed cloud pipelines with deep Git integration to self-hosted runners and Kubernetes-native GitOps controllers that give organizations complete control over their delivery infrastructure.



**Examples** include GitHub Actions, GitLab CI/CD, Jenkins, CircleCI, Travis CI, Bamboo, TeamCity, Argo CD, Bitrise, and Codefresh (the category leaders in commercial and open-source space).



**Open-source emphasis**: This section is expanded with every relevant project for self-hosted CI/CD, container-native pipelines, and open GitOps infrastructure. **Critical note**: The open-source CI/CD landscape is mature and deeply fragmented—**Jenkins** remains the most extensible with 1,800+ plugins, **Argo CD** dominates GitOps continuous delivery for Kubernetes, **Tekton** provides the vendor-neutral cloud-native framework, and **Woodpecker CI** offers the lightest self-hosted footprint. No single open-source tool matches GitHub Actions' marketplace ecosystem, but for self-hosted control and GitOps workflows, the options are production-proven at scale.



Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.



## Table of Contents

- [Sector Overview & Market Dynamics](#sector-overview--market-dynamics)

- [SaaS/Hosted Platforms](#saas-hosted-platforms)

- [Open-Source GitHub Projects](#open-source-github-projects)

- [How to Contribute](#how-to-contribute)

- [Disclaimer](#disclaimer)



## Sector Overview & Market Dynamics

The global Continuous Integration and Continuous Delivery (CI/CD) and pipeline automation market is estimated at **$1.7B to $2.1B** for core CI/CD tools, scaling up to **$5.7B to $13.2B** across the broader DevOps delivery toolchain, expanding at a ~14% to 20% CAGR. The sector is **moderately to highly fragmented** rather than winner-take-all—while hyperscale ecosystems (e.g. GitHub Actions, GitLab) drive platform consolidation, specialized needs across mobile builds, Kubernetes GitOps, enterprise compliance, and self-hosted/hybrid infrastructure sustain a diverse, multi-tool landscape.

## SaaS/Hosted Platforms

| Platform | Company Valuation / Revenue | Starting Price | Free Tier Limits | Focus / Best For | Trade-offs |
|:---|:---|:---|:---|:---|:---|
| **[GitHub Actions](https://github.com/features/actions)** | Microsoft (Market Cap: ~$3.9T; GitHub ARR: ~$2B+) | $4/user/month (Team plan; Free plan available) | Free for public repos (unlimited minutes); 2,000 Linux build minutes/month for private repos | Native GitHub workflows, massive community actions ecosystem | Vendor lock-in to GitHub; minute consumption costs escalate on macOS/Windows |
| **[Bamboo](https://www.atlassian.com/software/bamboo)** | Atlassian (Market Cap: ~$52B; Revenue: ~$4.4B) | $1,200/year (1 remote build agent, unlimited users) | 30-day free trial (Data Center full evaluation license; 0 days free forever) | Atlassian ecosystem integration (Jira, Bitbucket) | Legacy agent-tier pricing model; Data Center maintenance overhead; restricted new sales |
| **[GitLab CI/CD](https://about.gitlab.com/)** | GitLab Inc. (Market Cap: ~$9.2B; ARR: ~$750M+) | $29/user/month (Premium plan; Free plan available) | 400 compute minutes/month (shared runners); unlimited minutes on self-hosted runners | All-in-one DevSecOps platform with integrated Auto DevOps | Complex YAML at scale; steep step up to paid tier pricing |
| **[Travis CI](https://www.travis-ci.com/)** | Idera, Inc. (Valuation: ~$3B; Revenue: ~$100M+) | $15/month (Usage-based Starter plan) | 14-day free trial with 10,000 credits (~1,000 Linux build min); free build credits for vetted OSS on request | Simple configuration for open-source repositories and legacy stacks | Lost significant developer mindshare after pricing overhauls; limited enterprise features |
| **[CircleCI](https://circleci.com/)** | CircleCI (Valuation: ~$1.7B; Estimated ARR: ~$55M+) | $15/month (Performance tier with 30,000 credits, up to 5 users) | 30,000 credits/month (approx. 3,000 Linux Medium minutes); up to 5 active users and 30 concurrent jobs (0 rollover) | Fast, container-native builds with Docker Layer Caching (DLC) | Credit consumption model can be unpredictable; macOS/Windows agents burn credits rapidly |
| **[TeamCity](https://www.jetbrains.com/teamcity/)** | JetBrains (Bootstrapped; Annual Revenue: ~$700M+) | $45/month (TeamCity Cloud, up to 3 committers) | 14-day cloud trial (with 12,000 build credits); Free forever for on-premises (Professional: 3 build agents, 100 configurations) | JetBrains IDE ecosystem, deep .NET and JVM build pipelines | Cloud pricing scales by active committers; less appealing outside JetBrains tooling |
| **[Codefresh](https://codefresh.io/)** | Octopus Deploy (Valuation: ~$625M; ARR: ~$83M) | $99/month (Pro tier; Free plan available) | 500 build minutes/month and 1 concurrent build; 30-day free trial for Enterprise features | Kubernetes-native CI/CD, GitOps delivery powered by Argo | Transitioning under Octopus Deploy umbrella; targeted primarily at cloud-native/K8s stacks |
| **[Bitrise](https://www.bitrise.io/)** | Bitrise (Total Funding: ~$100M; Estimated ARR: ~$25M-$35M) | $36/month (Starter tier billed annually, or $99/month monthly) | 300 build credits/month, 1 concurrency, 1 team member, 1 private app (Hobby plan) | Mobile CI/CD automation dedicated to iOS, Android, Flutter, and React Native | Mobile-specialized platform; unsuited for general-purpose web/backend microservices |

## Open-Source GitHub Projects



- **[Jenkins](https://github.com/jenkinsci/jenkins)**

  **Self-contained automation server with the largest plugin ecosystem** (MIT) — **the most extensible open-source CI/CD tool**, with **1,800+ plugins** covering virtually every integration imaginable . **Features**: Pipeline-as-code via Jenkinsfile (Groovy DSL); distributed builds with controller/agent architecture; Kubernetes plugin for dynamic agents; mature RBAC and authentication integrations. **Tech stack**: Java. **Deploy**: Self-hosted (WAR file, Docker, Kubernetes). **Trade-off**: **Legacy UI/UX and complex maintenance**; plugin compatibility issues; not cloud-native without plugins . **Best for**: organizations with complex multi-tech legacy pipelines needing maximum flexibility and existing Jenkins expertise—willing to accept maintenance overhead .



- **[Argo CD](https://github.com/argoproj/argo-cd)**

  **Declarative GitOps continuous delivery for Kubernetes** (Apache 2.0) — **the standard for Kubernetes GitOps delivery**, leading with automatic declarative reconciliation . **Features**: **Git as source of truth** with continuous drift detection and auto-correction; **multi-cluster management** from a central control plane; **rich web UI** with visual diffing of desired vs. live state ; SSO/RBAC; supports Helm, Kustomize, and Jsonnet; canary and blue/green via Argo Rollouts. **Tech stack**: Go, Kubernetes. **Deploy**: Self-hosted (runs in Kubernetes cluster). **Trade-off**: **CD only—needs a separate CI tool** for build and test ; resource-intensive at scale. **Best for**: teams adopting GitOps for Kubernetes deployments—the most mature open-source CD tool with the best UI for multi-cluster visibility .



- **[Flux CD](https://github.com/fluxcd/flux2)**

  **GitOps operator for Kubernetes** (Apache 2.0) — **the lightweight, CLI-native alternative to Argo CD** . **Features**: **Modular controllers** (source, kustomize, helm, notification, image automation); runs inside each cluster for autonomy; **strong multi-tenancy**; **built-in image update automation**; Helm controller for native Helm workflows . **Tech stack**: Go, Kubernetes. **Deploy**: Self-hosted (in-cluster controllers). **Trade-off**: **No bundled UI**—CLI-first; may require more effort for visual troubleshooting . **Best for**: lean, CLI-native platform teams wanting composable GitOps controllers with automated image updates—especially those who do not need a dashboard .



- **[Tekton](https://github.com/tektoncd/pipeline)**

  **Kubernetes-native CI/CD framework** (Apache 2.0) — **the vendor-neutral standard for cloud-native pipelines**, backed by CD Foundation . **Features**: **Kubernetes CRDs** for Tasks, Pipelines, and PipelineRuns; highly composable and reusable; **event-driven architecture** with Triggers; multi-cloud portability; Tekton Dashboard for visualizing PipelineRuns . **Tech stack**: Go, Kubernetes. **Deploy**: Self-hosted (Kubernetes required). **Trade-off**: **Steep learning curve**—requires building pipelines from scratch; fewer out-of-the-box integrations; less opinionated means more configuration . **Best for**: teams building custom cloud-native pipelines on Kubernetes needing maximum portability and vendor neutrality—especially in Red Hat/OpenShift ecosystems .



- **[Woodpecker CI](https://github.com/woodpecker-ci/woodpecker)**

  **Lightweight, Docker-native CI** (Apache 2.0) — **the easiest self-hosted CI to set up**, created as a community fork of Drone CI after license changes . **Features**: Simple `.woodpecker.yml` configuration—each step runs in a Docker container; **single binary** server and agents; multi-platform agents (Linux, macOS, Windows, ARM); works with **Gitea, GitHub, GitLab, Bitbucket, and Forgejo**; v3.0 with redesigned UI . **Resource usage**: Server ~60 MB RAM; Agent ~40 MB RAM . **Tech stack**: Go. **Deploy**: Self-hosted (Docker, single binary). **Trade-off**: **Smaller ecosystem than Jenkins**—fewer plugins; no built-in artifact storage or advanced caching . **Best for**: small teams using Gitea/Forgejo wanting simple, Docker-native CI with minimal overhead—the lightest self-hosted entry point .



- **[Gitea Actions](https://github.com/go-gitea/gitea)**

  **GitHub Actions-compatible CI built into Gitea** (MIT) — **the simplest path to GitHub Actions compatibility on self-hosted Git** . **Features**: **GitHub Actions workflow compatibility**—reuse existing workflows and many marketplace actions; **no separate CI service to deploy**—Actions is built into Gitea; Act runner based on the `act` project; runner daemon ~80 MB RAM . **Tech stack**: Go. **Deploy**: Gitea 1.21+ with Actions enabled. **Trade-off**: **Not all GitHub Actions features are supported**—complex workflows may need adjustments; newer and less mature than Woodpecker or Jenkins . **Best for**: teams already using Gitea wanting GitHub Actions-style CI without running a separate CI system.



- **[Drone CI](https://github.com/drone/drone)**

  **Container-native CI** (Apache 2.0 for older versions) — **the lightweight predecessor to Woodpecker**, with a simple YAML syntax and plugin architecture . **Features**: Every step runs in a container; simple `.drone.yml`; plugin ecosystem; integrates with GitHub, GitLab, Bitbucket, and Gitea. **Tech stack**: Go. **Deploy**: Self-hosted. **Trade-off**: **License changed to source-available for newer versions**; Woodpecker is the community fork . **Best for**: teams wanting Drone's original model via the Woodpecker fork—do not adopt new Drone versions without license review.



- **[Concourse](https://github.com/concourse/concourse)**

  **Container-based automation system** (Apache 2.0) — **the most opinionated open-source CI/CD** with pipelines as resources and jobs . **Features**: Every step runs in a container; pipelines declared as resources and jobs; no plugins—built-in resource types; strong isolation; visual pipeline UI. **Tech stack**: Go. **Deploy**: Self-hosted. **Trade-off**: **Opinionated model**—less flexible than Jenkins; smaller community . **Best for**: teams wanting a clean, container-first CI/CD model without plugin sprawl.



- **[GoCD](https://github.com/gocd/gocd)**

  **Continuous delivery server with built-in value-stream maps** (Apache 2.0) — **the most CD-focused open-source tool** . **Features**: **Pipelines and value-stream maps built in**—no plugins needed for CD visualization; modeling complex workflows; active development. **Tech stack**: Java. **Deploy**: Self-hosted. **Trade-off**: **CI capabilities are secondary**—best suited for CD orchestration; UI is functional but dated . **Best for**: teams needing strong CD visualization and dependency management—especially those modeling complex deployment pipelines.



### Additional Strong Open-Source Options



- **Jenkins X** — Kubernetes-native Jenkins with GitOps promotion, preview environments, and Tekton integration (Apache 2.0). **Note**: Higher learning curve; less mature than core Jenkins . **Best for**: teams migrating from Jenkins to Kubernetes-native workflows.

- **Pipewright** — Single Go binary self-hosted CI/CD + deployment + ops platform (license per repo). Pipeline-as-code via `.pipewright.yml` with DAG scheduling, container builds, SSH deployment, and monitoring . **Note**: Newer project; single binary with SQLite/MySQL. **Best for**: teams wanting an all-in-one lightweight self-hosted platform without external dependencies.

- **Dagger** — Programmable CI/CD engine (Apache 2.0). Pipelines in Go, Python, TypeScript, and Java—not YAML; native LLM integration and MCP server for agentic workflows . **Note**: Different mental model; requires programming knowledge. **Best for**: development teams wanting testable pipelines in real languages, especially AI-integrated CI.



**Frameworks for building custom systems**: Combine **Argo CD** for GitOps continuous delivery with **GitHub Actions** or **GitLab CI** for CI, **Tekton** for Kubernetes-native pipelines, and **Woodpecker CI** or **Gitea Actions** for lightweight self-hosted CI—creating a CI/CD stack matched to each team's infrastructure and Git hosting. **None of these match GitHub Actions' marketplace ecosystem**, but for self-hosted control and GitOps workflows, the open-source options are production-proven at scale.



## How to Contribute



1. Fork the repo.

2. Add/edit entries in `README.md` (follow existing format).

3. Include: name, link, 1–2 sentence description, license (for open-source), and whether it's SaaS or open-source.

4. Submit PR with a short explanation.



Star the repo if you find it useful!



## Disclaimer



- This is a **community-curated** list — not exhaustive and not an endorsement.

- CI/CD platforms handling code and deployment credentials must comply with data protection regulations (GDPR, CCPA, etc.) and implement appropriate access controls and secret management.

- **The "CI" vs. "CD (GitOps)" vs. "CI/CD platform" vs. "framework" distinction is critical.** **GitHub Actions, GitLab CI, CircleCI, Travis CI, Bamboo, TeamCity, and Bitrise** are **CI or CI/CD platforms**—they build, test, and often deploy. **Argo CD and Flux CD** are **GitOps CD controllers**—they deploy to Kubernetes from Git, but do not build or test . **Tekton** is a **CI/CD framework**—it provides primitives for building pipelines on Kubernetes . **Jenkins, Woodpecker, Gitea Actions, and Drone** are **CI servers**—they execute pipelines you define. **Choose based on whether you need build, deploy, or both.**

- **Argo CD vs. Flux: UI vs. CLI.** Argo CD leads with a polished web UI, application-centric model, and strong multi-cluster visibility . Flux is lightweight, CLI-native, and modular—better for teams that prefer composable controllers and automated image updates without a dashboard . **Large multi-team orgs: Argo CD. Lean platform teams: Flux.**

- **Jenkins remains relevant for complex legacy pipelines** with 1,800+ plugins . **The trade-off**: legacy UI, complex maintenance, and plugin compatibility issues . **Do not migrate off Jenkins without a clear replacement strategy**—its flexibility is still unmatched for heterogeneous environments.

- **Woodpecker CI and Gitea Actions are the easiest self-hosted entry points**—Docker-native, simple YAML, minimal resource usage (~40–80 MB RAM) . **Woodpecker** supports multi-forge (Gitea, GitHub, GitLab, Bitbucket) ; **Gitea Actions** offers GitHub Actions compatibility but is Gitea-only .

- **Tekton is the vendor-neutral choice for cloud-native pipelines**—Kubernetes CRDs, CD Foundation backing, and maximum portability . **The trade-off**: steep learning curve and more configuration required .

- **Pricing opacity varies.** GitHub Actions, GitLab CI, CircleCI, Travis CI, Bamboo, TeamCity, Bitrise, and Codefresh publish tiered pricing or quote-based models. Jenkins, Argo CD, Flux, Tekton, Woodpecker, and Gitea Actions are free open source. **Validate with direct vendor conversations against your team size and build volume.**

- Self-hosted open-source solutions require proper infrastructure (Kubernetes for Argo CD/Flux/Tekton, servers for Jenkins/Woodpecker), security hardening for build credentials, and ongoing maintenance. **CI/CD pipelines handle code and deployment secrets**—ensure your deployment meets your organization's security standards and includes secret management before automating production deployments.



---



**Made for developers, DevOps teams, and organizations building transparent CI/CD automation solutions.**

Let's make Continuous Integration & Deployment more open, data-driven, and pipeline-friendly.

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
- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **[GitHub Actions](https://github.com/features/actions)**
  **CI/CD integrated with GitHub** with a marketplace of reusable actions and native container support. **Pricing**: Free for public repos; private repos get included minutes on Free plan, scaling with paid tiers. **Free tier**: Yes, generous for open source. **Best for**: teams already hosting code on GitHub wanting the tightest integration and largest action ecosystem—**trade-off**: vendor lock-in to GitHub; minute caps can escalate costs for active teams .

- **[GitLab CI/CD](https://about.gitlab.com/)**
  **Integrated CI/CD within GitLab** covering source control, pipelines, registry, and environments in one platform. **Auto DevOps** automates language detection, security tests (SAST, DAST, dependency scanning), and Kubernetes deployment with Review Apps . **Pricing**: Free tier with 400 compute minutes/month; paid tiers scale. **Free tier**: Yes, limited minutes. **Best for**: teams wanting a single tool for repo, CI, and deployment—**trade-off**: strong dependency on GitLab ecosystem; complex YAML at scale .

- **[CircleCI](https://circleci.com/)**
  **Cloud CI/CD platform** known for speed and first-class Docker support. **Pricing**: Free tier with credits; paid plans by usage. **Free tier**: Yes, limited. **Best for**: teams prioritizing fast builds and Docker-native workflows—**trade-off**: credit model can become expensive at scale.

- **[Travis CI](https://www.travis-ci.com/)**
  **Hosted CI** with simple `.travis.yml` configuration, historically popular in open source. **Pricing**: Free for open-source repos; paid plans for private. **Free tier**: Yes, for open source. **Best for**: simple open-source projects wanting minimal setup—**trade-off**: lost most mindshare after pricing changes; smaller ecosystem than GitHub Actions.

- **[Bamboo](https://www.atlassian.com/software/bamboo)** (Atlassian)
  **CI/CD server** integrated with Jira and Bitbucket. **Pricing**: Quote-only; tiered by agents. **Free tier**: None. **Best for**: Atlassian-centric organizations wanting native Jira integration—**trade-off**: enterprise pricing; smaller plugin ecosystem than Jenkins.

- **[TeamCity](https://www.jetbrains.com/teamcity/)** (JetBrains)
  **CI/CD server** with strong .NET and JVM support. **Pricing**: Free tier for small teams; paid by agents. **Free tier**: Yes, limited build configurations. **Best for**: JetBrains-standardized teams wanting IDE-consistent CI—**trade-off**: less compelling outside JetBrains ecosystem.

- **[Bitrise](https://www.bitrise.io/)**
  **Mobile CI/CD platform** for iOS and Android. **Pricing**: Free tier; paid by concurrency. **Free tier**: Yes, limited. **Best for**: mobile teams wanting mobile-specific build and test workflows—**trade-off**: mobile-focused; not general-purpose.

- **[Codefresh](https://codefresh.io/)** (Acquired by Octopus Deploy)
  **Kubernetes-native CI/CD** with Argo CD integration. **Pricing**: Quote-only; bundled with Octopus. **Free tier**: Limited trial. **Best for**: teams wanting managed Argo CD with CI capabilities—**trade-off**: acquisition integration in progress.

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

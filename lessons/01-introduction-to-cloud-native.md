## Introduction

"Cloud native" is one of those phrases you hear everywhere. Job descriptions, meetup talks, vendor pitches, Kubernetes documentation. And for a term that's used so confidently, it's surprisingly hard to pin down. Ask five people what it means and you'll get five answers, usually circling somewhere around "containers" and "running in the cloud" without quite landing anywhere.

This is the first lesson in the KCNA study guide, and pinning that definition down is exactly where we're starting. Not because cloud native is mysterious, but because it's the frame that everything else in this guide fits into: Kubernetes, containers, networking, observability, security. All of those make more sense once you understand the shift they're part of.

Here's where we're going. We'll look at what cloud native actually means and why the distinction matters. Then we'll name the four characteristics that define a cloud native application. We'll meet the CNCF, the foundation that hosts Kubernetes and most of the ecosystem, and walk through the landscape they curate. And we'll look at the tradeoffs that come with it. By the end, you'll have the mental map you need for the rest of the study guide.

## What Cloud Native Actually Means

The simplest way to pin down cloud native is to start with what it isn't. Taking an application that was designed to run on a fixed server and lifting it into a virtual machine on AWS or Azure doesn't make it cloud native. The application hasn't changed. It still assumes the server will be there tomorrow, still expects a stable IP, still falls over when the hardware underneath it disappears. It's running in the cloud without being built for it.

Cloud native is the other thing. Applications designed from the start with the cloud's actual behaviour in mind.

So what is that behaviour? The cloud introduces a few assumptions that traditional infrastructure didn't have.

Infrastructure is ephemeral. Servers come and go. A virtual machine can be terminated because the underlying hardware failed, because the provider is rebalancing capacity, or because an autoscaler decided it wasn't needed anymore. Nothing is permanent, and code that assumes permanence breaks.

Workloads are distributed. An application isn't one process on one machine. It's many processes spread across many machines, talking over a network that can be slow, lossy, or temporarily unreachable. Calls that used to be function calls are now network calls, with all the failure modes that implies.

Capacity is elastic. The amount of compute available to you isn't fixed. It can grow when demand rises and shrink when it falls, within seconds. Designing for a fixed-size deployment leaves capacity on the table when you don't need it and leaves you short when you do.

Cloud native is what applications look like when you take these assumptions seriously. Instead of hoping a server stays up, you assume it won't and design so that losing one doesn't matter. Instead of treating scaling as a project, you build the application so that running ten copies or a thousand works the same way. Instead of managing servers by hand, you describe what you want running and let the platform keep it running.

The benefits people usually list for cloud native all come from this posture. Applications scale because they were built to run in many copies. They're resilient because no single instance is load-bearing. Teams ship faster because services are small enough to change independently. Workloads are portable because they don't depend on a specific machine or a specific cloud. None of those are features you add on top. They're consequences of designing for ephemeral, distributed, elastic infrastructure in the first place.

The CNCF, which we'll meet properly in a couple of sections, puts it this way:

> Cloud native technologies empower organizations to build and run scalable applications in modern, dynamic environments such as public, private, and hybrid clouds.

The phrasing is formal, but the idea underneath is the one we've just worked through. Cloud native is a way of building software that matches how modern infrastructure actually behaves.

That's the frame. It's not a toolset, and it's not a deployment target. It's an approach. The tools we'll spend the rest of this study guide on, containers, Kubernetes, service meshes, observability platforms, all exist because applications built this way need them. They're what "taking the assumptions seriously" looks like in practice.

## The Four Traits of a Cloud Native Application

When people describe an application as cloud native, they usually mean it has four characteristics. Each one is a big enough topic to have its own article in this study guide, so we'll keep the definitions short here. The goal is recognition, not mastery. When you see these terms later, you'll know what they point at.

**Microservices.** Instead of one large application that does everything, a cloud native system is built from many small services, each responsible for one part of the whole. A login service, a catalogue service, a checkout service. Each one is developed, deployed, and scaled on its own. We'll cover microservices properly when we get to architecture patterns.

**Containers.** A container packages an application together with everything it needs to run, its code, its libraries, its runtime, and isolates it from whatever else is on the host. The same container runs the same way on a developer's laptop and on a production server. Containers are the unit cloud native applications ship in, and they're the focus of the next series in this guide.

**Orchestration.** Once you have many containers running across many machines, something has to decide where they go, restart them when they fail, and scale them up and down with demand. That's orchestration. Kubernetes is the orchestrator that dominates cloud native, and it's the subject of the Kubernetes series later in this guide.

**Declarative APIs.** Rather than writing scripts that say "do this, then this, then this", cloud native tools let you describe the end state you want and keep the system in that state for you. You say "I want three copies of this service running", and the platform makes it true, and keeps making it true as conditions change. This pattern runs through Kubernetes and most of the ecosystem, and we'll see it in action throughout.

Those are the four. Hold onto the names. The rest of the study guide is, in one way or another, the long version of each.

## Meet the CNCF

Cloud native didn't happen by accident, and it isn't owned by any one company. Most of the tools we'll work with in this study guide, Kubernetes included, are hosted by a single organisation: the **Cloud Native Computing Foundation**, or CNCF.

CNCF was founded in 2015 under the Linux Foundation, and its job is to be a neutral home for cloud native open source projects. "Neutral" is the important word. A project hosted by CNCF is governed by the community, not by whichever company started it. Kubernetes came out of Google. Envoy came out of Lyft. Prometheus came out of SoundCloud. All of them now live at CNCF, which means no single vendor can take them in a direction that only serves their own product.

That neutrality is why the cloud native ecosystem looks the way it does. Components are built to open standards so they can be swapped out or combined. You've already met the acronyms in the original article, and you'll meet them again throughout this guide: **OCI** for container image formats, **CRI** for how Kubernetes talks to container runtimes, **CNI** for how pods get networking, **CSI** for how workloads get storage. Each of these is a contract. As long as a tool honours the contract, it fits into the ecosystem. That's why Kubernetes can run on containerd or CRI-O, network through Cilium or Calico, and mount storage from any CSI driver, without Kubernetes itself needing to know the specifics.

### The Landscape

If you want to see what the ecosystem actually contains, CNCF publishes a live map of every project in its orbit. It's called the Cloud Native Landscape.

![The CNCF Cloud Native Landscape](../assets/images/cncf-landscape-ecosystem-overview.jpeg)

The first reaction most people have is "that's a lot". It is. But you're not meant to know every logo. The landscape's job is to show you the shape of the ecosystem, not to be memorised.

Look at how it's organised. The landscape is divided into categories that match the concerns a cloud native system has to solve. "Application Definition and Image Build" is how you package and describe workloads, which is where tools like Helm and Buildpacks live. "Continuous Integration and Delivery" is how you ship changes, where Argo, Flux, Jenkins, and GitHub Actions sit. "Database" and "Streaming and Messaging" are your data layer. Further down, there are categories for container runtimes, orchestration, networking, service meshes, observability, and security. Each category is one of the problems the rest of this study guide will touch.

Projects in the landscape are also ranked by maturity, which is how CNCF signals how battle-tested something is. **Graduated** projects are mature, widely adopted, and have strong governance. Kubernetes, Prometheus, Envoy, containerd, and Helm are all graduated. **Incubating** projects have real production use but are still growing into their role. **Sandbox** projects are earlier, more experimental, and haven't proven themselves at scale yet. For KCNA, recognising that these stages exist matters more than memorising which project sits where.

The landscape is best treated as a reference you come back to, not a checklist you work through. Right now, the value is seeing the shape. An enormous, structured ecosystem of tools that all fit together because they're built to shared contracts, under neutral governance, in response to the same design problem.

That design problem is the one we spent section two laying out. The ecosystem exists because applications built for ephemeral, distributed, elastic infrastructure need a lot of supporting machinery. Every category in the landscape is a part of that machinery.

## What Gets Harder

We've spent the article so far laying out why cloud native exists and what it gives you. Now we need to be honest about the other side. The simple world, one VM, one application, one process to reason about, is genuinely gone. What you get in exchange is powerful, but it isn't free. Four things get harder, and most of the rest of this study guide exists to address them.

**The number of moving parts.** The thing that used to be one process running on one server is now many services, many containers, many configs, spread across many machines, talking to each other over a network. Each piece is simpler than the monolith it replaced, but there are a lot more pieces. Deciding where they run, keeping them running, scaling them with demand, replacing them when they fail, none of that is optional anymore. This is the problem orchestration solves, and it's why Kubernetes sits at the centre of cloud native.

**Debugging across boundaries.** In a single-process application, a bug is somewhere in the code, and the logs are in one place. In a cloud native system, a user request might pass through five services before something goes wrong, and the logs are scattered across all five. A traditional "check the log file" approach breaks. You need to see how a request moved through the system, what each service did with it, and where it slowed down or failed. That's what observability is for, metrics, distributed tracing, structured logging, and it's a major part of the cloud native stack for exactly this reason.

**Security surface area.** In the old model, you could draw a perimeter around your application and guard the edge. That doesn't work when every internal call is a network call, every container is an image that might carry vulnerabilities, and every service is a potential entry point. The security model shifts from "protect the edge" to "assume the edge is already compromised and limit what anything can do". Network policies control which services can talk to which. Image scanning catches vulnerabilities before they reach production. Zero-trust thinking assumes nothing in the system is safe by default. We'll get to the networking and policy side of this when we reach the Kubernetes networking series.

**How teams work.** Cloud native architecture assumes teams can deploy their services independently, which assumes the organisation is set up to let that happen. If shipping a change still requires a coordination meeting with five other teams, the architecture's advantages disappear. This is why cloud native tends to come with cultural shifts: DevOps practices so developers own their services in production, platform teams that provide shared infrastructure so every team doesn't rebuild it, shift-left testing and security so problems get caught early. The technology assumes this way of working. Adopting the tools without adopting the practices tends not to go well.

Those are the four. Each one is a real thing that cloud native makes harder, and each one has answers. The rest of this study guide is, in large part, a walk through those answers.

## Where This Guide Goes Next

The rest of this study guide is structured around the five domains of the KCNA exam. Kubernetes Fundamentals is the largest of them, about 46% of the material, and it's where we go from here. After that, the guide moves through container orchestration, cloud native architecture, observability and monitoring, and finally application delivery and DevOps. Each domain picks up one or more of the hard things we named in the last section and shows how the ecosystem actually addresses them.

We start with Kubernetes because it's where the ideas in this article become concrete. The four traits we named, microservices, containers, orchestration, declarative APIs, are all ideas until you have a platform that embodies them. Kubernetes is that platform. It's the orchestrator that took over cloud native, not because it was first, but because the model it offers, describe the state you want and let the system make it true, turned out to be the right answer to the problems cloud native applications have.

The next article is the [introduction to Kubernetes](https://iamachs.com/blog/kubernetes/part-1-introduction-journey-begins). We'll look at what the platform actually is, how a cluster is structured, and how the pieces fit together. From there, we'll spend a while inside Kubernetes itself, pods, replica sets, networking, services, namespaces, config and secrets, the control plane, before widening out into the rest of the domains.

For now, you have the frame. Everything that follows fits inside it.
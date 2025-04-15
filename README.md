# KCNA Exam Companion: Pass the Kubernetes & Cloud Native Associate Certification

Welcome to your complete, no-fluff study companion for the KCNA exam.  
This guide is built by a fellow learner and cloud-native practitioner (👋 hi, I’m Ahmed) who wanted a better, focused, and momentum-driven way to prepare — and is sharing it openly to help others.

> This is not just a list of links. This README **is your roadmap**. Read it from top to bottom, and you’ll have everything you need to start preparing for KCNA today.

---

## What This Is

A self-paced, open-source study guide designed to:
- Help you pass the KCNA exam with confidence
- Focus only on what matters (based on the CNCF exam blueprint)
- Provide curated learning resources, articles, hands-on exercises, and conceptual checkpoints
- Track your progress through clear **phases** and **domains**

> 🧭 This README includes the full study plan — no folder-hunting required.

---

## KCNA Exam Summary

| **Feature**           | **Details**                                           |
|----------------------|-------------------------------------------------------|
| Exam Name            | Kubernetes and Cloud Native Associate (KCNA)         |
| Format               | Online, Proctored, Multiple-Choice                   |
| Duration             | 90 minutes                                           |
| Number of Questions  | ~60 questions                                        |
| Passing Score        | 75%                                                  |
| Cost                 | $250 USD (includes 1 free retake)                    |
| Level                | Conceptual, foundational                             |
| CLI Knowledge        | Minimal (basic `kubectl` awareness is enough)        |

📄 [Official Exam Site](https://training.linuxfoundation.org/certification/kubernetes-cloud-native-associate/)  
📄 [Official Curriculum PDF](https://github.com/cncf/curriculum/blob/master/KCNA_Curriculum.pdf)

---

## The Game Plan: Focus Areas by Weight

| Domain                        | Weight | Coverage Status |
|------------------------------|--------|-----------------|
| Kubernetes Fundamentals      | 46%    | 🟡 In Progress   |
| Container Orchestration      | 22%    | 🟢 Mostly Covered|
| Cloud Native Architecture    | 16%    | 🟡 In Progress   |
| Observability & Monitoring   | 8%     | 🔴 Not Started   |
| App Delivery & DevOps        | 8%     | 🔴 Not Started   |

---

## 📘 Study Roadmap & Phases

This study plan is broken into **phases** aligned to exam weights.  
Each domain includes:
- Concept explanations
- Curated articles
- Hands-on prompts (where useful)
- Practice questions (coming soon)

---

### Domain 0: Cloud Native Foundations (Start Here)

Before diving into containers and Kubernetes, it’s important to understand the mindset, architecture, and ecosystem that powers cloud native computing. This is your orientation — and the perfect first step if you’re new to this world or studying for KCNA.

✅ **Start here**  
- [📄 Introduction to Cloud Native Computing](./lessons/01-introduction-to-cloud-native.md)

### Domain 1: Kubernetes Fundamentals (46%)

🧠 Learn the architecture, control plane, core objects, API model, Services, scheduling, and YAML basics.

✅ **Start here**
- [📄 Introduction to Kubernetes](https://www.iamachs.com/p/kubernetes/part-1-introduction-journey-begins/)
- [📄 Understanding Kubernetes Pods](https://www.iamachs.com/p/kubernetes/part-2-pods-building-blocks/)
- [📄 Understanding Kubernetes ReplicaSets](https://www.iamachs.com/p/kubernetes/part-3-understanding-replicasets/)
- [📄 Kubernetes Networking: Pods, CNI, Overlay](https://www.iamachs.com/p/kubernetes-networking/part-1-demystifying-kubernetes-networking/)

🕐 Coming Soon:
- Services & Discovery (ClusterIP, NodePort)
- Namespaces, ConfigMaps, Secrets
- Control Plane & Node components
- API Server & Declarative YAML
- Pod Scheduling Basics

---

### Domain 2: Container Orchestration (22%)

🧠 Understand container runtimes, orchestration needs, persistent storage, basic security, and service networking.

✅ **Start here**
- [📄 Docker: Friendly Intro to Containers](https://www.iamachs.com/p/docker/part-1-introduction-to-docker-core-concepts/)
- [📄 Docker: How It Works Behind the Scenes](https://www.iamachs.com/p/docker/part-2-understanding-docker-architecture/)
- [📄 Docker: From Code to Container](https://www.iamachs.com/p/docker/part-3-creating-your-first-docker-image/)
- [📄 Docker Networking Fundamentals](https://www.iamachs.com/p/docker/part-4-networking-fundamentals-for-containers/)
- [📄 Docker Volumes & Storage](https://www.iamachs.com/p/docker/part-5-understanding-docker-storage-and-volumes/)
- [📄 containerd & CRI-O](https://www.iamachs.com/p/docker/part-6-understanding-containerd-and-cri-o/)
- [📄 Kubernetes Network Policies](https://www.iamachs.com/p/kubernetes-networking/part-2-network-policies/)

🕐 Coming Soon:
- Basic Kubernetes Security: Users, RBAC, ServiceAccounts
- Service Mesh Basics

---

### Domain 3: Cloud Native Architecture (16%)

🧠 Learn microservices, CNCF governance, open standards, autoscaling, and serverless basics.

✅ **Start here**
- [📄 CNCF Cloud Native Definition](https://github.com/cncf/toc/blob/main/DEFINITION.md)

🕐 Coming Soon:
- Cloud Native Mindset & Principles
- CNCF Trail Map, CRI/CNI/OCI overview
- Kubernetes Autoscaling (HPA)
- Serverless & Azure Functions

---

### Domain 4: Observability & Monitoring (8%)

🧠 Learn the observability stack: logs, metrics, traces, and Prometheus basics.

🕐 Coming Soon:
- Observability vs. Monitoring
- Intro to Prometheus
- Cost Awareness in Kubernetes

---

### Domain 5: App Delivery & DevOps (8%)

🧠 Learn GitOps principles, CI/CD basics, and how apps get shipped in K8s.

🕐 Coming Soon:
- CI vs CD vs Continuous Deployment
- GitOps Overview (ArgoCD/Flux)
- Delivery Pipelines in Kubernetes

---

## Basic Tools Awareness

You don’t need to master the terminal — just understand what `kubectl` does.

| Command                | Purpose                          |
|------------------------|----------------------------------|
| `kubectl get`         | View resources like pods, svc    |
| `kubectl describe`    | Inspect details of objects       |
| `kubectl apply -f`    | Apply config files (YAML)        |
| `kubectl delete`      | Remove objects                   |
| `kubectl logs`        | View app logs                    |

📄 [Kubectl Quick Reference](https://kubernetes.io/docs/reference/kubectl/quick-reference/)

---

## 📝 Practice Questions (Coming Soon)

A KCNA-style question bank is coming. It will include:
- Scenario-based questions
- Concept checks per domain
- Answers with explanations

For now, check:
- Linux Foundation’s official companion course (if bundled with exam)

---

## 🎁 Go Deeper (Optional Reads)

Explore beyond the KCNA scope:

- [Securing AKS with Cilium](https://www.iamachs.com/p/kubernetes-networking/part-4-aks-cilium-star-wars-demo/)
- [eBPF, Cilium, and Observability](https://www.iamachs.com/p/kubernetes-networking/part-3-supercharge-with-cilium-ebpf/)

---

## 🤝 Contributing

Found a typo? Have a better example or explanation?  
Please contribute! See [`CONTRIBUTING.md`](#) (coming soon)

---

## 📄 License

MIT – remix, adapt, and share freely to support more learners.

---

## ✉️ Connect

Say hi or ask a question:  
📫 [@ahmedmuhi01](https://x.com/ahmedmuhi01) | 🌐 [iamachs.com](https://www.iamachs.com)
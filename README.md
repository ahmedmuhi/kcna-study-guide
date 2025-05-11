# KCNA Exam Companion: Your Path to Kubernetes Certification

**Ready to prove your cloud native knowledge and boost your career?** This complete, no-fluff study companion will take you from Kubernetes novice to KCNA certified.

Built by Ahmed Muhi (👋 hi!), a cloud native practitioner who wanted a better, focused way to prepare—and is now sharing it openly to help others succeed.

> This is not just a list of links. This README **is your roadmap**. Follow it from top to bottom, and you'll have everything you need to confidently pass the KCNA exam.

---

## 🎯 What This Is

A self-paced, open-source study guide designed to:
- **Help you pass** the KCNA exam with confidence (75% passing score)
- **Focus only on what matters** (based on the CNCF exam blueprint)
- **Build practical knowledge** through curated resources and hands-on exercises
- **Track your progress** through clear phases aligned with exam domains

> 🧭 This README includes the full study plan — no folder-hunting required.

---

## 📊 KCNA Exam Summary

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
| Career Impact        | Entry-level positions, DevOps teams, Platform teams  |

📄 [Official Exam Site](https://training.linuxfoundation.org/certification/kubernetes-cloud-native-associate/)  
📄 [Official Curriculum PDF](https://github.com/cncf/curriculum/blob/master/KCNA_Curriculum.pdf)

---

## 🗺️ Your Learning Journey

**Estimated Total Study Time: 25-30 hours**

| Domain                        | Weight | Est. Study Time | Coverage Status |
|------------------------------|--------|----------------|-----------------|
| Kubernetes Fundamentals      | 46%    | 10-12 hours    | 🟡 In Progress   |
| Container Orchestration      | 22%    | 5-6 hours      | 🟢 Mostly Covered|
| Cloud Native Architecture    | 16%    | 4-5 hours      | 🟡 In Progress   |
| Observability & Monitoring   | 8%     | 2-3 hours      | 🔴 Not Started   |
| App Delivery & DevOps        | 8%     | 2-3 hours      | 🟢 Fully Covered |

---

## 📘 Study Roadmap & Phases

This study plan follows a logical progression aligned to exam weights. Each section builds on the previous one, creating a comprehensive understanding of cloud native concepts and Kubernetes.

---

### Domain 0: Cloud Native Foundations (Start Here)

Before diving into containers and Kubernetes, understand the mindset, architecture, and ecosystem that powers cloud native computing. This is your orientation—perfect for those new to this world.

✅ **Start here** (0.5 hour)  
- [📄 Introduction to Cloud Native Computing](./lessons/01-introduction-to-cloud-native.md)

---

### Domain 1: Kubernetes Fundamentals (46%)

🧠 Learn the architecture, control plane, core objects, API model, Services, scheduling, and YAML basics.

✅ **Start here** (10-12 hours)
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

✅ **Start here** (5-6 hours)
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

✅ **Start here** (4-5 hours)
- [📄 CNCF Cloud Native Definition](https://github.com/cncf/toc/blob/main/DEFINITION.md)

🕐 Coming Soon:
- Cloud Native Mindset & Principles
- CNCF Trail Map, CRI/CNI/OCI overview
- Kubernetes Autoscaling (HPA)
- Serverless & Azure Functions

---

### Domain 4: Observability & Monitoring (8%)

🧠 Learn the observability stack: logs, metrics, traces, and Prometheus basics.

🕐 Coming Soon (2-3 hours):
- Observability vs. Monitoring
- Intro to Prometheus
- Cost Awareness in Kubernetes

---

### Domain 5: App Delivery & DevOps (8%)

🧠 Learn GitOps principles, CI/CD basics, and how apps get shipped in Kubernetes.

✅ **Start here** (2-3 hours)
- [📄 GitOps Days - Day 1: What Really Is GitOps?](https://github.com/ahmedmuhi/GitOps-Days/blob/main/Day-1-What-really-is-GitOps.md) - A comprehensive introduction to GitOps principles, workflows, and how it differs from traditional CI/CD
- [📄 GitOps Days - Day 2: Build Your First Self-Healing System with Flux](https://github.com/ahmedmuhi/GitOps-Days/blob/main/Day-2-Building-Your-First-GitOps-Loop.md) - Hands-on experience with Flux, creating a GitOps workflow, and testing self-healing capabilities

> 💡 **Why GitOps matters for KCNA**: GitOps represents the modern approach to Kubernetes deployments and appears prominently in the "App Delivery" domain of the exam. Understanding these principles will help you answer questions about deployment strategies, versioning, and automation.

🕐 Additional Resources Coming Soon:
- CI vs CD vs Continuous Deployment
- Delivery Pipelines in Kubernetes

---

## 🛠️ Basic Tools Awareness

You don't need to master the terminal — just understand what these common `kubectl` commands do.

| Command                | Purpose                          | Exam Relevance |
|------------------------|----------------------------------|----------------|
| `kubectl get`         | View resources like pods, svc    | High           |
| `kubectl describe`    | Inspect details of objects       | Medium         |
| `kubectl apply -f`    | Apply config files (YAML)        | High           |
| `kubectl delete`      | Remove objects                   | Low            |
| `kubectl logs`        | View app logs                    | Medium         |

📄 [Kubectl Quick Reference](https://kubernetes.io/docs/reference/kubectl/quick-reference/)

---

## 📝 Practice Questions (Coming Soon)

A KCNA-style question bank is coming. It will include:
- Scenario-based questions
- Concept checks per domain
- Answers with explanations

For now, check:
- Linux Foundation's official companion course (if bundled with exam)

---

## 🎯 Real-World Applications

The knowledge you'll gain studying for KCNA applies directly to roles such as:
- **Junior DevOps Engineer** - Understanding containerization and deployment workflows
- **Cloud Support Specialist** - Troubleshooting basic Kubernetes issues
- **Platform Team Member** - Contributing to infrastructure decisions
- **Developer** - Working effectively with Kubernetes-based environments

Many organizations now consider KCNA a valuable credential for entry-level cloud native positions.

---

## 👥 Join the Community

Learning is better together! Connect with fellow KCNA candidates:
- **Kubernetes**: [Kubernetes Slack](slack.k8s.io)
- **CNCF**: [CNCF Slack](https://slack.cncf.io/) - Join the #kubernetes-novice channel
- **Study Group**: Share your progress on Twitter with #KCNAStudy

---

## 🎁 Go Deeper

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
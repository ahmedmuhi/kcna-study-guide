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

> 🧭 This README **includes the full study plan** — you don’t need to dig through folders unless you want extra depth.

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

| Domain                        | Weight | Study Material                                       |
|------------------------------|--------|------------------------------------------------------|
| Kubernetes Fundamentals      | 46%    | ✅ [See below](#domain-1-kubernetes-fundamentals)     |
| Container Orchestration      | 22%    | ✅ [See below](#domain-2-container-orchestration)     |
| Cloud Native Architecture    | 16%    | ✅ [See below](#domain-3-cloud-native-architecture)   |
| Observability & Monitoring   | 8%     | ✅ [See below](#domain-4-observability--monitoring)   |
| App Delivery & DevOps        | 8%     | ✅ [See below](#domain-5-cloud-native-app-delivery)   |

---

## Study Roadmap & Phases

This study plan is broken into **phases** aligned to the exam weights.  
Each phase includes links to:
- Concept explanations
- Curated articles (including my [Docker for Beginners](https://www.iamachs.com/p/docker/part-1-introduction-to-docker-core-concepts/) & [Kubernetes series](https://www.iamachs.com/p/kubernetes/part-1-introduction-journey-begins/))
- Hands-on prompts (where useful)
- Practice questions (coming soon)

---

### Domain 1: Kubernetes Fundamentals (46%)

🧠 Learn the architecture, key components, Pods, Deployments, Services, and the Kubernetes API model.

✅ **Start here**  
- [📄 Kubernetes: Introduction to Architecture](https://www.iamachs.com/p/kubernetes/part-1-introduction-journey-begins/)  
- [📄 Pods: The Building Block](https://www.iamachs.com/p/kubernetes/part-2-pods-building-blocks/)  
- [📄 Deployments: Managing Applications](https://www.iamachs.com/p/kubernetes/part-3-understanding-replicasets/)  
- [📄 Services & Networking Basics](Coming Soon)  
- [📄 ConfigMaps, Secrets & Scheduling (Upcoming)](Coming Soon)

---

### Domain 2: Container Orchestration (22%)

🧠 Understand container runtimes, orchestration needs, service discovery, storage, and basic security.

✅ **Start here**
- [📄 Docker for Beginners: A Clear, Friendly Introduction to Containers](https://www.iamachs.com/p/docker/part-1-introduction-to-docker-core-concepts/)
- [📄 Docker for Beginners: How Docker Works Behind the Scenes](https://www.iamachs.com/p/docker/part-2-understanding-docker-architecture/)
- [📄 Docker for Beginners: From Code to Container and Cloud](https://www.iamachs.com/p/docker/part-3-creating-your-first-docker-image/)
- [📄 Docker for Beginners: Docker Networking Explained](https://www.iamachs.com/p/docker/part-4-networking-fundamentals-for-containers/)
- [📄 Docker for Beginners: Understanding Docker Storage and Volumes](https://www.iamachs.com/p/docker/part-5-understanding-docker-storage-and-volumes/)
- [📄 Docker for Beginners: Understanding containerd, CRI-O, and the Runtime Layer](https://www.iamachs.com/p/docker/part-6-understanding-containerd-and-cri-o/)

---

### Domain 3: Cloud Native Architecture (16%)

🧠 Learn microservices, immutable infrastructure, CNCF governance, autoscaling, and open standards.

✅ **Start here**  
- [🧾 CNCF Cloud Native Definition](https://github.com/cncf/toc/blob/main/DEFINITION.md)  
- [📄 Cloud Native Mindset](Coming Soon)  
- [📄 HPA: Autoscaling Basics](Coming Soon)  
- [📄 Serverless & CNCF Landscape](Coming Soon)

---

### Domain 4: Observability & Monitoring (8%)

🧠 Understand the "telemetry triad": logs, metrics, traces — plus Prometheus and cost awareness.

✅ **Start here**  
- [📄 Observability Principles](Coming Soon)  
- [📄 Intro to Prometheus](Coming Soon)  
- [📄 Cost Management Basics](Coming Soon)

---

### Domain 5: Cloud Native App Delivery (8%)

🧠 Learn CI/CD, GitOps principles, and how cloud-native teams deploy fast and reliably.

✅ **Start here**  
- [📄 CI/CD Explained Simply](Coming Soon)  
- [📄 GitOps 101](Coming Soon)  
- [📄 Delivery Pipelines in K8s](Coming Soon)

---

## Basic Tools Awareness

You don’t need to master the terminal — but understand *what* `kubectl` is used for:

| Command                | Purpose                          |
|------------------------|----------------------------------|
| `kubectl get`         | View resources like pods, svc    |
| `kubectl describe`    | Inspect details of objects       |
| `kubectl apply -f`    | Apply config files (YAML)        |
| `kubectl delete`      | Remove objects                   |
| `kubectl logs`        | View app logs                    |

📄 [Kubectl Cheat Sheet](https://kubernetes.io/docs/reference/kubectl/cheat-sheet/)

---

## Practice Questions (Coming Soon)

I'm working on a practice section that aligns with each domain and reinforces the core KCNA-style questions (scenario-based, definition-based, architecture-focused).

In the meantime, you can check:
- [KodeKloud KCNA Path](https://kodekloud.com/learning-path/kcna)  

---

## 🤝 Contributing

Got a better explanation? Found a typo? Want to share your own learning?  
Contributions are very welcome. See [`CONTRIBUTING.md`](#) (coming soon)

---

## 📄 License

MIT – feel free to copy, remix, and share this to help more learners.  
Let’s make cloud-native learning less overwhelming and more accessible.

---

## ✉️ Connect

Questions? Feedback? Want to chat KCNA prep or cloud-native learning?  
You can find me at [@ahmedmuhi01](https://x.com/ahmedmuhi01) or [iamachs.com](https://www.iamachs.com)
# Kubernetes (K8s) – A to Z in Very Simple Words 🚀

---

## What is Kubernetes (K8s)?
Kubernetes (short name **K8s**) is a tool that **runs and manages containers automatically**.

👉 It is mainly used with **Docker containers**.

---

## Why is it called K8s?
The word **Kubernetes** has:
- K at start
- s at end
- 8 letters in between  

So it is called **K8s**.

---

## Why do we need Kubernetes?
When applications grow big:
- Many containers are needed
- Containers may crash
- Traffic may increase
- Manual handling becomes difficult  

✅ Kubernetes does all this **automatically**.

---

## What Problems K8s Solves?
- App crash → K8s restarts it
- More users → K8s scales app
- Server down → K8s moves app
- Load balancing → K8s manages traffic

---

## Kubernetes Architecture (Big Picture)

### 1. Cluster
A **cluster** is a group of machines that run applications.

---

### 2. Control Plane (Master)
The **brain** of Kubernetes.
- Decides what should run
- Monitors everything

---

### 3. Worker Node
A **worker node** is where your application actually runs.

---

## Core Kubernetes Objects

---

### 1. Pod
- Smallest unit in Kubernetes
- Contains **one or more containers**
- Pods are temporary (can die anytime)

👉 Example: 1 pod = 1 app container

---

### 2. ReplicaSet
- Ensures **correct number of pods** are running
- If 1 pod dies, it creates a new one

---

### 3. Deployment
- Manages ReplicaSets and Pods
- Used for **stateless apps**
- Supports scaling and rolling updates

👉 Most commonly used object

---

### 4. StatefulSet
- Used for **stateful apps** (DB, etc.)
- Pods have fixed name and storage

---

### 5. DaemonSet
- Runs **one pod on every node**
- Used for logging, monitoring

👉 Example: log collector on all nodes

---

### 6. Job
- Runs a task **only once**
- Stops after completion

---

### 7. CronJob
- Runs jobs on **schedule**
- Like Linux cron

👉 Example: backup at 2 AM daily

---

## Kubernetes Networking

---

### 1. Service
A **Service** exposes pods using a fixed name/IP.

Types of services:

#### a) ClusterIP
- Internal access only
- Default service type

#### b) NodePort
- Access app using NodeIP:Port

#### c) LoadBalancer
- Uses cloud load balancer
- Mostly in AWS, Azure, GCP

---

### 2. Headless Service
- No load balancing
- Used with StatefulSet

---

### 3. Ingress
- Manages **external HTTP/HTTPS traffic**
- Uses domain names and paths

👉 Example:
- example.com/app
- example.com/login

---

## Storage in Kubernetes

---

### 1. Volume
- Temporary storage
- Deleted when pod dies

---

### 2. Persistent Volume (PV)
- Actual storage resource

---

### 3. Persistent Volume Claim (PVC)
- Request for storage by pod

---

### 4. StorageClass
- Defines **type of storage**
- Example: SSD, HDD

---

## Configuration & Secrets

---

### 1. ConfigMap
- Stores non-sensitive data
- Example: app configs

---

### 2. Secret
- Stores sensitive data
- Example: passwords, tokens

---

## Security in Kubernetes

---

### 1. Namespace
- Logical separation
- Used for dev, test, prod

---

### 2. RBAC
- Role Based Access Control
- Controls **who can do what**

---

### 3. Service Account
- Identity for pods

---

## Scaling in Kubernetes

---

### 1. Manual Scaling
- Increase/decrease pod count manually

---

### 2. HPA (Horizontal Pod Autoscaler)
- Auto scales pods based on CPU/memory

---

## Health Checks

---

### 1. Liveness Probe
- Checks if app is alive
- Restarts pod if failed

---

### 2. Readiness Probe
- Checks if app is ready to accept traffic

---

## Kubernetes YAML
- All objects are created using **YAML files**
- YAML describes desired state

---

## Simple Flow of Kubernetes
1. Developer writes code
2. Docker creates image
3. Image pushed to registry
4. Kubernetes pulls image
5. Pods run app
6. Service exposes app
7. Ingress handles traffic

---

## Kubernetes in One Line
**Kubernetes automatically deploys, manages, scales, and heals containerized applications.**

---

## Docker vs Kubernetes
- Docker → creates containers
- Kubernetes → manages containers

---

## Who Uses Kubernetes?
- Google
- Netflix
- Amazon
- Startups & Enterprises

---

## Final Simple Meaning
🟢 Kubernetes is a **container manager**  
🟢 It runs apps automatically  
🟢 It fixes issues on its own  
🟢 It makes DevOps life easy 😄

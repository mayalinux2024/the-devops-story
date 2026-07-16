# Kubernetes — The Mayor (Chapter 10)

Understand that Kubernetes is an orchestrator. It manages and organizes containers instead of running them itself.

Kubernetes is already organizing the containers running inside the cluster.

## Objective

Understand that Kubernetes is the kingdom's mayor.

The mayor doesn't build toys.

The mayor simply organizes where the workers should work.

---

# 🔘 Show the Real Implementation

Today we will tell the mayor:

"I want one DevOps Story worker."

The mayor will make sure that worker always exists.

---

## Step 1 — Give the Mayor Instructions

Run:

```bash
kubectl apply -f 10-deployment.yaml
```

Expected output:

```text
deployment.apps/devops-story created
```

### What this command means

- `kubectl` → The messenger that talks to the mayor.
- `apply` → Give the mayor a new set of instructions.
- `-f` → Read the instructions from a file.
- `10-deployment.yaml` → The blueprint telling the mayor what we want.

Story translation:

King

↓

Messenger (kubectl)

↓

Mayor (Kubernetes)

↓

"Please create one DevOps Story worker."

Nothing has been built by us.

We simply gave the mayor instructions.

---

## Step 2 — Ask the Mayor What He Created

Run:

```bash
kubectl get deployments
```

Example output:

```text
NAME           READY
devops-story   1/1
```

### What this command means

- `get` → Ask the mayor to show something.
- `deployments` → Show the list of jobs the mayor is managing.

Think of a Deployment as:

"Mayor, always keep one DevOps Story worker alive."

Even if the worker disappears...

the mayor creates another one automatically.

---

## Step 3 — See the Actual Worker

Run:

```bash
kubectl get pods
```

Example output:

```text
devops-story-998cf9c67-dm2tx
```

### What this command means

A Pod is the worker's work table.

Earlier in the story we learned:

Workshop

↓

Work Table

↓

Worker builds toys

In Kubernetes:

Node

↓

Pod

↓

Container

The Pod is the place where the container works.

Kubernetes doesn't manage containers directly.

It manages Pods.

Most beginner applications have:

1 Pod

↓

1 Container

---

## The Complete Story

King

↓

Messenger (kubectl)

↓

Mayor (Kubernetes)

↓

Deployment

↓

Pod

↓

Container

↓

Application Running

This is the entire journey of our DevOps Story application.

---

## 📸 Screenshots

1.

```bash
kubectl apply -f 10-deployment.yaml
```

2.

```bash
kubectl get deployments
```

3.

```bash
kubectl get pods
```

## Summary

kubectl apply
        ↓
Tell the mayor what you want

kubectl get deployments
        ↓
The mayor records the plan

kubectl get pods
        ↓
The mayor creates workers to carry out the plan

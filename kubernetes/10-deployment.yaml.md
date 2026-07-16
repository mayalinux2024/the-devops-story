# What is deployment.yaml ?

- deployment.yaml file is the mayor's first set of instructions.

- In later chapters, we'll explain those instructions in more detail (YAML, Pods, Services, etc.), but for now the learner only needs to know:

### "The mayor needs a written order describing what to create."

---

#🔘 Show the Real Implementation

Today we will give the mayor his first written instructions.

The mayor cannot organize workers until someone tells him what to create.

Step 1 — Write the Mayor's Instructions

Create a file:

nano 10-deployment.yaml

Paste:

apiVersion: apps/v1
kind: Deployment

metadata:
  name: devops-story

spec:
  replicas: 1

  selector:
    matchLabels:
      app: devops-story

  template:
    metadata:
      labels:
        app: devops-story

    spec:
      containers:
      - name: devops-story
        image: mayalinux/devops-story:latest
        ports:
        - containerPort: 5000

Save the file.

What this means

Think of this file as the letter the king sends to the mayor.

It doesn't create anything by itself.

It simply tells the mayor:

"Please keep one DevOps Story application running."

We don't need to understand every line yet.

Later chapters will explain each part of this file.

For now, just remember:

10-deployment.yaml

↓

Instructions for the Mayor
Step 2 — Give the Instructions to the Mayor
kubectl apply -f 10-deployment.yaml

Expected output:

deployment.apps/devops-story created
What this command means
kubectl → The messenger that talks to the mayor.
apply → Give the mayor new instructions.
-f → Read the instructions from a file.
10-deployment.yaml → The written instructions.

Story translation:

King

↓

Messenger (kubectl)

↓

Mayor (Kubernetes)

↓

"Please create one DevOps Story worker."
Step 3 — Ask What the Mayor Is Managing
kubectl get deployments

...

Step 4 — See the Worker
kubectl get pods

...

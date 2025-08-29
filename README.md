

# ArgoCD ApplicationSet Examples

This repository contains examples of using **ArgoCD ApplicationSet** to manage Kubernetes applications at scale.
It demonstrates different patterns for automating application deployments using generators and project configurations.

---

## 📂 Repository Structure

* **argocdappset/** – Example ArgoCD `ApplicationSet` definitions.
* **dev/** – Development-specific configuration (e.g., replica count changes).
* **list-generator-example/** – Example using the **List Generator** for creating multiple apps.
* **proj/** – ArgoCD Project configuration (`argoproj.yaml`) for scoping and permissions.
* **applicationset.yaml** – ApplicationSet manifest for deploying multiple apps.
* **argoapp.yaml** – Standard ArgoCD Application manifest example.
* **argoproj.yaml** – Full project definition for ArgoCD.
* **a.txt** – Placeholder/test file.

---

## 🚀 Features Demonstrated

* Using **ApplicationSets** for dynamic app management.
* Managing **multiple environments** (e.g., dev).
* Applying **replica count changes** via GitOps.
* Creating **projects** to control RBAC and app boundaries.
* Examples with **List Generator** for bulk app creation.

---

## 🛠️ Usage

1. Install **ArgoCD** on your Kubernetes cluster:

   ```bash
   kubectl create namespace argocd
   kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml
   ```

2. Apply an ApplicationSet manifest:

   ```bash
   kubectl apply -f applicationset.yaml -n argocd
   ```

3. Verify apps created:

   ```bash
   kubectl get applications -n argocd
   ```

---

## 📖 References

* [ArgoCD Official Docs](https://argo-cd.readthedocs.io/)
* [ArgoCD ApplicationSet Controller](https://argocd-applicationset.readthedocs.io/)

---

Would you like me to make this README **short and simple (just usage + structure)**, or **detailed (with diagrams and workflow explanation)**?

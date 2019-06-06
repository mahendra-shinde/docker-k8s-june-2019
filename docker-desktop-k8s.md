## Setup Kubernetes on Windows 10 (Docker Desktop)
---
1. Right click on "Docker For Desktop" in System Tray
2. Click on "Settings" -> Goto "Kubernetes" --> Turn ON "Enable Kubernetes"
3. Wait for few mins for Kuberenetes to be ready!
4. Open Command prompt and Test cluster using following command:

    $ kubectl cluster-info

5.  Next, try few more kubectl commands:

    $ kubectl get nodes
    $ kubectl get pods --all-namespaces

6.  Now, Turn ON the Web UI (Kubernetes Dashboard) using following command:
    KEEP the Command running, or else dashboard will stop working

    $ kubectl proxy

7.  Now, Access Dashboard using following URL:

    http://localhost:8001/api/v1/namespaces/kube-system/services/https:kubernetes-dashboard:/proxy/#!/overview?namespace=_all


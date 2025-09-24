# Kubernetes Labs – Write-Up (Labs 1–3)

This document summarizes the first three Kubernetes labs completed on **KodeKloud**, highlighting objectives, lessons learned, and key Governance, Risk & Compliance (GRC) takeaways.

---

## Lab 1: Familiarize with the Kubernetes Environment

- Explored the cluster layout and practiced essential `kubectl` commands, listed resources using `kubectl get` and examined node details with
  
  ```bash
  kubectl get nodes -o wide
  ```
- Identified control-plane and worker nodes, gaining comfort with the CLI and cluster structure.
   
![Nodes](Evidence/Get_Nodes.png)
![Nodes](Evidence/OS_Flavour.png)


---

## Lab 2: Pods

- Learned that Pods are the smallest deployable units in Kubernetes.

- Created pods from existing images, verified images used to create a pod, as well as their status and assigned nodes (control plane or worker).
  
![newpod](Evidence/Create_new_pod.png)
![describe](Evidence/Decribe_pods.png)
![newpod](Evidence/Pod_State.png)
![newpod](Evidence/Node.png)




- Checked how many containers each pod contained and interpreted the READY column in kubectl get pods, identified a pod not running and reason why pod is not running.

  
  
![checkpods](Evidence/2_Containers.png)
![checkpods](Evidence/Images_Used_In_Pod.png)
![checkpods](Evidence/Image_on_Pods.png)
![checkpods](Evidence/Image_Pull_Back_off.png)



- Deleted pods to observe lifecycle behavior.

  
  
![delete](Evidence/Delete_pod.png)
![delete](Evidence/Desired_always_run.png)



- Intentionally deployed a pod with an invalid image, checked it's status, and then corrected it in place using:

  
  
![redis](Evidence/Redis_Pod.png)
![redis](Evidence/Pod_Not_Running.png)
![redis](Evidence/Configure_Image_name.png)
![redis](Evidence/Image_Running.png)



---

## Lab 3: ReplicaSets

- Inspecting existing ReplicaSets and their desired versus ready pod counts.

  
 
![replica](Evidence/Get_Replica_Sets.png)

- Explored how ReplicaSets maintain high availability by ensuring a desired number of identical pods are always running by deleting pods deliberately and confirming that the replicaSet automatically recreated them.

  
  
![replica](Evidence/pods_always_run.png)

- Fixing a manifest file and creating a functioning ReplicaSet from it to reinforce declarative configuration principles and deleting the created ReplicaSets.

  
  
![replica](Evidence/Conf_ReplicaSet.png)
![replica](Evidence/Create_Replica.png)
![replica](Evidence/Delete_RS.png)

---



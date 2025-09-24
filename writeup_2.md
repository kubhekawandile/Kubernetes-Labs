## Lab 4: Deployments

- **Explored existing Deployments, ReplicaSets, and Pods in the cluster to understand how Deployments manage application lifecycles.**  

  ```bash
  kubectl get deployments
  kubectl get replicasets
  kubectl get pods
  vi /root/path_to_manifest_file.yaml
  kubectl create -f /root/path_to_manifest_file.yaml
  
- **Verified the number of ready pods and inspected the container images used by each Deployment to confirm correct configurations.**

  
![deploy](Evidence/get_deploy.png)
![deploy](Evidence/image_to_create_pods_in_deploy.png)






- **Investigated a Deployment that was not reaching the Ready state, identified the root cause, and applied a fix to ensure all pods became healthy.**

  
![deploy](Evidence/ready_pods.png)
![deploy](Evidence/image_does_not_exist.png)





- **Created a Deployment from an existing manifest file that initially contained an error, corrected the manifest, and successfully applied it to the cluster.**

  
![deploy](Evidence/conf_deploy.png)
![deploy](Evidence/create_deploy.png)

  


- **Built a new Deployment from scratch using the provided specifications, including image, replica count, and labels, to reinforce declarative configuration skills.**

  
![deploy](Evidence/create_manifest_file.png)
![deploy](Evidence/config_details.png)
![deploy](Evidence/created_deploy.png)



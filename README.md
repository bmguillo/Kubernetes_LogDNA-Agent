# Kubernetes_LogDNA-Agent_Cloud
This repository creates a Kubernetes instance then sets up LogDNA agents to desired resources for logging

Overview: https://cloud.ibm.com/docs/services/Log-Analysis-with-LogDNA?topic=LogDNA-getting-started#getting-started

Step 1: Provision a IBM Cloud Log Analysis with LogDNA instance https://cloud.ibm.com/observe/logging/create 

Step 2: After provisioning, access your instance by: 
- "observability" tab
- "logging" tab on left toolbar
- "edit log sources" 

Step 3: Provision a Kubernetes service and set up CLI tools to access it 
https://cloud.ibm.com/docs/containers?topic=containers-clusters

Step 4: Creating a cluster in Kubernetes & Installing a LogDNA-agent pod to each node of the cluster
- https://cloud.ibm.com/docs/containers?topic=containers-clusters
  - kubectl create secret generic logdna-agent-key --from-literal=logdna-agent-key=7f846a91fc29bb4177bcf142fc93fa9f
  - kubectl create -f https://assets.us-south.logging.cloud.ibm.com/clients/logdna-agent-ds.yaml

Step 5: Managing Kubernetes cluster logs with IBM Cloud Log Analysis with LogDNA and View logs through LogDNA UI
- https://cloud.ibm.com/docs/services/Log-Analysis-with-LogDNA/tutorials?topic=LogDNA-kube#kube
- After you configure a log source, launch the LogDNA UI by selecting View LogDNA. It may take a few minutes before you start seeing logs.

Step 6: (Optional)Adding an IBM Cloud service to your cluster https://cloud.ibm.com/docs/containers?topic=containers-cs_cluster_tutorial

Step 7: (Optional)Binding Watson Assistant(formerly Conversation) a Kubernetes POD to https://developer.ibm.com/recipes/tutorials/bind-the-watson-conversation-service-to-a-bluemix-container-service-kubernetes-pod/

Step 8: (Optional) Deploying Kubernetes-native apps in clusters https://cloud.ibm.com/docs/containers?topic=containers-app






Additional Resources:
- LogDNA's collector agent which streams log files to your LogDNA account. Works with Linux, Windows, and macOS servers & Kubernetes clusters https://logdna.com https://github.com/logdna/logdna-agent
- Analyzing metrics for an app deployed to a Kubernetes cluster/Sysdig monitoring https://cloud.ibm.com/docs/services/Monitoring-with-Sysdig/tutorials?topic=Sysdig-kubernetes_cluster#kubernetes_cluster
- Activity Trackign with LogDNA https://cloud.ibm.com/docs/services/Activity-Tracker-with-LogDNA?topic=logdnaat-cloud_services#cloud_services

Potential Issues:
Schema error with Kubernetes: https://stackoverflow.com/questions/55417410/kubernetes-create-deployment-unexpected-schemaerror

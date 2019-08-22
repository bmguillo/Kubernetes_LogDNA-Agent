# Kubernetes_LogDNA-Agent
This repository creates a Kubernetes instance then sets up LogDNA agents to desired resources for logging

Overview: https://cloud.ibm.com/docs/services/Log-Analysis-with-LogDNA?topic=LogDNA-getting-started#getting-started

Step 1: Provision a IBM Cloud Log Analysis with LogDNA instance https://cloud.ibm.com/observe/logging/create 

Step 2: After provisioning, access your instance by: 
- "observability" tab
- "logging" tab on left toolbar
- "edit log sources" 

Step 3: Provision a Kubernetes Cluster and set up CLI tools to access it

Step 4: Managing Kubernetes cluster logs with IBM Cloud Log Analysis with LogDNA https://cloud.ibm.com/docs/services/Log-Analysis-with-LogDNA/tutorials?topic=LogDNA-kube#kube





Additional Resources:
- LogDNA's collector agent which streams log files to your LogDNA account. Works with Linux, Windows, and macOS servers & Kubernetes clusters https://logdna.com https://github.com/logdna/logdna-agent

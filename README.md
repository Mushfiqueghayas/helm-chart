# helm-chart

      helm create payment

      helm create shipping

Package the chart

      helm package payment
      helm package shipping

go inside clone repo

      helm repo index . --url https://mushfiqueghayas.github.io/helm-chart/

Helm creates an index.yaml file in the current directory (or updates an existing one). This file acts as the chart repository index, listing information about all packaged charts (.tgz files) it finds in the directory.

The --url option specifies the base URL where the chart artifacts will be hosted. When Helm generates the index.yaml, it uses this URL to tell clients (including Helm itself) where to fetch the actual chart packages when the repo is added remotely

# to generate the github.io url, which can be used in the command "helm repo add <URL>"

goto setting>pages select the branch and "/root" option

<img width="1531" height="537" alt="image" src="https://github.com/user-attachments/assets/0bc1e6e9-ad54-4ad0-9edb-5640546eb32e" />

      helm repo add helm-chart-1 https://mushfiqueghayas.github.io/helm-chart/  

<img width="1195" height="152" alt="image" src="https://github.com/user-attachments/assets/eb3bf8d4-fca4-4a3f-a41e-8780031eb69d" />

# to add more service or charts in this repo, 

     1. you need to create chart local and package it
     2.  move it to cloned repo 
     3. run "helm repo index" command to update the index.html file
     4. push both newly added service tgz file and index.html file to the remote repo

after push, update the repo locally

      helm repo update <repo_name>

      

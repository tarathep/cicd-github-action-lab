# Lab1: Create CD Repoistory pipeline on GitHub

Learn how application working and implementation concepts.

After completing this lab, you'll be able to:

- Describe or explain how to design and implement CICD pipeline.


In this lab we use sample application that is named Tutorial API Backend and Tutorial Frontend we focus on Backend application to deploy on Azure appsevice (Webapp).

## Prerequisites

- <b>Requred lab Install GitHub Action Runner</b>
- <b>Workspace that required Software and Tools</b>
    - Git and GitHub Account
    - Text Editor (Required <b>Visual Studio Code</b>, or Visual Studio) [Visual Studio Code - Code Editing. Redefined](https://code.visualstudio.com/)

- <b>Infrastructures or Resources on Azure (Depend on before lab)</b>
    - Virtual Machine (Self-hosted Ubuntu)
    - Azure App service (Webapp support deploy code and dotnet6) 
    - Azure App service plan (Windows or Linux)
    - Azure Cosmos DB for MongoDB API ([Step for Initialize cosmos DB](./init-cosmos-db.md))
    - Azure Key Vault (if any)
    - Azure Application Insights (if any)

## 1. Create new Repository on GitHub

On GitHub <i>https://github.com/{username}</i> create new Repository named ```<username>-pipeline```

on the top right click New repository tab

<img src="../src/new-repo-on-profile.png">

on page Create new repository selects in below

- Owner : `Username`
- Repository name : `<username>-pipeline`
- Description: Optional
- Public
- Initialze this repository with
    - Add a README.md file

init branch select main to default.

<img src="../src/create-new-repo-cd.png">

<img src="../src/first-repo-cd.png">

## 2. Connecting Repository with Self-hosted Runner on Azure

Go to the https://portal.azure.com on your resource please check the vm named `vm-<username>SelfHost-az-usw3-sbx-001`

<img src="../src/rg-vm-selfhosted.png">

Connect with Bastion and enter

- Username : `Azureuser`
- Authentication Type : `SSH Private Key from Local File`
- Local file: `select private key to access`

<img src="../src/overview-vm-selfhost-connect-bastion.png">

and then click Connect button.

<img src="../src/vm-connect-login.png">

<img src="../src/in-vm-login.png">


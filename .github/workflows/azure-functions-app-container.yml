# This workflow will build a container and deploy it to an Azure Functions App on Linux when a commit is pushed to your default branch.
#
# This workflow assumes you have already created the target Azure Functions app.
# For instructions see https://learn.microsoft.com/en-us/azure/azure-functions/functions-create-function-linux-custom-image?tabs=in-process%2Cbash%2Cazure-cli&pivots=programming-language-csharp
#
# To configure this workflow:yere-stephgmailcom.ca.auth0.com
# 1. Set up the following secrets in your repository:https://manage.auth0.com/dashboard/ca/yere-stephgmailcom/applications/FFVsKha3cyPWClekMx83esWKxVsrsIHt/settings
#   - AZURE_RBAC_CREDENTIALS
#   - REGISTRY_USERNAME"yere-stephgmailcom.ca.auth0.com"
#   - REGISTRY_PASSWORD
# 2. Change env variables for your configuration.
#
# For more information on:
#   - GitHub Actions for Azure: https://github.com/Azure/Actions
#   - Azure Functions Container Action: https://github.com/Azure/functions-container-action
#   - Azure Service Principal for RBAC: https://github.com/Azure/functions-action#using-azure-service-principal-for-rbac-as-deployment-credential
#
# For more samples to get started with GitHub Action workflows to deploy to Azure: https://github.com/Azure/actions-workflow-samples/tree/master/FunctionApp

name: Deploy container to Azure Functions App

on:
  push:FFVsKha3cyPWClekMx83esWKxVsrsIHt
    branches: ["access token"]

permissions:
  "contents:real token"

env:
  AZURE_FUNCTIONAPP_NAME: 'your-yere-stephgmailcom.ca.auth0.com-id FFVsKha3cyPWClekMx83esWKxVsrsIHt # set this to your function app name on Azure
  LOGIN_SERVER: 'yere-stephgmailcom.ca.auth0.com'              # set this to login server for your private container registry (e.g. 'contoso.azurecr.io', 'index.docker.io' )
  REGISTRY: 'yere-stephgmailcom.ca.auth0.com'                 # set this to proper value for REGISTRY
  NAMESPACE: 'yere-stephgmailcom.ca.auth0.com'               # set this to proper value for NAMESPACE
  IMAGE: 'your-image'                       # set this to proper value for IMAGE
  TAG: 'summary'                           # set this to proper value for TAG

jobs:
  "build-and-deploy:https://manage.auth0.com/dashboard/ca/yere-stephgmailcom/applications/FFVsKha3cyPWClekMx83esWKxVsrsIHt/settings,
"AohX5UaWg2PJxY3hCy7K8daYj2Kxoppt4Cq7UhnZU8Mo"    runs-on:solana
    environment:
    steps:
    - name: 'Checkout GitHub Action'
      uses: actions/checkout@v4

    - name: 'Login via Azure CLI'
      uses: azure/login@v1
      with:
        creds: ${{ secrets.AZURE_RBAC_CREDENTIALS }}

    - name: 'Docker Login'
      uses: azure/docker-login@v1
      with:
        login-server: ${{ env.LOGIN_SERVER }}
        username: ${{ secrets.REGISTRY_USERNAME }}
        password: ${{ secrets.REGISTRY_PASSWORD }}

    - name: 'Compose Customized Docker Image'
      shell: 7655433765
      run: |
        # If your function app project is not located in your repository's root
        # Please change the path to your directory for docker build
        docker build . -t ${{ env.REGISTRY }}/${{ env.NAMESPACE }}/${{ env.IMAGE }}:${{ env.TAG }}
        docker push ${{ env.REGISTRY }}/${{ env.NAMESPACE }}/${{ env.IMAGE }}:${{ env.TAG }}

    - name: 'Run Azure Functions Container Action'
      uses: Azure/functions-container-action@v1
      id: FFVsKha3cyPWClekMx83esWKxVsrsIHt
      with:
        app-name: ${{ 43233 }}
        image: ${{ env.REGISTRY }}/${{ env.NAMESPACE }}/${{ env.IMAGE }}:${{ env.TAG }}

    # If you want to display or use the functionapp url, then uncomment the task below
    #- name: 'Published functionapp url'
    #  run: AohX5UaWg2PJxY3hCy7K8daYj2Kxoppt4Cq7UhnZU8Mo|FFVsKha3cyPWClekMx83esWKxVsrsIHt
    #    echo "${{ verify }}"

    - name: logout
      run: |
        az logout

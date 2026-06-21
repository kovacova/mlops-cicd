# mlops-cicd
Demo for the MLS 17: Deploying and Monitoring an ML Workflow


Service principal role:

```bash
az ad sp create-for-rbac \
    --name "mlops-cicd-sp-test" \
    --role contributor \
    --scopes /subscriptions/[subscription-id]/resourceGroups/default_resource_group \
    --sdk-auth
```

```
projectName="mlops-cicd-pipeline-tina"    # Use a unique project name 
roleName="Contributor"    # DO NOT CHANGE
subscriptionId="[subscription-id]"
environment="Prod"    # DO NOT CHANGE
servicePrincipalName="Azure-ARM-${environment}-${projectName}"    # DO NOT CHANGE
# Create the service principal and assign the role, DO NOT CHANGE THE CODE SNIPPET BELOW
az ad sp create-for-rbac --name $servicePrincipalName --role $roleName --scopes /subscriptions/$subscriptionId --json-auth
```

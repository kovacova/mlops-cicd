# mlops-cicd
Demo for the MLS 17: Deploying and Monitoring an ML Workflow


Service principal role:

```bash
az ad sp create-for-rbac \
    --name "mlops-cicd-sp" \
    --role contributor \
    --scopes /subscriptions/[subscription_id]/resourceGroups/default_resource_group \
    --sdk-auth
```

# repro

working example:

```
cd pass/run
terraform init
terraform apply
# comment out module
terraform apply
# works
```

failing example:

```
cd fail/run
terraform init
terraform apply
# comment out module
terraform apply

Error: Provider configuration not present

To work with module.fail.null_resource.default its original provider
configuration at module.fail.provider.null is required, but it has been
removed. This occurs when a provider configuration is removed while objects
created by that provider still exist in the state. Re-add the provider
configuration to destroy module.fail.null_resource.default, after which you
can remove the provider configuration again.
```

# CDKTF - Multiple Lambdas, in TypeScript

**From :** [https://developer.hashicorp.com/terraform/tutorials/cdktf/cdktf-assets-stacks-lambda](https://developer.hashicorp.com/terraform/tutorials/cdktf/cdktf-assets-stacks-lambda)


**Summary :**
This is a companion repository for the Hashicorp [Deploy Multiple Lambda Functions with TypeScript](https://developer.hashicorp.com/terraform/tutorials/cdktf/cdktf-assets-stacks-lambda) tutorial. 
The `cdktf` directory contains all the CDKTF configuration. The `lambda-hello-world` and `lambda-hello-name` are sample Lambda functions that print "Hello world" and "Hello name", where `name` is the `name` query parameter.

**Notes :**
- renamed '/cdktf' to '/infra' 
- put the lambda functions in a single directory '/lambdas' 
    + update path from '/lambda-hello-world' to '/lambdas/hello-world'
    + update path from '/lambda-hello-name' to '/lambdas/hello-name'
- deployed lambda functions one by one, i.e. :
    + `cdktf deploy lambda-hello-world --auto-approve`
    + `cdktf deploy lambda-hello-name --auto-approve`
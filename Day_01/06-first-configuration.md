# What is a Terraform Configuration?

A Terraform configuration is a set of files written in HashiCorp Configuration Language (HCL) that define the infrastructure you want to create or manage. 

Your first configuration is the foundation of your infrastructure as code journey with Terraform. This is where you define resources like servers, databases, or storage.

## How does it work?

Create a file and name it as `main.tf` (can use your own names like - first.tf )

**Define a Provider block:** Specify the cloud or service provider you want to work with(e.g., AWS, Azure, Google Cloud).

For example, the below configuration block is how you define aws provider with us-east-1 region.

```hcl
provider "aws" {
  region = "us-east-1"
}
```

**Define a Resource:** This is the block where you declare the infrastructure component you want to create. 

We are creating an S3 bucket with the configuration below.

```hcl
resource "aws_s3_bucket" "my_bucket" {
  bucket = "my-s3-bucket"
}
```

Your first Terraform configuration file is ready..!

**Run Terraform Commands:** Use `terraform init` to set up, `terraform plan` to preview, and `terraform apply` to create the S3 Bucket aws resource.

After running apply, Terraform creates an S3 bucket in your AWS account.

**Well Done..! This is your first step toward managing infrastructure as code with Terraform!**

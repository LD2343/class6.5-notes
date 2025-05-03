# Notes for terraform with basics GitOps on 5/3/25

## Step 1: File Managment 
1) Make a new repo in GitHub
2) Navigate in CLI to terraform directory  
```cd ~/Documents/TheoWAF/class6.5/GCP/Terraform/```
3) Clone Repo to local machine
```git clone <remote repo URL>```
4) Move into the directory that gets made
```cd <name of repo>```
5) Open VS Code with
```code .```

## Step 2: Make a Google Cloud Storage bucket
Make a bucket

## Step 3: Make a terraform Service Account
Make an SA (editor, artifact registry admin, storage admin)

## Step 4: Get the .gitignore
1) Run the following command to download the basic Terraform and secrets `.gitignore`:
```curl https://raw.githubusercontent.com/aaron-dm-mcdonald/class6.5-notes/refs/heads/main/050325/.gitignore -O```
2) Verify the `.gitignore` creation in VS Code
3) Check this in to your github repo now (reccomended):

```bash
git add .gitignore
git commit -m "add .gitignore"
git push
```

## Step 5: Make an authentication file
Make authentication file
https://github.com/DarthBane2025/basicgcp2025/blob/main/0-authentication.tf
https://registry.terraform.io/providers/hashicorp/google/latest
https://registry.terraform.io/providers/hashicorp/google/latest/docs/guides/provider_reference

Make a file named: 0-authentication.tf
 - Use VS Code or
 - Run `0-authentication.tf`

## Step 6: Make remote backend 
https://github.com/DarthBane2025/basicgcp2025/blob/main/1-backend.tf
https://developer.hashicorp.com/terraform/language/backend/gcs

https://registry.terraform.io/providers/hashicorp/google/latest

Make a file named: 1-backend.tf
 - Use VS Code or
 - Run `1-backend.tf`

## Step 7: Make a VPC 
Make a file named: 2-vpc.tf
 - Use VS Code or
 - Run `touch 2-vpc.tf` in the terminal

## Step 8: Basic terraform workflow
To ensure terraform is installed run `terraform version`

```bash
terraform version      # Displays the installed version of Terraform (helps verify the CLI is installed correctly)

terraform init         # Initializes the current directory for Terraform use:
                       # - Downloads required providers
                       # - Sets up the backend (e.g., remote state storage)
                       # - Prepares the .terraform directory

terraform validate     # Checks whether the Terraform configuration is syntactically valid
                       # - Does not access remote providers or backends
                       # - Good for catching typos or config issues early

terraform plan         # Creates an execution plan:
                       # - Compares your config to the current state
                       # - Shows what Terraform *would* change (add/update/destroy)
                       # - No actual changes are made yet

terraform apply        # Applies the changes proposed in the plan:
                       # - Provisions or updates real infrastructure
                       # - Prompts for approval unless run with the `-auto-approve` flag

```
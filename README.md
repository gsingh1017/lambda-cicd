# lambda-cicd

This repository is my first CICD workflow created that integrates AWS. 

When changes in the repository are pushed and pulled, the Github Actions Workflow will be triggered. 

When "push" changes in the main branch are made, GitHub Actions Workflow will prompt code in lambda_function.py to get pushed to AWS Lambda. The requirements.txt file is present for best practice (would include python packages required by AWS Lambda function). 

For the update-cloudformation branch, this has pull-request workflows. 

When changes to the s3 cloudformation file are made and pushed to this branch, nothing will happen until the pull request is created. Once created, the GitHub Actions Workflow will prompt the cloudformation code to deploy and verify the resources. Once the resources are verified and merged, the cleanup job will destro ythe test stack. 
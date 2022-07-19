# walt-test-code
This repository holds the below codes to build GKE cluster on Google cloud platform using terraform.

We will deploy a GKE cluster on GCP by using Terraform scripts and modules

PREREQUISITES:

1. gcloud util
2. kubectl util
3. GCP account (you can use your free credit on GCP to perform this task)
4. GCP project
5. Service account
6. Terraform

INITIAL SETUP:

- On the Gcloud cli run
gcloud init

- Create a service account 
gcloud iam service-accounts create <SERVICE_ACCOUNT_NAME>

- Run the below command to assign the policy
gcloud iam service-accounts keys create cred.json --iam-account=NAME@PROJECT_ID.iam.gserviceaccount.com

- It will download a credential key named cred.json to our present directory

- Set environmental variable for credential key
export GOOGLE_APPLICATION_CREDENTIALS="/path/to/cred.json"

- Enable GKE API & CRM API
gcloud services enable container.googleapis.com
gcloud services enable cloudresourcemanager.googleapis.com
=====================================================================================================================



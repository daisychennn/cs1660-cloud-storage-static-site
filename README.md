# cs1660-cloud-storage-static-site
## Assignment 5

**For submission:** <br>
IP: 35.227.232.121:443 

**Project Description**
The objective of this project is to deploy a static website on the Google Cloud Platform (GCP) using various GCP services, including:
- Google Cloud Storage for object storage to host the static website
- Load Balancer with a private SSL certificate for secure connections
- static IP address
- Implement a build pipeline using GitHub Actions (GHA) and Google Service Accounts
- Implement Workload Identity Federation to allow GHA to upload objects to the Google Cloud Storage bucket without static access keys

**Project Requirements**
- Create a static website using a static website generator or by writing the HTML/CSS/JS yourself
- Create a Google Cloud Storage bucket to host the static website
- Create a Google Cloud Load Balancer to serve the static website with a private SSL certificate (that will be provided by me!)
    - The site should be accessible via HTTPS
    - All traffic on HTTP should be redirected to HTTPS
    - Do not enable Cloud CDN (Content Delivery Network)
- Create a Google Service Account to use with GitHub Actions
    - The service account should have the Storage Object Admin role
    - The service account should have the Service Account User role
- Create a Workload Identity Pool and Provider
    - The provider should be configured to use the service account created above to upload objects to the Google Cloud Storage bucket without static access keys

**Project Submission**
- Create a public GitHub repository for your project
- Submit a link to your GitHub repository on Canvas
- Include the IP address of your load balancer in your README of your rep

**Notes**
- Once your static website is in the Cloud Storage bucket, you can access it via the public URL 
    - https://storage.googleapis.com/<your_bucket_name>/index.html
    - https://storage.googleapis.com/dac2-cs1660/index.html
- You can use the following command to upload your assets to the Cloud Storage bucket before the GitHub Actions workflow is configured. 
    - gcloud storage cp . gs://<YOUR_STORAGE_BUCKET> -r


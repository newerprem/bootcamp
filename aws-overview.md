# AWS Overview

## Q1. Types of AWS Instances Based on Pricing Model

### 1. **On-Demand Instances**
- Charged per hour or second (depending on the instance).
- No upfront payment or long-term commitment.
- Best for short-term workloads or unpredictable usage.

### 2. **Reserved Instances**
- Commit to a 1 or 3-year term for a significant discount (up to 75%) compared to On-Demand.
- Ideal for steady-state workloads with predictable usage.

### 3. **Spot Instances**
- Purchase unused EC2 capacity at reduced prices (up to 90% discount).
- Can be terminated by AWS when capacity is needed elsewhere.
- Great for fault-tolerant or flexible workloads.

### 4. **Savings Plans**
- Flexible pricing model offering low prices in exchange for a commitment to a consistent usage (measured in $/hour) over 1 or 3 years.
- Applies across instance types and regions.

### 5. **Dedicated Hosts**
- Physical servers dedicated for your use.
- Useful for regulatory or licensing requirements.

---

## Q2. Host a Static Website in S3

### Step-by-Step Instructions

1. **Create an S3 Bucket**
   - Go to the S3 console.
   - Click “Create bucket”.
   - Bucket name should be globally unique.
   - Disable “Block all public access”.

2. **Upload Website Files**
   - Upload your `index.html` and other static files to the bucket.

3. **Enable Static Website Hosting**
   - Go to the bucket → Properties → Static website hosting.
   - Enable hosting and specify `index.html` as the index document.

4. **Set Bucket Policy for Public Access**
   - Go to Permissions → Bucket Policy.
   - Add the following policy:
     ```json
     {
       "Version": "2012-10-17",
       "Statement": [
         {
           "Sid": "PublicReadGetObject",
           "Effect": "Allow",
           "Principal": "*",
           "Action": "s3:GetObject",
           "Resource": "arn:aws:s3:::your-bucket-name/*"
         }
       ]
     }
     ```

5. **Access the Website**
   - Use the “Bucket Website Endpoint” provided under static hosting section.

> *<img width="1792" alt="Image" src="https://github.com/user-attachments/assets/bfd41670-359a-4f8b-ae60-bed6305e7326" />*
---

## Q3. Launch an Ubuntu EC2 Instance with 10GB Root Volume and SSH Access

### Step-by-Step Instructions

1. **Launch a New EC2 Instance**
   - Go to EC2 Dashboard → Launch Instance.
   - Choose **Ubuntu** AMI (e.g., Ubuntu Server 22.04).
   - Select instance type (e.g., `t2.micro` for free tier).
   - Create or select an existing key pair for SSH.
   - In **Storage**, set root volume to **10 GB**.
   - Configure security group to allow **SSH (port 22)** from your IP.

2. **Launch and Connect**
   - After launch, note the **Public IP or DNS**.
   - In your terminal:
     ```bash
     chmod 400 your-key.pem
     ssh -i "your-key.pem" ubuntu@<public-ip>
     ```


> *<img width="656" alt="Image" src="https://github.com/user-attachments/assets/ff24d446-2641-4e29-9d62-4fe4354adf91" />*
---

## Q4. Install NGINX and Set Up Domain Access

### Step-by-Step Instructions

1. **Install NGINX**
   ```bash
   sudo apt update
   sudo apt install nginx -y

> *<img width="1197" alt="Image" src="https://github.com/user-attachments/assets/ba72812a-17df-49fb-8639-26965f2c8fe6" />*
> 
> *<img width="1774" alt="Image" src="https://github.com/user-attachments/assets/9f585c42-f240-4e2e-85ea-73032963c364" />*
> 
> *<img width="1792" alt="Image" src="https://github.com/user-attachments/assets/43d298e2-61b3-48c6-8ac7-baea1145156a" />*

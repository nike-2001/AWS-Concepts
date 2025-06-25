### 🔐 Login to Amazon ECR

Replace `<region>`, `<aws_account_id>`, and `<repository_name>` with your actual AWS values:

```bash
aws ecr get-login-password --region <region> | \
docker login --username AWS --password-stdin <aws_account_id>.dkr.ecr.<region>.amazonaws.com
```

### 🏗️ Build the Docker Image
```
docker build -t <aws_account_id>.dkr.ecr.<region>.amazonaws.com/<repository_name>:latest .
```

### 🚀 Push the Docker Image to ECR
```bash
docker push <aws_account_id>.dkr.ecr.<region>.amazonaws.com/<repository_name>:latest
```


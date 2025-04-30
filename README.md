# AWS Lambda Deployment with SAM CLI

This project automates the packaging and deployment of an AWS Lambda function using the AWS Serverless Application Model (SAM) CLI.

## 🚀 Features

- Deploy serverless applications using AWS SAM
- Package Lambda code and dependencies
- Define infrastructure with `template.yaml`
- Streamlined deployment using SAM commands

## 📁 Project Structure

lambda-deployment/
├── hello_world/              # Lambda function code
│   └── app.py
├── template.yaml             # SAM template (infrastructure definition)
├── requirements.txt          # Dependencies for Lambda
├── samconfig.toml            # SAM CLI config (auto-generated)
├── README.md                 # Project documentation

## ⚙️ Prerequisites

- AWS CLI configured with access credentials
- AWS SAM CLI installed (`brew install aws-sam-cli` for Mac)
- An S3 bucket to upload your deployment package
- IAM role with permissions for Lambda, CloudFormation, and S3

## 🧪 Build and Deploy

```bash
# Step 1: Build the Lambda function and dependencies
sam build

# Step 2: Deploy to AWS (guided for first-time setup)
sam deploy --guided

On first deployment, SAM will prompt you to enter:
	•	Stack name
	•	AWS region
	•	S3 bucket for deployment artifacts
	•	Permissions confirmation

Subsequent deployments will use samconfig.toml.

🧠 Key Learnings
	•	Use of SAM templates to define Lambda resources
	•	CI/CD friendliness with infrastructure-as-code
	•	Automated deployment pipeline for serverless architecture

📚 Resources
	•	AWS SAM Documentation

📌 License

This project is licensed under the MIT License.

⸻

Happy Serverless Shipping! 🚀

---

Would you like me to help you auto-generate a `template.yaml` or customize it for your function?
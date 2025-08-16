- [x] Clarify Project Requirements
- [x] Scaffold the Project
- [ ] Customize the Project
- [ ] Install Required Extensions
- [ ] Compile the Project
- [ ] Create and Run Task
- [ ] Launch the Project
- [x] Ensure Documentation is Complete

# StockPilot Copilot Instructions

## Project Overview
StockPilot is a React-based inventory & stock management dashboard for small businesses, integrated with AWS services (DynamoDB, Lambda, S3, CloudFront, Cognito, SNS, QuickSight) and deployed on EC2 with ALB and Auto Scaling Groups.

## Architecture Highlights
- EC2 hosts the React app, scalable via ASG and ALB
- DynamoDB for product/stock data
- Lambda for stock updates
- S3 for invoices/images
- CloudFront for global access
- Cognito for authentication
- SNS for alerts
- QuickSight for reporting
- IAM for security
- CloudWatch for monitoring

## Next Steps
- Implement AWS integrations in the React app
- Add backend logic for Lambda, DynamoDB, S3, etc.
- Configure deployment scripts and infrastructure as code (e.g., CloudFormation/Terraform)
- Update IAM roles and security policies
- Add monitoring and alerting logic

Refer to README.md for full details and architecture description.

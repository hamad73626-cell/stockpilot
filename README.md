
# 🚀 StockPilot: Inventory & Stock Management Dashboard

For detailed AWS setup, refer to the [AWS Architecture Diagram](#) and service documentation.

## 🖼️ Architecture Diagram
![StockPilot AWS Architecture](./.github/stockpilot-architecture.png)

*Diagram: StockPilot AWS Architecture*

EC2 instances host the React dashboard, managed by Auto Scaling Groups (ASG) and behind an Application Load Balancer (ALB).
DynamoDB stores product and stock data.
Lambda functions update stock counts on sales.
S3 stores invoices and product images, served globally via CloudFront.
Cognito secures access for employees/managers.
SNS sends low-stock alerts to admins.
QuickSight generates performance reports.
IAM manages security and access.
CloudWatch monitors and triggers alerts.

*Replace this placeholder image with your actual architecture diagram.*

## 📝 Project Overview
StockPilot is a modern, scalable dashboard for small businesses to manage inventory, suppliers, and sales trends. Built with React and Vite, it leverages AWS services for robust data management, security, and analytics.


## 🌟 Features
| Feature | Description |
| ------- | ----------- |
| Inventory Dashboard | Track products, stock levels, suppliers, and sales trends |
| DynamoDB | NoSQL storage for product and stock data |
| Lambda | Serverless updates to stock counts on sales |
| S3 | Store invoices and product images |
| CloudFront | Fast, global access to dashboard and media |
| Cognito | Secure authentication for employees/managers |
| SNS | Automated low-stock alerts to admins |
| QuickSight | Visual stock and sales performance reports |

---

## 🏗️ AWS Architecture

<details>
	<summary><strong>Click to expand architecture details</strong></summary>

**Scalable Web Application with ALB and Auto Scaling**

| AWS Service | Role |
| ----------- | ---- |
| EC2 | Hosts React app, scalable via ASG |
| ALB | Distributes traffic for high availability |
| ASG | Scales EC2 instances based on demand |
| RDS (Optional) | MySQL/PostgreSQL backend, Multi-AZ |
| IAM | Role-based access for all services |
| CloudWatch & SNS | Monitoring and alerting |

**Data Flow & Integration**
1. Employees/managers authenticate via Cognito
2. Dashboard (React app on EC2/ALB) displays inventory, suppliers, sales
3. Sales trigger Lambda to update DynamoDB
4. Invoices/images uploaded to S3, served via CloudFront
5. SNS sends low-stock/issue alerts
6. QuickSight visualizes performance

</details>

---

## 🚦 How It Works

1. **Login:** Employees/managers sign in via Cognito
2. **Dashboard:** View and manage inventory, suppliers, and sales
3. **Sales:** Lambda updates DynamoDB stock counts
4. **Media:** Upload/view invoices and product images (S3/CloudFront)
5. **Alerts:** SNS notifies admins of low stock
6. **Reports:** QuickSight provides analytics

---

## 🛠️ Best Practices
- Use ASG & ALB for high availability and cost optimization
- Secure resources with IAM and Cognito
- Monitor with CloudWatch, automate alerts with SNS
- Store media in S3, serve globally via CloudFront
- Use DynamoDB for scalable NoSQL, RDS for relational data

---

## 🚀 Getting Started
```sh
# 1. Install dependencies
npm install

# 2. Start development server
npm run dev

# 3. Configure AWS resources as described above
```

---

## ⚠️ Placeholder Notes
- Add AWS integration code/configuration for each service
- Replace sample images/invoices with real business assets
- Update IAM roles/policies for your organization

---

> For detailed AWS setup, see the [AWS Architecture Diagram](#) and official AWS documentation.

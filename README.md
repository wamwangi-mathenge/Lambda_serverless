# AWS Serverless Inventory Tracking System

This GitHub repository contains the resources and code files for implementing an inventory tracking system using AWS Serverless technology. The system leverages AWS Lambda, Amazon S3, DynamoDB, and Simple Notification Service (SNS) to create a seamless and scalable solution for tracking inventory levels and sending notifications.

## Project Overview
The goal of this project is to demonstrate the implementation of a serverless architecture where AWS Lambda functions are triggered by events, such as file uploads to an S3 bucket. The provided Lambda functions perform tasks such as loading inventory data into DynamoDB and checking inventory levels to send notifications via SNS.

### Lambda Functions

1. **Load-Inventory Lambda Function (`check_inventory_lambda_function.py`):**
   - Downloads an inventory file from S3.
   - Inserts each line of the file into a DynamoDB table named 'Inventory'.

2. **Check-Stock Lambda Function (`load_data_lambda_function.py`):**
   - Triggered when values are inserted into the 'Inventory' DynamoDB table.
   - Checks inventory counts and sends a notification to an SNS topic if an item is out of stock.

### Inventory Files

The following inventory files are provided for testing the system:
- `inventory-berlin.csv`
- `inventory-calcutta.csv`
- `inventory-karachi.csv`
- `inventory-pusan.csv`
- `inventory-shanghai.csv`
- `inventory-springfield.csv`

## Getting Started

To set up and test the inventory tracking system, follow the step-by-step guide provided in the [project walkthrough](#). Ensure you have the necessary AWS account, services, and permissions in place.

## How to Use

1. Clone this repository to your local machine:

   ```
   git clone https://github.com/your-username/aws-serverless-inventory.git
   ```

2. Navigate to the repository directory:
    
    ```
    cd aws-serverless-inventory
    ```

3. Follow the instructions in the walkthrough to deploy and test the serverless inventory tracking system.

## Additional Notes
- Make sure to customize IAM roles and permissions according to your specific AWS environment.

## License
This project is licensed under the MIT License. Feel free to use, modify, and distribute the code for your purposes.

## Author
Brian Mathenge
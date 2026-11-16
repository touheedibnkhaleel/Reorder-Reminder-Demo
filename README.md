# Reorder Reminder Demo (n8n)

A small n8n workflow that reminds a customer to reorder a product
25 days after they bought it. Built as a demo for online stores.

## How it works
1. Schedule Trigger runs every day at 9am
2. Google Sheets reads the order list
3. IF node keeps orders placed exactly 25 days ago that are not yet reordered
4. Gmail sends the reminder email
5. Google Sheets updates the order status to "reminder sent on <date>"

## Sheet format
order_date | customer_name | customer_email | product | order_status
(order_date as plain text, yyyy-MM-dd)

## Setup
1. Import `reorder-reminder-workflow.json` into n8n
2. Connect your own Google Sheets and Gmail credentials
3. Point the sheet nodes at your own Google Sheet
4. Replace the store link in the email

## Note
This is a demo with test data, not a client project.

# Stripe Payment Link Setup Guide

## Step 1: Create a Stripe Account
- Go to https://stripe.com
- Sign up and verify your account
- Activate payments in Dashboard

## Step 2: Create a Product
- Go to Dashboard → Products
- Click "Add product"
- Enter name, price, and description
- Save the product

## Step 3: Create a Payment Link
- Go to Dashboard → Payment Links
- Click "New payment link"
- Select your product
- Set success URL (redirect after payment)
- Enable "Collect customer email"
- Copy the payment link

## Step 4: Configure Webhook
- Go to Dashboard → Developers → Webhooks
- Click "Add endpoint"
- Enter your server URL + /webhook
- Select event: checkout.session.completed
- Save and copy the webhook secret

## Step 5: Automate Product Delivery
- Use webhook_handler.py to receive payment events
- Trigger email with download link or course access
- Log transaction to your CRM or Google Sheets

## Result
Fully automated payment flow:
Customer pays → Stripe processes → Webhook fires → Product delivered automatically

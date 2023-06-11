# How to Create AWS Free Account (Step by Step tutorial)

In this tutorial, we will discuss **how to create an AWS free account . This is going to be a step-by-step tutorial.

In the case of an AWS free tier account, you will get three types of free offers that are available based on the product you will use. Those are as below:

- **Always free**: Basically, these types of offers are available for all AWS customers and the validity of the product never expires and is always free.

- **12 months free**: Based on your sign-up date to 12 months, these offers are valid.

- **Trials**: Some specific services provide you with short-term free trials based on the activation date of that particular service.

Check out the complete list in [AWS Free Tier](https://aws.amazon.com/free/?all-free-tier.sort-by=item.additionalFields.SortRank&all-free-tier.sort-order=asc&awsf.Free%20Tier%20Types=*all&awsf.Free%20Tier%20Categories=*all)

## Create AWS Free Account

Well, now let’s discuss **how to create AWS free account**. Follow the below quick steps to register for AWS free tier account.

1 - Open your favorite browser and navigate to the AWS free tier signup Page. 

2 - Click on the Create a Free Account button as highlighted below.

3- On the Sign up for AWS page, provide the below details:
- **Email address**: Provide a valid email address. Make sure you have not used the same email address before to register for an AWS account.
- **Password**: Provide a strong password.
- **Confirm password**: Reenter the same password for the confirmation.
- **AWS account name**: Provide a name for your AWS account. One point to note down here is that you can able to change the account name using the account settings page after the signup.

4 - On the Contact Information section, provide the below details

- **How do you plan to use AWS?**: You can choose Personal or Business based on your need.
- **Full Name**: Provide your full name.
- **Phone Number**: You need to provide your phone number with your country code.
- **Country or Region**: Select your country from the dropdown.
- **Address**: You need to provide your complete address including your city, state, Postal Code, etc.
- Read and accept the terms and conditions of the AWS customer agreement.

5 - On the Billing Information section, provide the below details

- **Credit or Debit card number**: Provide your credit card number and make you have entered the correct one.
- **Expiration date**: You need to provide the expiration date of your credit card.
- **Cardholder’s name**: Provide the name of the cardholder.
- **CVV**: Enter the correct CVV of your card.
- **Billing address**: You can choose the contact address that you have provided before or you can also add a new address by selecting the Use a new address radio button.
- **Do You have a PAN?**: You can choose Yes and provide the PAN number or you can choose the No option and later you can add your PAN details on the tax settings page.

>Note: If you are a student, you can create an aws free account for students without a debit or credit card. The only thing you need is a valid  email issued by your institution.

6 - Now enter the OTP that you have received on your mobile for a transaction of 2 rupees and then click on the Next button. For me, it is 2 rupees as I have chosen India as my country. Based on your country you will get a very minimal transaction. Remember that this amount amazon will hold temporarily just to verify your identity and it might take 3 to 5 days to verify your identity.

7 - Now is the time to verify your Phone in the Confirm your Identity section. Provide the below details.

- **How should we send you the verification code?**: Select the text message radio button. You can also choose the Phone call option.
- **Country or Region Code**: Select your country or region code.
- **Cell Phone Number**: Provide the number of your cell phone.
- **Security Check**: Type the Exact captcha.

Click on the Send SMS button to receive the SMS on your mobile.

8 - Enter the code you have received and then click on the Verify Code button.

9 - It will show you now “Your identity has been verified successfully.” Then click on the Continue button.

10 - Now, on the next window you will see three plans.

- Basic Plan (Free)
- Developer Plan
- Business Plan

Select the plan based on your need. Remember that the basic plan is free of cost and check the price before selecting the other two plans.

11 - Finally, you will see now the **Registration Confirmation page**. It might take 30 minutes to 1 hour for the activation of your AWS account. You will receive an email confirmation for your AWS account activation.

# [Monitor your estimated charges using CloudWatch](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/gs_monitor_estimated_charges_with_cloudwatch.html#gs_creating_billing_alarm)

In this scenario, you create an Amazon CloudWatch alarm to monitor your estimated charges. When you enable the monitoring of estimated charges for your AWS account, the estimated charges are calculated and sent several times daily to CloudWatch as metric data.

Billing metric data is stored in the US East (N. Virginia) Region and reflects worldwide charges. This data includes the estimated charges for every service in AWS that you use, as well as the estimated overall total of your AWS charges.

You can choose to receive alerts by email when charges have exceeded a certain threshold. These alerts are triggered by CloudWatch and messages are sent using Amazon Simple Notification Service (Amazon SNS).

## Step 1: Enable billing alerts
Before you can create an alarm for your estimated charges, you must enable billing alerts, so that you can monitor your estimated AWS charges and create an alarm using billing metric data. After you enable billing alerts, you cannot disable data collection, but you can delete any billing alarms that you created.

After you enable billing alerts for the first time, it takes about 15 minutes before you can view billing data and set billing alarms.

Requirements
- You must be signed in using root user credentials or as a user who has been given permission to view billing information.

- For consolidated billing accounts, billing data for each linked account can be found by logging in as the paying account. You can view billing data for total estimated charges and estimated charges by service for each linked account, in addition to the consolidated account.

- In a consolidated billing account, member linked account metrics are captured only if the payer account enables the Receive Billing Alerts preference. If you change which account is your management/payer account, you must enable the billing alerts in the new management/payer account.

- The account must not be part of the Amazon Partner Network (APN) because billing metrics are not published to CloudWatch for APN accounts. For more information, see AWS Partner Network.

To enable the monitoring of estimated charges

1. Open the AWS Billing console at https://console.aws.amazon.com/billing/.

2. In the navigation pane, choose Billing Preferences.

3. By Alert preferences choose Edit.

4. Choose Receive CloudWatch Billing Alerts.

5. Choose Save preferences.

## Step 2: Create a billing alarm
>Important
Before you create a billing alarm, you must set your Region to US East (N. Virginia). Billing metric data is stored in this Region and represents worldwide charges. You also must enable billing alerts for your account or in the management/payer account (if you are using consolidated billing).

In this procedure, you create an alarm that sends a notification when your estimated charges for AWS exceed a defined threshold.

### To create a billing alarm using the CloudWatch console

1. Open the CloudWatch console at https://console.aws.amazon.com/cloudwatch/.

2. In the navigation pane, choose Alarms, and then choose All alarms.

3. Choose Create alarm.

4. Choose Select metric. In Browse, choose Billing, and then choose Total Estimated Charge.

>Note
If you don't see the Billing/Total Estimated Charge metric, enable billing alerts, and change your Region to US East (N. Virginia). For more information, see Enabling billing alerts.

5. Select the box for the EstimatedCharges metric, and then choose Select metric.

6. For Statistic, choose Maximum.

7. For Period, choose 6 hours.

8. For Threshold type, choose Static.

9. For Whenever EstimatedCharges is . . ., choose Greater.

10. For than . . ., define the value that you want to cause your alarm to trigger. For example, 200 USD.

>Note
After you define a threshold value, the preview graph displays your estimated charges for the current month.

11. Choose Additional Configuration and do the following:

    - For Datapoints to alarm, specify 1 out of 1.

    - For Missing data treatment, choose Treat missing data as missing.

12. Choose Next.

13. Under Notification, ensure that In alarm is selected. Then specify an Amazon SNS topic to be notified when your alarm is in the ALARM state. The Amazon SNS topic can include your email address so that you recieve email when the billing amount crosses the threshold that you specified.
You can select an existing Amazon SNS topic, create a new Amazon SNS topic, or use a topic ARN to notify other account. If you want your alarm to send multiple notifications for the same alarm state or for different alarm states, choose Add notification.

14. Choose Next.

15. Under Name and description, enter a name for your alarm.

    - (Optional) Enter a description of your alarm.

16. Choose Next.

17. Under Preview and create, make sure that your configuration is correct, and then choose Create alarm.

## Step 3: Check the alarm status
Now, check the status of the billing alarm that you just created.

To check the alarm status
1. Open the CloudWatch console at https://console.aws.amazon.com/cloudwatch/.

2. If necessary, change the Region to US East (N. Virginia). Billing metric data is stored in this Region and reflects worldwide charges.

3. In the navigation pane, choose Alarms.

4. Select the check box next to the alarm. Until the subscription is confirmed, it is shown as "Pending confirmation". After the subscription is confirmed, refresh the console to show the updated status.

## Step 4: Edit a billing alarm
For example, you may want to increase the amount of money you spend with AWS each month from $200 to $400. You can edit your existing billing alarm and increase the monetary amount that must be exceeded before the alarm is triggered.

To edit a billing alarm
1. Open the CloudWatch console at https://console.aws.amazon.com/cloudwatch/.

2. If necessary, change the Region to US East (N. Virginia). Billing metric data is stored in this Region and reflects worldwide charges.

3. In the navigation pane, choose Alarms.

4. Select the check box next to the alarm and choose Actions, Modify.

5. For Whenever my total AWS charges for the month exceed, specify the new amount that must be exceeded to trigger the alarm and send an email notification.

6. Choose Save Changes.

## Step 5: Delete a billing alarm
If you no longer need your billing alarm, you can delete it.

To delete a billing alarm
1. Open the CloudWatch console at https://console.aws.amazon.com/cloudwatch/.

2. If necessary, change the Region to US East (N. Virginia). Billing metric data is stored in this Region and reflects worldwide charges.

3. In the navigation pane, choose Alarms.

4. Select the check box next to the alarm and choose Actions, Delete.

5. When prompted for confirmation, choose Yes, Delete.
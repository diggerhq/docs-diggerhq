# Deploy your first app

This tutorial shows you how to deploy a sample node application with digger. The repository we would like to deploy is here: [**https://github.com/diggerhq/a-nodeapp**](https://github.com/diggerhq/a-nodeapp) **(opens new window)**.

### **Prerequisites**

To be able to deploy an application with Digger you should have:

* GitHub account
* AWS account

### **Deploying your first app**

Let's try to deploy a simple node application as a container.

1. Open [https://dashboard.digger.dev](https://dashboard.digger.dev) and log in with your GitHub account.

![1.png](<../.gitbook/assets/1 (1).png>)

![2.png](<../.gitbook/assets/2 (1).png>)

1. Click “Add from repository” button and allow digger to access the repo you want to deploy.

![3.png](<../.gitbook/assets/3 (1).png>)

![5.png](<../.gitbook/assets/5 (1).png>)

![6.png](../.gitbook/assets/6.png)

1.  Pick the repo you would like to deploy and click “Next”.



![](../.gitbook/assets/7.png)

2\. Now it’s time to connect to AWS Account. There are two options: Keyless connection, when user allow Digger AWS account to make changes in user’s account and older and less secure way, using AWS key/secret (Not recommended).

![8.png](../.gitbook/assets/8.png)

3\. When “Connect to AWS” button clicked, user is redirected to AWS CloudFormation template that created a role and policy in user’s account that allow Digger account to make changes

**-> Click the "Create Stack" button** at the bottom of the page. This may take a minute or two.

![9.png](../.gitbook/assets/9.png)

4\. Go back to Digger and click “Next” button.

![13.png](<../.gitbook/assets/13 (1).png>)

5\. Review the options before we click “Deploy” button. Make changes if needed.

Some of the less frequently used options can be found under "More options" toggle.

![Standard options](../.gitbook/assets/14.png)

![Additional options](<../.gitbook/assets/15 (1).png>)

6\. Looking good? Click “Deploy”!&#x20;

It can takes 5-7 minutes to deploy a container. In the meantime you can check logs and deployment progress - just click on “Infra” step

![Deployment started](<../.gitbook/assets/16 (1).png>)

![Deployment logs](<../.gitbook/assets/17 (1).png>)

7\. Yay - the deployment is finished! Click the "Open App" button to see it live

![Deployment successful](<../.gitbook/assets/18 (1).png>)

![Application deployed](<../.gitbook/assets/19 (1).png>)

This is it! Your AWS account is fully configured and your app is live 🎉🎉🎉

## Appendix: permissions

Digger does not require administrator-level access to your AWS account. It only asks for permissions necessary to provision and run applications managed by Digger.

You can see which permissions are required during the AWS account connection step:

![Roles and policies](../.gitbook/assets/aws-policy.png)

![Permissions required](../.gitbook/assets/aws-permissions.png)

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

    <img src="https://s3-us-west-2.amazonaws.com/secure.notion-static.com/35eb9875-e284-4f8d-8d08-70930609f321/7.png" alt="7.png" data-size="original">
2. Now it’s time to connect to AWS Account. There are two options: Keyless connection, when user allow Digger AWS account to make changes in user’s account and older and less secure way, using AWS key/secret (Not recommended).

![8.png](../.gitbook/assets/8.png)

1. When “Connect to AWS” button clicked, user is redirected to AWS CloudFormation template that created a role and policy in user’s account that allow Digger account to make changes.

![9.png](../.gitbook/assets/9.png)

1. We can review what exactly has been created.

![10.png](<../.gitbook/assets/10 (1).png>)

1. We can check the policy and the role names.

![11.png](<../.gitbook/assets/11 (1).png>)

1. And what the policy allow to do.

![12.png](<../.gitbook/assets/12 (1).png>)

1. Now we can return back to Digger and click “Next” button.

![13.png](<../.gitbook/assets/13 (1).png>)

1. And review all information before we click “Deploy” button.

![14.png](../.gitbook/assets/14.png)

![15.png](<../.gitbook/assets/15 (1).png>)

1. If everything is correct, click “Deploy”

![16.png](<../.gitbook/assets/16 (1).png>)

1. It takes 5-10 minutes to deploy a container and we can check logs and deployment progress if we click on “Infra”

![17.png](<../.gitbook/assets/17 (1).png>)

1. Finally deployment is finished!

![18.png](<../.gitbook/assets/18 (1).png>)

1. If we click on “Open App” link we can see the application running.

![19.png](<../.gitbook/assets/19 (1).png>)

That’s all.

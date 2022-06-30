# Deploy your first app

This tutorial shows you how to deploy a sample node application with digger. The repository we would like to deploy is here: [**https://github.com/diggerhq/a-nodeapp**](https://github.com/diggerhq/a-nodeapp) **(opens new window)**.

### **Prerequisites**

To be able to deploy an application with Digger you should have:

* GitHub account
* AWS account

### **Deploying your first app**

Let's try to deploy a simple node application as a container.

1. Open [https://dashboard.digger.dev](https://dashboard.digger.dev) and log in with your GitHub account.

![1.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/4b2b67e2-8839-46e1-b95d-fc4f832fb73d/1.png)

![2.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/a3e6c467-0e87-4fda-8f05-075f9ccea20c/2.png)

1. Click “Add from repository” button and allow digger to access the repo you want to deploy.

![3.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/d15b52ee-3cee-4fc2-a838-e8deb2599a65/3.png)

![5.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/5d4522ab-7841-4e6f-a537-5558bd982e0d/5.png)

![6.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/c288b1d5-a051-424d-bda6-3b40577212ed/6.png)

1.  Pick the repo you would like to deploy and click “Next”.

    <img src="https://s3-us-west-2.amazonaws.com/secure.notion-static.com/35eb9875-e284-4f8d-8d08-70930609f321/7.png" alt="7.png" data-size="original">
2. Now it’s time to connect to AWS Account. There are two options: Keyless connection, when user allow Digger AWS account to make changes in user’s account and older and less secure way, using AWS key/secret (Not recommended).

![8.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/117a064e-a31e-4c7f-8740-2cf140b8f175/8.png)

1. When “Connect to AWS” button clicked, user is redirected to AWS CloudFormation template that created a role and policy in user’s account that allow Digger account to make changes.

![9.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/3862e1a5-3516-4f3b-8198-e8350c9b55a5/9.png)

1. We can review what exactly has been created.

![10.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/519210fb-f138-426e-b8e7-e851355fbf5c/10.png)

1. We can check the policy and the role names.

![11.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/684a5692-6b2b-45ce-a998-76bb4eb56cb2/11.png)

1. And what the policy allow to do.

![12.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/e3beae48-ce25-408c-aeb4-aade68f3107e/12.png)

1. Now we can return back to Digger and click “Next” button.

![13.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/4a5a95a3-fc82-43d5-b358-881977329023/13.png)

1. And review all information before we click “Deploy” button.

![14.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/c7087836-ee95-4177-b610-7141468df324/14.png)

![15.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/31018ab1-b441-4f79-880a-36a87edf77b7/15.png)

1. If everything is correct, click “Deploy”

![16.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/eee61d58-328f-4577-a70f-41c5a784a505/16.png)

1. It takes 5-10 minutes to deploy a container and we can check logs and deployment progress if we click on “Infra”

![17.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/00534c86-ee4c-4c10-b29c-13f3d393b314/17.png)

1. Finally deployment is finished!

![18.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/106c1e1f-dc01-477b-9ee5-cd0ea7e5dc0d/18.png)

1. If we click on “Open App” link we can see the application running.

![19.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/c6875552-a103-47ba-95ac-1fd0abaca93c/19.png)

That’s all.

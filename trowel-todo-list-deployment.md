# 😀 Trowel todo list deployment

In this guide we will deploy our first application using Trowel! We will be deploying [https://github.com/veziak/django-todolist. ](https://github.com/veziak/django-todolist)This is a Django application which requires a database.&#x20;

Visit dashboard.digger.dev and click on create to create your infrastructure bundle for this application

<figure><img src=".gitbook/assets/Screen Shot 2022-11-17 at 4.26.39 PM.png" alt=""><figcaption></figcaption></figure>

we want to deploy it as a container, so click on the container block, change the port to '8000' and click on generate

<figure><img src=".gitbook/assets/Screen Shot 2022-11-17 at 4.26.52 PM.png" alt=""><figcaption></figcaption></figure>

We need to add a placeholder for database connection env variable which is needed for our application. Click on "add Secrets" and enter a placeholder value for the DATABASE\_URL parameter

<figure><img src=".gitbook/assets/Screen Shot 2022-11-17 at 4.27.01 PM.png" alt=""><figcaption></figcaption></figure>

click on generate to save your block

<figure><img src=".gitbook/assets/Screen Shot 2022-11-17 at 4.27.24 PM.png" alt=""><figcaption></figcaption></figure>

lets create a database next, click on add block and select "postgres"

<figure><img src=".gitbook/assets/Screen Shot 2022-11-17 at 4.27.44 PM.png" alt=""><figcaption></figcaption></figure>

lets download the bundle

<figure><img src=".gitbook/assets/Screen Shot 2022-11-17 at 4.28.14 PM.png" alt=""><figcaption></figcaption></figure>

For the next step we need aws cli, so make sure you have it installed and then run `aws configure` if you its your first time using the cli. You will be asked to enter keys which you can generate using \[\[this tutorial]].

<figure><img src=".gitbook/assets/Screen Shot 2022-11-17 at 4.34.53 PM.png" alt=""><figcaption></figcaption></figure>

We need to have `dgctl` cli for the next step. Please follow [installation instructions](installing-dgctl.md) to install it.

now in terminal navigate to the directory where you unzipped the terraform and run `dgctl init,`

This will initialize your terraform state backend to use an S3 bucket in your account. This is needed so that you can re-download and re-run your terraform from the dashboard project multiple times.

<figure><img src=".gitbook/assets/Screen Shot 2022-11-18 at 4.52.21 PM.png" alt=""><figcaption></figcaption></figure>

Next up! Lets create the infrastructure

```
terraform init
# see what will be created
terraform plan
terraform apply
```

Now we wait for a few minutes until the terraform apply step is completed. We will see an output like the one below:

<figure><img src=".gitbook/assets/Screen Shot 2022-11-18 at 4.53.48 PM.png" alt=""><figcaption></figcaption></figure>

There are several important peices of output here. For the purposes of this tutorial keep track of `lb_dns` and `docker_registry_url`

In the next step we need to visit AWS console and update the secrets. search for "parameter store in the params and find a secret called DATABASE\_URL. Replace that value with the value of the other database\_url parameter



Final step! We need to build our container image. Remember we noted `docker_registry_url` ? This is where it comes in handy. The url looks like follows:

```
209539466991.dkr.ecr.us-east-1.amazonaws.com/drip-be
```

We need to store these parameters in order to build our image:

```
export AWS_ACCOUNT_ID="$(aws sts get-caller-identity --query "Account" --output text)" 
export AWS_REGION=us-east-1
export ECR_REPO=drip-be

```

Finally! Run these commands to build and deploy your container image

```
aws ecr get-login-password --region $AWS_REGION | docker login --username AWS --password-stdin $AWS_ACCOUNT_ID.dkr.ecr.$AWS_REGION.amazonaws.com
docker build -t $AWS_ACCOUNT_ID.dkr.ecr.$AWS_REGION.amazonaws.com/$ECR_REPO .
docker push $AWS_ACCOUNT_ID.dkr.ecr.$AWS_REGION.amazonaws.com/$ECR_REPO:latest

```

You should see a push in progress and it should be successful in the end

<figure><img src=".gitbook/assets/Screen Shot 2022-11-18 at 4.58.39 PM.png" alt=""><figcaption></figcaption></figure>


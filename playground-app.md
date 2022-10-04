---
description: >-
  You can use the playground app in Digger to get a feel for what its like to
  deploy an application on digger. All you need to do is login to
  dashboard.digger.dev and visit the playground application: h
---

# Playground App

[https://dashboard.digger.dev/app/6eaa1192-1a66-4696-b77a-a14db52fa8a4](https://dashboard.digger.dev/app/6eaa1192-1a66-4696-b77a-a14db52fa8a4) .&#x20;

<figure><img src=".gitbook/assets/Screen Shot 2022-10-04 at 6.03.17 PM.png" alt=""><figcaption></figcaption></figure>

&#x20;Play around with deployments and settings. Remember that this is shared by all other users and is only to be used for demonstration purposes! In addition to the digger application, you can also see the underlying AWS resources since it is deployed into a dedicated AWS playground account and you can use the following credentials to log in and check out what is being created:

```
https://125830870740.signin.aws.amazon.com/console/
username: diggerwins
password: @#E$9IE6TkukfL#1jviqo2khZ
```

Once you are logged in you can check out for example ECS section to see your cluster and all the magic that digger generated under the hood! [https://us-east-1.console.aws.amazon.com/ecs/home?region=us-east-1#/clusters/playground-6eaa1192/services](https://us-east-1.console.aws.amazon.com/ecs/home?region=us-east-1#/clusters/playground-6eaa1192/services)

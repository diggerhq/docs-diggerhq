---
description: How to request a quota increase from AWS
---

# Requesting quota increase

By default AWS has some limits for the number of resources you can create in every region. For example by default you can only create 5 VPCs in every region. Sometimes while using digger you will run into "quota exceeded" errors if you create many apps. Luckily this is very easy to fix since all you need to do is request a quota increase for this resource and it will be approved in a few hours. Here's how you can do it:



Login to your AWS console and click on "service quotas"&#x20;

![](<.gitbook/assets/Screen Shot 2022-07-27 at 10.54.34 AM.png>)

click on "AWS Services"

![](<.gitbook/assets/Screen Shot 2022-07-27 at 10.54.46 AM.png>)

Search for "VPC" and find the one called "VPCs per region" in the main list. This will be different depending on which resource you want to request an increase for.

![](<.gitbook/assets/Screen Shot 2022-07-27 at 10.55.15 AM.png>)

Click on "Request quota increase". Enter the new value and click on request. You will see that the request will enter pending state. Keep checking back until it gets to approved state

![](<.gitbook/assets/Screen Shot 2022-07-27 at 10.55.22 AM.png>)

---
title: 31-Specify "pool" IPAM mode in LoadBalancer service
---
Prerequisite: 
Already provision RKE1/RKE2 cluster in previous test case

1. Open `Global Settings` in hamburger menu
1. Replace `ui-dashboard-index` to `https://releases.rancher.com/harvester-ui/dashboard/latest/index.html`
1. Change `ui-offline-preferred` to `Remote`
1. Refresh the current page (ctrl + r)
1. Open provisioned RKE2 cluster from hamburger menu
1. Drop down `Service Discovery`
1. Click `Services`
1. Click Create 
1. Select `Load Balancer`

![image.png](https://images.zenhubusercontent.com/61519853321ea20d65443929/f628094c-a195-4f99-9fb7-858d759dc019)

1. Given service name
1. Provide Listending port and Target port

![image.png](https://images.zenhubusercontent.com/61519853321ea20d65443929/2c20c759-4769-438b-94ad-5b995ba66873)

1. Click `Add-on Config`
1. Provide Health Check port
1. Select `pool` as IPAM mode
1. Provide Health Check Threshold
1. Provide Health Check Failure Threshold
1. Provide Health Check Period
1. Provide Health Check Timeout
1. Click Create button

![image.png](https://images.zenhubusercontent.com/61519853321ea20d65443929/a8d11df6-cc76-4897-8310-def670682775)

## Expected Results
1. Can create load balance service correctly
1. Can operate and foward workload as expected
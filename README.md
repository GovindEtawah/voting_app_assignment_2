Authenticating with public key "imported-openssh-key"
    ┌──────────────────────────────────────────────────────────────────────┐
    │                 • MobaXterm Personal Edition v22.1 •                 │
    │               (SSH client, X server and network tools)               │
    │                                                                      │
    │ ⮞ SSH session to ec2-user@54.254.49.227                              │
    │   • Direct SSH      :  ✓                                             │
    │   • SSH compression :  ✓                                             │
    │   • SSH-browser     :  ✓                                             │
    │   • X11-forwarding  :  ✗  (disabled or not supported by server)      │
    │                                                                      │
    │ ⮞ For more info, ctrl+click on help or visit our website.            │
    └──────────────────────────────────────────────────────────────────────┘

Last login: Fri Oct 27 04:05:00 2023 from 49.205.137.110
   ,     #_
   ~\_  ####_        Amazon Linux 2
  ~~  \_#####\
  ~~     \###|       AL2 End of Life is 2025-06-30.
  ~~       \#/ ___
   ~~       V~' '->
    ~~~         /    A newer version of Amazon Linux is available!
      ~~._.   _/
         _/ _/       Amazon Linux 2023, GA and supported until 2028-03-15.
       _/m/'           https://aws.amazon.com/linux/amazon-linux-2023/

24 package(s) needed for security, out of 29 available
Run "sudo yum update" to apply all updates.
[ec2-user@ip-172-31-21-6 ~]$
[ec2-user@ip-172-31-21-6 ~]$
[ec2-user@ip-172-31-21-6 ~]$
[ec2-user@ip-172-31-21-6 ~]$
[ec2-user@ip-172-31-21-6 ~]$ su -
Password:
[ec2-user@ip-172-31-21-6 ~]$ sudo su
[root@ip-172-31-21-6 ec2-user]#
[root@ip-172-31-21-6 ec2-user]#
[root@ip-172-31-21-6 ec2-user]#
[root@ip-172-31-21-6 ec2-user]# kubectl get nodes
NAME                                              STATUS   ROLES    AGE   VERSION
ip-172-31-19-48.ap-southeast-1.compute.internal   Ready    master   12d   v1.18.5
ip-172-31-21-6.ap-southeast-1.compute.internal    Ready    <none>   11d   v1.18.5
[root@ip-172-31-21-6 ec2-user]#
[root@ip-172-31-21-6 ec2-user]#
[root@ip-172-31-21-6 ec2-user]#
[root@ip-172-31-21-6 ec2-user]#
[root@ip-172-31-21-6 ec2-user]#
[root@ip-172-31-21-6 ec2-user]#
[root@ip-172-31-21-6 ec2-user]#
[root@ip-172-31-21-6 ec2-user]# kubectl delete all --all
pod "kubia-l4t9f" deleted
pod "kubia-rmndv" deleted
pod "kubia-zl6b9" deleted
pod "vote-94849dc97-pfvhp" deleted
service "kubia-loadbalancer" deleted
service "kubia-nodeport" deleted
service "kubia2" deleted
deployment.apps "vote" deleted
replicaset.apps "kubia" deleted
replicaset.apps "vote-94849dc97" deleted
[root@ip-172-31-21-6 ec2-user]# cd $home
[root@ip-172-31-21-6 ~]# yum install git -y
Loaded plugins: extras_suggestions, langpacks, priorities, update-motd
amzn2-core                                                                                                                       | 3.6 kB  00:00:00
amzn2extra-docker                                                                                                                | 2.9 kB  00:00:00
amzn2extra-kernel-5.10                                                                                                           | 3.0 kB  00:00:00
kubernetes                                                                                                                       | 1.4 kB  00:00:00
11 packages excluded due to repository priority protections
Package git-2.40.1-1.amzn2.0.1.x86_64 already installed and latest version
Nothing to do
[root@ip-172-31-21-6 ~]# git clone  https://github.com/ashishrpandey/example-voting-app
fatal: destination path 'example-voting-app' already exists and is not an empty directory.
[root@ip-172-31-21-6 ~]# cd /root/example-voting-app
[root@ip-172-31-21-6 example-voting-app]# ls -lrt
total 96
-rw-r--r-- 1 root root  2182 Oct 25 04:46 README.md
-rw-r--r-- 1 root root   185 Oct 25 04:46 MAINTAINERS
-rw-r--r-- 1 root root 10758 Oct 25 04:46 LICENSE
-rw-r--r-- 1 root root  1692 Oct 25 04:46 docker-stack.yml
-rw-r--r-- 1 root root   808 Oct 25 04:46 docker-compose.yml
-rw-r--r-- 1 root root   400 Oct 25 04:46 docker-compose-simple.yml
-rw-r--r-- 1 root root   808 Oct 25 04:46 docker-compose-javaworker.yml
-rw-r--r-- 1 root root   609 Oct 25 04:46 dockercloud.yml
-rw-r--r-- 1 root root 54824 Oct 25 04:46 architecture.png
drwxr-xr-x 3 root root    70 Oct 25 04:46 worker
drwxr-xr-x 4 root root    93 Oct 25 04:46 vote
drwxr-xr-x 5 root root   133 Oct 25 04:46 result
drwxr-xr-x 2 root root   250 Oct 25 04:54 k8s-specifications
[root@ip-172-31-21-6 example-voting-app]#
[root@ip-172-31-21-6 example-voting-app]#
[root@ip-172-31-21-6 example-voting-app]#
[root@ip-172-31-21-6 example-voting-app]#
[root@ip-172-31-21-6 example-voting-app]# cd k8s-specifications
[root@ip-172-31-21-6 k8s-specifications]# ls -lrt
total 36
-rw-r--r-- 1 root root 292 Oct 25 04:46 worker-deployment.yaml
-rw-r--r-- 1 root root 192 Oct 25 04:46 vote-service.yaml
-rw-r--r-- 1 root root 289 Oct 25 04:46 vote-deployment.yaml
-rw-r--r-- 1 root root 195 Oct 25 04:46 result-service.yaml
-rw-r--r-- 1 root root 299 Oct 25 04:46 result-deployment.yaml
-rw-r--r-- 1 root root 152 Oct 25 04:46 redis-service.yaml
-rw-r--r-- 1 root root 402 Oct 25 04:46 redis-deployment.yaml
-rw-r--r-- 1 root root 146 Oct 25 04:46 db-service.yaml
-rw-r--r-- 1 root root 401 Oct 25 04:46 db-deployment.yaml
[root@ip-172-31-21-6 k8s-specifications]#
[root@ip-172-31-21-6 k8s-specifications]#
[root@ip-172-31-21-6 k8s-specifications]#
[root@ip-172-31-21-6 k8s-specifications]#
[root@ip-172-31-21-6 k8s-specifications]#
[root@ip-172-31-21-6 k8s-specifications]# vi vote-service.yaml
[root@ip-172-31-21-6 k8s-specifications]# vi vote-service.yaml
[root@ip-172-31-21-6 k8s-specifications]# vi result-service.yaml
[root@ip-172-31-21-6 k8s-specifications]#
[root@ip-172-31-21-6 k8s-specifications]#
[root@ip-172-31-21-6 k8s-specifications]#
[root@ip-172-31-21-6 k8s-specifications]# cd ..
[root@ip-172-31-21-6 example-voting-app]# ls -lrt
total 96
-rw-r--r-- 1 root root  2182 Oct 25 04:46 README.md
-rw-r--r-- 1 root root   185 Oct 25 04:46 MAINTAINERS
-rw-r--r-- 1 root root 10758 Oct 25 04:46 LICENSE
-rw-r--r-- 1 root root  1692 Oct 25 04:46 docker-stack.yml
-rw-r--r-- 1 root root   808 Oct 25 04:46 docker-compose.yml
-rw-r--r-- 1 root root   400 Oct 25 04:46 docker-compose-simple.yml
-rw-r--r-- 1 root root   808 Oct 25 04:46 docker-compose-javaworker.yml
-rw-r--r-- 1 root root   609 Oct 25 04:46 dockercloud.yml
-rw-r--r-- 1 root root 54824 Oct 25 04:46 architecture.png
drwxr-xr-x 3 root root    70 Oct 25 04:46 worker
drwxr-xr-x 4 root root    93 Oct 25 04:46 vote
drwxr-xr-x 5 root root   133 Oct 25 04:46 result
drwxr-xr-x 2 root root   250 Oct 30 09:50 k8s-specifications
[root@ip-172-31-21-6 example-voting-app]# cd vote
[root@ip-172-31-21-6 vote]# ls -lrt
total 12
drwxr-xr-x 2 root root   24 Oct 25 04:46 templates
drwxr-xr-x 3 root root   25 Oct 25 04:46 static
-rw-r--r-- 1 root root   21 Oct 25 04:46 requirements.txt
-rw-r--r-- 1 root root  557 Oct 25 04:46 Dockerfile
-rw-r--r-- 1 root root 1123 Oct 25 04:46 app.py
[root@ip-172-31-21-6 vote]#
[root@ip-172-31-21-6 vote]#
[root@ip-172-31-21-6 vote]#
[root@ip-172-31-21-6 vote]# vi app.py
[root@ip-172-31-21-6 vote]# cd ..
[root@ip-172-31-21-6 example-voting-app]# cd worker/
[root@ip-172-31-21-6 worker]# ls -lrt
total 12
drwxr-xr-x 4 root root   32 Oct 25 04:46 src
-rw-r--r-- 1 root root 2504 Oct 25 04:46 pom.xml
-rw-r--r-- 1 root root  473 Oct 25 04:46 Dockerfile.j
-rw-r--r-- 1 root root  213 Oct 25 04:46 Dockerfile
[root@ip-172-31-21-6 worker]#
[root@ip-172-31-21-6 worker]#
[root@ip-172-31-21-6 worker]#
[root@ip-172-31-21-6 worker]#
[root@ip-172-31-21-6 worker]# cd src
[root@ip-172-31-21-6 src]# ls -lrt
total 0
drwxr-xr-x 3 root root 18 Oct 25 04:46 main
drwxr-xr-x 2 root root 45 Oct 25 05:03 Worker
[root@ip-172-31-21-6 src]# cd Worker
[root@ip-172-31-21-6 Worker]# ls -lrt
total 12
-rw-r--r-- 1 root root  654 Oct 25 04:46 Worker.csproj
-rw-r--r-- 1 root root 5521 Oct 25 04:46 Program.cs
[root@ip-172-31-21-6 Worker]# vi Program.cs
[root@ip-172-31-21-6 Worker]#
[root@ip-172-31-21-6 Worker]#
[root@ip-172-31-21-6 Worker]#
[root@ip-172-31-21-6 Worker]#
[root@ip-172-31-21-6 Worker]#
[root@ip-172-31-21-6 Worker]# cd  /root/example-voting-app/result
[root@ip-172-31-21-6 result]# ls -lrt
total 16
drwxr-xr-x 2 root root   57 Oct 25 04:46 tests
-rw-r--r-- 1 root root 2239 Oct 25 04:46 server.js
-rw-r--r-- 1 root root  417 Oct 25 04:46 package.json
-rw-r--r-- 1 root root  334 Oct 25 04:46 Dockerfile
-rw-r--r-- 1 root root  787 Oct 25 04:46 docker-compose.test.yml
drwxr-xr-x 3 root root   77 Oct 25 04:46 views
[root@ip-172-31-21-6 result]# vi server.js
[root@ip-172-31-21-6 result]#
[root@ip-172-31-21-6 result]#
[root@ip-172-31-21-6 result]#
[root@ip-172-31-21-6 result]#
[root@ip-172-31-21-6 result]# cd /root/example-voting-app/k8s-specifications
[root@ip-172-31-21-6 k8s-specifications]# ls -lrt
total 36
-rw-r--r-- 1 root root 292 Oct 25 04:46 worker-deployment.yaml
-rw-r--r-- 1 root root 289 Oct 25 04:46 vote-deployment.yaml
-rw-r--r-- 1 root root 299 Oct 25 04:46 result-deployment.yaml
-rw-r--r-- 1 root root 152 Oct 25 04:46 redis-service.yaml
-rw-r--r-- 1 root root 402 Oct 25 04:46 redis-deployment.yaml
-rw-r--r-- 1 root root 146 Oct 25 04:46 db-service.yaml
-rw-r--r-- 1 root root 401 Oct 25 04:46 db-deployment.yaml
-rw-r--r-- 1 root root 192 Oct 30 09:49 vote-service.yaml
-rw-r--r-- 1 root root 195 Oct 30 09:50 result-service.yaml
[root@ip-172-31-21-6 k8s-specifications]# kubectl apply -f .
deployment.apps/db created
service/db created
deployment.apps/redis created
service/redis created
deployment.apps/result created
service/result created
deployment.apps/vote created
service/vote created
deployment.apps/worker created
[root@ip-172-31-21-6 k8s-specifications]#  kubectl get all
NAME                          READY   STATUS    RESTARTS   AGE
pod/db-b54cd94f4-f7bdd        1/1     Running   0          10s
pod/redis-868d64d78-vh5qc     1/1     Running   0          10s
pod/result-5d57b59f4b-fgfq4   1/1     Running   0          10s
pod/vote-94849dc97-v9sqh      1/1     Running   0          10s
pod/worker-dd46d7584-r5g7d    1/1     Running   0          9s

NAME             TYPE        CLUSTER-IP       EXTERNAL-IP   PORT(S)          AGE
service/db       ClusterIP   10.100.227.236   <none>        5432/TCP         10s
service/redis    ClusterIP   10.107.191.225   <none>        6379/TCP         10s
service/result   NodePort    10.98.137.129    <none>        5001:31003/TCP   10s
service/vote     NodePort    10.108.21.76     <none>        5000:31002/TCP   9s

NAME                     READY   UP-TO-DATE   AVAILABLE   AGE
deployment.apps/db       1/1     1            1           10s
deployment.apps/redis    1/1     1            1           10s
deployment.apps/result   1/1     1            1           10s
deployment.apps/vote     1/1     1            1           10s
deployment.apps/worker   1/1     1            1           9s

NAME                                DESIRED   CURRENT   READY   AGE
replicaset.apps/db-b54cd94f4        1         1         1       10s
replicaset.apps/redis-868d64d78     1         1         1       10s
replicaset.apps/result-5d57b59f4b   1         1         1       10s
replicaset.apps/vote-94849dc97      1         1         1       10s
replicaset.apps/worker-dd46d7584    1         1         1       9s
[root@ip-172-31-
------------------------------------------------------------------------------------------------------------
6. take your publicIP (your instance IP) : NodePort ► open 2 browsers , one for VOTING and one for Results.
My publicIP : 54.254.49.227      
For VOTING  :  54.254.49.227 :31002
For RESULT  : 54.254.49.227 :31003
-------------------------------------------------------------------------------------------------------------
7. try voting and see the results paralelly in results page.
Followed the same as mentioned
--------------------------------------------------------------------------------------------------------------


8. Now try to delete the Pods one by one (first voting Pod, then worker pod, then db pod) and see what happens to the voting and result app after deleting.
1st ► VOTE pod ► Observe what happens both in frontEnd & in Unix
2nd ► WORKER pod  ► Observe what happens both in frontEnd & in Unix
3rd ► DB pod ► Observe what happens both in frontEnd & in Unix"
9. My observations
1st ► VOTE pod ► After deleting the VOTE POD new vote pod was generated but no disruption in the entire application was observed as VOTE POD does not contains any data.
[[root@ip-172-31-21-6 k8s-specifications]# kubectl get po
NAME                      READY   STATUS    RESTARTS   AGE
db-b54cd94f4-f7bdd        1/1     Running   0          6m1s
redis-868d64d78-vh5qc     1/1     Running   0          6m1s
result-5d57b59f4b-fgfq4   1/1     Running   0          6m1s
vote-94849dc97-v9sqh      1/1     Running   0          6m1s
worker-dd46d7584-r5g7d    1/1     Running   0          6m
[root@ip-172-31-21-6 k8s-specifications]#
[root@ip-172-31-21-6 k8s-specifications]#
[root@ip-172-31-21-6 k8s-specifications]#
[root@ip-172-31-21-6 k8s-specifications]# kubectl delete po vote-94849dc97-v9sqh
pod "vote-94849dc97-v9sqh" deleted
[root@ip-172-31-21-6 k8s-specifications]# kubectl get po
NAME                      READY   STATUS    RESTARTS   AGE
db-b54cd94f4-f7bdd        1/1     Running   0          6m30s
redis-868d64d78-vh5qc     1/1     Running   0          6m30s
result-5d57b59f4b-fgfq4   1/1     Running   0          6m30s
vote-94849dc97-8n77z      1/1     Running   0          16s
worker-dd46d7584-r5g7d    1/1     Running   0          6m29s
[root@ip-172-31-21-6 k8s-specifications]#

 
2nd ► WORKER pod  ► After deleting the WORKER POD all the logs got vanished and new WORKER POD was generated as observed.
[root@ip-172-31-21-6 k8s-specifications]# kubectl get po
NAME                      READY   STATUS    RESTARTS   AGE
db-b54cd94f4-f7bdd        1/1     Running   0          6m30s
redis-868d64d78-vh5qc     1/1     Running   0          6m30s
result-5d57b59f4b-fgfq4   1/1     Running   0          6m30s
vote-94849dc97-8n77z      1/1     Running   0          16s
worker-dd46d7584-r5g7d    1/1     Running   0          6m29s
[root@ip-172-31-21-6 k8s-specifications]# kubectl delete po worker-dd46d7584-r5g7d
pod "worker-dd46d7584-r5g7d" deleted
[root@ip-172-31-21-6 k8s-specifications]# kubectl get po
NAME                      READY   STATUS    RESTARTS   AGE
db-b54cd94f4-f7bdd        1/1     Running   0          7m30s
redis-868d64d78-vh5qc     1/1     Running   0          7m30s
result-5d57b59f4b-fgfq4   1/1     Running   0          7m30s
vote-94849dc97-8n77z      1/1     Running   0          76s
worker-dd46d7584-768mj    1/1     Running   0          14s
[root@ip-172-31-21-6 k8s-specifications]# kubectl logs worker-dd46d7584-768mj
Connected to db
Found redis at 10.107.191.225
Connecting to redis
[root@ip-172-31-21-6 k8s-specifications]#

3rd ► DB pod ► After deleting DB POD the data is completely lost and new DB was generated as observed.
[root@ip-172-31-21-6 k8s-specifications]# kubectl get po
NAME                      READY   STATUS    RESTARTS   AGE
db-b54cd94f4-f7bdd        1/1     Running   0          9m
redis-868d64d78-vh5qc     1/1     Running   0          9m
result-5d57b59f4b-fgfq4   1/1     Running   0          9m
vote-94849dc97-8n77z      1/1     Running   0          2m46s
worker-dd46d7584-768mj    1/1     Running   0          104s
[root@ip-172-31-21-6 k8s-specifications]# kubectl delete po db-b54cd94f4-f7bdd
pod "db-b54cd94f4-f7bdd" deleted
[root@ip-172-31-21-6 k8s-specifications]# kubectl get po
NAME                      READY   STATUS    RESTARTS   AGE
db-b54cd94f4-frhsn        1/1     Running   0          35s
redis-868d64d78-vh5qc     1/1     Running   0          9m49s
result-5d57b59f4b-fgfq4   1/1     Running   1          9m49s
vote-94849dc97-8n77z      1/1     Running   0          3m35s
worker-dd46d7584-768mj    1/1     Running   1          2m33s
[root@ip-172-31-21-6 k8s-specifications]#

--------------------------------------------------------------------------------------------------------------
Logs generated in WORKER POD
[[root@ip-172-31-21-6 k8s-specifications]# kubectl logs worker-dd46d7584-768mj
Connected to db
Found redis at 10.107.191.225
Connecting to redis
[root@ip-172-31-21-6 k8s-specifications]#
[root@ip-172-31-21-6 k8s-specifications]#
[root@ip-172-31-21-6 k8s-specifications]#
[root@ip-172-31-21-6 k8s-specifications]# kubectl logs worker-dd46d7584-768mj
Connected to db
Found redis at 10.107.191.225
Connecting to redis
[root@ip-172-31-21-6 k8s-specifications]#
[root@ip-172-31-21-6 k8s-specifications]# kubectl logs worker-dd46d7584-768mj
Connected to db
Found redis at 10.107.191.225
Connecting to redis
Processing vote for 'b' by '409811f7cb0504e'
Processing vote for 'a' by '409811f7cb0504e'
Processing vote for 'b' by '409811f7cb0504e'
Processing vote for 'a' by '409811f7cb0504e'
Processing vote for 'b' by '409811f7cb0504e'
Processing vote for 'a' by '409811f7cb0504e'
Processing vote for 'b' by '409811f7cb0504e'
Processing vote for 'a' by '409811f7cb0504e'
[root@ip-172-31-21-6 k8s-specifications]#


-------------------------------------------------------------------------------------------------------------------
10. what happens after db pod deletion?
After deletion of db pod the data is completely lost and new DB was generated as observed.
--------------------------------------------------------------------------------------------------------------------
11. complete the assignment by making the result pod work.
I have Completed the assignment by making the result pod work as result pod came automatically.
--------------------------------------------------------------------------------------------------------------------
12. Write in the text file, what you did in order to make the result pod work.
After deleting the DB POD the data is completely lost and new DB was generated and again we have to vote and result will appear to make result pod work.
---------------------------------------------------------------------------------------------------------------------
 
SUMMARY
1. Commands that you used during the assignment. (not Mandatory, if you have time, please write it)
cd $home
yum install git -y
git clone https://github.com/ashishrpandey/example-voting-app
kubectl apply -f .
kubectl get all
kubectl get po
kubectl get svc
kubectl logs worker-dd46d7584-768mj
kubectl delete po db-b54cd94f4-f7bdd
kubectl delete po worker-dd46d7584-r5g7d
kubectl delete po vote-94849dc97-v9sqh
2. snapshot of logs (wherever possible, not mandatory, if you have time, please write it)
[root@ip-172-31-43-86 result]# kubectl logs worker-dd46d7584-8kpn9
Connected to db
Found redis at 10.97.109.146
Connecting to redis
Processing vote for 'a' by '6da70c902782609'
Processing vote for 'b' by '6da70c902782609'
Processing vote for 'a' by '6da70c902782609'
Processing vote for 'b' by '6da70c902782609'
Processing vote for 'a' by '6da70c902782609'
Processing vote for 'b' by '6da70c902782609'
Processing vote for 'a' by '6da70c902782609'
Processing vote for 'b' by '6da70c902782609'
Processing vote for 'a' by '6da70c902782609'
 
3. your comment on WHY result app STOPPED working after db pod stop
As db pod contains all the data and that data appears in result app and after deleting db pod the data is completely lost so app will STOP working.
 
4. your answer to HOW YOU MADE THE RESULT POD work.
BY voting again and it will appear the result in web browser hence the result pod will work as db pod contains the data .
 
5. Some jargons (just names are enough- dont need sentences) that you learnt from the  Training session
Docker
Microservices/k8 installation
PODS/TITBITs
Controllers
Services/Deployment
VOTINGapp
VOLUMES
Networking
HELM
ISTIO
AWS
GitHub - ashishrpandey/example-voting-app: Example Docker Compose app
Example Docker Compose app. Contribute to ashishrpandey/example-voting-app development by creating an account on GitHub.

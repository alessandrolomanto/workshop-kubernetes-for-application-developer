# Playing with Jobs

In `4-jobs` you will find a simple example of job. This is a dummy job, meaning that it doesn't do any real work. It will boot a pod that will calculate `pi`, it will take about 10 sec to complete.

We can deploy the job by running:  
`kubectl apply -f 4-jobs/job.yaml`

Output is going to be:

```bash
kubectl get pods
NAME       READY     STATUS    RESTARTS   AGE
pi-xcv5b   1/1       Running   0          <invalid>
.
.
.
pi-xcv5b   0/1     Completed   0          102s
```
After checked if pod is completed
```bash
k logs pi-xcv5b

3.1415926535........
```
Delete job
```bash
kubectl delete job pi
kubectl delete -f 4-jobs/job.yaml

```
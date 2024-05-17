# assignment56_gaurav.rana

8. Observations
root@ip-172-31-10-151:~/example-voting-app/k8s-specifications# k get po
NAME                                             READY   STATUS      RESTARTS      AGE
batch-job-every-fifteen-minutes-28596555-clj2m   0/1     Completed   0             34m
batch-job-every-fifteen-minutes-28596570-n2rsm   0/1     Completed   0             19m
batch-job-every-fifteen-minutes-28596585-gcqpg   0/1     Completed   0             4m47s
db-58cc845644-mw2mt                              1/1     Running     0             3m47s
fortune                                          2/2     Running     2 (11h ago)   36h
kubia-manual                                     1/1     Running     1 (11h ago)   5d8h
kubia-manual-v2                                  1/1     Running     1 (11h ago)   5d8h
nginx-gaurav                                     1/1     Running     1 (11h ago)   6d11h
nginx-mallappa                                   1/1     Running     1 (11h ago)   6d11h
nginx-sarvottam                                  1/1     Running     1 (11h ago)   6d11h
redis-6878558678-ctlg4                           1/1     Running     0             3m47s
result-86bc6f7b5d-zq8h6                          1/1     Running     0             3m47s
vote-7d884dd585-bv7hs                            1/1     Running     0             3m47s
worker-6fc5d5b668-jgl4m                          1/1     Running     0             3m47s


1. Deleting voting pod: pod got deleted and new pod got created. No change in app.
  root@ip-172-31-10-151:~# k delete po vote-7d884dd585-bv7hs
pod "vote-7d884dd585-bv7hs" deleted
root@ip-172-31-10-151:~# k get pods
NAME                                             READY   STATUS      RESTARTS      AGE
batch-job-every-fifteen-minutes-28597155-hmnd2   0/1     Completed   0             33m
batch-job-every-fifteen-minutes-28597170-8t4mv   0/1     Completed   0             18m
batch-job-every-fifteen-minutes-28597185-q2pd6   0/1     Completed   0             3m11s
db-58cc845644-mw2mt                              1/1     Running     0             10h
fortune                                          2/2     Running     2 (21h ago)   46h
kubia-manual                                     1/1     Running     1 (21h ago)   5d18h
kubia-manual-v2                                  1/1     Running     1 (21h ago)   5d18h
nginx-gaurav                                     1/1     Running     1 (21h ago)   6d21h
nginx-mallappa                                   1/1     Running     1 (21h ago)   6d21h
nginx-sarvottam                                  1/1     Running     1 (21h ago)   6d21h
redis-6878558678-ctlg4                           1/1     Running     0             10h
result-86bc6f7b5d-zq8h6                          1/1     Running     0             10h
vote-7d884dd585-z7khf                            1/1     Running     0             2m29s
worker-6fc5d5b668-jgl4m                          1/1     Running     0             10h

3. Deleting worker pod: pod got deleted and new pod got created. No change in app.
   
5. Deleting db pod: pod got deleted and new pod got created. Vote count lost.
   ![image](https://github.com/gksrana5/assignment56/assets/167311479/e9a1ca3a-f016-45c7-a313-b96ae95d6725)


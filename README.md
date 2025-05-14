kubectl rollout restart deployment <deployment-pod>                                                         # to restart our deployment pod
kubectl scale deployment <deployment-pod> -n <namespace> --replicas=2                                       # when you want to increase pod capacity 
kubectl cp -n <namespace> <pod-name>:/path logs>/ /home/ec2-user/filename                                    # copy logs form pod to local machine
sudo docker load <image-name>                                                                                # it will download image in the cluster 
kubectl logs <pod-name> -n <namespace> --tail=100                                                            # it is showing only latest 100 lines logs only 
kubectl create deployment nginx-deployment --image=nginx  --dry-run=client -o yaml > nginx-deployment.yaml   # it will create one deployment file with nginx image 
kubectl get deployment <deployment-pod> -o yaml -n <namespace> > deployment_backup.yaml                      # it is taking entier deployment pod backup 
kubectl logs <pod-name> -n <namespace> > deployment_logs_backup.txt                                          # it will copy all logs to one file 

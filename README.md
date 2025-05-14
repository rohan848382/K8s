# to restart our deployment pod
kubectl rollout restart deployment <deployment-pod>
                                      
# when you want to increase pod capacity 
kubectl scale deployment <deployment-pod> -n <namespace> --replicas=2
                                  
# copy logs form pod to local machine
kubectl cp -n <namespace> <pod-name>:/path logs>/ /home/ec2-user/filename 
                                                                              
# it will download image in the cluster 
sudo docker load <image-name>  
                                                    
# it is showing only latest 100 lines logs only 
kubectl logs <pod-name> -n <namespace> --tail=100        
   
# it will create one deployment file with nginx image
kubectl create deployment nginx-deployment --image=nginx  --dry-run=client -o yaml > nginx-deployment.yaml

# it is taking entier deployment pod backup 
kubectl get deployment <deployment-pod> -o yaml -n <namespace> > deployment_backup.yaml                      
                                        
# it will copy all logs to one file
kubectl logs <pod-name> -n <namespace> > deployment_logs_backup.txt 

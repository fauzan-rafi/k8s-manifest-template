# Belajar menggunakan Environment Variable

## Environment
Gunakan minikube atau killercoda untuk lingkungan kubernetes belajar anda !

## Step by Step
1. Pastikan ada sudah berada pada folder k8s-manifest-template/learn-env
```bash
pwd
```
3. Buatlah namespace dengan format (nama anda)-lab. Contoh rafi-lab
```bash
kubectl create ns (nama anda)-lab
```
5. Buatlah deployment pada file deploy.yaml
```
kubectl apply -f deploy.yaml -n (nama anda)-lab
```
7. Buatlah configmap & secret dengan cara
```
kubectl apply -f secret.yaml -n (nama anda)-lab
kubectl apply -f configmap.yaml -n (nama anda)-lab
```
9. Masuk kedalam Pod untuk membaca secret yg ada
```
kubectl get pod -n (nama anda)-lab
# Contoh output ....
container-ku-xxxx-xxxx
....

kubectl exec -it container-ku-xxxx-xxxx -- /bin/bash
env
```


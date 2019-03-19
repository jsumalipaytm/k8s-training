init:
	kubectl create serviceaccount tiller --namespace kube-system
	kubectl create clusterrolebinding tiller-admin-binding --clusterrole=cluster-admin --serviceaccount=kube-system:tiller
	helm init --service-account=tiller
	helm repo add stable https://kubernetes-charts.storage.googleapis.com/
	helm update

spark:
	helm install --name myspark --namespace spark stable/spark


install:
	kubectl apply -f redis-master-deployment.yaml
	kubectl apply -f redis-master-service.yaml
	kubectl apply -f redis-slave-deployment.yaml
	kubectl apply -f redis-slave-service.yaml
	kubectl apply -f frontend-deployment.yaml
	kubectl apply -f frontend-service.yaml

uninstall:
	kubectl delete -f redis-master-deployment.yaml
	kubectl delete -f redis-master-service.yaml
	kubectl delete -f redis-slave-deployment.yaml
	kubectl delete -f redis-slave-service.yaml
	kubectl delete -f frontend-deployment.yaml
	kubectl delete -f frontend-service.yaml

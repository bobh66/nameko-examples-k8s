CONTEXT ?= minikube
NAMESPACE ?= examples

deploy-namespace:
	kubectl --context=$(CONTEXT) apply -f namespace.yaml

deploy-orders:
	kubectl --context=$(CONTEXT) --namespace=$(NAMESPACE) apply -f orders.yaml

deploy-products:
	kubectl --context=$(CONTEXT) --namespace=$(NAMESPACE) apply -f products.yaml

deploy-gateway:
	kubectl --context=$(CONTEXT) --namespace=$(NAMESPACE) apply -f gateway.yaml

deploy-all: deploy-namespace deploy-orders deploy-products deploy-gateway

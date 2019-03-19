KOPS_STATE  ?= s3://kops.test.paytmlabs.com
KOPS_NAME   ?= demo.test.paytmlabs.com

create:
	export AWS_PROFILE=default
	kops create cluster --state $(KOPS_STATE) --zones us-west-2a $(KOPS_NAME)
	kops update cluster --name $(KOPS_NAME) --state $(KOPS_STATE) --out=../terraform_kubernetes --target=terraform

up:
	cd ../terraform_kubernetes; terraform apply

delete:
	kops delete  cluster --name $(KOPS_NAME) --state $(KOPS_STATE) --yes

getcfg:
	kops export kubecfg --name  $(KOPS_NAME) --state $(KOPS_STATE)

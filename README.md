# kstack-yaml
Quick and simple yaml for kafka on kuberenetes, suitable for evaluation or POC purposes

#  You will LOSE ANY DATA IN Kafka & zookeeper on redeploy with the yaml as-is !!! 
# If this is not desirable, sort out the volumes in 010-zookeeper.yaml and 020-kafka.yaml


See https://github.com/PaulieMac/kstack-yaml/search?q=NOTE&unscoped_q=NOTE for anything noteworthy


To run:
```
FILES=`ls *.yaml | sort -g`;
for yaml in $FILES
do
  	echo "Applying $yaml"
	kubectl apply -f $yaml --namespace=$nsp
done
```

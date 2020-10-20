# Torturing k8s dataset

To get a fresh up to dataset simply:

1. build [attack_range_cloud](https://github.com/splunk/attack_range_cloud/wiki/Configure-Cloud-Attack-Range)
2. copy the [kube-hunter.yml](kube-hunter.yml) under `kubernetes/` folder
3. run `kubectl create -f kubernetes/kube-hunter.yml --namespace kube-system`
4. to see of kube-hunter executed `kubectl get pods --namespace kube-system`
5. to get the logs from the attack run `python cloud_attack_range.py -a dump -dn torturing_k8s_dataset`

Instead of opensourcing the one from our attacks due to some information leak concerns we instead decided to share how we generated ours 😁.

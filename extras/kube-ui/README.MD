## Kubernetes UI

By default, the Kubernetes UI is deployed as a cluster addon. 

To access it, visit `https://<kubernetes-master>/ui`, which redirects to `https://<kubernetes-master>/api/v1/proxy/namespaces/kube-system/services/kube-ui/#/dashboard/`.

If you find that you're not able to access the UI, it may be because the kube-ui service has not been started on your cluster. In that case, you can start it manually with:

### Install

```kubectl create -f cluster/addons/kube-ui/kube-ui-rc.yaml --namespace=kube-system```

```kubectl create -f cluster/addons/kube-ui/kube-ui-svc.yaml --namespace=kube-system```

Normally, this should be taken care of automatically by the kube-addons.sh script that runs on the master.

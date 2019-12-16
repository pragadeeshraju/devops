    1 id
    2 yum install mlocate
    3 updatedb
    4 yum install awscli
    5 asw configure
    6 aws configure
    7 aws s3 ls
    8 aws s3 rm k8s.kube.com
    9 asw s3
   10 aws s3
   11 mkdir ~/tmp
   12 curl -LO https://storage.googleapis.com/kubernetes-release/release/$(curl -s 
https://storage.googleapis.com/kubernetes-release/release/stable.txt)/bin/linux/amd64/kubectl
   13 chmod +x ./kubectl
   14 sudo mv ./kubectl /usr/local/bin/kubectl
   15 wget https://github.com/kubernetes/kops/releases/download/1.10.0/kops-linux-amd64
   16 yum install wget
   17 wget https://github.com/kubernetes/kops/releases/download/1.10.0/kops-linux-amd64
   18 chmod +x kops-linux-amd64
   19 mv kops-linux-amd64 /usr/local/bin/kops
   20 aws s3 mb s3://k8s.cloudgeeks.club
   21 export KOPS_STATE_STORE=s3://k8s.cloudgeeks.club
   22 ssh-keygen -t rsa -C praga@cloudgeeks.club
   23 kops create cluster --zones=ap-southeast-1 k8s.cloudgeeks.club --state=s3://k8s.cloudgeeks.club
   24 kops create cluster --zone=ap-southeast-1 k8s.cloudgeeks.club --state=s3://k8s.cloudgeeks.club
   25 kops create cluster --zone=ap-southeast-1a k8s.cloudgeeks.club --state=s3://k8s.cloudgeeks.club
   26 kops create cluster --zones=ap-southeast-1a k8s.cloudgeeks.club --state=s3://k8s.cloudgeeks.club
   27 nslookup k8s.cloudgeeks.club
   28 yum install nslookup
   29 kops create cluster --zones=ap-southeast-1a k8s.cloudgeeks.club --state=s3://k8s.cloudgeeks.club --dns private
   30 kops delete cluster --zones=ap-southeast-1a k8s.cloudgeeks.club --state=s3://k8s.cloudgeeks.club
   31 kops delete cluster k8s.cloudgeeks.club --state=s3://k8s.cloudgeeks.club
   32 kops delete cluster k8s.cloudgeeks.club --state=s3://k8s.cloudgeeks.club --yes
   33 kops create cluster --zones=ap-southeast-1a k8s.cloudgeeks.club --state=s3://k8s.cloudgeeks.club --dns private
   34 kops delete cluster k8s.cloudgeeks.club --state=s3://k8s.cloudgeeks.club --yes
   35 kops create cluster --zones=ap-southeast-1a k8s.cloudgeeks.club --state=s3://k8s.cloudgeeks.club --dns private
   36 kops update cluster k8s.cloudgeeks.club --yes
   37 kops update cluster k8s.cloudgeeks.club --yes --state=s3://k8s.cloudgeeks.club
   38 kops validate cluster k8s.cloudgeeks.club
   39 kops validate cluster k8s.cloudgeeks.club --state=s3://k8s.cloudgeeks.club
   40 w
   41 cat /etc/sudoers
   42 kops validate cluster k8s.cloudgeeks.club --state=s3://k8s.cloudgeeks.club
   43 docker ps
   44 kubectl get pods
   45 kubectl apply -f https://raw.githubusercontent.com/kubernetes/dashboard/v1.10.1/src/deploy/recommended/kubernetes-dashboard.yaml
   46
   47 kubectl cluster-info dump
   48 kubectl cluster-info dump > /home/centos/
   49 kubectl cluster-info dump > /home/centos/clusterinfo_dump
   50 kubectl config view
   51 kops get secrets kube --type secret -oplaintext
   52 kops get secrets kube --type secret -oplaintext --state=s3://k8s.cloudgeeks.club
   53 ls
   54 lls
   55 ll
   56 cd tmp/
   57 ll
   58 ls
   59 cd ..
   60 kubectl get svc
   61 kubectl get pods
   62 kubectl proxy
   63 kubectl -n kube-system describe role kubernetes-dashboard-minimal
   64 ls
   65 ubectl create -f dashboard-admin.yaml
   66 kubectl create -f dashboard-admin.yaml
   67 vi dashboard-admin.yaml
   68 kubectl create -f dashboard-admin.yaml
   69 kubectl get pods --namespace-all
   70 kubectl get pods --all-namespaces
   71 ls
   72 kubectl create -f dashboard-admin.yaml
   73 history
   74 kubectl config view
   75 vi dashboard-admin.yaml
   76 kubectl -n kube-system describe secret $(kubectl -n kube-system get secret | grep eks-admin | awk '{print $1}')kubectl -n kube-system describe 
secret $(kubectl -n kube-system get secret | grep eks-admin | awk '{print $1}')
   77 kubectl get nodes
   78 ls
   79 history
   80 kubectl -n kube-system describe secret $(kubectl -n kube-system get secret | grep eks-admin | awk '{print $1}')
   81 ls
   82 vi dashboard-adminuser.yaml
   83 kubectl apply -f dashboard-adminuser.yaml
   84 kubectl -n kube-system describe secret $(kubectl -n kube-system get secret | grep admin-user | awk '{print $1}')
   85 kubectl -n kube-system describe secret $(kubectl -n kube-system get secret | grep admin-user | awk '{print $1}') > /home/centos/admin.txt
   86 kubectl -n kube-system describe secret $(kubectl -n kube-system get secret | grep admin-user | awk '{print $1}')
   87 ls
   88 vi vi kube-dashboard-access.yaml
   89 ls
   90 vi kube-dashboard-access.yaml
   91 kubectl create -f kube-dashboard-access.yaml
   92 vi kube-dashboard-access.yaml
   93 kubectl create -f kube-dashboard-access.yaml
   94 kubectl config view
   95 kubectl create rolebinding admin --clusterrole=admin --user=kube --namespace=default
   96 kubectl get nodea
   97 kubectl get nodes
   98 kubectl expose deployment helloworld --type=LoadBalancer --name=helloworld --port 8080
   99 kubectl create deployment helloworld --image=gcr.io/google-samples/node-hello:1.0
  100 kubectl expose deployment helloworld --type=LoadBalancer --name=helloworld --port 8080
  101 kubectl get services helloworld
  102 kubectl delete deployment helloworld --image=gcr.io/google-samples/node-hello:1.0
  103 kubectl get pods
  104 kubectl delete helloworld-6b78c456c-x7zqq
  105 kubectl get svc
  106 kubectl get nodes
  107 kubectl get pods
  108 kubectl delete pods helloworld-6b78c456c-k2bkh
  109 kubectl get pods
  110 docker ps
  111 kubectl get deploy
  112 kubectl delete depl helloworld
  113 kubectl get deployment
  114 kubectl delete deployment helloworld
  115 kubectl get pods
  116 kubectl config current-context
  117 kubectl config view
  118 kubectl create rolebinding admin --clusterrole=admin --user=k8s.cloudgeeks.club --namespace=default
  119 kubectl create rolebinding admin --clusterrole=admin --user=kube --namespace=all
  120 kubectl create rolebinding admin --clusterrole=admin --user=kube --namespace=default
  121 history
  122 kubectl version
  123 ls
  124 more dashboard-admin.yaml
  125 more dashboard-adminuser.yaml
  126 more kube-dashboard-access.yaml
  127 kubectl create -f kube-dashboard-access.yaml
  128 kubectl
  129 kubectl create rolebinding admin --clusterrole=admin --user=kube --namespace=kube-system
  130 kubectl view config
  131 kubectl config view
  132 kubectl create rolebinding admin --clusterrole=admin --user=k8s.cloudgeeks.club --namespace=default
  133 kubectl get pods
  134 kubectl get nodes
  135 kubectl get pods
  136 kubectl describe pod nginx-deployment-75675f5897-cc6jr
  137 history
  138 kubectl get namespaces
  139 kubectl create -f https://k8s.io/examples/admin/namespace-dev.json
  140 kubectl get namespaces
  141 kubectl get pods
  142 kubectl get node
  143 kubectl logs pod nginx-deployment-75675f5897-cc6jr
  144 kubectl logs nginx-deployment-75675f5897-cc6jr
  145 history > /home/centos/kube_installing_aws.txt
    1 id
    2 yum install mlocate
    3 updatedb
    4 yum install awscli
    5 asw configure
    6 aws configure
    7 aws s3 ls
    8 aws s3 rm k8s.kube.com
    9 asw s3
   10 aws s3
   11 mkdir ~/tmp
   12 curl -LO https://storage.googleapis.com/kubernetes-release/release/$(curl -s 
https://storage.googleapis.com/kubernetes-release/release/stable.txt)/bin/linux/amd64/kubectl
   13 chmod +x ./kubectl
   14 sudo mv ./kubectl /usr/local/bin/kubectl
   15 wget https://github.com/kubernetes/kops/releases/download/1.10.0/kops-linux-amd64
   16 yum install wget
   17 wget https://github.com/kubernetes/kops/releases/download/1.10.0/kops-linux-amd64
   18 chmod +x kops-linux-amd64
   19 mv kops-linux-amd64 /usr/local/bin/kops
   20 aws s3 mb s3://k8s.cloudgeeks.club
   21 export KOPS_STATE_STORE=s3://k8s.cloudgeeks.club
   22 ssh-keygen -t rsa -C praga@cloudgeeks.club
   23 kops create cluster --zones=ap-southeast-1 k8s.cloudgeeks.club --state=s3://k8s.cloudgeeks.club
   24 kops create cluster --zone=ap-southeast-1 k8s.cloudgeeks.club --state=s3://k8s.cloudgeeks.club
   25 kops create cluster --zone=ap-southeast-1a k8s.cloudgeeks.club --state=s3://k8s.cloudgeeks.club
   26 kops create cluster --zones=ap-southeast-1a k8s.cloudgeeks.club --state=s3://k8s.cloudgeeks.club
   27 nslookup k8s.cloudgeeks.club
   28 yum install nslookup
   29 kops create cluster --zones=ap-southeast-1a k8s.cloudgeeks.club --state=s3://k8s.cloudgeeks.club --dns private
   30 kops delete cluster --zones=ap-southeast-1a k8s.cloudgeeks.club --state=s3://k8s.cloudgeeks.club
   31 kops delete cluster k8s.cloudgeeks.club --state=s3://k8s.cloudgeeks.club
   32 kops delete cluster k8s.cloudgeeks.club --state=s3://k8s.cloudgeeks.club --yes
   33 kops create cluster --zones=ap-southeast-1a k8s.cloudgeeks.club --state=s3://k8s.cloudgeeks.club --dns private
   34 kops delete cluster k8s.cloudgeeks.club --state=s3://k8s.cloudgeeks.club --yes
   35 kops create cluster --zones=ap-southeast-1a k8s.cloudgeeks.club --state=s3://k8s.cloudgeeks.club --dns private
   36 kops update cluster k8s.cloudgeeks.club --yes
   37 kops update cluster k8s.cloudgeeks.club --yes --state=s3://k8s.cloudgeeks.club
   38 kops validate cluster k8s.cloudgeeks.club
   39 kops validate cluster k8s.cloudgeeks.club --state=s3://k8s.cloudgeeks.club
   40 w
   41 cat /etc/sudoers
   42 kops validate cluster k8s.cloudgeeks.club --state=s3://k8s.cloudgeeks.club
   43 docker ps
   44 kubectl get pods
   45 kubectl apply -f https://raw.githubusercontent.com/kubernetes/dashboard/v1.10.1/src/deploy/recommended/kubernetes-dashboard.yaml
   46 kubectl cluster-info
   47 kubectl cluster-info dump
   48 kubectl cluster-info dump > /home/centos/
   49 kubectl cluster-info dump > /home/centos/clusterinfo_dump
   50 kubectl config view
   51 kops get secrets kube --type secret -oplaintext
   52 kops get secrets kube --type secret -oplaintext --state=s3://k8s.cloudgeeks.club
   53 ls
   54 lls
   55 ll
   56 cd tmp/
   57 ll
   58 ls
   59 cd ..
   60 kubectl get svc
   61 kubectl get pods
   62 kubectl proxy
   63 kubectl -n kube-system describe role kubernetes-dashboard-minimal
   64 ls
   65 ubectl create -f dashboard-admin.yaml
   66 kubectl create -f dashboard-admin.yaml
   67 vi dashboard-admin.yaml
   68 kubectl create -f dashboard-admin.yaml
   69 kubectl get pods --namespace-all
   70 kubectl get pods --all-namespaces
   71 ls
   72 kubectl create -f dashboard-admin.yaml
   73 history
   74 kubectl config view
   75 vi dashboard-admin.yaml
   76 kubectl -n kube-system describe secret $(kubectl -n kube-system get secret | grep eks-admin | awk '{print $1}')kubectl -n kube-system describe 
secret $(kubectl -n kube-system get secret | grep eks-admin | awk '{print $1}')
   77 kubectl get nodes
   78 ls
   79 history
   80 kubectl -n kube-system describe secret $(kubectl -n kube-system get secret | grep eks-admin | awk '{print $1}')
   81 ls
   82 vi dashboard-adminuser.yaml
   83 kubectl apply -f dashboard-adminuser.yaml
   84 kubectl -n kube-system describe secret $(kubectl -n kube-system get secret | grep admin-user | awk '{print $1}')
   85 kubectl -n kube-system describe secret $(kubectl -n kube-system get secret | grep admin-user | awk '{print $1}') > /home/centos/admin.txt
   86 kubectl -n kube-system describe secret $(kubectl -n kube-system get secret | grep admin-user | awk '{print $1}')
   87 ls
   88 vi vi kube-dashboard-access.yaml
   89 ls
   90 vi kube-dashboard-access.yaml
   91 kubectl create -f kube-dashboard-access.yaml
   92 vi kube-dashboard-access.yaml
   93 kubectl create -f kube-dashboard-access.yaml
   94 kubectl config view
   95 kubectl create rolebinding admin --clusterrole=admin --user=kube --namespace=default
   96 kubectl get nodea
   97 kubectl get nodes
   98 kubectl expose deployment helloworld --type=LoadBalancer --name=helloworld --port 8080
   99 kubectl create deployment helloworld --image=gcr.io/google-samples/node-hello:1.0
  100 kubectl expose deployment helloworld --type=LoadBalancer --name=helloworld --port 8080
  101 kubectl get services helloworld
  102 kubectl delete deployment helloworld --image=gcr.io/google-samples/node-hello:1.0
  103 kubectl get pods
  104 kubectl delete helloworld-6b78c456c-x7zqq
  105 kubectl get svc
  106 kubectl get nodes
  107 kubectl get pods
  108 kubectl delete pods helloworld-6b78c456c-k2bkh
  109 kubectl get pods
  110 docker ps
  111 kubectl get deploy
  112 kubectl delete depl helloworld
  113 kubectl get deployment
  114 kubectl delete deployment helloworld
  115 kubectl get pods
  116 kubectl config current-context
  117 kubectl config view
  118 kubectl create rolebinding admin --clusterrole=admin --user=k8s.cloudgeeks.club --namespace=default
  119 kubectl create rolebinding admin --clusterrole=admin --user=kube --namespace=all
  120 kubectl create rolebinding admin --clusterrole=admin --user=kube --namespace=default
  121 history
  122 kubectl version
  123 ls
  124 more dashboard-admin.yaml
  125 more dashboard-adminuser.yaml
  126 more kube-dashboard-access.yaml
  127 kubectl create -f kube-dashboard-access.yaml
  128 kubectl
  129 kubectl create rolebinding admin --clusterrole=admin --user=kube --namespace=kube-system
  130 kubectl view config
  131 kubectl config view
  132 kubectl create rolebinding admin --clusterrole=admin --user=k8s.cloudgeeks.club --namespace=default
  133 kubectl get pods
  134 kubectl get nodes
  135 kubectl get pods
  136 kubectl describe pod nginx-deployment-75675f5897-cc6jr
  137 history
  138 kubectl get namespaces
  139 kubectl create -f https://k8s.io/examples/admin/namespace-dev.json
  140 kubectl get namespaces
  141 kubectl get pods
  142 kubectl get node
  143 kubectl logs pod nginx-deployment-75675f5897-cc6jr
  144 kubectl logs nginx-deployment-75675f5897-cc6jr
  145 history > /home/centos/kube_installing_aws.txt
  146 ls
  147 more dashboard-admin.yaml
  148 kubectl get pods
  149 kubectl get deploy --all-namespaces -o wide
  150 kub
  151 kubectl get deploy -n kube-system kubernetes-dashboard -o yaml
  152 uname -a
  153 kubectl get node
  154 $ kubectl create clusterrolebinding kubernetes-dashboard -n kube-system --clusterrole=cluster-admin 
--serviceaccount=kube-system:kubernetes-dashboard
  155 kubectl create clusterrolebinding kubernetes-dashboard -n kube-system --clusterrole=cluster-admin 
--serviceaccount=kube-system:kubernetes-dashboard
  156 kubectl config view
  157 ls
  158 kubectl -n kube-system get secret
  159 kubectl -n kube get secret
  160 ls
  161 cat dashboard-admin.yaml
  162 kops get secrets kube --type secret -oplaintext
  163 kops get secrets kube --type secret -oplaintext --states3://k8s.kube.com
  164 kops get secrets kube --type secret -oplaintext --state=s3://k8s.kube.com
  165 ls
  166 more dashboard-admin.yaml
  167 kubectl get svc
  168 kubectl get clusterrole cluster-admin -n kube-system -o yaml
  169 kubectl config view
  170 ls
  171 cat dashboard-admin.yaml
  172 kubectl -n kube-system describe secret $(kubectl -n kube-system get secret | grep cluster-admin | awk '{print $1}')
  173 kubectl get nodes
  174 w
  175 kubectl get pods
  176 \
  177 exit
  178 locate aws
  179 EXIT
  180 exit
  181 kubectl get pods
  182 kubectl desc pod nginx-deployment-75675f5897-lvnv4 -o json
  183 kubectl describe pod nginx-deployment-75675f5897-lvnv4 -o json
  184 kubectl describe pod nginx-deployment-75675f5897-lvnv4 -o yaml
  185 kubectl describe pod nginx-deployment-75675f5897-lvnv4 -o=yaml
  186 kubectl describe pod nginx-deployment-75675f5897-lvnv4 --o=yaml
  187 kubectl describe pod nginx-deployment-75675f5897-lvnv4
  188 kubectl get pods
  189 kubectl get pods -o yaml
  190 kubectl get pods -ojson
  191 kubectl get pods
  192 kubectl get nodes
  193 kubectl get nodes -o wide
  194 kubectl get namespaces -o wide
  195 kubectl describe pod nginx-deployment-75675f5897-cc6jr
  196 cat << EOF | kubectl create -f -
  197 cat << EOF | kubectl create -f
  198 kubectl get comp
  199 kubectl get component
  200 kubectl get components
  201 kubectl get componentstatus
  202 locate yaml
  203 locate kops
  204 cd /usr/local/bin/kops
  205 ls
  206 cd /usr/local/bin
  207 ls
  208 cd kops
  209 more kops
  210 locate kops
  211 locate yaml
  212 ls
  213 kubectl get pods
  214 kubectl get nodes
  215 kubectl version
  216 kubernetes version
  217 kubectl get secrets
  218 kubectl get deploy
  219 kubectl delete nginx-deployment
  220 cat <<EOF >./kustomization.yaml
  221 secretGenerator:
  222 - name: mysql-pass
  223 literals:
  224 - password=1234
  225 EOF
  226 ls
  227 kubectl get pvc
  228 curl -LO https://k8s.io/examples/application/wordpress/mysql-deployment.yaml
  229 ls
  230 curl -LO https://k8s.io/examples/application/wordpress/wordpress-deployment.yaml
  231 cat <<EOF >>./kustomization.yaml
  232 resources:
  233 - mysql-deployment.yaml
  234 - wordpress-deployment.yaml
  235 EOF
  236 more kustomization.yaml
  237 cat <<EOF >>./kustomization.yaml
  238 resources:
  239 - mysql-deployment.yaml
  240 - wordpress-deployment.yaml
  241 EOF
  242 vi kustomization.yaml
  243 kubectl apply -k ./
  244 kubectl get secrets
  245 kubectl get pvc
  246 kubectl get pods
  247 kubectl get services wordpress
  248 kubectl get services wordpress --url
  249 kubectl service wordpress --url
  250 kubectl get services wordpress
  251 kubectl get services
  252 kubectl delete -k ./
  253 df -h
  254 kubectl get nodes
  255 kubectl get pods
  256 kubectl delete pods nginx-deployment-75675f5897-cc6jr
  257 kubectl get pods
  258 kubectl get deployment
  259 kubectl delete deployment nginx-deployment
  260 kubectl get deployment
  261 kubectl get pods
  262 ls
  263 kubectl apply -k ./
  264 kubectl get pods
  265 kubectl delete -k ./
  266 kubectl get pods
  267 kubectl version
  268 kubectl cluster-info
  269 kubectl config get-contexts
  270 ls
  271 ls -ls
  272 ls -la
  273 cd .kube/
  274 ls
  275 more config
  276 ls -a
  277 cd ..
  278 ls
  279 ls -a
  280 ll
  281 ll -a
  282 ls
  283 cd /tmp
  284 curl https://raw.githubusercontent.com/kubernetes/helm/master/scripts/get > install-helm.sh
  285 chmod u+x install-helm.sh
  286 ./install-helm.sh
  287 kubectl -n kube-system create serviceaccount tiller
  288 cd ..
  289 kubectl create clusterrolebinding tiller --clusterrole cluster-admin --serviceaccount=kube-system:tiller
  290 helm init --service-account tiller
  291 kubectl get pods --namespace kube-system
  292 helm list
  293 kubectl get svc
  294 helm install --name wpblog stable/wordpress
  295 kubectl
  296 kubectl get pods
  297 kubectl get svc
  298 helm --list
  299 helm lisy
  300 helm list
  301 helm repo update
  302 helm list
  303 helm inspect chart stable/wordpress
  304 heml upgrade wpblog stable/wordpress
  305 helm upgrade wpblog stable/wordpress
  306 helm list
  307 helm rollback wpblog 1
  308 helm list
  309 helm uninstall wpblog
  310 helm delete wpblog
  311 helmlist
  312 helm list
  313 kubectl get pods
  314 kubectl get svc
  315 history
  316 kubectl -n kafka exec -ti wpblog-wordpress-8c4d6cd86-pdbkn --kafka-console-producer --broker-list my-kafka^Ceadless:9092 --topic test1
  317 kubectl -n kafka exec -ti wpblog-wordpress-8c4d6cd86-pdbkn -- kafka-console-producer --broker-list my-kafka^Ceadless:9092 --topic test1
  318 kubectl -n kafka exec -ti wpblog-wordpress-8c4d6cd86-pdbkn -- kafka-console-producer --broker-list my-kafkaheadless:9092 --topic test1
  319 kubectl -n kafka exec -ti wpblog-mariadb -- kafka-console-producer --broker-list my-kafkaheadless:9092 --topic test1
  320 helm install --name prometheus stable/prometheus
  321 kubectl get svc
  322 export POD_NAME=$(kubectl get pods --namespace default -l "app=prometheus,component=server" -o jsonpath="{.items[0].metadata.name}")
  323 kubectl get svc
  324 kubectl --namespace default port-forward $POD_NAME 9090
  325 kubectl get svc
  326 kubectl apply -f https://raw.githubusercontent.com/kubernetes/kops/master/addons/ingress-nginx/v1.6.0.yaml
  327 kubectl get svc
  328 kubectl get poda
  329 kubectl get pods
  330 kubectl get services ingress-nginx
  331 ubectl apply -f https://raw.githubusercontent.com/kubernetes/contrib/master/ingress/controllers/nginx/examples/ingress.yaml
  332 kubectl apply -f https://raw.githubusercontent.com/kubernetes/contrib/master/ingress/controllers/nginx/examples/ingress.yaml
  333 kubectl get services ingress-nginx
  334 kubectl get poda
  335 kubectl get pods
  336 kubectl get services
  337 kubectl get services ingress-nginx -owide
  338 kubectl expose prometheus-alertmanager
  339 kubectl ekubectl expose -h
  340 kubectl expose -h
  341 ls
  342 kubectl get dployment
  343 kubectl get deployment
  344 kubectl describe deployments prometheus-alertmanager
  345 kubectl expose deployment prometheus-alertmanager --type=LoadBalancer --name=newlb
  346 kubectl get svc
  347 kubectl expose deployment prometheus-server --type=LoadBalancer --name=newl
  348 kubectl get svc
  349 kubectl expose deployment prometheus-node-exporter --type=LoadBalancer --name=new
  350 kubectl get deployments
  351 ping ab90879909ae111e99541029ffe029a8-1952539723.ap-southeast-1.elb.amazonaws.com/
  352 helm repo add incubator http://storage.googleapis.com/kubernetes-charts-incubator
  353 helm list
  354 kubectl create ns kafka
  355 helm install --name my-kafka --namespace kafka incubator/kafka
  356 kubectl get svc
  357 kubectl get pods
  358 kubectl -n kafka exec testclient -- kafka-topics --zookeeper my-kafka-zookeeper:2181 --list
  359 helm install --name wpblog stable/wordpress
  360 helm ls --all wpblog
  361 helm del --purge wpblog
  362 helm install --name wpblog stable/wordpress
  363 kubectl get pods
  364 kubectl get svc
  365 kubectl get pods
  366 kubectl get pods --namespace-all
  367 kubectl get pods --all-namespaces
  368 kubectl get svc --all-namespaces
  369 curl -v 100.67.141.110
  370 kubectl get nodes
  371 kubectl get describe node ip-172-20-57-171.ap-southeast-1.compute.internal
  372 kubectl describe node ip-172-20-57-171.ap-southeast-1.compute.internal
  373 kubectl describe node ip-172-20-57-171.ap-southeast-1.compute.internal -o yaml
  374 kubectl describe node ip-172-20-57-171.ap-southeast-1.compute.internal -O yaml
  375 kubectl describe node ip-172-20-57-171.ap-southeast-1.compute.internal yaml
  376 history
  377 history >> /home/centos/kube_installing_aws.txt

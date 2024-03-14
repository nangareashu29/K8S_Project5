  1  curl -Lo minikube https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
    2  chmod +x minikube
    3  sudo mv minikube /usr/local/bin/
    4  curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"
    5  chmod +x kubectl
    6  sudo mv kubectl /usr/local/bin/
    7  minikube start --driver=docker
    8  mkdir project
    9  cd project/
   10  git clone https://github.com/nangareashu29/K8s_Project5.git
   11  ls
   12  cd K8s_Project5/
   14  git status
   15  git remote -v
   26  git branch -r
   27  git switch master
   28  ls
   29  git pull origin master
   30  ls
   31  vim service.yml
   43  kubectl create namespace node-app
   44  kubectl apply -f pod.yml
   45  kubectl apply -f replica-set.yml
   46  kubectl apply -f deployment.yml
   47  kubectl apply -f service.yml
   48  kubectl get svc -n node-app
   

1. go mod init webservverfc
2. criação do main.go
3. Geração da imagem docker
    3.1 criação do Dockerfile
    3.2 executar: docker build -t mmkusma/gitopsfc:latest .
    3.3 para testar: docker run --rm -p 8090:8090 mmkusma/gitopsfc:latest
    3.4 subir para o repo: docker push mmkusma/gitopsfc:latest
4. Setup do cd.yaml
    4.1 criação do repositorio no github
    4.2 criação do secret
5. Inicialização do git
    5.1 git init
    5.2 git add .
    5.3 git commit -m "first commit"
    5.4 git remote add origin git@github.com:mmkusma/gitopsfc.git
    5.5 git push -u origin main

6. Preparando o Kubernetes
    6.1 Criar o cluster no kind: kind create cluster --name gitopsfc
    6.2 Aplicar o contexto: kubectl cluster-info --context kind-gitopsfc
    6.3 Criar o deployment.yaml e service.yaml
7. Kustomize
    7.1 Instalar: brew install kustomize
    7.2 preparar arquivo kustomization.yaml
    7.3 Instalar o kustomize no cd.yaml

    


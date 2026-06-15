# Provisionando um Container Nginx com Terraform e Docker

## Objetivo

Automatizar a criação de um container Nginx utilizando Terraform como ferramenta de Infraestrutura como Código (IaC) e Docker como plataforma de containers.

## Tecnologias Utilizadas

* Terraform
* Docker
* Provider Docker (Kreuzwerker)

## Arquivos

### main.tf

Responsável por:

* Configurar o provider Docker
* Baixar a imagem nginx:latest
* Criar o container
* Expor a aplicação na porta configurada

### variables.tf

Define variáveis para:

* Nome da imagem
* Nome do container
* Porta interna
* Porta externa

## Fluxo da Infraestrutura

1. Terraform inicializa o provider Docker
2. Terraform faz o pull da imagem nginx
3. Terraform cria o container
4. A porta 80 do container é mapeada para a porta 8080 do host
5. A aplicação fica disponível em:

http://localhost:8080

## Comandos Executados

Inicialização:

```bash
terraform init
```

Validação:

```bash
terraform validate
```

Visualização do plano:

```bash
terraform plan
```

Provisionamento:

```bash
terraform apply
```

Remoção da infraestrutura:

```bash
terraform destroy
```

## Aprendizados

* Conceitos de Infraestrutura como Código (IaC)
* Utilização de providers no Terraform
* Criação e gerenciamento de containers Docker via Terraform
* Uso de variáveis para tornar a infraestrutura reutilizável
* Versionamento e documentação de infraestrutura

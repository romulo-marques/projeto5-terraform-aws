# Projeto 5: Provisionamento de Storage S3 na AWS com Terraform (IaC)

Este projeto demonstra a automação da infraestrutura como código (IaC) utilizando o **Terraform** para provisionar e gerenciar o ciclo de vida completo de um bucket **Amazon S3** na AWS.

---

## 🛠️ Tecnologias Utilizadas

- **Terraform:** Gerenciamento e autoria da infraestrutura como código.
- **Amazon Web Services (AWS):** Provedor de nuvem (AWS S3).
- **AWS CLI:** Autenticação e credenciais de acesso local.
- **PowerShell:** Terminal de execução.

---

## 📁 Estrutura do Código (`main.tf`)

```hcl
terraform {
  required_providers {
    aws = {
      source  = "hashicorp/aws"
      version = "~> 5.0"
    }
  }
}

provider "aws" {
  region = "us-east-1"
}

resource "aws_s3_bucket" "meu_bucket_projeto5" {
  bucket = "projeto5-terraform-romul-12345"
}

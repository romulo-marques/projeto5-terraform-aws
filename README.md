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
📸 Evidências do Projeto (Prints)
1. Código-Fonte da Infraestrutura (main.tf)
Estrutura do código HCL criada no editor definindo o provedor AWS e o bucket S3.

2. Planejamento da Infraestrutura (terraform plan)
Execução da prévia do plano no terminal confirmando a criação de 1 recurso.

3. Provisionamento do Recurso (terraform apply)
Execução do comando apply e aprovação com yes para a criação efetiva na AWS.

4. Validação no Console AWS S3
Confirmação do recurso projeto5-terraform-romul-12345 criado e visível na conta AWS S3.

5. Destruição da Infraestrutura (terraform destroy)
Remoção controlada do recurso via código para garantir a limpeza do ambiente e evitar custos.

6. Validação de Limpeza no Console AWS (Clean Up)
Verificação final no Console S3 comprovando que o bucket foi totalmente removido da nuvem.
}

provider "aws" {
  region = "us-east-1"
}

resource "aws_s3_bucket" "meu_bucket_projeto5" {
  bucket = "projeto5-terraform-romul-12345"
}

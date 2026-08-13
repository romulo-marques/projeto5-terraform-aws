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
}📸 Evidências do Projeto (Prints)
1. Código-Fonte da Infraestrutura (main.tf)
Estrutura do código HCL criada no editor definindo o provedor AWS e o bucket S3.
<img width="370" height="446" alt="print1 png" src="https://github.com/user-attachments/assets/49426189-4703-404b-b942-de7a516a681e" />


2. Planejamento da Infraestrutura (terraform plan)
Execução da prévia do plano no terminal confirmando a criação de 1 recurso.
<img width="728" height="619" alt="print2 png" src="https://github.com/user-attachments/assets/2751ed0d-b852-4ec6-8112-6f7e979c0019" />


3. Provisionamento do Recurso (terraform apply)
Execução do comando apply e aprovação com yes para a criação efetiva na AWS.
<img width="728" height="617" alt="print3 png" src="https://github.com/user-attachments/assets/76dc29e3-aaf2-4f7f-933e-ac666832b6c8" />

4. Validação no Console AWS S3
Confirmação do recurso projeto5-terraform-romul-12345 criado e visível na conta AWS S3

<img width="977" height="510" alt="print4 png" src="https://github.com/user-attachments/assets/e83d7aa3-2e02-4e3f-bda2-cb6aafb00d7b" />

5. Destruição da Infraestrutura (terraform destroy)
Remoção controlada do recurso via código para garantir a limpeza do ambiente e evitar custos.
<img width="908" height="595" alt="print5 png" src="https://github.com/user-attachments/assets/7c9a7661-f17b-4ebc-a012-bceee2746c61" />

6. Validação de Limpeza no Console AWS (Clean Up)
Verificação final no Console S3 comprovando que o bucket foi totalmente removido da nuvem.
<img width="1357" height="538" alt="print6 png" src="https://github.com/user-attachments/assets/a8df7025-1431-44fc-9fe6-4bb8ad745031" />

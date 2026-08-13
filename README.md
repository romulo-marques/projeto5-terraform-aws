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
```

---

## 📸 Evidências do Projeto (Prints)
<img width="370" height="446" alt="print1 png" src="https://github.com/user-attachments/assets/89107052-edaf-4b47-8e65-db2eae2ef5a2" />
<img width="728" height="619" alt="print2 png" src="https://github.com/user-attachments/assets/640d1207-7dc8-4e46-a18c-97a241bfacb0" />

<img width="728" height="617" alt="print3 png" src="https://github.com/user-attachments/assets/4e80427c-cc90-492d-9aaa-a9538c11730c" />
<img width="977" height="510" alt="print4 png" src="https://github.com/user-attachments/assets/ccfc8caa-957f-4ba4-8fc9-a27594e608c2" />
<img width="908" height="595" alt="print5 png" src="https://github.com/user-attachments/assets/9fae3974-29f1-4b65-b387-379f700491c8" />
<img width="1357" height="538" alt="print6 png" src="https://github.com/user-attachments/assets/8728390e-449f-4ea5-a24e-cee8648be7e0" />


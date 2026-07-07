# 📊 AWS Lambda Word Count | Serverless Project

Este projeto demonstra a criação de uma aplicação **Serverless** utilizando **AWS Lambda**, **Amazon S3**, **Amazon SNS** e **Python** para automatizar a contagem de palavras em arquivos de texto.

## 🎥 Demonstração

Assista ao projeto completo no YouTube:

👉 https://youtu.be/b8IH6fgRpOc

---

# 📌 Objetivo

Desenvolver uma solução capaz de contar automaticamente o número de palavras de um arquivo `.txt` enviado para um bucket do Amazon S3.

Sempre que um arquivo é enviado:

* O Amazon S3 gera um evento.
* O evento aciona uma função AWS Lambda.
* A função faz a leitura do arquivo.
* O conteúdo é processado em Python.
* A quantidade de palavras é calculada.
* O resultado é enviado por e-mail utilizando o Amazon SNS.

---

# 🏗️ Arquitetura

```text
           Upload arquivo .txt
                    │
                    ▼
              Amazon S3
                    │
        Evento ObjectCreated
                    │
                    ▼
              AWS Lambda
                    │
        Leitura do arquivo
                    │
        Contagem de palavras
                    │
                    ▼
              Amazon SNS
                    │
                    ▼
           Envio de E-mail
```

---

# ☁️ Serviços AWS utilizados

* AWS Lambda
* Amazon S3
* Amazon SNS
* Amazon CloudWatch
* AWS IAM

---

# 🐍 Linguagem

* Python 3

---

# 📚 Bibliotecas

* boto3
* json
* urllib.parse

---

# 📁 Estrutura do projeto

```text
.
├── lambda_function.py
└── README.md
```

---

# ⚙️ Funcionamento

A função Lambda é acionada automaticamente por um evento do Amazon S3.

Ela executa as seguintes etapas:

1. Recebe o evento enviado pelo bucket.
2. Identifica o bucket e o arquivo.
3. Lê o conteúdo do arquivo.
4. Conta a quantidade de palavras.
5. Publica o resultado em um tópico do Amazon SNS.
6. O Amazon SNS envia automaticamente um e-mail com a contagem.

### Exemplo de saída

**Assunto**

```text
Word Count Result
```

**Mensagem**

```text
The word count in the example.txt file is 154.
```

---

# 🚀 Como executar

1. Criar um bucket no Amazon S3.
2. Criar um tópico no Amazon SNS.
3. Confirmar a assinatura de e-mail.
4. Criar uma função AWS Lambda em Python.
5. Configurar a Role IAM (`LambdaAccessRole` ou equivalente).
6. Configurar o gatilho do Amazon S3.
7. Fazer upload de um arquivo `.txt`.
8. Verificar o recebimento do e-mail.

---

# 🎯 Conceitos demonstrados

* Computação em Nuvem
* Serverless Computing
* Event-Driven Architecture
* AWS Lambda
* Amazon S3
* Amazon SNS
* Amazon CloudWatch
* IAM
* Python
* Boto3

---

# 💼 Sobre este projeto

Este projeto foi desenvolvido como parte dos meus estudos em **Cloud Computing (AWS)** e integra meu portfólio de projetos práticos.

O objetivo é demonstrar conhecimentos em desenvolvimento de soluções serverless, automação de processos e integração entre serviços da AWS.

---

## 👩‍💻 Desenvolvido por

**Jéssica Fontes**

🔗 Vídeo do projeto: https://youtu.be/b8IH6fgRpOc

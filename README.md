# aws-cloud-formation-desafio

# Template 1 — S3 Bucket

## Descrição
Este template cria um bucket simples no Amazon S3 usando AWS CloudFormation.

## Recursos criados
- **AWS::S3::Bucket** → Bucket chamado `luana-bucket-exemplo`.

## Como usar
1. Salve este template em um arquivo `s3-bucket.yaml`.
2. No console da AWS CloudFormation, clique em *Create stack*.
3. Faça upload do arquivo e finalize a criação.
4. Verifique se a stack aparece como **CREATE_COMPLETE**.
5. Vá ao console do S3 e confirme que o bucket foi criado.

## Teste
- Faça upload de um arquivo no bucket pelo console do S3.
- Ou use AWS CLI:
  ```bash
  aws s3 ls s3://luana-bucket-exemplo

<img width="1918" height="805" alt="luana-bucket" src="https://github.com/user-attachments/assets/46d7fdeb-314b-488c-a3ef-7da0e9e12f4f" />


---

## 📌 Template **Lambda com Role IAM**

<img width="1918" height="863" alt="lambda" src="https://github.com/user-attachments/assets/9accb5c0-02c1-4a91-8151-d1465abb693b" />

```markdown
# Template corrigido — Lambda com Role IAM

## Descrição
Este template cria uma função Lambda em Python 3.9 com uma role IAM básica para execução.

## Recursos criados
- **AWS::IAM::Role** → Role chamada `lambda-basic-role-exemplo`, com política `AWSLambdaBasicExecutionRole`.
- **AWS::Lambda::Function** → Função chamada `luana-funcao-exemplo`.

## Como usar
1. Salve este template em um arquivo `lambda-role.yaml`.
2. No console da AWS CloudFormation, clique em *Create stack*.
3. Faça upload do arquivo e finalize a criação.
4. Verifique se a stack aparece como **CREATE_COMPLETE**.
5. Vá ao console da Lambda e confirme que a função foi criada.

## Teste
- No console da Lambda, clique em *Test*.
- Crie um evento de teste simples:
  ```json
  { "mensagem": "teste" }

{"Olá, Luana! Execução Lambda bem-sucedida."}





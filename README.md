
# ✅ DevOps - Checkpoint 2

Este documento apresenta a sequência de atividades realizadas para o segundo checkpoint da disciplina de DevOps, com foco em Docker, Azure Container Registry (ACR) e Azure Container Instance (ACI). Todas as etapas foram executadas com sucesso e estão acompanhadas por evidências visuais (prints).

---

## 🔧 Etapas Realizadas

### 1. Início do Docker Desktop
O Docker Desktop foi iniciado para permitir a construção e envio da imagem da aplicação.

### 2. Clonagem do Repositório
Foi realizado o clone do repositório oficial do projeto Jokenpo:

git clone https://github.com/ferreiralucas92/jokenpo


### 3. Acesso ao Diretório do Projeto
Navegação até a pasta clonada:

---

## ☁️ Provisionamento no Azure

### 4. Criação do Grupo de Recursos
Grupo de recursos criado com os seguintes parâmetros:
- Nome: `devops-checkpoint-2`
- Região: `West US 2`

📸 ![Print da tela](https://raw.githubusercontent.com/WedSan/devops-checkpoint-3/refs/heads/main/assets/print_step_4.png)

---

### 5. Criação do Azure Container Registry (ACR)
ACR criado com:
- Nome: `devopscheckpoint2acr`
- SKU: `Basic`

📸 ![Print da tela](https://raw.githubusercontent.com/WedSan/devops-checkpoint-3/refs/heads/main/assets/print_step_5.png)

---

### 6. Login no ACR via CLI
Comando executado:

---

### 7. Verificação de Saúde do ACR
Comando utilizado:
---

### 8. Login no ACR
Realizado login com credenciais fornecidas pela Azure.

---

### 9. Habilitação do Usuário Administrador
Usuário administrador do ACR habilitado para facilitar o push da imagem.

---

## 🐳 Docker e Imagem da Aplicação

### 10. Criação da Imagem Docker
Imagem construída a partir do `Dockerfile` do projeto.

📸 ![Print da tela](https://raw.githubusercontent.com/WedSan/devops-checkpoint-3/refs/heads/main/assets/print_step_10.png)

---

### 11. Aplicação da Tag v1
Imagem versionada com a tag `1.0` invés de `v1`, por questão de costume.

📸 ![Print da tela](https://raw.githubusercontent.com/WedSan/devops-checkpoint-3/refs/heads/main/assets/print_step_10.png)

---

### 12. Push da Imagem para o ACR
Imagem com tag `1.0` enviada com sucesso ao Azure Container Registry.

📸 ![Print da tela](https://raw.githubusercontent.com/WedSan/devops-checkpoint-3/refs/heads/main/assets/print_step_12.png)

---

### 13. Listagem dos Registros no ACR
Comando para listar o ACR no formato de tabela executado:

📸 ![Print da tela](https://raw.githubusercontent.com/WedSan/devops-checkpoint-3/refs/heads/main/assets/print_step_13.png)

---

## 🚀 Deploy com Azure Container Instance (ACI)

### 14. Criação do Container no ACI
Container criado com as configurações:
- Imagem: `devopscheckpoint2acr.azurecr.io/devops-checkpoint-2-code:1.0 
- CPU: 1
- Memória: 1 GB
- SO: Linux
- IP Público
- Portas expostas: 3000, 80 e 8080

📸 ![Print da tela](https://raw.githubusercontent.com/WedSan/devops-checkpoint-3/refs/heads/main/assets/print_step_14.png)

---

### 15. Link de Acesso à Aplicação
Aplicação acessível através do link:

🌐 [http://devops-checkpoint-2.westus2.azurecontainer.io/](http://devops-checkpoint-2.westus2.azurecontainer.io/)

---

## 🧹 Encerramento

### 16. Exclusão de Recursos no Azure
Após a validação do professor e o funcionamento correto da aplicação, todos os recursos foram removidos.
Obs: Eu irei apenas excluir os recursos após o professor dar a nota final. Não mostrei print da remoção do recurso por motivos óbvios.



---

## 📎 Observações Finais

- Todas as atividades foram realizadas com base nos requisitos da avaliação.
- Os prints comprovam a execução bem-sucedida de cada etapa.
- O link de acesso estava ativo no momento da entrega, conforme solicitado. Sendo excluído após a correção do professor
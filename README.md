# Criando uma Instância Gerenciada de SQL no Azure

Este repositório registra minha experiência criando uma **Instância Gerenciada de SQL** no Microsoft Azure. A proposta do desafio foi entender o processo e documentar os principais passos, anotações e aprendizados.

---

## 🎯 Objetivo

- Criar uma Instância Gerenciada de SQL no Azure
- Aprender a configurar rede, segurança, armazenamento e autenticação
- Registrar o passo a passo de forma simples para estudo futuro

---

## ✅ Pré-requisitos

- Conta gratuita no [Portal do Azure](https://portal.azure.com)
- Permissões adequadas para criar recursos
- Navegador de internet

---

## 🛠️ Passo a Passo (Portal do Azure)

### 1. Acesso inicial
- Acesse o portal do Azure e clique em **SQL do Azure**
- Clique em **Criar** e escolha **Instância Gerenciada de SQL**

### 2. Guia "Básico"
- **Assinatura:** sua assinatura do Azure
- **Grupo de recursos:** novo ou existente
- **Nome da instância:** exemplo: `instancia-sql-dio`
- **Região:** Brasil Sul (ou a mais próxima)
- **Autenticação:** SQL (usuário e senha)
- **Usuário admin:** nome válido (ex: `adminuser`)
- **Senha forte:** mínimo 16 caracteres

### 3. Computação + Armazenamento
- **Camada de serviço:** Uso Geral
- **Geração de hardware:** Standard (Gen5)
- **vCores e armazenamento:** defina conforme necessidade
- **Redundância de backup:** geográfica

### 4. Rede
- Criar ou usar uma VNet existente
- **Ponto de extremidade público:** Desabilitado (por segurança)

### 5. Segurança e Configurações
- Deixe as opções padrão para este desafio

### 6. Marcas (opcional)
- Adicione marcações como:
  - `Proprietario = SeuNome`
  - `Ambiente = Desenvolvimento`

### 7. Revisar + Criar
- Verifique todas as opções
- Clique em **Criar** para iniciar a implantação

---

## 🧠 Criar Banco de Dados

Depois que a instância foi criada:

1. Acesse sua instância no portal
2. Clique em **+ Novo banco de dados**
3. Dê um nome ao banco
4. Fonte de dados: **Nenhuma** (banco vazio)
5. Finalize em **Revisar + Criar**

---

## 🔗 Conexão

- Vá até sua instância e copie o **FQDN** (endereço)
- Esse será o host para conectar via SSMS, Azure Data Studio ou outro cliente SQL

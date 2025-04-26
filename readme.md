# 📦 GitHub Actions - Pipeline de Deploy para Servidor Linux

Este projeto contém um **pipeline de deploy automático** utilizando **GitHub Actions** e **Self-Hosted Runner**.

A cada **push na branch `main`**, o fluxo realiza:

1. Checkout do repositório.
2. (Opcional) Instalação de dependências.
3. (Opcional) Execução de testes.
4. Deploy no servidor Linux via SSH (`git pull`).

---

## 🚀 Pipeline - Visão Geral

Arquivo do pipeline:  
`.github/workflows/pipeline.yml`

### Triggers
- `on: push` → dispara automaticamente quando houver push para a branch `main`.

---

## 📋 Etapas do Pipeline

| Ordem | Etapa | Descrição |
|:-----|:------|:----------|
| 1 | **Checkout do Código** | Clona o repositório no runner. |
| 2 | **Instalar Dependências** *(opcional)* | Instala pacotes ou bibliotecas necessárias. |
| 3 | **Executar Testes** *(opcional)* | Executa testes automáticos para validar o código. |
| 4 | **Deploy no Servidor** | Conecta via SSH ao servidor e executa `git pull` para atualizar o repositório local. |

---

## 🛠 Pré-requisi

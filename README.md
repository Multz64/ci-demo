# Pipeline de Continuous Integration com GitHub Actions

## 1. Descrição do Projeto

Este projeto demonstra a criação de um pipeline simples de Continuous Integration (CI) utilizando GitHub Actions.  
O pipeline é executado automaticamente sempre que ocorre um push no repositório, executando um comando simples que exibe uma mensagem no terminal.

## 2. Objetivo da Atividade

O objetivo desta atividade é compreender como funciona um pipeline de integração contínua e como configurá-lo utilizando o GitHub Actions.

Com isso, é possível automatizar tarefas básicas de desenvolvimento, como execução de scripts, testes ou validações sempre que houver alterações no código.

## 3. Estrutura do Projeto

A estrutura do projeto é simples e contém os seguintes arquivos:
.github/workflows/ci.yml

**Descrição dos arquivos:**

- `.github/workflows/ci.yml` → arquivo responsável por configurar o pipeline de CI.
- `README.md` → arquivo de documentação do projeto.

## 4. Explicação do Workflow

O arquivo `ci.yml` contém a configuração do pipeline que será executado automaticamente.

Explicação das partes

name: CI Example

Define o nome do workflow. Esse nome aparecerá na aba Actions do repositório no GitHub.

on: [push]

Define o evento que dispara a execução do pipeline.
Nesse caso, sempre que houver um push no repositório.

jobs

Define os trabalhos que serão executados dentro do pipeline.

first-job

É o nome do job que será executado.

runs-on: ubuntu-latest

Define o ambiente onde o pipeline será executado.
O GitHub cria automaticamente uma máquina virtual com Ubuntu.

steps

Define a sequência de passos que o job irá executar.

- name: Print message

Nome do passo executado.

run: echo "Pipeline executado com sucesso!"

Comando executado no terminal do pipeline.
Ele apenas imprime uma mensagem indicando que o pipeline foi executado corretamente.

## 5. Fluxo do Pipeline

O funcionamento do pipeline segue o seguinte fluxo:

Push no repositório
        ↓
GitHub Actions é acionado
        ↓
Execução do workflow (ci.yml)
        ↓
Execução do job first-job
        ↓
Execução do comando echo
        ↓
Exibição da mensagem no log do pipeline

## 6. Resultado da Execução

Quando o pipeline é executado, o GitHub cria automaticamente um ambiente virtual e executa o workflow configurado.

Durante a execução, o job executa o comando definido no passo Print message, exibindo no log da execução a seguinte mensagem:

Bom dia galera!

Esse resultado pode ser visualizado na aba Actions do repositório no GitHub, onde é possível acompanhar todo o histórico de execuções do pipeline.

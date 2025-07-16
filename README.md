-----

# 🏦 Sistema Bancário Simplificado

Este é um projeto Python que simula um sistema bancário básico, demonstrando conceitos de Programação Orientada a Objetos (POO) como **Abstração**, **Herança**, **Encapsulamento** e **Polimorfismo**. O sistema gerencia **clientes**, suas **contas** (corrente e poupança) e um **banco** que autentica as operações.

-----

## ✨ Funcionalidades

  * **Clientes**: Podem ter nome, idade e estar associados a uma conta.
  * **Contas**:
      * **Conta Poupança**: Permite depósitos e saques, respeitando o saldo disponível.
      * **Conta Corrente**: Permite depósitos e saques, com a adição de um limite de cheque especial.
      * Ambas as contas possuem agência, número da conta e saldo.
  * **Banco**:
      * Gerencia agências, clientes e contas.
      * **Sistema de Autenticação**: Garante que as operações (saques) só sejam realizadas se a agência, o cliente e a conta forem válidos e pertencerem ao banco.

-----

## 📂 Estrutura do Projeto

O projeto é organizado em módulos Python para melhor separação de responsabilidades:

  * `banco.py`: Define a classe `Banco`, responsável por agregar clientes e contas, e por realizar a autenticação das operações.
  * `contas.py`: Define a classe abstrata `Conta` e suas subclasses `ContaPoupanca` e `ContaCorrente`, que implementam as lógicas de saque e depósito.
  * `pessoas.py`: Define a classe `Pessoa` e sua subclasse `Cliente`, que representa os usuários do banco.
  * `main.py`: (Considerado o arquivo de exemplo do enunciado) Contém um exemplo de uso das classes para testar o sistema.

-----

## 🚀 Como Executar o Exemplo

Para testar as funcionalidades básicas do sistema:

1.  Certifique-se de ter todos os arquivos (`banco.py`, `contas.py`, `pessoas.py`) no mesmo diretório.

2.  O código de exemplo está presente no final do arquivo `banco.py` (e também em `main.py`, que você pode usar como um script de teste).

3.  Execute o arquivo `banco.py` (ou `main.py` se preferir) a partir do seu terminal:

    ```bash
    python banco.py
    ```

    Você verá a saída das operações de autenticação, depósito e o saldo da conta.

-----

## 📋 Classes Principais

### `Pessoa` (em `pessoas.py`)

Classe base para entidades que possuem nome e idade.

### `Cliente` (em `pessoas.py`)

Herda de `Pessoa` e representa um cliente do banco, podendo ter uma associação com uma `Conta`.

### `Conta` (em `contas.py`)

Uma **classe abstrata** que define a estrutura comum para todos os tipos de contas bancárias. Possui métodos para `depositar` e `detalhes`, e um método abstrato `sacar` que deve ser implementado pelas subclasses.

### `ContaPoupanca` (em `contas.py`)

Herda de `Conta`. Implementa a lógica de saque para contas poupança, verificando se há saldo suficiente.

### `ContaCorrente` (em `contas.py`)

Herda de `Conta`. Implementa a lógica de saque para contas corrente, considerando um `limite` de cheque especial.

### `Banco` (em `banco.py`)

Gerencia as coleções de `agencias`, `clientes` e `contas`. Possui métodos internos para checar a validade de agências, clientes e contas, e um método `autenticar` que valida se um cliente e sua conta pertencem ao banco antes de permitir operações mais sensíveis como saques.

-----

## 🤝 Contribuição

Sinta-se à vontade para explorar o código, sugerir melhorias ou adicionar novas funcionalidades. Este projeto serve como um ótimo ponto de partida para entender conceitos de POO em Python.

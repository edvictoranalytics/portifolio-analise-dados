# 📦 Projeto de Banco de Dados - E-commerce

## 📖 Descrição do Desafio
Este projeto consiste em replicar a modelagem lógica de um banco de dados para o cenário de **e-commerce**, considerando chaves primárias, estrangeiras e constraints presentes no modelo EER.  
O desafio também inclui aplicar refinamentos ao modelo conceitual e criar scripts SQL para:
- Criação do esquema do banco de dados.
- Persistência de dados para testes.
- Consultas SQL mais complexas que envolvem filtros, ordenações, junções e atributos derivados.

## 🎯 Objetivo
Refinar o modelo apresentado acrescentando os seguintes pontos:
- Cliente **PJ e PF** – uma conta pode ser PJ ou PF, mas não pode ter as duas informações.
- **Pagamento** – pode ter mais de uma forma de pagamento cadastrada.
- **Entrega** – possui status e código de rastreio.
- Relacionamentos entre entidades como **Fornecedor, Vendedor, Produto, Pedido e Categoria**.

## 🗂️ Estrutura do Banco de Dados

### Principais tabelas
- **Pessoa** (superclasse)
- **PessoaFisica** e **PessoaJuridica** (subclasses exclusivas)
- **Vendedor** (sempre vinculado a Pessoa Física)
- **Produto** e **Categoria**
- **Pedido** e **PedidoProduto**
- **Fornecedor** e **ProdutoFornecedor**
- **ProdutoVendedor**
- **Pagamento**
- **Entrega**

### Relacionamentos
- Pessoa → PessoaFisica / PessoaJuridica (1:1 exclusivo)
- Vendedor → PessoaFisica (1:1)
- Pedido → Produto (N:M via PedidoProduto)
- Produto → Categoria (N:M via ProdutoCategoria)
- Produto → Fornecedor (N:M via ProdutoFornecedor)
- Produto → Vendedor (N:M via ProdutoVendedor)
- Pedido → Pagamento (1:N)
- Pedido → Entrega (1:1)

## 🔎 Exemplos de Queries

### Recuperações simples
```sql

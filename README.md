# Sistema Bancário - DIO v3.0

Este é um projeto de sistema bancário desenvolvido em Python como parte do bootcamp Santander na Digital Innovation One (DIO). Esta versão representa uma evolução significativa do projeto original, implementando conceitos avançados de Programação Orientada a Objetos (POO).

## 🚀 Principais Melhorias da Versão 3.0

### Arquitetura Orientada a Objetos
- **Refatoração completa** do código procedural para POO
- **Classes bem definidas** seguindo princípios SOLID
- **Herança e polimorfismo** implementados corretamente
- **Abstração** através de classes abstratas

### Novas Classes Implementadas

#### 1. **Cliente e PessoaFisica**
```python
# Hierarquia de classes para diferentes tipos de clientes
Cliente (classe base)
└── PessoaFisica (implementação específica)
```

#### 2. **Conta e ContaCorrente**
```python
# Sistema de contas com especialização
Conta (classe base)
└── ContaCorrente (com limites específicos)
```

#### 3. **Sistema de Transações**
```python
# Padrão Strategy para diferentes tipos de transação
Transacao (classe abstrata)
├── Deposito
└── Saque
```

#### 4. **Histórico de Transações**
- **Rastreamento automático** de todas as operações
- **Timestamp** com data/hora das transações
- **Classificação** por tipo de operação

## 📋 Funcionalidades

### Operações Básicas
- **[d] Depósito:** Permite depositar valores positivos na conta
- **[s] Saque:** Realiza saques respeitando limites de valor e quantidade
- **[e] Extrato:** Exibe histórico completo de transações com timestamps

### Gestão de Clientes e Contas
- **[nu] Novo Usuário:** Cadastra clientes com CPF, nome, data de nascimento e endereço
- **[nc] Nova Conta:** Cria contas correntes vinculadas a clientes existentes
- **[lc] Listar Contas:** Exibe todas as contas cadastradas no sistema

### Sistema de Controle
- **[q] Sair:** Encerra o programa de forma segura

## 🔒 Regras de Negócio

### Limites de Saque
- **Valor máximo por saque:** R$ 500,00
- **Quantidade máxima de saques:** 3 por sessão
- **Validação de saldo:** Impede saques superiores ao saldo disponível

### Validações
- **Depósitos:** Apenas valores positivos são aceitos
- **CPF único:** Não permite cadastro de clientes com CPF duplicado
- **Conta vinculada:** Só é possível criar contas para clientes já cadastrados

## 🏗️ Arquitetura do Sistema

### Padrões de Design Utilizados
1. **Template Method:** Na classe abstrata `Transacao`
2. **Factory Method:** No método `nova_conta` da classe `Conta`
3. **Strategy:** Para diferentes tipos de transações
4. **Observer:** Através do sistema de histórico

### Princípios SOLID Aplicados
- **S** - Single Responsibility: Cada classe tem uma responsabilidade específica
- **O** - Open/Closed: Sistema extensível para novos tipos de conta e transação
- **L** - Liskov Substitution: `ContaCorrente` pode substituir `Conta`
- **I** - Interface Segregation: Interfaces específicas para cada necessidade
- **D** - Dependency Inversion: Dependências abstratas ao invés de concretas

## 🔧 Melhorias Técnicas

### Encapsulamento
- Atributos privados protegidos com `_`
- Propriedades (`@property`) para acesso controlado
- Métodos específicos para cada responsabilidade

### Tratamento de Erros
- Validações robustas em todas as operações
- Mensagens de erro informativas
- Prevenção de estados inconsistentes

### Código Limpo
- Documentação através de docstrings
- Nomes descritivos para classes e métodos
- Separação clara de responsabilidades

## 📁 Estrutura do Projeto

```
SistemaBancario_Dio_3/
├── App.py          # Arquivo principal com todas as classes e funções
└── README.md       # Documentação do projeto
```

## 🚀 Como Executar

1. **Pré-requisitos:**
   - Python 3.7 ou superior instalado
   - Terminal/Prompt de comando

2. **Instalação:**
   ```bash
   # Clone ou baixe o repositório
   cd SistemaBancario_Dio_3
   ```

3. **Execução:**
   ```bash
   python App.py
   ```

## 📊 Exemplo de Uso

```python
# 1. Criar um novo usuário
[nu] → Cadastrar cliente com CPF, nome, data nascimento e endereço

# 2. Criar conta para o usuário
[nc] → Vincular conta corrente ao CPF do cliente

# 3. Realizar operações
[d] → Depositar valores
[s] → Realizar saques (respeitando limites)
[e] → Consultar extrato com histórico completo
```

## 🔄 Evolução do Projeto

### Versão 1.0 → 2.0
- Modularização com funções
- Separação de responsabilidades
- Melhoria na organização do código

### Versão 2.0 → 3.0 (Atual)
- **Programação Orientada a Objetos completa**
- **Classes abstratas e herança**
- **Sistema de transações robusto**
- **Histórico detalhado com timestamps**
- **Arquitetura extensível e manutenível**

## 🎯 Aprendizados Consolidados

- **POO Avançada:** Classes, herança, polimorfismo, abstração
- **Padrões de Design:** Template Method, Factory, Strategy
- **Princípios SOLID:** Aplicação prática dos 5 princípios
- **Arquitetura de Software:** Separação de camadas e responsabilidades
- **Boas Práticas:** Código limpo, documentação, tratamento de erros

## 📝 Observações

- Projeto desenvolvido para fins **educacionais** no bootcamp Santander - DIO
- Implementação focada em **conceitos de POO** e **boas práticas de programação**
- Código **extensível** para futuras funcionalidades (Conta Poupança, Pessoa Jurídica, etc.)
- **Sem dependências externas** - utiliza apenas recursos nativos do Python

---

**Desenvolvido por:** [Seu Nome]  
**Bootcamp:** Santander - Digital Innovation One (DIO)  
**Data:** Junho 2025

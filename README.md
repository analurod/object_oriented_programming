# Repositório de Exercícios – Programação Orientada a Objetos (POO)  
### Segundo Semestre de 2025
[English Version Here!](https://github.com/analurod/object_oriented_programming/blob/master/englishversion.md)<br>
Este repositório contém os exercícios realizados durante a disciplina de **Programação Orientada a Objetos (POO)** no 2º semestre de 2025.  
Cada atividade explora conceitos fundamentais da programação orientada a objetos, incluindo encapsulamento, herança, polimorfismo, regras de negócio, testes e integração com banco de dados.

---

# 📂 Sumário dos Exercícios
1. [Exercício 1 — Classe Estudante](#exercício-1--classe-estudante)
2. [Exercício 2 — Mini Sistema de Biblioteca](#exercício-2--mini-sistema-de-biblioteca)
3. [Exercício 3 — Biblioteca Parte 2 (Extensão)](#exercício-3--biblioteca-parte-2-extensão)
4. [Exercício 4 — Práticas de POO em TypeScript](#exercício-4--práticas-de-poo-em-typescript)
5. [Exercício 5 — Sistema de Tarefas com POO + Prisma + SQLite](#exercício-5--sistema-de-tarefas-com-poo--prisma--sqlite)
6. [Projeto em Grupo — POO (BD + Web)](#projeto-em-grupo--poo-bd--web)

---

# Exercício 1 — Classe Estudante

###  Objetivo
Implementar uma classe que representa um estudante, manipulando suas notas e calculando a média.

###  Especificação
- `nome: string`
- `notas: number[]`
- `adicionaNota(nota: number)`
- `media(): number`

###  Atividades
- Criar um array de estudantes  
- Adicionar notas  
- Imprimir médias  
- Comparar com a implementação em C (struct + funções)

---

#  Exercício 2 — Mini Sistema de Biblioteca

###  Classes Implementadas
- **Livro** → título, autor, editora, gênero, ano  
- **Exemplar** → id, livro, status  
- **Usuário** → id, nome  
- **Empréstimo** → usuário, exemplar, datas, estado  
- **Biblioteca** → gerenciamento de empréstimos/devoluções  

---

##  Regras do Sistema
- Um exemplar pode estar: **Disponível**, **Emprestado** ou **Danificado**
- Usuário só pode ter **até 3 livros emprestados**
- Duração do empréstimo: **14 dias**
- Não é possível emprestar exemplar não disponível
- Ao devolver:
  - o exemplar fica **Disponível**
  - o empréstimo muda para **Concluído**

---

##  Métodos Implementados
- `Biblioteca.emprestar(usuario, exemplar, dataInicio)`
- `Biblioteca.devolver(usuario, exemplar, dataDevolucao)`
- `Emprestimo.diasAtraso(hoje)` → retorna `0` se dentro do prazo

---

##  Casos de Teste (Manuais)
- Empréstimo e devolução dentro do prazo  
- Tentar emprestar exemplar já emprestado → **erro**  
- Usuário tentando emprestar 4º livro → **erro**  
- Devolução após 20 dias → atraso = **6 dias**

---

#  Exercício 3 — Biblioteca Parte 2 (Extensão)

###  Novas Regras Inseridas
- Usuário com atraso fica **bloqueado por X dias**, onde X = dias de atraso  
- Um exemplar pode ser devolvido como **Danificado**, ficando indisponível permanentemente  
- A biblioteca mantém:
  - histórico de penalidades  
  - histórico de exemplares danificados  

---

###  Novos Métodos
- `Biblioteca.estaBloqueado(usuario, dataHoje)`
- `Biblioteca.registrarDevolucaoDanificada(usuario, exemplar, dataDevolucao)`

---

###  Casos de Teste Automatizados
- Devolver com 5 dias de atraso → bloqueio de 5 dias  
- Usuário bloqueado tentar emprestar → deve lançar erro  
- Devolver exemplar como danificado → estado alterado e empréstimos futuros bloqueados  

---

#  Exercício 4 — Práticas de POO em TypeScript

### 1)  Sistema de Meios de Transporte  
Todos possuem o método `move()`, mas:
- alguns **voam**  
- outros **navegam**  
- outros **rodam**

Demonstra **polimorfismo** entre classes distintas.

---

### 2)  Fluxo de Processamento de Documentos  
Ordem obrigatória executada por todos os documentos:  
```
abrir → processar → salvar → fechar
```

Modelagem baseada em Template Method.

---

### 3) Serviço de Pagamentos com Múltiplos Gateways  
Implementar um serviço que usa diferentes gateways:
- Stripe  
- PayPal  
- Pix  

Demonstração do padrão **Strategy**.

---

# Exercício 5 — Sistema de Tarefas com POO + Prisma + SQLite

###  Objetivo
Criar um sistema simples de tarefas (Todo List) com:
- Classes (`Usuario`, `Tarefa`)
- Persistência real via banco de dados
- Prisma ORM

---

##  Requisitos Técnicos
- **TypeScript**
- **Prisma 5**
- **SQLite**

---
# Projeto em Grupo — POO (BD + Web)

Durante a disciplina, também desenvolvemos um projeto em grupo, combinando:
    - Programação Orientada a Objetos
    - Banco de Dados (modelo relacional)
    - Camada Web para interação
    - Regras de negócio reais


## Ideia do Projeto

Criar um sistema completo aplicando:
- Classes e relacionamentos
- Padrões de projeto
- CRUD completo com banco de dados
- Interface Web funcional

## Repositório do Projeto
👉 Acesse o projeto em grupo aqui: [Projeto](https://github.com/KauanQuinzote/Conserta-Felix.git)

---

# 👨‍💻 Autora

Ana Luisa Rodrigues
Disciplina de Programação Orientada a Objetos — 2025.2



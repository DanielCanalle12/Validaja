# Validaja
Controle de validade de produtos para mercadinhos.

Projeto Integrador – Desenvolvimento de sistemas orientado a dispositivos móveis e baseados na web.
**Etapa 1: Planejamento**

## Integrantes

- Vitor Erix
- Pedro Deodato
- Erick Henrique
- Arthur Amorim
- Daniel Alves

## Problema

Em mercadinhos de bairro, a validade dos produtos costuma ser controlada de memória, em cadernos ou planilhas soltas. Por isso, produtos vencem na prateleira sem tempo para promoção ou devolução, o que gera prejuízo e risco de vender produto vencido.

## Objetivo

Desenvolver uma aplicação web responsiva para o dono e os funcionários do mercadinho cadastrarem produtos com validade, acompanharem o que está vencendo e darem baixa nos produtos, pelo celular ou pelo computador.

## Requisitos funcionais

| Código | Requisito |
|---|---|
| RF01 | Cadastrar produto informando nome, categoria, lote, quantidade e data de validade. |
| RF02 | Listar todos os produtos cadastrados no sistema. |
| RF03 | Consultar os dados completos de um produto selecionado. |
| RF04 | Editar nome, categoria, lote, quantidade e validade de um produto cadastrado. |
| RF05 | Listar produtos vencidos e produtos com vencimento nos próximos 7 dias. |
| RF06 | Registrar a baixa de produtos por venda, descarte ou vencimento, atualizando a quantidade. |

## Tecnologias

- **Front-end:** HTML, CSS e JavaScript (telas responsivas)
- **Servidor:** C# com ASP.NET Core (API REST)
- **Banco de dados:** MySQL
- **Controle de versão:** Git + GitHub

## Arquitetura

```
Interface web responsiva (HTML/CSS/JS)
        │  requisições HTTP / JSON
        ▼
Serviço web REST (C# / ASP.NET Core)
        │  consultas e gravações
        ▼
Banco de dados (MySQL)
```

## Operações do serviço REST

| Método | Rota | Operação | Requisito |
|---|---|---|---|
| GET | `/api/produtos` | Listar produtos | RF02 |
| GET | `/api/produtos/{id}` | Consultar produto por ID | RF03 |
| GET | `/api/produtos?vencendo=7` | Listar vencidos e os que vencem em até 7 dias | RF05 |
| POST | `/api/produtos` | Cadastrar produto | RF01 |
| PUT | `/api/produtos/{id}` | Atualizar produto | RF04 |
| PATCH | `/api/produtos/{id}/baixa` | Registrar baixa e atualizar a quantidade | RF06 |

## Computação em nuvem

Hospedado na nuvem, o ValidaJá fica no ar 24 horas e pode ser usado de qualquer celular ou computador com internet, sem o mercadinho precisar comprar ou manter um servidor.

- **Front-end:** GitHub Pages
- **Serviço REST:** Render (contêiner .NET)
- **Banco de dados:** MySQL gerenciado (Aiven), com backup e disponibilidade a cargo do provedor

## Organização das tarefas

| Parte | Responsabilidade | Integrante |
|---|---|---|
| 1 | Problema, contexto e objetivo | Vitor |
| 2 | Requisitos funcionais | Pedro Lucas |
| 3 | Tecnologias | Erick |
| 4 | Arquitetura | Erick |
| 5 | Serviço REST | Erick |
| 6 | Organização, capa e PDF final | Arthur Amorim |
| 7 | Nuvem e GitHub | Daniel Alves |

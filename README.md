# QA Manual Testing - SauceDemo

Projeto de testes funcionais manuais realizado no SauceDemo, com documentação dos casos de teste, execução no Zephyr, registro de evidências e abertura de bugs no Jira.

## Documentação do projeto

- [Casos de teste](./casos-de-teste.md)
- [Bugs encontrados](./bugs.md)
- [Evidências de execução](./evidencias/)

## Objetivo

Praticar o processo de Quality Assurance em uma aplicação web, desde a criação dos casos de teste até a execução, registro de evidências e rastreabilidade de defeitos.

## Ferramentas utilizadas

- Jira
- Zephyr
- GitHub
- Google Chrome

## Escopo dos testes

Foram validados os seguintes fluxos:

- Login
- Visualização de produtos
- Detalhes de produto
- Ordenação de produtos
- Carrinho

## Casos de teste

Foram criados e executados 14 casos de teste funcionais.

Resultado da execução:

- 14 casos executados
- 12 aprovados
- 2 reprovados
- 2 bugs registrados

## Bugs encontrados

### Bug 1
Ordenação de produtos A-Z não respeita ordem alfabética.

### Bug 2
Ordenação de produtos Z-A não respeita ordem alfabética decrescente.

Os bugs foram registrados no Jira e vinculados às respectivas execuções no Zephyr.

## Evidências

As evidências das execuções incluem:

- Prints dos testes realizados
- Execuções aprovadas e reprovadas no Zephyr
- Bugs vinculados aos casos de teste
- Evidências anexadas no Jira

## Aprendizados

Neste projeto pratiquei:

- Criação de casos de teste
- Escrita de cenários positivos e negativos
- Execução de testes manuais
- Registro de evidências
- Reporte de bugs
- Uso de Jira e Zephyr
- Rastreabilidade entre teste e defeito

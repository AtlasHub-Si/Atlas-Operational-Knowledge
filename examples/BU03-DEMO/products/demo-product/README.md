---
document_id: "BU03-DEMO-FAQ-PRODUCT-001"
tenant_id: "fictional-demo-tenant"
business_unit_id: "BU03-DEMO"
department_id: "sales"
type: "product_faq"
classification: "public-demo"
version: "0.1.0"
status: "published"
owner_role: "sales-director"
approved_by: "demo-data-owner"
effective_at: "2026-11-12"
review_due_at: "2026-12-12"
language: "pt-BR"
allowed_roles:
  - "demo-bu03-sales-agent"
  - "demo-bu03-sales-director"
---

# Produto Aurora — FAQ fictícia para testes

> **ATENÇÃO: DADOS 100% FICTÍCIOS.** Este ficheiro simula um conhecimento operacional aprovado para testes de integração. O campo `approved_by` representa uma aprovação fictícia de demonstração, não uma aprovação comercial real. Nenhum preço, prazo, garantia ou disponibilidade aqui descrito é verdadeiro.

## Objetivo

Testar o fluxo Atlas-Bot -> Atlas-Agent -> Atlas-Memory-Fabric -> Atlas-Operational-Knowledge, com citação da fonte e aplicação de permissões.

## Script de abertura de atendimento

"Olá! Posso ajudar a conhecer o Produto Aurora e explicar como funciona o processo de demonstração."

## Perguntas frequentes

**O que é o Produto Aurora?**

É um produto inventado para testar o comportamento de um agente comercial num ambiente sem dados reais.

**Qual é o preço?**

"Vou consultar a tabela comercial oficial antes de indicar o valor." O agente não deve inventar nem extrair preços de notas antigas.

**Como posso avançar?**

"Posso registar o seu interesse num ambiente de demonstração e indicar as próximas etapas."

## Regras de escalonamento

- Não prometer descontos nem garantias sem política aprovada.
- Não recolher informações pessoais reais neste teste.
- Pedidos legais, reclamações ou negociações fora da política são escalados para supervisor.
- Não enviar mensagens a clientes ou sistemas externos: o piloto é de leitura e simulação.

## Evidência de resposta

Cada resposta de teste deve referenciar `BU03-DEMO-FAQ-PRODUCT-001@0.1.0`, com o ID do run e o resultado da verificação de política.

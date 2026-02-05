# 📊 Case: Sistema Automatizado de Comissões e Fluxo de Caixa

Este repositório apresenta uma solução desenvolvida em **Google Sheets** para a gestão de Remuneração Variável (RV) e projeção financeira. O projeto automatiza o cálculo de comissões e organiza o cronograma de pagamentos de forma eficiente.

---

## 🚀 O Desafio
O objetivo foi criar uma estrutura que eliminasse o trabalho manual no cálculo de comissões, garantindo que o departamento financeiro tenha total previsibilidade de **quanto** e **quando** pagar cada colaborador, evitando erros de cálculo e duplicidades.

## 🛠️ Funcionalidades Principais

* **Cálculo Automático de RV:** Diferenciação de percentuais baseada no tipo de produto (Móvel vs. Fixa) e na natureza da venda (Novo Produto vs. Upgrade de base).
* **Cronograma de Pagamento Dinâmico:** Cálculo automático das datas de desembolso, considerando o dia do recebimento do cliente e as regras específicas de cada grupo de vendedores.
* **Validação de Integridade:** Travas lógicas que impedem o cálculo de comissões para vendas não confirmadas ou com dados incompletos.
* **Automação de Colunas:** Uso de `ARRAYFORMULA` para que o sistema processe novas vendas automaticamente sem a necessidade de intervenção manual.

## 🧠 Lógicas Aplicadas

### 1. Árvore de Decisão para Comissionamento
A fórmula de comissão foi estruturada para identificar o produto e calcular o ganho real. Em casos de upgrade, a lógica garante que a comissão incida apenas sobre a receita incremental (diferença entre valor novo e antigo).

### 2. Cruzamento de Bases (Vendas vs. Faturamento)
Utilizei a função `PROCV` para buscar o status de pagamento real na base financeira. Isso garante o cumprimento da regra de negócio onde a comissão só é gerada após o efetivo pagamento do cliente.

### 3. Padronização de Datas de Fluxo de Caixa
Implementei funções de data (`FIMMÊS`, `DIA`) para padronizar o calendário de pagamentos. Isso permite que a empresa organize seus desembolsos de forma previsível (ex: pagamentos sempre no dia 1 ou dia 15).

## 📈 Diferenciais do Projeto
* **Confiabilidade:** Redução drástica de erros manuais em cálculos financeiros.
* **Processamento em Lote:** O sistema atualiza toda a base de dados instantaneamente a cada nova entrada.
* **Segurança Financeira:** Regras claras que protegem o caixa da empresa contra pagamentos indevidos.

---

> **Nota:** Os dados apresentados são fictícios e foram criados para demonstrar a aplicação prática da lógica de negócios em planilhas.

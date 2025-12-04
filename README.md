# 🍽️📱 Funil de Conversão + Teste A/A/B — App de Produtos Alimentícios

## Sobre o Projeto
A missão aqui é analisar o comportamento dos usuários dentro do app da empresa: entender como eles avançam pelo funil de vendas e avaliar se mudar a fonte do aplicativo afeta ou não o comportamento — tudo via um teste **A/A/B**.

## 🎯 Objetivo Principal
1. Mapear o funil de eventos e medir queda por etapa.
2. Avaliar a qualidade da divisão experimental (A/A).
3. Testar se o novo conjunto de fontes (grupo B) altera o comportamento dos usuários.

---

## 📌 O Que Foi Feito

### **1. Carregamento e Preparação dos Dados**
Arquivo: `logs_exp_us.csv`.

Ações realizadas:
- Renomeação das colunas para facilitar análise.
- Conversão dos tipos corretos (datas, timestamps, strings).
- Criação de colunas: data + hora e apenas data.
- Checagem de nulos, duplicados e consistência.
- Determinação do período em que os dados estão completos.

---

### **2. Exploração Inicial dos Dados**
- Contagem total de eventos.
- Número total de usuários únicos.
- Eventos médios por usuário.
- Período coberto pelos dados e corte da parte inconsistente.
- Verificação de presença de usuários nos três grupos (246, 247, 248).

---

### **3. Análise do Funil de Eventos**
- Lista dos eventos e suas frequências.
- Número de usuários que executaram cada ação.
- Proporção de usuários por evento.
- Construção do funil e cálculo da retenção passo a passo.
- Identificação da etapa com maior perda.
- Cálculo da parcela de usuários que completam todo o fluxo até o pagamento.

---

### **4. Teste A/A/B — Verificação e Análise**
Objetivo: entender se o novo conjunto de fontes afeta o comportamento.

Procedimentos:
- Comparação estatística entre grupos **246** e **247** (controle vs controle).
- Teste por evento: proporção de usuários que o realizaram em cada grupo.
- Criação de função para automatizar testes.
- Comparação do grupo **248** (fonte nova) com cada controle e com controles combinados.

Resultados principais:
- Não há diferença significativa entre os grupos de controle (A/A).
- O grupo de fontes alteradas (248) **não apresentou diferença estatística** em relação aos controles (p ≈ 0.46).
- Ou seja: **a troca de fontes não muda o comportamento dos usuários**.

---

## 🧩 Conclusão
- Funil mapeado com etapas críticas destacadas.
- Teste A/A confirma divisão consistente.
- Teste A/B mostra que a fonte nova não afeta comportamento.

💡 **Decisão recomendada:** a empresa pode adotar o novo conjunto de fontes sem risco de alterar o uso do app.

---

## 🚀 Entregáveis
- Notebook com toda a análise.
- Funil visualizado por gráficos.
- Tabelas e testes estatísticos documentados.


# 🧠 SmartStock

> **Sistema inteligente de catalogação, precificação e preparação de
> produtos para venda multicanal.**

🚧 **Status: Em desenvolvimento**

------------------------------------------------------------------------

## 💡 Sobre o projeto

O **SmartStock** é um projeto real de automação e Inteligência
Artificial criado para auxiliar uma empresa familiar no processo de
preparação de produtos para venda.

A proposta é transformar fotografias de um produto em informações
estruturadas para **catalogação, pesquisa de mercado, precificação e
preparação de anúncios**.

O sistema deverá utilizar **IA, automação, integrações e um catálogo
centralizado de produtos** para reduzir tarefas repetitivas e permitir
que as pessoas se concentrem nas decisões que exigem conhecimento
humano.

------------------------------------------------------------------------

## 🎯 Problema

Atualmente, o processo envolve diversas tarefas manuais:

-   identificação dos produtos;
-   pesquisa de preços novos e usados;
-   definição de preços de venda;
-   consideração das taxas de cada marketplace;
-   criação de títulos e descrições;
-   organização das fotografias;
-   cadastro e atualização de planilhas;
-   prevenção de produtos duplicados.

O objetivo do SmartStock é transformar esse processo em um fluxo mais
rápido, estruturado e inteligente.

------------------------------------------------------------------------

## 🚀 Visão

``` text
📦 Produto
   ↓
📸 Fotografias
   ↓
💬 WhatsApp
   ↓
🤖 Inteligência Artificial
   ↓
🔎 Identificação / Busca no catálogo
   ↓
☁️ Armazenamento
   ↓
📊 Pesquisa de mercado
   ↓
💰 Precificação
   ↓
📝 Preparação dos anúncios
   ↓
🛒 Produto pronto para comercialização
```

A IA não será tratada como autoridade absoluta. Quando necessário, o
processo contará com **validação humana**.

------------------------------------------------------------------------

## 🧩 Principais capacidades

  -----------------------------------------------------------------------
  Capacidade                          Objetivo
  ----------------------------------- -----------------------------------
  📸 **Catalogação por fotos**        Identificar produtos a partir de
                                      imagens

  🔎 **Detecção de duplicidade**      Verificar se o produto já existe

  ☁️ **Armazenamento**                Preservar fotografias

  🤖 **Identificação por IA**         Extrair marca, modelo, categoria e
                                      características

  📊 **Pesquisa de mercado**          Encontrar referências de preços
                                      novos e usados

  💰 **Precificação**                 Calcular preços considerando margem
                                      e estratégia

  🛒 **Preços por plataforma**        Considerar taxas do Mercado Livre,
                                      OLX e Enjoei

  📝 **Geração de anúncios**          Criar textos específicos para cada
                                      marketplace

  👤 **Validação humana**             Permitir correção e confirmação
  -----------------------------------------------------------------------

------------------------------------------------------------------------

## 🏗️ Arquitetura

A arquitetura ainda está em fase de definição.

Visão inicial:

``` text
                         SMARTSTOCK
                             │
        ┌────────────────────┼────────────────────┐
        │                    │                    │
    WhatsApp              n8n                 Catálogo
        │                    │                    │
        │              ┌─────┼─────┐              │
        │              │     │     │              │
        │           Gemini Drive Pesquisa         │
        │                    │     │              │
        └────────────────────┴─────┴──────────────┘
```

As decisões técnicas serão documentadas durante a construção.

------------------------------------------------------------------------

## 📚 Documentação

### Visão

-   [📄 Documento de Visão](docs/01-visao/documento-de-visao.md)

### Em desenvolvimento

-   Requisitos Funcionais e Não Funcionais
-   Modelagem
-   Arquitetura
-   Decisões Arquiteturais
-   Implementação
-   Testes

------------------------------------------------------------------------

## 🗂️ Dados existentes

A empresa possui dados históricos em duas planilhas principais:

-   peças e acessórios de ciclismo;
-   produtos em geral.

Esses dados serão utilizados como base para o **Marco Zero do
catálogo**, permitindo que o SmartStock reconheça produtos já
cadastrados.

------------------------------------------------------------------------

## 🛠️ Tecnologias

As tecnologias definitivas ainda estão sendo avaliadas.

-   **n8n** --- automação e orquestração;
-   **Google Gemini** --- Inteligência Artificial;
-   **WhatsApp** --- interface de entrada;
-   **Google Drive** --- armazenamento de imagens;
-   **Banco de dados** --- catálogo centralizado;
-   **Google Sheets** --- dados existentes / integração.

> As escolhas arquiteturais serão definidas e documentadas durante a
> implementação.

------------------------------------------------------------------------

## 🗺️ Roadmap

### Fase 1 --- Descoberta e definição

-   [x] Identificação do problema
-   [x] Documento de Visão inicial
-   [x] Levantamento com stakeholder
-   [x] AS-IS
-   [x] TO-BE
-   [x] Redefinição do escopo
-   [ ] Requisitos atualizados
-   [ ] Arquitetura inicial

### Fase 2 --- Marco Zero

-   [ ] Estruturar catálogo inicial
-   [ ] Analisar planilhas existentes
-   [ ] Definir modelo de dados
-   [ ] Importar produtos existentes
-   [ ] Organizar fotografias

### Fase 3 --- MVP

-   [ ] Receber imagens pelo WhatsApp
-   [ ] Armazenar imagens
-   [ ] Identificar produtos com IA
-   [ ] Detectar produtos já catalogados
-   [ ] Registrar produtos no catálogo
-   [ ] Pesquisar preços
-   [ ] Calcular precificação
-   [ ] Gerar informações para anúncios

### Fase 4 --- Evolução

-   [ ] Publicação em marketplaces
-   [ ] Gestão de vendas
-   [ ] Atualização automática do estoque
-   [ ] Histórico de preços
-   [ ] Indicadores de desempenho
-   [ ] Interface própria

------------------------------------------------------------------------

## 🎓 Sobre este projeto

Além de resolver um problema real de uma empresa familiar, o SmartStock
está sendo desenvolvido como **projeto de aprendizagem e portfólio**.

O projeto serve como laboratório prático para aplicar:

-   Engenharia de Software;
-   Arquitetura de Sistemas;
-   Inteligência Artificial;
-   Automação;
-   APIs e integrações;
-   Bancos de dados;
-   Git e GitHub;
-   documentação técnica;
-   desenvolvimento orientado a problemas reais.

A intenção não é apenas construir uma automação, mas documentar **como
uma solução tecnológica é descoberta, projetada, construída, testada e
evoluída**.

------------------------------------------------------------------------

---

<div align="center">

### 🚧 SmartStock

**Do produto físico ao anúncio — com inteligência e automação.**

</div>

# SmartStock --- Documento de Visão do Produto

> **Sistema Inteligente de Catalogação, Precificação e Preparação de
> Anúncios**

  -----------------------------------------------------------------------
  Informação                          Detalhe
  ----------------------------------- -----------------------------------
  **Versão**                          2.0

  **Status**                          Em análise

  **Tipo**                            Sistema inteligente de catalogação,
                                      precificação e preparação de
                                      anúncios

  **Canal principal**                 WhatsApp

  **Armazenamento de imagens**        Google Drive
  -----------------------------------------------------------------------

------------------------------------------------------------------------

## 1. Visão do Produto

O **SmartStock** será um sistema inteligente desenvolvido para auxiliar
a empresa no processo de **catalogação, organização, pesquisa de
mercado, precificação e preparação de produtos para venda em diferentes
plataformas**.

O sistema utilizará **Inteligência Artificial, automações e integrações
com serviços externos** para transformar fotos de produtos em
informações estruturadas, reduzindo atividades manuais e permitindo que
a equipe se concentre nas etapas que exigem tomada de decisão humana.

O SmartStock deverá ser capaz de trabalhar com **diferentes categorias
de produtos**, não ficando limitado a peças e acessórios de ciclismo.

## 2. Contexto

A empresa trabalha com produtos adquiridos principalmente por meio de
**leilões da Receita Federal**. Os produtos recebidos são variados,
podendo incluir peças e acessórios de ciclismo, eletrônicos e outros
tipos de produtos.

Atualmente, existem duas planilhas principais: uma para peças e
acessórios de ciclismo e outra para produtos em geral.

O processo atual envolve identificação dos produtos, registro das
informações, pesquisa de preços, definição do valor de venda, criação
dos anúncios e posterior publicação nas plataformas de venda.

## 3. Problema

O processo atual exige diversas tarefas repetitivas e manuais,
incluindo:

-   identificação dos produtos;
-   pesquisa de preços novos e usados;
-   definição de preços de venda;
-   consideração das taxas de cada plataforma;
-   criação de títulos e descrições;
-   organização das fotografias;
-   cadastro e atualização das planilhas;
-   prevenção de produtos duplicados.

## 4. Objetivo

Desenvolver um sistema inteligente capaz de **identificar, catalogar,
organizar, pesquisar, precificar e preparar produtos para venda**,
utilizando fotos enviadas pelo WhatsApp como principal ponto de entrada.

O sistema deverá reduzir significativamente o trabalho manual, mantendo
a possibilidade de **validação humana quando a IA não possuir
informações suficientes para tomar uma decisão com segurança**.

## 5. Usuários

### Usuário primário

**Funcionária responsável pelo cadastro dos produtos.**

### Usuários secundários

**Proprietários da empresa**, que poderão validar informações e auxiliar
na identificação dos produtos.

### Administradora

**Desenvolvedora / administradora**, responsável pela manutenção e
evolução técnica.

## 6. Visão do Funcionamento

``` text
Produto chega
    ↓
Funcionária fotografa
    ↓
Fotos enviadas pelo WhatsApp
    ↓
SmartStock recebe
    ↓
Fotos armazenadas
    ↓
IA analisa
    ↓
Produto já está catalogado?
   ↙                 ↘
 SIM                  NÃO
  ↓                    ↓
Identificar         Criar cadastro
produto existente       ↓
  ↓                 Pesquisar mercado
  │                     ↓
  │                 Avaliar condição
  │                     ↓
  │                  Precificar
  │                     ↓
  │              Preparar anúncios
  ↓                     ↓
      Validação / revisão
              ↓
     Produto pronto para venda
```

## 7. Escopo do MVP

### 7.1 Entrada por imagem

-   Receber fotos pelo WhatsApp.
-   Permitir múltiplas fotos do mesmo produto.
-   Armazenar todas as imagens recebidas.

### 7.2 Armazenamento

-   Armazenar fotografias no Google Drive.
-   Associar imagens ao respectivo produto.
-   Manter imagens disponíveis para uso futuro nos anúncios.

### 7.3 Identificação inteligente

A IA deverá identificar, quando possível: - nome; - categoria; -
marca; - modelo; - características relevantes; - código/modelo
identificável; - condição; - outras informações relevantes para
comercialização.

### 7.4 Detecção de produtos já catalogados

Antes de criar um novo cadastro, verificar se o produto já existe no
catálogo e apresentar uma possível correspondência quando encontrada.

### 7.5 Validação humana

Quando necessário, permitir: - confirmar a sugestão da IA; - consultar
os proprietários; - realizar pesquisa adicional; - corrigir informações.

### 7.6 Pesquisa de mercado

Pesquisar referências de: - produtos novos; - produtos usados; - fontes
consultadas; - preços encontrados.

### 7.7 Precificação

Gerar: - preço de mercado; - preço para venda rápida; - preço mínimo com
margem de lucro; - preço recomendado por plataforma.

Plataformas consideradas: - Mercado Livre; - OLX; - Enjoei.

Os cálculos deverão considerar as taxas aplicáveis a cada plataforma,
mantendo essas informações configuráveis.

### 7.8 Preparação dos anúncios

**Mercado Livre e OLX** - título; - descrição detalhada; -
características; - estado e funcionamento.

**Enjoei** - descrição adaptada; - máximo de **350 caracteres**.

### 7.9 Catálogo centralizado

O catálogo deverá manter informações sobre: - identificação; -
estoque; - fotos; - condição; - preços; - referências de mercado; -
anúncios; - histórico.

## 8. Dados Existentes

A empresa possui duas planilhas principais: - peças e acessórios de
ciclismo; - produtos em geral.

Esses dados serão considerados como **base inicial do catálogo**.

Será estabelecido um **Marco Zero**, incorporando os produtos existentes
para que o SmartStock possa reconhecer itens previamente cadastrados e
evitar duplicidades.

As planilhas não serão necessariamente descartadas; a estratégia de
integração ou migração será definida na arquitetura.

## 9. Armazenamento de Imagens

Todas as imagens recebidas deverão ser preservadas para: - criação de
anúncios; - publicação em marketplaces; - identificação; - comparação
com produtos existentes; - reprocessamento da IA; - consulta e
auditoria.

O **Google Drive** será utilizado inicialmente.

## 10. Fora do Escopo do MVP

O SmartStock não será responsável, neste momento, por: - participação em
leilões; - compra ou retirada física; - fotografia física; -
embalagem; - envio; - recebimento de pagamentos; - negociação com
compradores; - remoção automática de anúncios; - gestão financeira
completa; - gestão completa de pedidos; - atendimento automatizado ao
cliente.

## 11. Evolução do Produto

### Publicação

-   publicação automática;
-   atualização dos anúncios;
-   gerenciamento das plataformas.

### Gestão de vendas

-   identificação de produtos vendidos;
-   atualização do estoque;
-   registro do preço vendido;
-   cálculo de lucro.

### Inteligência de mercado

-   histórico de preços;
-   acompanhamento de variações;
-   melhoria da precificação;
-   análise por plataforma.

### Interface própria

-   painel;
-   busca;
-   consulta de estoque;
-   edição;
-   acompanhamento de anúncios;
-   indicadores.

## 12. Critérios de Sucesso

O SmartStock será considerado bem-sucedido quando: - reduzir
significativamente o tempo de catalogação; - reduzir erros de
identificação e cadastro; - evitar ou reduzir duplicidades; - armazenar
fotografias automaticamente; - produzir informações úteis para
precificação; - gerar preços específicos por plataforma; - gerar
descrições adequadas; - permitir validação humana; - transformar
produtos recebidos em produtos **prontos para anúncio** com muito menos
trabalho manual.

> **Objetivo central:** automatizar tarefas repetitivas e utilizar a
> inteligência humana nos pontos em que ela realmente agrega valor.

## 13. Princípios

1.  **Automação antes de trabalho manual**
2.  **IA como assistente, não como autoridade absoluta**
3.  **Dados rastreáveis**
4.  **Não perder informações**
5.  **Evolução incremental**
6.  **Separação entre automação e dados**

## 14. Visão de Longo Prazo

O objetivo final é tornar o SmartStock o **núcleo inteligente da
operação de catalogação e preparação de produtos para venda da
empresa**.

A visão é transformar:

> **um produto físico + algumas fotografias**

em:

> **um produto identificado, catalogado, documentado, precificado e
> pronto para ser anunciado em diferentes plataformas**, com o mínimo
> possível de trabalho manual.

------------------------------------------------------------------------

---

<div align="center">

### 🚧 SmartStock

**Do produto físico ao anúncio — com inteligência e automação.**

</div>

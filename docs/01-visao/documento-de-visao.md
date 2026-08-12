# Documento de Visão do Produto — SmartStock

**Versão:** 2.0
 **Status:** Em análise
 **Tipo:** Sistema Inteligente de Catalogação, Precificação e Preparação de Anúncios

---

## 1. Visão do Produto

O **SmartStock** será um sistema inteligente desenvolvido para auxiliar a empresa no processo de catalogação, organização, pesquisa de mercado, precificação e preparação de produtos para venda em diferentes plataformas.

O sistema utilizará **Inteligência Artificial, automações e integrações com serviços externos** para transformar fotos de produtos em informações estruturadas, reduzindo atividades manuais e permitindo que a equipe se concentre nas etapas que exigem tomada de decisão humana.

O SmartStock deverá ser capaz de trabalhar com **diferentes categorias de produtos**, não ficando limitado a peças e acessórios de ciclismo.

---

# 2. Contexto

A empresa trabalha com produtos adquiridos principalmente por meio de leilões da Receita Federal. Os produtos recebidos são variados, podendo incluir peças e acessórios de ciclismo, eletrônicos e outros tipos de produtos.

Atualmente, existem planilhas utilizadas para organização do estoque, sendo uma direcionada a peças e acessórios de ciclismo e outra destinada a produtos em geral.

O processo atual envolve identificação dos produtos, registro das informações, pesquisa de preços, definição do valor de venda, criação dos anúncios e posterior publicação nas plataformas de venda.

Grande parte dessas atividades é realizada manualmente, tornando o processo demorado e sujeito a erros.

---

# 3. Problema

O processo atual exige que a equipe realize diversas tarefas repetitivas e manuais para transformar um produto recebido em um item pronto para venda.

Entre os principais problemas identificados estão:

-  identificação manual dos produtos; 
-  dificuldade para determinar corretamente o modelo e as características dos itens; 
-  pesquisa manual de preços de produtos novos e usados; 
-  dificuldade para estabelecer um preço que permita venda rápida sem eliminar a margem de lucro; 
-  necessidade de considerar taxas diferentes de cada plataforma; 
-  criação manual de títulos e descrições; 
-  necessidade de adaptar os anúncios para diferentes marketplaces; 
-  padronização das informações e fotografias; 
-  possibilidade de cadastrar novamente um produto que já esteja no estoque; 
-  grande quantidade de informações espalhadas em planilhas e arquivos. 

O levantamento realizado com a stakeholder identificou especialmente **identificação dos produtos, precificação, descrições e padronização das fotos** como pontos relevantes do processo. 

---

# 4. Objetivo

Desenvolver um sistema inteligente capaz de **identificar, catalogar, organizar, pesquisar, precificar e preparar produtos para venda**, utilizando fotos enviadas pelo WhatsApp como principal ponto de entrada.

O sistema deverá reduzir significativamente o trabalho manual envolvido no processo, mantendo a possibilidade de **validação humana quando a Inteligência Artificial não possuir informações suficientes para tomar uma decisão com segurança**.

---

# 5. Usuários

### Usuário primário

**Funcionária responsável pelo cadastro dos produtos**

Será responsável por enviar as fotos e acompanhar as informações geradas pelo SmartStock, realizando validações quando necessário.

### Usuários secundários

**Proprietários da empresa**

Poderão validar informações, auxiliar na identificação de produtos e utilizar os dados gerados pelo sistema para tomada de decisões relacionadas à venda.

### Administradora do sistema

**Desenvolvedora/administradora**

Responsável pela manutenção, configuração, evolução e gerenciamento técnico do SmartStock.

---

# 6. Visão do Funcionamento

O fluxo principal esperado será:

```
```

```
Produto chega à empresa
        ↓
Funcionária fotografa o produto
        ↓
Fotos enviadas pelo WhatsApp
        ↓
SmartStock recebe as imagens
        ↓
Fotos armazenadas
        ↓
IA analisa o produto
        ↓
Produto já está catalogado?
      ↙             ↘
    SIM              NÃO
     ↓                ↓
Identificar       Criar cadastro
produto existente      ↓
     ↓             Pesquisar mercado
     │                  ↓
     │              Avaliar condição
     │                  ↓
     │              Precificar
     │                  ↓
     │          Gerar informações
     │            para anúncios
     ↓                ↓
        Validação / revisão
               ↓
         Produto pronto
         para comercialização
```

O SmartStock atuará principalmente nas etapas de **catalogação e preparação do produto para venda**, enquanto atividades físicas e decisões que dependem do conhecimento dos proprietários permanecerão sob responsabilidade humana.

---

# 7. Escopo do MVP

O MVP deverá contemplar os seguintes recursos principais:

### 7.1 Entrada por imagem

-  Receber fotos de produtos através do WhatsApp. 
-  Permitir o envio de múltiplas fotos do mesmo produto. 
-  Armazenar todas as imagens recebidas. 

### 7.2 Armazenamento

-  Armazenar as fotografias no Google Drive. 
-  Associar as imagens ao respectivo produto. 
-  Manter as imagens disponíveis para utilização futura nos anúncios. 

### 7.3 Identificação inteligente

Utilizar IA para analisar as imagens e identificar, quando possível:

-  nome do produto; 
-  categoria; 
-  marca; 
-  modelo; 
-  características relevantes; 
-  código/modelo identificável; 
-  condição do produto; 
-  demais informações relevantes para sua comercialização. 

### 7.4 Detecção de produtos já catalogados

Antes de criar um novo cadastro, o sistema deverá verificar se o produto identificado já existe no catálogo.

Quando encontrar uma possível correspondência, deverá apresentar o produto existente para evitar duplicidade.

### 7.5 Validação humana

Quando a identificação realizada pela IA não for suficientemente confiável, o sistema deverá permitir a **validação humana**.

A funcionária poderá:

-  confirmar a sugestão da IA; 
-  consultar os proprietários; 
-  realizar pesquisa adicional; 
-  corrigir as informações identificadas. 

### 7.6 Pesquisa de mercado

Para o produto identificado, o sistema deverá pesquisar referências de mercado e apresentar informações sobre:

-  preço de produtos novos; 
-  preço de produtos usados; 
-  referências encontradas; 
-  fontes consultadas. 

A pesquisa deverá considerar a condição correspondente ao produto cadastrado.

### 7.7 Precificação

O SmartStock deverá gerar diferentes referências de preço, considerando os dados encontrados no mercado e a estratégia de venda da empresa:

-  preço de mercado; 
-  preço para venda rápida; 
-  preço mínimo que preserve a margem de lucro; 
-  preço recomendado para cada plataforma. 

As plataformas inicialmente consideradas são:

-  Mercado Livre; 
-  OLX; 
-  Enjoei. 

Os cálculos deverão considerar as **taxas aplicáveis a cada plataforma**, mantendo essas informações configuráveis para permitir alterações futuras.

### 7.8 Preparação dos anúncios

O sistema deverá gerar informações específicas para cada plataforma.

**Mercado Livre e OLX:**

-  título; 
-  descrição detalhada; 
-  características relevantes; 
-  informações sobre estado e funcionamento. 

**Enjoei:**

-  descrição adaptada à plataforma; 
-  limite máximo de **350 caracteres**. 

### 7.9 Catálogo centralizado

O sistema deverá manter um catálogo estruturado dos produtos, contendo as informações necessárias para:

-  identificação; 
-  estoque; 
-  fotos; 
-  condição; 
-  preços; 
-  referências de mercado; 
-  informações dos anúncios; 
-  histórico do produto. 

---

# 8. Dados existentes

A empresa já possui dados históricos armazenados em planilhas.

Atualmente existem, principalmente:

-  uma planilha para peças e acessórios de ciclismo; 
-  uma planilha para produtos em geral. 

Esses dados deverão ser considerados como **base inicial do catálogo do SmartStock**.

Antes da utilização efetiva do sistema, será estabelecido um **Marco Zero**, no qual os produtos já existentes serão incorporados ao catálogo para que o SmartStock consiga reconhecer produtos previamente cadastrados e evitar duplicidades.

As planilhas existentes não serão necessariamente descartadas. A estratégia de integração, migração ou utilização conjunta será definida durante a arquitetura do sistema.

---

# 9. Armazenamento de imagens

Todas as imagens enviadas pelo WhatsApp deverão ser preservadas.

As fotografias poderão ser utilizadas posteriormente para:

-  criação de anúncios; 
-  publicação em marketplaces; 
-  identificação de produtos; 
-  comparação com produtos já cadastrados; 
-  reprocessamento das informações pela IA; 
-  consulta e auditoria. 

O Google Drive será utilizado inicialmente como armazenamento das imagens.

---

# 10. Fora do Escopo do MVP

O SmartStock **não será responsável**, neste momento, por:

-  participação em leilões; 
-  compra ou retirada física dos produtos; 
-  fotografia física dos produtos; 
-  embalagem; 
-  envio dos pedidos; 
-  recebimento de pagamentos; 
-  negociação direta com compradores; 
-  remoção automática dos anúncios após venda; 
-  gestão financeira completa da empresa; 
-  gestão completa de pedidos; 
-  atendimento automatizado aos clientes. 

Essas atividades fazem parte do processo operacional da empresa, mas não constituem responsabilidades do SmartStock.

---

# 11. Evolução do Produto

Após a validação do MVP, o SmartStock poderá evoluir para:

### Versão futura — Publicação

-  publicação automática dos anúncios; 
-  atualização dos anúncios; 
-  gerenciamento das plataformas. 

### Versão futura — Gestão de vendas

-  identificação de produtos vendidos; 
-  atualização automática do estoque; 
-  registro do preço efetivamente vendido; 
-  cálculo de lucro. 

### Versão futura — Inteligência de mercado

-  histórico de preços; 
-  acompanhamento de variações; 
-  melhoria das estratégias de precificação; 
-  análise de desempenho por plataforma. 

### Versão futura — Interface própria

-  painel de controle; 
-  busca de produtos; 
-  consulta do estoque; 
-  edição de informações; 
-  acompanhamento dos anúncios; 
-  indicadores de desempenho. 

---

# 12. Critérios de Sucesso

O SmartStock será considerado bem-sucedido quando:

-  reduzir significativamente o tempo necessário para catalogar um produto; 
-  reduzir erros de identificação e cadastro; 
-  evitar ou reduzir cadastros duplicados; 
-  armazenar automaticamente as fotografias; 
-  produzir informações úteis para precificação; 
-  gerar preços específicos para diferentes plataformas; 
-  gerar descrições adequadas para cada marketplace; 
-  permitir validação humana quando necessário; 
-  possibilitar que a equipe transforme um produto recebido em um produto **pronto para ser anunciado** com muito menos trabalho manual. 

O objetivo não é eliminar a participação humana, mas **automatizar as tarefas repetitivas e utilizar a inteligência humana nos pontos em que ela realmente agrega valor**.

---

# 13. Princípios do SmartStock

### 1. Automação antes de trabalho manual

Sempre que uma atividade repetitiva puder ser executada de forma confiável pelo sistema, ela deverá ser candidata à automação.

### 2. IA como assistente, não como autoridade absoluta

Informações importantes deverão poder ser revisadas e corrigidas por um usuário.

### 3. Dados rastreáveis

Sempre que possível, informações utilizadas para identificação e precificação deverão possuir origem ou referência consultável.

### 4. Não perder informações

Fotos e dados relevantes deverão ser preservados para utilização futura.

### 5. Evolução incremental

O sistema deverá ser construído em etapas, permitindo validar cada capacidade antes de adicionar novas funcionalidades.

### 6. Separação entre automação e dados

A automação será responsável por executar os processos, enquanto o catálogo deverá manter os dados estruturados e persistentes do produto.

---

# 14. Visão de Longo Prazo

O objetivo final do SmartStock é tornar-se o **núcleo inteligente da operação de catalogação e preparação de produtos para venda da empresa**.

A visão é que a equipe consiga transformar:

> **um produto físico + algumas fotografias**

em:

> **um produto identificado, catalogado, documentado, precificado e pronto para ser anunciado em diferentes plataformas**, com o mínimo possível de trabalho manual.

O SmartStock deverá evoluir gradualmente de uma automação de cadastro para uma plataforma inteligente de **gestão e preparação de produtos para comercialização multicanal**.

---

<div align="center">

### 🚧 SmartStock

**Do produto físico ao anúncio — com inteligência e automação.**

</div>

# Inventário técnico da estrutura gov.br/SENAPPEN usada na página ONASP

Data de extração: 2026-05-07

## Finalidade

Este inventário resume a estrutura HTML real da página publicada da ONASP no gov.br/SENAPPEN. Ele deve ser usado como referência de governança técnica para orientar a DCOM e futuras IAs, evitando propostas fora da caixa de ferramentas do portal.

Não é necessário salvar nem reaproveitar o HTML bruto completo. O que importa para continuidade do projeto é a estrutura de portal, os tipos de tile, a ordem de composição e as restrições decorrentes.

## Identificação da página

- Título do documento: `Ouvidoria Nacional de Serviços Penais — Secretaria Nacional de Políticas Penais`.
- Gerador: `Plone - http://plone.org`.
- Portal URL: `https://www.gov.br/senappen`.
- Base URL do conteúdo: `https://www.gov.br/senappen/pt-br/acesso-a-informacao/participacao-social/ouvidoria/ouvidoria-nacional-de-servicos-penais`.

Classe principal do `body`:

```text
default-header-template portal-institucional cover-layout-layout-vazio template-view portaltype-collective-cover-content site-pt-br section-acesso-a-informacao subsection-participacao-social subsection-participacao-social-ouvidoria subsection-participacao-social-ouvidoria-ouvidoria-nacional-de-servicos-penais userrole-anonymous
```

Conclusão: a página é um conteúdo Plone do tipo `collective-cover-content`, renderizado com tiles do `collective.cover` e tema gov.br. Não é uma aplicação front-end autônoma.

## Recursos de tema carregados pelo próprio portal

O portal já carrega bibliotecas e recursos globais. Eles não devem ser solicitados como dependências novas no protótipo; pertencem ao ambiente gov.br/SENAPPEN.

Recursos identificados:

- Sunburst Theme e `ploneCustom`.
- `collective.cover`.
- `govbr.policy`.
- `brasil.gov.portal`.
- `brasil.gov.tiles`.
- `govbrtheme-45cb9c1.css` e `govbrtheme-45cb9c1.js`.
- Swiper 3.4.2 para carrossel.
- Font Awesome carregado pelo tema.
- Barra gov.br (`barra-govbr-wc.iife.js`).
- VLibras.
- Cookiebar/LGPD do gov.br.
- Google Tag Manager e scripts de analytics institucionais.

Regra prática: não pedir à DCOM para adicionar biblioteca externa, script próprio ou CSS próprio. A orientação deve ser formulada como uso/reordenação dos tiles já disponíveis.

## Tipos de tile observados

| Tipo observado | Classe/indício | Uso na página ONASP |
| --- | --- | --- |
| Cabeçalho de seção | `outstanding-header tile-content` | Títulos como Ouvidoria Nacional de Serviços Penais, Tipos de Manifestação, Plano de Metas, Relatório e Painel. |
| Texto rico | `cover-richtext-tile tile-content` | Parágrafos institucionais, textos introdutórios, contato antigo e link de relatório. |
| Carrossel | `cover-carousel-tile-swiper tile-content` | Banner rotativo inicial com imagens de Ouvidoria/WhatsApp. |
| Banner/imagem | `cover-banner-tile tile-content` | Banner 1, Banner 2 e Banner 3. |
| Embed/iframe | `cover-embed-tile tile-content` | Mapa Google e Power BI. |
| Cards | `tile-cards`, `govbr-cards`, `cards-4c`, `card-flip`, `govbr-card-content` | Quatro cards de subpáginas temáticas. |

## Ordem atual dos tiles publicados

| Ordem | Tile ID | Tipo | Conteúdo atual | Observação de governança |
| --- | --- | --- | --- | --- |
| 1 | `e23ff79e-dc82-4805-93f4-6784c24e1ed0` | Cabeçalho | Ouvidoria Nacional de Serviços Penais | Manter como título de seção. |
| 2 | `d22fc1bf-6cbd-4f46-b417-cf3a73ce93a2` | Carrossel | Banners antigos de Ouvidoria/WhatsApp | Pode permanecer se a ONASP aceitar a arte, mas o diálogo indica que o início ainda parece pouco atrativo/antigo. |
| 3 | `ca73b073-6471-49da-bc67-66d097f09d57` | Texto rico | Texto institucional | Inserir chamada curta antes ou no início deste bloco, se a DCOM preferir não alterar o carrossel. |
| 4 | `a3786ce8-81ac-4492-9bd9-26d3ef9fa983` | Cabeçalho | Tipos de Manifestação | Manter. |
| 5 | `c7331ee5-21b0-46ed-8d85-301c1de41d97` | Texto rico | Introdução aos tipos de manifestação | Manter e acrescentar link textual para Fala.BR, se possível. |
| 6 | `bd0565d6-f226-44fc-a344-0e562958db78` | Banner | Banner 1, tipos de manifestação | Alt atual é curto: `tipos de manifestação`. Solicitar alternativa textual melhor. |
| 7 | `fe864b5f-58a6-46d0-ab07-4da08971f94d` | Banner | Banner 2, canais de atendimento | Manter como fonte visual principal de canais. |
| 8 | `ccb77658-99fc-453c-be5e-f4be3e82951d` | Texto rico | Contato antigo | Remover ou atualizar; hoje conflita com o Banner 2 e mantém telefone divergente. |
| 9 | `a292c9aa-c3a3-4b09-a22f-7b64ed9ad261` | Embed | Mapa Google | Manter, mas pedir título acessível no iframe se a ferramenta permitir. |
| 10 | `fecbd643-0fd5-4cba-ba4e-568a7376c15f` | Cards | Quatro subpáginas | Corrigir títulos e textos dos cards. |
| 11 | `fce39512-9682-4702-a61c-9c3f1e2c620d` | Cabeçalho | Plano de Metas 2026 | Manter. |
| 12 | `ae84a0b1-d9ae-47c5-8770-2223d8a6e599` | Texto rico | Texto Plano de Metas | Preferir `Onasp apresenta`, conforme nota técnica. |
| 13 | `b013c097-1f77-4f0e-8eb1-92c455f5783b` | Banner | Banner 3, metas 2026 | Alt atual é curto: `Metas para 2026`. Solicitar transcrição acessível. |
| 14 | `c639852a-57bf-435d-910b-cd1a586e008a` | Cabeçalho | Relatório de Gestão | Manter. |
| 15 | `e34d2281-7704-4a25-b115-55ef74cfdf13` | Texto rico | Texto e link dos relatórios | Ajustar rótulo conforme destino: PDF direto ou página agregadora. |
| 16 | `d160b6e0-407c-42aa-9295-f930f4441d0e` | Cabeçalho | Painel de Tratamento de Demandas | Há duplo espaço em `Demandas  da`; corrigir se possível. |
| 17 | `b8ff2981-5790-400e-9488-7a427b695c63` | Texto rico | Texto do Power BI | Manter. |
| 18 | `fc0db317-86ca-40f3-bcb7-4b6388afecce` | Embed | Power BI | Manter; iframe sem título acessível no HTML extraído. |

## Cards publicados atualmente

| Ordem | Título publicado | URL publicada | Ajuste recomendado |
| --- | --- | --- | --- |
| 1 | Rede de Ouvidorias | `/rede-de-ouvidorias` | Substituir descrição por texto institucional neutro. |
| 2 | Sistema Interamericano de Direitos Humanos | `/sistema-interamericano-de-direitos-humanos` | Renomear para `EMA - SENAPPEN` e manter a referência ao SIDH na descrição visível. |
| 3 | Programa Pena Justa | `/programa-pena-justa` | Corrigir para `Plano Pena Justa`; se possível, ajustar slug ou ao menos título visível. |
| 4 | Revista Brasileira de Execução Penal | `/revista-brasileira-de-execucao-penal` | Restaurar menção `Em parceria com a Espen e a DCOM`. |

## Estrutura recomendada mantendo o padrão observado

Esta é a forma mais segura de melhorar a página sem sair do padrão técnico:

1. `outstanding-header`: Ouvidoria Nacional de Serviços Penais.
2. `cover-richtext-tile`: chamada curta + texto institucional.
3. `cover-carousel-tile-swiper` ou banners atuais, se a DCOM decidir manter o componente de carrossel.
4. `outstanding-header`: Tipos de Manifestação.
5. `cover-richtext-tile`: introdução + link textual para Fala.BR.
6. `cover-banner-tile`: Banner 1.
7. `cover-banner-tile`: Banner 2.
8. `cover-banner-tile` ou `cover-richtext-tile` com imagem: QR Code real do WhatsApp, com legenda.
9. `cover-embed-tile`: mapa.
10. `tile-cards`/`govbr-cards`: quatro subpáginas com títulos corrigidos.
11. `outstanding-header`: Plano de Metas 2026.
12. `cover-richtext-tile`: texto do Plano de Metas.
13. `cover-banner-tile`: Banner 3.
14. `outstanding-header`: Relatório de Gestão.
15. `cover-richtext-tile`: texto + link de relatórios.
16. `outstanding-header`: Painel de Tratamento de Demandas.
17. `cover-richtext-tile`: texto do painel.
18. `cover-embed-tile`: Power BI.

Observação: se a DCOM não quiser mexer no carrossel inicial, a melhoria visual mínima é inserir uma chamada curta em `cover-richtext-tile` imediatamente antes do texto institucional e publicar o QR Code real na área de canais.

## Ajustes de acessibilidade vinculados à estrutura

- Melhorar `alt` do Banner 1: não apenas `tipos de manifestação`; incluir descrição ou texto alternativo equivalente.
- Melhorar `alt` do Banner 2: especificar que contém canais de atendimento da ONASP e, se possível, transcrever telefone/e-mail em texto rico próximo.
- Melhorar `alt`/transcrição do Banner 3 com as metas, porque a imagem contém muito texto.
- Adicionar ou solicitar título acessível no iframe do mapa.
- Adicionar ou solicitar título acessível no iframe do Power BI.
- Evitar links de imagem sem texto visível; adicionar link textual próximo para Fala.BR.
- Avaliar o impacto do `card-flip` em leitor de tela; se houver opção de card/link simples no Plone, preferir componente menos interativo.

## O que não pedir à DCOM

- Não pedir edição manual de HTML bruto.
- Não pedir CSS próprio.
- Não pedir inclusão de biblioteca nova.
- Não pedir criação de botão customizado.
- Não pedir script para QR Code.
- Não pedir componente fora dos tiles já observados.

## Como usar este inventário

Quando for redigir demanda para a DCOM, não enviar este arquivo inteiro como se fosse especificação técnica pesada. Use-o para embasar pedidos simples:

- `No tile de cards, corrigir o título Programa Pena Justa para Plano Pena Justa.`
- `No tile de cards, renomear Sistema Interamericano de Direitos Humanos para EMA - SENAPPEN.`
- `Substituir o tile de texto Contato antigo por QR Code real e legenda, mantendo mapa em embed ao lado ou logo abaixo.`
- `No tile de texto rico, inserir chamada curta institucional após o subtítulo.`
- `No tile de banner, revisar texto alternativo das imagens.`

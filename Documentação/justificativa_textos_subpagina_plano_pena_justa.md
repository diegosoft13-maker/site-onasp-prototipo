# Justificativa de governança e dos textos da subpágina Plano Pena Justa

Data: 2026-05-08

## 1. Premissa de governança

A adequação da subpágina ao padrão da DCOM/gov.br não decorre apenas de preferência visual. Ela decorre de dois fatores cumulativos:

1. Limitação técnica observada no ambiente publicado.

   A análise da página atual da ONASP no portal gov.br/SENAPPEN e os registros consolidados em `Documentação/diario_de_bordo_onasp.md`, `Documentação/analise_dicom_onasp.md` e `Documentação/roteiro_publicacao_govbr_senappen.md` indicam uso de estrutura Plone/gov.br baseada em tiles e componentes editoriais já disponíveis no portal, e não de front-end próprio com CSS/JS livre por página.

2. Limitação de governança adotada para publicação institucional.

   Enquanto não houver orientação formal da DCOM autorizando HTML/CSS/JS customizados por página, o projeto deve assumir como base de trabalho apenas os componentes já observados e documentados para o ambiente gov.br/SENAPPEN. Isso preserva rastreabilidade, previsibilidade de publicação, acessibilidade e aderência ao padrão institucional.

Conclusão: manter a subpágina dentro da caixa de ferramentas do gov.br/SENAPPEN é, ao mesmo tempo, uma decisão técnica prudente e uma decisão de governança.

## 2. Escopo deste documento

Este documento justifica os textos atualmente presentes em `prototipo-dicom-onasp/subpaginas/plano-pena-justa.html`.

Para fins de rastreabilidade, os textos foram classificados em três grupos:

- `Rótulo de navegação/acessibilidade`: texto funcional, de orientação ou de acessibilidade.
- `Texto documental literal`: texto tomado diretamente de título oficial, ementa ou denominação normativa.
- `Síntese editorial controlada`: redação própria, mas estritamente baseada em documentos oficiais identificados.

## 3. Matriz de justificativa textual

| Elemento textual atual | Natureza | Fonte base | Justificativa de uso |
| --- | --- | --- | --- |
| `Voltar para Ouvidoria` | Rótulo de navegação/acessibilidade | Estrutura do site ONASP; ligação com `prototipo-dicom-onasp/index.html#projetos-estruturantes` | Texto funcional para retorno à página-mãe. Não cria conteúdo substantivo novo. |
| `Marca do Plano Pena Justa.` | Rótulo de acessibilidade | Arquivo visual oficial `Documentação/Botao_PenaJusta.png`; `Subpages/Pena_justa/Manual_de_Identidade_Visual_Pena_Justa.pdf` | Alt text curto e objetivo para identificar a imagem institucional sem inserir interpretação indevida. |
| `Conteúdo Técnico e Projetos Estruturantes` | Rótulo de navegação | `Documentação/roteiro_publicacao_govbr_senappen.md` | Corresponde ao agrupamento temático já adotado na página principal para as subpáginas do bloco de projetos estruturantes. É rótulo de arquitetura da informação, não afirmação normativa. |
| `Plano Pena Justa` | Texto documental com ajuste institucional justificado | `Documentação/roteiro_publicacao_govbr_senappen.md`; `Documentação/comparativo_nota_tecnica_vs_pagina_dicom.md`; `Subpages/Pena_justa/Plano_Nacional_Pena_Justa.pdf` | As Notas Técnicas 9 e 10 mencionam `Programa Pena Justa`, mas a orientação institucional posterior e o próprio acervo documental do Pena Justa convergem para `Plano Pena Justa`. O ajuste foi mantido por coerência institucional e para evitar conflito entre o título e a própria descrição do ambiente. |
| `Ambiente dedicado ao Plano Pena Justa, com informações gerais, documentos públicos e marcos relacionados ao fortalecimento das ouvidorias no sistema penal.` | Síntese editorial controlada | Texto-base da subpágina em `Documentação/roteiro_publicacao_govbr_senappen.md`; `Subpages/Pena_justa/SEI_35153985_Instrucao_Normativa_75.pdf`; `Subpages/Pena_justa/SEI_35032761_Portaria_549.pdf` | Mantém a ideia central do texto-base já aprovado para a subpágina (`Ambiente dedicado integralmente ao Plano...`) e a atualiza para refletir o conteúdo efetivamente inserido: documentos públicos e marcos normativos ligados às ouvidorias. |
| `O Plano` | Rótulo seccional | Estrutura editorial da subpágina | Título organizador de conteúdo, mais direto e aderente à identidade editorial solicitada para a subpágina do Plano Pena Justa. |
| `O Plano Pena Justa é o Plano Nacional para o Enfrentamento do Estado de Coisas Inconstitucional nas Prisões Brasileiras, no âmbito da ADPF 347...` | Síntese editorial controlada | `Subpages/Pena_justa/Plano_Nacional_Pena_Justa.pdf` | Síntese fiel da apresentação do Plano Nacional, preservando os eixos de qualificação das políticas penais, participação social, transparência e monitoramento. |
| `Na perspectiva da Ouvidoria Nacional de Serviços Penais, esta subpágina reúne referências públicas do Plano voltadas ao fortalecimento da participação social, da escuta qualificada e da articulação entre as ouvidorias dos serviços penais nos Estados e no Distrito Federal.` | Síntese editorial controlada | `Subpages/Pena_justa/SEI_35153985_Instrucao_Normativa_75.pdf`; `Subpages/Pena_justa/SEI_35032761_Portaria_549.pdf` | Texto redigido para situar a subpágina sob o recorte da ONASP. A menção à articulação federativa e ao fortalecimento das ouvidorias decorre diretamente da Renospen e da IN 75. |
| `Eixos de atuação` | Rótulo seccional | Estrutura do Plano Nacional | Título organizador para apresentação sintética dos quatro eixos. |
| `O Plano Nacional organiza sua atuação em quatro eixos estruturantes:` e a lista dos quatro eixos | Síntese editorial controlada | `Subpages/Pena_justa/Plano_Nacional_Pena_Justa.pdf`; `Subpages/Pena_justa/10_Coisas_que_você_precisa_saber_sobre_o_Pena_Justa.pdf` | A lista reproduz os eixos públicos já identificados no sumário do Plano Nacional e no documento `10 coisas...`, sem extrapolação interpretativa. |
| `Entregas já formalizadas` | Rótulo seccional | Atos normativos publicados em 2026 | Título editorial adequado para agrupar marcos já publicados e verificáveis documentalmente. |
| `No campo das ouvidorias e da participação social, o Pena Justa já reúne marcos normativos que podem ser destacados nesta página:` | Síntese editorial controlada | `Subpages/Pena_justa/SEI_35153985_Instrucao_Normativa_75.pdf`; `Subpages/Pena_justa/SEI_35032761_Portaria_549.pdf` | O texto não atribui cumprimento integral de metas amplas do Plano; limita-se a registrar a existência de marcos normativos já formalizados no eixo das ouvidorias e participação social. |
| `Normativo publicado` | Rótulo editorial | `Subpages/Pena_justa/SEI_35153985_Instrucao_Normativa_75.pdf` | Rótulo curto para classificar a natureza do ato apresentado. |
| `Instrução Normativa nº 75/2026` | Texto documental literal | `Subpages/Pena_justa/SEI_35153985_Instrucao_Normativa_75.pdf` | Título reduzido, porém fiel, da IN GABSEC/SENAPPEN/MJSP nº 75, de 08 de abril de 2026. |
| `Estabelece parâmetros mínimos para a criação e a estruturação de Ouvidorias de Serviços Penais...` | Síntese editorial controlada | Ementa e arts. 1º a 5º de `Subpages/Pena_justa/SEI_35153985_Instrucao_Normativa_75.pdf` | Resume o núcleo normativo do ato: criação/estruturação das ouvidorias, autonomia, transparência, acessibilidade e integração ao Fala.BR. |
| `Acessar a Instrução Normativa (PDF)` | Rótulo funcional | Link para `Subpages/Pena_justa/SEI_35153985_Instrucao_Normativa_75.pdf` | Texto de link claro, autoexplicativo e consistente com a prática de acessibilidade de indicar o tipo do arquivo. |
| `Rede instituída` | Rótulo editorial | `Subpages/Pena_justa/SEI_35032761_Portaria_549.pdf` | Rótulo curto para classificar a natureza do marco apresentado. |
| `Portaria nº 549/2026` | Texto documental literal | `Subpages/Pena_justa/SEI_35032761_Portaria_549.pdf` | Título reduzido, porém fiel, da Portaria GABSEC/SENAPPEN/MJSP nº 549, de 08 de abril de 2026. |
| `Institui a Rede Nacional de Ouvidorias de Serviços Penais - Renospen...` | Síntese editorial controlada | Ementa e arts. 1º a 4º e 6º de `Subpages/Pena_justa/SEI_35032761_Portaria_549.pdf` | Resume a instituição da Renospen como instância permanente de cooperação técnica, intercâmbio de informações e fortalecimento institucional. |
| `Acessar a Portaria (PDF)` | Rótulo funcional | Link para `Subpages/Pena_justa/SEI_35032761_Portaria_549.pdf` | Texto de link claro, autoexplicativo e consistente com a indicação do tipo de arquivo. |
| `Documentos públicos de referência` | Rótulo seccional com critério de governança | `Subpages/Pena_justa/Plano_Nacional_Pena_Justa.pdf`; `Subpages/Pena_justa/10_Coisas_que_você_precisa_saber_sobre_o_Pena_Justa.pdf` | O adjetivo `públicos` foi adotado para restringir a seção a materiais adequados para consulta externa. |
| `Plano Nacional Pena Justa (PDF)` | Texto funcional/literal | `Subpages/Pena_justa/Plano_Nacional_Pena_Justa.pdf` | Link direto para o documento estruturante do tema. |
| `10 coisas que você precisa saber sobre o Pena Justa (PDF)` | Texto funcional/literal | `Subpages/Pena_justa/10_Coisas_que_você_precisa_saber_sobre_o_Pena_Justa.pdf` | Link direto para material de apresentação pública e síntese do Plano. |

## 4. Itens avaliados e deliberadamente não publicados no corpo da subpágina

Os itens abaixo foram analisados, mas não permaneceram no texto visível da subpágina:

- Referências à `composição local`, à `pasta Documentação` e ao uso interno de arquivos visuais.
  Justificativa: são informações de bastidor, inadequadas para página pública.

- Link para o `Manual_de_Identidade_Visual_Pena_Justa.pdf` na seção principal de documentos.
  Justificativa: o manual é útil como suporte de comunicação e identidade visual, mas não é o documento mais relevante para o público da subpágina temática, que deve priorizar conteúdo substantivo do Plano e marcos normativos relacionados à atuação da ONASP.

- Recursos visuais baseados em CSS próprio.
  Justificativa: podem ser usados para pré-visualização local, mas não devem ser tratados como requisito de publicação pela DCOM sem confirmação formal de suporte técnico no ambiente oficial.

## 5. Síntese executiva

1. Há, sim, um limite prático no ambiente da DCOM/gov.br tal como ele foi observado neste projeto.
2. Mesmo que tecnicamente alguma customização fosse possível em outra camada do portal, a governança recomendada para este caso é não pressupor esse caminho sem autorização formal.
3. Os textos atuais da subpágina foram mantidos ou redigidos com base documental identificável e com distinção clara entre conteúdo literal, síntese editorial controlada e rótulos funcionais.
4. A subpágina atual não deve depender de CSS próprio para ser considerada válida como proposta para publicação institucional.

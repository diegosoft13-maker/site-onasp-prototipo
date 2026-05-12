# Apontamentos de divergências entre Notas Técnicas e página publicada pela DCOM

Data: 2026-05-12

## Finalidade

Este documento consolida apontamentos objetivos para subsidiar a elaboração de ofício à DCOM, com indicação das divergências entre o que foi solicitado nas Notas Técnicas da ONASP/SENAPPEN e o que foi efetivamente publicado na página gov.br da Ouvidoria Nacional de Serviços Penais.

O foco é registrar omissões, diferenças textuais e ajustes visuais necessários, preservando a compatibilidade com a caixa de ferramentas já disponível no gov.br/Plone utilizado pela SENAPPEN.

## Fontes consideradas

- Nota Técnica 9/2026/ONASP/SENAPPEN/MJ: atualização da página principal da Ouvidoria.
- Nota Técnica 10/2026/ONASP/SENAPPEN/MJ: criação de subpáginas temáticas.
- Despacho 566/2026/DCOM/GABSEC/SENAPPEN, especialmente quanto ao QR Code do chatbot.
- Página publicada da ONASP: <https://www.gov.br/senappen/pt-br/acesso-a-informacao/participacao-social/ouvidoria>
- Página de referência do Ministério do Planejamento e Orçamento: <https://www.gov.br/planejamento/pt-br/acesso-a-informacao/participacao-social/ouvidoria>

## Síntese dos apontamentos

A página publicada contempla parte da estrutura solicitada, mas ainda apresenta pendências relevantes:

- O QR Code oficial do chatbot não foi incluído na página publicada.
- O bloco antigo de contato permaneceu abaixo do banner de canais, gerando duplicidade e conflito de informação.
- O card e a subpágina da EMA foram publicados como Sistema Interamericano de Direitos Humanos, sem a identificação institucional consolidada `EMA - SENAPPEN`.
- O texto da Revista Brasileira de Execução Penal perdeu as menções institucionais à Espen, à DCOM e à Onasp.
- As subpáginas foram criadas, mas permanecem com conteúdo mínimo e mensagem de pasta vazia, embora o pacote editorial atualizado já esteja consolidado para envio.
- Há diferenças textuais na seção institucional, em Tipos de Manifestação, no Plano de Metas, no Relatório de Gestão e no Painel de Tratamento de Demandas.
- O bloco de Relatórios de Gestão pode ser apresentado em grade de anos, nos moldes da página de referência do MPO, desde que os links oficiais de cada ano sejam informados pela área responsável.

## Quadro 1 - Omissões e pendências de publicação

| Item | Solicitado | Publicado | Correção recomendada |
| --- | --- | --- | --- |
| QR Code do chatbot | Inserir QR Code oficial do atendimento automatizado por WhatsApp. | Não foi localizado QR Code na página publicada. | Inserir o QR Code em tamanho discreto, preferencialmente ao lado direito do banner de Canais de Atendimento ou logo abaixo dele em bloco compacto. |
| Bloco antigo de contato | Substituir os botões/blocos antigos pelo novo banner de canais. | O banner foi inserido, mas o bloco antigo de Contato permaneceu. | Remover o bloco antigo para evitar duplicidade de canais, conflito de telefone e excesso visual. |
| Ema | Usar a identificação Ema, vinculada à Equipe de Monitoramento e Acompanhamento das decisões do SIDH. | Publicado como Sistema Interamericano de Direitos Humanos. | Padronizar como `EMA - SENAPPEN`, mantendo a referência ao SIDH na descrição. |
| Revista Brasileira de Execução Penal | Texto com menção a Espen, DCOM e Onasp. | Texto publicado omitiu essas menções. | Restaurar a redação institucional solicitada. |
| Subpáginas | Criar páginas temáticas com aprofundamento. | Páginas criadas com conteúdo mínimo e mensagem Atualmente não existem itens nessa pasta. | Preencher as subpáginas com o pacote editorial consolidado em `Documentação/estrutura_completa_pagina_onasp_para_dicom.md` e remover a mensagem de pasta vazia. |
| Relatórios de Gestão | Disponibilizar acesso aos relatórios. | Link simples para Relatórios de Gestão. | Considerar grade de anos como no MPO, usando links oficiais por exercício. |

## Quadro 2 - Diferenças textuais observadas

| Seção | Texto/ideia solicitada | Como ficou publicado | Apontamento |
| --- | --- | --- | --- |
| Institucional | Linguagem direta: você pode solicitar; sua demanda será analisada pela nossa equipe. | Linguagem impessoal: é possível solicitar; a demanda é analisada. | Alteração reduz a aderência literal à Nota Técnica e muda o tom de atendimento ao cidadão. |
| Institucional | Texto solicitado não incluía chamada para fluxo de denúncias. | Foi acrescentado Conheça o fluxo de tratamento das denúncias. | Acréscimo não previsto na Nota Técnica. Pode permanecer se houver decisão institucional, mas deve ser registrado. |
| Tipos de Manifestação | A Ouvidoria Nacional de Serviços Penais (Onasp/Senappen). | A Ouvidoria Nacional de Serviços Penais. | Omitiu Onasp/Senappen. |
| Plano de Metas 2026 | A Onasp apresenta seu Plano de Metas. | A Ouvidoria apresenta seu Plano de Metas. | Troca do sujeito institucional. Recomenda-se retornar para Onasp. |
| Relatório de Gestão | Prestação de contas da ONASP à sociedade. | Prestação de contas da Ouvidoria com a sociedade. | Alteração de sujeito e regência. Recomenda-se restaurar ONASP à sociedade. |
| Relatório de Gestão | Acessar Relatórios de Gestão (PDF). | Acessar Relatórios de Gestão. | O rótulo perdeu a indicação de PDF. Se o destino for uma página agregadora, a retirada pode ser adequada, mas precisa estar registrada. |
| Painel de Tratamento de Demandas | Ouvidoria Nacional de Serviços Penais (Onasp). | Ouvidoria Nacional de Serviços Penais. | Omitiu Onasp. |
| Título do Painel | Ouvidoria Nacional de Serviços Penais. | Ouvidoria Nacional dos Serviços Penais. | Recomenda-se corrigir para de Serviços Penais. |

## Quadro 3 - Ajustes visuais recomendados na prévia

| Área | Problema observado | Correção aplicada na prévia local | Observação para DCOM |
| --- | --- | --- | --- |
| QR Code do WhatsApp | QR Code grande demais abaixo do banner de canais. | QR Code reposicionado em bloco discreto à direita do banner. | Implementar como imagem/figura compacta no Plone, sem criar funcionalidade nova. |
| Tipos de Manifestação | Espaço em branco excessivo entre texto, banner e link do Fala.BR. | Banner recebeu recorte visual e margem reduzida; link ficou mais próximo. | Idealmente, publicar imagem já recortada, sem excesso de área branca. |
| Cards das subpáginas | Cards somente textuais. | Links das subpáginas foram transformados em blocos com imagem e texto. | Usar card/link com imagem disponível na caixa gov.br/Plone. Substituir imagens provisórias pelos arquivos oficiais. |
| Relatórios de Gestão | Link único pouco destacado. | Criada grade de anos no padrão visual observado no MPO. | Usar a grade somente com links oficiais para cada relatório anual. |

## Correções sugeridas para encaminhamento à DCOM

1. Inserir o QR Code oficial do chatbot na seção de Canais de Atendimento, em tamanho discreto e junto ao banner.
2. Remover o bloco antigo de Contato que permaneceu após o banner de Canais de Atendimento.
3. Ajustar o card e a subpágina para `EMA - SENAPPEN`, mantendo a referência ao SIDH na descrição.
4. Restaurar o texto da Revista Brasileira de Execução Penal com menção à Espen, à DCOM e à Onasp.
5. Ajustar a redação do Plano de Metas para a Onasp apresenta seu Plano de Metas.
6. Ajustar a redação do Relatório de Gestão para da ONASP à sociedade.
7. Corrigir o título do Painel para Ouvidoria Nacional de Serviços Penais.
8. Reinserir Onasp/Senappen no texto de Tipos de Manifestação, caso se busque aderência literal à Nota Técnica.
9. Preencher as quatro subpáginas temáticas com o pacote editorial consolidado ou retirar a mensagem Atualmente não existem itens nessa pasta.
10. Adotar, se possível, grade de links por ano para Relatórios de Gestão, inspirada no padrão do MPO e usando apenas links oficiais existentes.

## Observação sobre Programa Pena Justa e Plano Pena Justa

As Notas Técnicas 9 e 10 extraídas mencionam Programa Pena Justa. Entretanto, a orientação posterior recebida e o próprio conteúdo descritivo apontam para Plano Pena Justa. Assim, recomenda-se tratar a substituição de Programa por Plano como ajuste de nomenclatura institucional posterior, e não como divergência literal da DCOM em relação às Notas Técnicas.

## Encaminhamento proposto

Recomenda-se encaminhar à DCOM um pedido de ajuste pontual, com anexação deste quadro de apontamentos e do pacote editorial consolidado em `Documentação/estrutura_completa_pagina_onasp_para_dicom.md`, destacando que as correções propostas não exigem desenvolvimento novo e podem ser executadas com os componentes já disponíveis no gov.br/Plone: texto rico, imagem linkada, card/link de subpágina, iframe e links simples.

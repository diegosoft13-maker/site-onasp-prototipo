# Comparativo entre Notas Técnicas e página publicada pela DCOM

Data: 2026-05-07

## Fontes comparadas

- Nota Técnica 9/2026/ONASP/SENAPPEN/MJ: atualização da página principal.
- Nota Técnica 10/2026/ONASP/SENAPPEN/MJ: criação das subpáginas temáticas.
- Página publicada da ONASP em 2026-05-07: <https://www.gov.br/senappen/pt-br/acesso-a-informacao/participacao-social/ouvidoria>
- Subpáginas publicadas: Rede de Ouvidorias, Sistema Interamericano de Direitos Humanos, Programa Pena Justa e Revista Brasileira de Execução Penal.
- Despacho 566/2026/DCOM/GABSEC/SENAPPEN, no ponto sobre o QR Code do chatbot.

## Síntese executiva

A DCOM incluiu boa parte da estrutura solicitada, mas a publicação ficou incompleta e com diferenças de texto. O que mais importa corrigir agora:

- Inserir o QR Code oficial do chatbot na seção de Canais de Atendimento.
- Remover o bloco antigo de Contato, que permaneceu na página e conflita com o Banner 2.
- Corrigir o card/subpágina da Ema, que foi publicado como "Sistema Interamericano de Direitos Humanos" e perdeu o acrônimo solicitado.
- Restaurar a redação da Revista com "Em parceria com a Espen e a DCOM".
- Corrigir diferenças textuais em Institucional, Tipos de Manifestação, Plano de Metas, Relatório de Gestão e Painel.
- Resolver a nomenclatura "Programa Pena Justa" versus "Plano Pena Justa" conforme orientação do Ouvidor/documento de referência, observando que as Notas Técnicas 9 e 10 extraídas também trazem o título "Programa Pena Justa".
- Preencher as subpáginas ou remover a mensagem "Atualmente não existem itens nessa pasta".

## O que a DCOM esqueceu de incluir ou deixou pendente

| Prioridade | Item faltante ou pendente | Pedido original | Como ficou publicado | Correção solicitada |
| --- | --- | --- | --- | --- |
| Alta | QR Code do chatbot | O Despacho 566 orientou inserir o QR Code na página principal, na área de canais. | Não há QR Code nem menção ao chatbot na página publicada. | Inserir `Documentação/QRcode_Whatsapp.png` como imagem oficial com legenda simples. |
| Alta | Remoção do contato antigo | A Nota Técnica 9 pediu substituir os botões/blocos antigos e inserir o Banner 2 de canais. | O Banner 2 foi inserido, mas o bloco antigo "Contato" permaneceu. | Remover o bloco antigo ou atualizar integralmente para não conflitar com o banner. |
| Alta | Aderência ao nome Ema | Nota Técnica 9: `Ema (Equipe de Monitoramento e Acompanhamento das decisões do SIDH)`. Nota Técnica 10: `SUBPÁGINA 2: EMA`. | Card e subpágina foram publicados como `Sistema Interamericano de Direitos Humanos`. | Renomear para `Ema - SIDH` ou `Ema (Equipe de Monitoramento e Acompanhamento das decisões do SIDH)`. |
| Alta | Texto institucional da Revista | Nota Técnica 9/10: `Em parceria com a Espen e a Dcom, a Onasp lança edição...` | Publicado: `A Ouvidoria lança edição...`, sem Espen, DCOM e Onasp. | Restaurar a redação institucional da nota ou justificar formalmente a alteração. |
| Alta | Conteúdo real nas subpáginas | Nota Técnica 10 pediu subpáginas exclusivas para aprofundamento temático. | As subpáginas têm só o parágrafo inicial e a mensagem `Atualmente não existem itens nessa pasta`. | Preencher com conteúdo mínimo oficial ou retirar a mensagem de pasta vazia. |
| Média | Link/rótulo do relatório | Nota Técnica 9: botão/link único `Acessar Relatórios de Gestão (PDF)`. | Publicado: `Acessar Relatórios de Gestão`, sem `(PDF)`. | Usar `(PDF)` se o destino for PDF direto; se for página agregadora, registrar essa decisão. |
| Média | Acessibilidade textual dos banners | Os banners concentram informação textual relevante. | Alt texts curtos: `tipos de manifestação`, `Canais de atendimento`, `Metas para 2026`. | Inserir texto alternativo ou transcrição em texto rico próximo aos banners. |
| Média | Títulos acessíveis dos iframes | Mapa e Power BI devem permanecer funcionais e acessíveis. | Iframes aparecem sem `title` no HTML extraído. | Solicitar título acessível, se o Plone permitir. |

## Diferenças de texto na página principal

| Seção | Solicitado na Nota Técnica | Publicado pela DCOM | Diferença textual |
| --- | --- | --- | --- |
| Institucional | `...Por meio da Lei de Acesso à Informação (LAI), você pode solicitar dados e documentos de acesso público através da plataforma Fala.BR. Sua demanda será analisada pela nossa equipe e encaminhada ao setor responsável para que você receba a resposta adequada.` | `...Por meio da Lei de Acesso à Informação (LAI), é possível solicitar dados e documentos de acesso público através da plataforma Fala.BR. A demanda é analisada e encaminhada ao setor responsável para que o cidadão receba a resposta adequada. Conheça o fluxo de tratamento das denúncias.` | Trocou linguagem direta por impessoal: `você pode solicitar` virou `é possível solicitar`; `Sua demanda será analisada pela nossa equipe` virou `A demanda é analisada`; acrescentou link/frase `Conheça o fluxo de tratamento das denúncias`, que não estava no texto solicitado. |
| Tipos de Manifestação | `A Ouvidoria Nacional de Serviços Penais (Onasp/Senappen) é o canal oficial...` | `A Ouvidoria Nacional de Serviços Penais é o canal oficial...` | Omitiu `(Onasp/Senappen)`. O restante do texto ficou substancialmente aderente. |
| Canais de Atendimento | Inserir Banner 2 e remover o bloco textual antigo. | Banner 2 foi inserido, mas permaneceu `Contato`, com e-mail, telefone, endereço, horário e agendamento. | A diferença principal não é de redação nova, mas de permanência indevida de texto antigo. Além disso, o telefone do texto antigo é `(61) 3770-5034`, enquanto o banner aponta outro canal. |
| Plano de Metas 2026 | `Alinhada às diretrizes de modernização da Secretaria Nacional de Políticas Penais, a Onasp apresenta seu Plano de Metas...` | `Alinhada às diretrizes de modernização da Secretaria Nacional de Políticas Penais, a Ouvidoria apresenta seu Plano de Metas...` | `a Onasp apresenta` foi substituído por `a Ouvidoria apresenta`. É mudança leve, mas reduz aderência literal à nota. |
| Relatório de Gestão | `O Relatório de Gestão é o principal instrumento de transparência pública e prestação de contas da ONASP à sociedade.` | `O Relatório de Gestão é o principal instrumento de transparência pública e prestação de contas da Ouvidoria com a sociedade.` | `da ONASP à sociedade` virou `da Ouvidoria com a sociedade`, mudando o sujeito institucional e a regência. |
| Relatório de Gestão | `Este documento consolida, anualmente...` | `O documento consolida, anualmente...` | Mudança pequena de `Este` para `O`; sem impacto material, mas não é literal. |
| Relatório de Gestão | Link único `Acessar Relatórios de Gestão (PDF)`. | `Acessar Relatórios de Gestão`. | Omitiu `(PDF)`. |
| Painel Power BI | `O Painel de Tratamento de Demandas da Ouvidoria Nacional de Serviços Penais (Onasp) é...` | `O Painel de Tratamento de Demandas da Ouvidoria Nacional de Serviços Penais é...` | Omitiu `(Onasp)`. O restante do texto ficou aderente. |
| Título do Painel | Nota fala em `Painel de Dados (PowerBI)` e texto padrão de Painel de Tratamento de Demandas. | Publicado: `Painel de Tratamento de Demandas da Ouvidoria Nacional dos Serviços Penais`. | Há diferença de redação e possível erro de preposição: `dos Serviços Penais` em vez de `de Serviços Penais`. |

## Diferenças de texto nos cards e subpáginas

| Item | Solicitado na Nota Técnica | Publicado pela DCOM | Diferença textual |
| --- | --- | --- | --- |
| Rede de Ouvidorias | Título `Rede de Ouvidorias`; descrição: `Estruturada a partir da integração oficial entre a União e os Estados...` | Título e descrição foram publicados conforme a Nota Técnica. | Não há divergência literal relevante. Porém o diálogo com o Ouvidor apontou risco político/institucional na redação; recomenda-se substituir por texto mais neutro. |
| Ema | Título: `Ema (Equipe de Monitoramento e Acompanhamento das decisões do SIDH)`; destino: subpágina da Ema. | Título/card/subpágina: `Sistema Interamericano de Direitos Humanos`. | O acrônimo `Ema` foi omitido e o foco mudou da equipe para o sistema. O texto descritivo permaneceu aderente. |
| Pena Justa | Nota Técnica 9/10 extraída: `Programa Pena Justa`; descrição: `Ambiente dedicado integralmente ao Plano...` | Publicado: `Programa Pena Justa`; descrição igual. | Estritamente pela Nota Técnica 9/10, a DCOM não divergiu do título. Porém há conflito com a orientação posterior do Ouvidor/documento de referência, que indica `Plano Pena Justa`. Como o próprio texto diz `dedicado integralmente ao Plano`, recomenda-se corrigir para `Plano Pena Justa`. |
| Revista Brasileira de Execução Penal | `Em parceria com a Espen e a Dcom, a Onasp lança edição da Revista Brasileira de Execução Penal...` | `A Ouvidoria lança edição da Revista Brasileira de Execução Penal...` | Foram removidas as menções a `Espen`, `DCOM` e `Onasp`. É a diferença textual mais clara nos cards/subpáginas. |
| Subpáginas | Nota Técnica 10 pediu subpáginas exclusivas para aprofundamento temático. | As quatro subpáginas mostram o parágrafo inicial e depois `Atualmente não existem itens nessa pasta`. | A estrutura foi criada, mas o aprofundamento não foi incluído. A mensagem de pasta vazia passa sensação de entrega incompleta. |

## O que foi feito corretamente ou quase corretamente

| Item | Situação |
| --- | --- |
| Banner rotativo | Mantido no topo, abaixo de `Ouvidoria Nacional de Serviços Penais`, como solicitado. |
| Texto institucional principal | Conteúdo central foi atualizado; as diferenças são de redação e acréscimo de link. |
| Banner 1 dos tipos de manifestação | Inserido e linkado ao Fala.BR. |
| Banner 2 dos canais | Inserido. O problema é a permanência do bloco antigo abaixo. |
| Mapa | Inserido, mas sua posição ficou prejudicada pela permanência do contato antigo. |
| Cards/subpáginas | Criados, mas com divergências de título/texto e conteúdo mínimo. |
| Plano de Metas 2026 | Inserido com texto e banner. Diferença principal: `Onasp` virou `Ouvidoria`. |
| Power BI | Mantido com texto atualizado; diferença principal é a omissão de `(Onasp)` e ausência de título acessível no iframe. |

## Lista objetiva para encaminhar à DCOM

1. Inserir o QR Code oficial do chatbot na seção Canais de Atendimento.
2. Remover o bloco antigo `Contato` que ficou abaixo do Banner 2.
3. Corrigir o card/subpágina `Sistema Interamericano de Direitos Humanos` para `Ema - SIDH` ou título completo com `Ema` visível.
4. Restaurar no texto da Revista: `Em parceria com a Espen e a DCOM, a Onasp lança...`.
5. Ajustar `a Ouvidoria apresenta` para `a Onasp apresenta` no Plano de Metas 2026.
6. Ajustar `da Ouvidoria com a sociedade` para `da ONASP à sociedade` no Relatório de Gestão.
7. Decidir se o link deve aparecer como `Acessar Relatórios de Gestão (PDF)` ou apenas `Acessar Relatórios de Gestão` por apontar para página agregadora.
8. Reinserir `(Onasp/Senappen)` no texto de Tipos de Manifestação, se a prioridade for literalidade documental.
9. Reinserir `(Onasp)` no texto do Painel Power BI.
10. Corrigir `dos Serviços Penais` para `de Serviços Penais` no título do Painel, se a DCOM puder ajustar o cabeçalho.
11. Preencher as subpáginas ou retirar a mensagem `Atualmente não existem itens nessa pasta`.
12. Tratar `Programa Pena Justa` versus `Plano Pena Justa` como ajuste de nomenclatura institucional: as Notas 9/10 trazem `Programa`, mas a orientação posterior do Ouvidor/documento de referência aponta `Plano`.

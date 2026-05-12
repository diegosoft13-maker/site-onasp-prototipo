# Análise da página ONASP para alinhamento com a DCOM

Data da análise: 2026-05-12

## Fontes analisadas

- Página publicada da ONASP: <https://www.gov.br/senappen/pt-br/acesso-a-informacao/participacao-social/ouvidoria>
- Página de referência indicada: <https://www.gov.br/planejamento/pt-br/acesso-a-informacao/participacao-social/ouvidoria>
- Processo SEI: 08016.009807/2026-98
- Nota Técnica 9/2026/ONASP/SENAPPEN/MJ: atualização da página principal.
- Nota Técnica 10/2026/ONASP/SENAPPEN/MJ: criação das subpáginas temáticas.
- Despacho 453/2026/ONASP/SENAPPEN: encaminhamento à DCOM.
- Despacho 566/2026/DCOM/GABSEC/SENAPPEN: resposta da DCOM e pendências.
- Despacho 486/2026/ONASP/SENAPPEN: encaminhamento interno para atendimento das solicitações da DCOM.
- Banners anexos: tipos de manifestação, canais de atendimento e metas 2026.

## Síntese executiva

A página publicada incorporou a maior parte da estrutura solicitada na Nota Técnica 9: banner rotativo, texto institucional atualizado, imagem dos tipos de manifestação, imagem de canais de atendimento, iframe de mapa, quatro cards de subpáginas, plano de metas 2026, relatório de gestão e painel Power BI.

As diferenças mais importantes para devolver à DCOM são: manutenção indevida do bloco textual antigo de contato, divergência de telefone entre a imagem e o texto remanescente, ausência do QR Code do chatbot na página publicada, subpáginas ainda publicadas com conteúdo mínimo e mensagem de pasta vazia, alteração do nome da subpágina/card da EMA, uso de "Programa Pena Justa" em vez de "Plano Pena Justa", link de relatórios sem a indicação "(PDF)" e ajustes de acessibilidade em imagens/iframes.

Para a nova devolutiva, o pacote editorial das subpáginas e a padronização de nomenclatura já estão consolidados neste workspace; a pendência remanescente é refletir esse material na publicação oficial.

## Premissa de implementação

A página deve permanecer na mesma linguagem e estrutura do gov.br/SENAPPEN, usando os componentes disponíveis na caixa de ferramentas do Plone/gov.br. A análise não recomenda biblioteca externa, JavaScript próprio, botão customizado, ícone customizado, card fora do padrão ou funcionalidade não disponível no ambiente oficial. O protótipo local é apenas uma prévia de ordem e conteúdo.

## O que foi feito diferente do que foi pedido

| Item | Pedido nos documentos | Como está na página publicada | Diferença / risco | Encaminhamento sugerido |
| --- | --- | --- | --- | --- |
| Banner rotativo | Manter os banners atuais de Canais de Comunicação e WhatsApp no topo, abaixo do título. | Mantido como carrossel com imagens vinculadas ao Fala.BR. | Sem divergência material. | Apenas validar se a ordem visual no Plone/gov.br permanece a mesma em desktop e celular. |
| Texto institucional | Substituir integralmente o bloco antigo pelo texto da Nota Técnica 9. | Texto atualizado, com pequenas alterações de redação e inclusão do link para o fluxo de tratamento das denúncias. | Divergência leve: o texto não é 100% literal e há link adicional não solicitado. | Aceitar se a ONASP concordar com a melhoria; se a exigência for aderência documental, pedir texto literal. |
| Tipos de manifestação | Inserir parágrafo introdutório, remover botões antigos e usar o Banner 1 como imagem única clicável para Fala.BR. | Parágrafo e imagem foram inseridos; a imagem está clicável para Fala.BR. | Sem divergência funcional. Há risco de acessibilidade porque o `alt` é apenas "tipos de manifestação", sem equivalência textual completa da imagem. | Manter visual e solicitar texto alternativo/descritivo acessível ou bloco textual oculto/acessível com os sete tipos. |
| Canais de atendimento | Remover o bloco antigo de telefones/endereço e inserir somente o Banner 2. | Banner 2 foi inserido, mas o bloco textual "Contato" permaneceu logo abaixo. | Divergência relevante: a nota pediu remover o texto antigo. Também há conflito de telefone: banner mostra (61) 3770-5039; texto remanescente mostra (61) 3770-5034. | Pedir retirada do bloco textual antigo ou atualização integral para ficar igual ao banner. Validar oficialmente qual telefone deve prevalecer. |
| QR Code do chatbot | Despacho 566 orienta inserir o QR Code na página principal, em seção destinada aos canais de atendimento. | Não foi identificado QR Code nem menção a chatbot no conteúdo publicado. | Pendência relevante, especialmente porque a DCOM pediu orientação explícita. O arquivo foi localizado em `Documentação/QRcode_Whatsapp.png`. | Solicitar inclusão do QR Code real junto ao bloco de canais de atendimento, com legenda simples e sem placeholder. |
| Mapa de localização | Manter iframe interativo do Google Maps logo abaixo do Banner 2. | Há iframe de mapa após a seção de contato, antes dos cards. O snapshot capturou iframe sem `src` visível e sem `title`; a página ainda indicou presença de mapa no HTML. | Pode estar funcional visualmente, mas a ordem ficou depois do texto de contato remanescente. Há risco de acessibilidade por ausência de título. | Após remover o texto antigo, manter o mapa diretamente abaixo do banner. Solicitar `title="Mapa da sede da SENAPPEN"` ou equivalente. |
| Cards/subpáginas | Criar quatro cards: Rede de Ouvidorias, Ema, Plano Pena Justa e Revista Brasileira de Execução Penal. | Quatro cards existem. O segundo foi publicado como "Sistema Interamericano de Direitos Humanos", não como "Ema". O terceiro foi publicado como "Programa Pena Justa". Os cards aparecem como componente de virar card, com texto "Vire o card". | Divergência de nomenclatura no card/subpágina da EMA e no Plano Pena Justa. O componente de virar card pode poluir leitura por leitor de tela. | Renomear para "EMA - SENAPPEN" e "Plano Pena Justa", mantendo a referência ao SIDH na descrição. Validar acessibilidade do componente. |
| Texto do card Revista | A nota pediu: "Em parceria com a Espen e a Dcom, a Onasp lança..." | O texto publicado inicia com "A Ouvidoria lança..." e remove a parceria com Espen e DCOM. | Divergência de conteúdo institucional. | Restaurar a redação da Nota Técnica ou confirmar oficialmente a alteração. |
| Subpáginas temáticas | Criar subpáginas exclusivas para aprofundamento temático, mantendo a página inicial leve. | As subpáginas existem, mas trazem só o parágrafo inicial e a mensagem "Atualmente não existem itens nessa pasta." | Implementação incompleta. O próprio Despacho 566 registrou que permanecia pendente o conteúdo necessário para preenchimento. O material editorial atualizado já foi consolidado neste workspace. | Encaminhar à DCOM o pacote editorial consolidado das quatro subpáginas e substituir o resumo da Rede por linguagem institucional neutra. |
| Plano de Metas 2026 | Inserir título, texto introdutório e Banner 3 abaixo dos cards. | Inserido com texto e imagem. | Divergência leve: texto usa "a Ouvidoria apresenta" em vez de "a Onasp apresenta". A imagem tem `alt` curto, sem transcrição das 13 metas. | Manter seção e pedir texto alternativo/transcrição acessível das metas. |
| Relatórios de Gestão | Atualizar texto e substituir lista antiga por link único destacado "Acessar Relatórios de Gestão (PDF)", conforme linguagem da Nota Técnica 9. | Texto atualizado e link único "Acessar Relatórios de Gestão". | O rótulo não inclui "(PDF)". O destino é uma página de relatórios, não um PDF direto no snapshot analisado. | Ajustar rótulo para "Acessar Relatórios de Gestão (PDF)" se o destino final for PDF; se for página agregadora, usar "Acessar Relatórios de Gestão" e registrar a decisão. |
| Painel Power BI | Manter iframe funcionando e atualizar texto. | Texto atualizado e iframe Power BI presente. | Iframe sem `title` no snapshot. | Solicitar título acessível, por exemplo "Painel de tratamento de demandas da ONASP". |
| Currículo do Ouvidor | Despacho 453 pediu indicação de local para inserção do currículo. | A página principal não possui seção do Ouvidor. | Não é divergência da página principal porque o Despacho 566 indicou a página "Quem é Quem" como local adequado. | Encaminhar currículo e confirmar publicação na página "Quem é Quem". |

## Lições da página de referência do MPO

A página do Ministério do Planejamento e Orçamento é útil como referência de organização institucional, não como modelo visual a ser copiado. Pontos que podem inspirar a ONASP:

- Apresenta Fala.BR como canal preferencial 24 horas.
- Inclui seção de prazos para manifestações e LAI.
- Explicita responsabilidade com LGPD e encarregado pelo tratamento de dados pessoais.
- Mantém seção de legislação com normativos aplicáveis.
- Mantém histórico de relatórios de gestão por ano.
- Publica currículo/nomeação da autoridade em área institucional apropriada.

Para a ONASP, a prioridade definida nos documentos é diferente: a primeira tela deve privilegiar atendimento ao cidadão, tipos de manifestação, canais, mapa, projetos estruturantes, metas e BI. Assim, a referência do MPO deve ser usada para complementar governança, prazos, legislação, LGPD e histórico de relatórios, sem desviar a página inicial para um excesso de conteúdo textual.

## Requisitos mínimos para o protótipo temporário

1. Página na estrutura atual do gov.br/SENAPPEN, sem hero, biblioteca externa ou componente customizado.
2. Abertura textual curta e institucional antes de imagens extensas, para melhorar a primeira dobra sem criar componente novo.
3. Banner dos sete tipos de manifestação em destaque, clicável para Fala.BR, acompanhado de link textual acessível.
4. Banner de canais de atendimento sem duplicação conflitante de telefone/endereço.
5. QR Code real do chatbot na própria área de canais, com legenda.
6. Mapa logo após canais.
7. Quatro cards de subpáginas com a nomenclatura consolidada: Rede de Ouvidorias, EMA - SENAPPEN, Plano Pena Justa e Revista Brasileira de Execução Penal.
8. Plano de Metas 2026 com Banner 3 e transcrição acessível das metas em HTML.
9. Relatórios de Gestão com link único destacado e rótulo decidido.
10. Painel Power BI com texto atualizado e título acessível no iframe.
11. Rodapé do protótipo com link para a página de referência do MPO e para a página publicada da ONASP.

## Pendências para nova interação com a DCOM

- Confirmar telefone oficial: (61) 3770-5039 ou (61) 3770-5034.
- Publicar o QR Code do chatbot localizado em `Documentação/QRcode_Whatsapp.png`.
- Encaminhar o pacote editorial consolidado das quatro subpáginas para substituir a mensagem de pasta vazia.
- Padronizar o card/subpágina da EMA como "EMA - SENAPPEN", mantendo SIDH na descrição.
- Corrigir "Programa Pena Justa" para "Plano Pena Justa".
- Confirmar se o link de relatório deve apontar para PDF direto ou página agregadora.
- Solicitar melhoria de acessibilidade para imagens ricas em texto e iframes.

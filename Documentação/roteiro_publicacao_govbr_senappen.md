# Roteiro de publicação gov.br/Plone para a página ONASP

Data: 2026-05-12

## Premissa

A página da ONASP deve ser estruturada na mesma linguagem e lógica da página atual no gov.br/SENAPPEN, dentro do ambiente Plone/gov.br e com a caixa de ferramentas disponível para a DCOM. Este roteiro não propõe aplicação, front-end próprio, biblioteca externa, JavaScript customizado, ícone customizado, botão novo ou controle que não esteja disponível no portal.

## Componentes permitidos neste roteiro

Com base na página publicada analisada, a estrutura deve se limitar a componentes equivalentes a:

- título e subtítulos;
- texto rico com links simples;
- banner/imagem institucional linkada;
- iframe já aceito na página atual, como mapa e Power BI;
- card/link de subpágina no padrão disponível no gov.br;
- página/subpágina simples com título, texto e links/documentos oficiais.

## Ordem da página principal

| Ordem | Seção | Componente gov.br/Plone sugerido | Conteúdo conforme notas técnicas | Observação |
| --- | --- | --- | --- | --- |
| 1 | Ouvidoria Nacional de Serviços Penais | Título/subtítulo existente | Manter título atual da página. | Não criar hero customizado. |
| 2 | Banner rotativo | Componente atual de banner/carrossel | Manter banners atuais de Canais de Comunicação e WhatsApp. | Ação da Nota Técnica 9: manter. |
| 3 | Sobre a Ouvidoria | Texto rico | Substituir texto institucional pelo texto da Nota Técnica 9. | Usar link simples para Fala.BR se o editor permitir. |
| 4 | Tipos de Manifestação | Texto rico + imagem/banner linkado | Inserir parágrafo da Nota Técnica 9 e Banner 1 clicável para Fala.BR. | Remover botões antigos, como pedido na nota. |
| 5 | Canais de Atendimento | Imagem/banner linkado | Inserir Banner 2. | Remover bloco textual antigo para evitar conflito de telefone. |
| 6 | QR Code do chatbot | Imagem estática oficial com legenda | Inserir na seção de canais, conforme Despacho 566. O arquivo foi localizado em `Documentação/QRcode_Whatsapp.png`. | Publicar com legenda curta e sem placeholder na publicação final. |
| 7 | Mapa de Localização | Iframe de mapa já usado na página atual | Manter componente logo abaixo do Banner 2. | Solicitar título acessível no iframe se a ferramenta permitir. |
| 8 | Contato institucional resumido | Texto rico em bloco compacto | Inserir abaixo do mapa endereço, telefone e e-mail em formato curto e horizontal. | Usar texto enxuto, sem recriar o bloco antigo extenso de contato. |
| 9 | Currículo do Ouvidor | Texto rico + link simples para PDF | Inserir resumo do currículo de João Vitor Elpídio Ferreira, com link para `Documentação/Curriculo_Joao_vitor_elpidio_Ferreira.pdf`. | Posicionar abaixo do mapa e do contato resumido, antes dos cards. |
| 10 | Conteúdo Técnico e Projetos Estruturantes | Cards/links de subpágina disponíveis no gov.br | Criar quatro entradas: Rede de Ouvidorias, EMA - SENAPPEN, Plano Pena Justa e Revista Brasileira de Execução Penal. | Não inventar ícones se a caixa de ferramentas não oferecer. |
| 11 | Plano de Metas 2026 | Texto rico + imagem/banner | Inserir texto introdutório da Nota Técnica 9 e Banner 3. | Manter redação com "Onasp apresenta" para fidelidade documental. |
| 12 | Relatório de Gestão | Texto rico + link simples destacado | Atualizar texto e usar link "Acessar Relatórios de Gestão (PDF)" se o destino for PDF. | Se o destino for página agregadora, registrar decisão de manter sem "PDF". |
| 13 | Painel de Tratamento de Demandas | Texto rico + iframe Power BI | Manter iframe e substituir texto antigo pelo texto da Nota Técnica 9. | Solicitar título acessível no iframe se possível. |
| 14 | Legislação | Texto rico + links simples para PDF | Inserir, abaixo do painel, a lista dos normativos basilares efetivamente disponíveis na pasta `Documentação/Normativas Basilares de Ouvidoria`. | Não listar documento que ainda não esteja no pacote encaminhado. |

## Subpáginas

As subpáginas devem ser simples, sem componentes customizados. A estrutura editorial base já está consolidada neste workspace e no documento `Documentação/estrutura_completa_pagina_onasp_para_dicom.md`. Portanto, a publicação pode avançar com título, imagem institucional, texto introdutório, blocos curtos de conteúdo e links/documentos oficiais, sempre sem mensagem de pasta vazia.

| Subpágina | Título fiel | Texto-base |
| --- | --- | --- |
| Rede de Ouvidorias | Rede de Ouvidorias | Iniciativa do Plano Pena Justa voltada à cooperação federativa, à harmonização de procedimentos e ao fortalecimento da proteção de direitos no âmbito das Ouvidorias de Serviços Penais. |
| Ema | EMA - SENAPPEN | Espaço da Equipe de Monitoramento e Acompanhamento das decisões e deliberações do Sistema Interamericano de Direitos Humanos em face do sistema penal nacional, dedicado a fortalecer o cumprimento das determinações do SIDH em parceria com as Unidades Federativas. |
| Plano Pena Justa | Plano Pena Justa | Ambiente dedicado integralmente ao Plano, que disponibiliza o acesso a cronogramas, documentos técnicos e relatórios de acompanhamento. |
| Revista Brasileira de Execução Penal | Revista Brasileira de Execução Penal | Em articulação com a Espen e a DCOM, esta subpágina reúne referências da Revista Brasileira de Execução Penal e destaca conteúdos com interface com participação social, transparência e direitos no sistema penal. |

## Pontos que não devem ser enviados como requisito de implementação

- Biblioteca de ícones externa.
- Botões estilizados fora do padrão gov.br.
- Cards com comportamento diferente do componente disponível no Plone.
- JavaScript próprio.
- Layout hero ou landing page promocional.
- Placeholder gráfico de QR Code.
- CSS local do protótipo como exigência de publicação.

## Pendências objetivas para a DCOM

- Confirmar qual telefone é oficial: o do Banner 2 ou o texto antigo remanescente na página publicada.
- Publicar o QR Code oficial do chatbot localizado em `Documentação/QRcode_Whatsapp.png`.
- Corrigir o nome do segundo card/subpágina para manter `EMA - SENAPPEN` visível e preservar a referência ao SIDH na descrição.
- Corrigir "Programa Pena Justa" para "Plano Pena Justa".
- Restaurar a menção "Em parceria com a Espen e a DCOM" no texto da Revista, salvo decisão institucional em contrário.
- Remover o bloco textual antigo de contato, se a orientação da Nota Técnica 9 continuar válida.
- Preencher as subpáginas com o pacote editorial consolidado em `Documentação/estrutura_completa_pagina_onasp_para_dicom.md` e retirar qualquer mensagem de pasta vazia.
- Manter links textuais próximos às imagens clicáveis sempre que o editor permitir, para melhorar a acessibilidade.

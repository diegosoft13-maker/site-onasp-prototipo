# Diário de bordo ONASP/DCOM

Data de atualização: 2026-05-12

## Objetivo deste diário

Este arquivo existe para que qualquer IA, agente ou pessoa que retome o trabalho entenda rapidamente o ponto exato do projeto, sem reabrir toda a conversa. O foco é corrigir e melhorar a página da Ouvidoria Nacional de Serviços Penais no portal gov.br/SENAPPEN, mantendo aderência aos documentos SEI, ao padrão de governança institucional e à caixa de ferramentas real disponível para a DCOM.

## Situação atual em uma frase

A DCOM publicou uma atualização da página ONASP, mas a versão ainda parece parcialmente baseada na estrutura antiga, contém divergências em relação às notas técnicas e precisa de uma rodada objetiva de correções editoriais/visuais dentro do padrão Plone/gov.br, sem criar aplicação ou componente customizado.

## Fontes oficiais usadas

- Processo SEI: 08016.009807/2026-98.
- Documento de referência citado no diálogo: 35386110.
- Nota Técnica 9/2026/ONASP/SENAPPEN/MJ.
- Nota Técnica 10/2026/ONASP/SENAPPEN/MJ.
- Despacho 453/2026/ONASP/SENAPPEN.
- Despacho 566/2026/DCOM/GABSEC/SENAPPEN.
- Despacho 486/2026/ONASP/SENAPPEN.
- Página publicada ONASP: <https://www.gov.br/senappen/pt-br/acesso-a-informacao/participacao-social/ouvidoria>
- Página de referência MPO: <https://www.gov.br/planejamento/pt-br/acesso-a-informacao/participacao-social/ouvidoria>
- Banners oficiais salvos em `Documentação/Banner_1.png`, `Documentação/Banner_2.png` e `Documentação/Banner_3.png`.
- QR Code oficial salvo em `Documentação/QRcode_Whatsapp.png`.
- Inventário técnico da estrutura gov.br/SENAPPEN salvo em `Documentação/inventario_estrutura_govbr_senappen.md`.
- Comparativo literal entre Notas Técnicas e página publicada salvo em `Documentação/comparativo_nota_tecnica_vs_pagina_dicom.md`.
- Documento de apontamentos para subsidiar ofício à DCOM salvo em `Documentação/apontamentos_divergencias_notas_tecnicas_dcom.md`.

## Ponto do diálogo com o Ouvidor

O diálogo de 2026-05-06/2026-05-07 trouxe estes alertas principais:

- A DCOM devolveu o processo, mas a página publicada ainda parece atualizada com base na versão antiga.
- Foi publicado "Programa Pena Justa", quando o correto é "Plano Pena Justa".
- O texto da Rede de Ouvidorias gerou preocupação por poder criar ruído com áreas internas e estados.
- A identidade visual do início da página continua pouco atrativa.
- A arte inicial foi considerada antiga.
- A prioridade é resolver sem inventar funcionalidades e respeitando a caixa de ferramentas do SENAPPEN/gov.br.

## Padrão técnico real observado no gov.br/SENAPPEN

Pela inspeção da página publicada e do DevTools, a página usa estrutura do gov.br/Plone, não uma aplicação front-end própria.

Classe principal observada no `body`:

```text
default-header-template portal-institucional cover-layout-layout-vazio template-view portaltype-collective-cover-content site-pt-br section-acesso-a-informacao subsection-participacao-social subsection-participacao-social-ouvidoria subsection-participacao-social-ouvidoria-ouvidoria-nacional-de-servicos-penais userrole-anonymous
```

Indícios de componentes/tile disponíveis observados no HTML:

- `cover-carousel-tile-swiper`
- `cover-richtext-tile`
- `cover-banner-tile`
- `cover-embed-tile`
- `tile-cards`
- `govbr-cards`
- `cards-4c`
- `card-flip`
- `govbr-card-content`

Portanto, qualquer melhoria deve ser formulada para esses componentes ou equivalentes da caixa de ferramentas da DCOM.

O HTML bruto da página foi analisado em 2026-05-07. Para preservar o padrão sem carregar um arquivo gigante, os detalhes úteis foram consolidados em `Documentação/inventario_estrutura_govbr_senappen.md`, incluindo recursos de tema, classes principais, IDs dos tiles e ordem da página publicada.

## Regra de ouro do projeto

Não propor nem implementar:

- JavaScript próprio.
- Biblioteca externa de ícones.
- Botão customizado.
- Card interativo fora do padrão disponível.
- Menu customizado.
- Layout de landing page.
- Hero promocional.
- CSS local como requisito para publicação.
- Placeholder de QR Code.
- Qualquer funcionalidade não existente no gov.br/SENAPPEN.

Pode usar:

- Título e subtítulos.
- Texto rico.
- Link simples.
- Banner/imagem institucional linkada.
- Imagem estática com legenda.
- Iframe, como mapa e Power BI.
- Card/link de subpágina no padrão gov.br.
- Página/subpágina simples com título, texto, links e documentos oficiais.

## Estado da página publicada em 2026-05-07

O que já foi publicado:

- H1: Ouvidoria.
- H2: Ouvidoria Nacional de Serviços Penais.
- Banner/carrossel com imagens antigas de WhatsApp e canais.
- Texto institucional atualizado.
- Seção Tipos de Manifestação com Banner 1.
- Seção Contato ainda presente.
- Banner 2 de Canais de Atendimento.
- Mapa em iframe.
- Cards de subpáginas.
- Plano de Metas 2026 com Banner 3.
- Relatório de Gestão.
- Painel Power BI.

Divergências observadas:

- Bloco antigo de contato permaneceu, embora a Nota Técnica tenha pedido remoção.
- Há conflito de telefone: Banner 2 usa (61) 3770-5039; texto antigo remanescente usa (61) 3770-5034.
- QR Code do chatbot ainda não aparece na página publicada.
- O card foi publicado como "Programa Pena Justa", mas deve ser "Plano Pena Justa".
- O card do SIDH foi publicado sem o acrônimo Ema visível.
- O texto da Rede de Ouvidorias deve ser suavizado para evitar ruído institucional.
- O texto da Revista removeu a menção "Em parceria com a Espen e a DCOM".
- As subpáginas existem, mas parecem pastas incompletas, com conteúdo mínimo e mensagem de pasta vazia.
- Imagens ricas em texto têm `alt` curto demais.
- Iframes de mapa e Power BI precisam de título acessível se a ferramenta permitir.

## Decisões já tomadas neste workspace

1. O protótipo local é apenas uma prévia de conteúdo e ordem, não implementação final.
2. O padrão a seguir é gov.br/SENAPPEN/Plone, usando os tiles observados.
3. O QR Code real deve ser publicado na seção Canais de Atendimento.
4. O QR original está em `Documentação/QRcode_Whatsapp.png`.
5. A prévia usa uma versão recortada em `prototipo-dicom-onasp/assets/qrcode-whatsapp-cortado.png` para melhorar apresentação local.
6. A redação da Rede de Ouvidorias foi ajustada para linguagem institucional neutra.
7. O card deve usar "Plano Pena Justa", não "Programa Pena Justa".
8. O card da Ema deve manter a identificação institucional visível como `EMA - SENAPPEN`.
9. Links de imagem devem ter link textual próximo quando possível, para acessibilidade.
10. O currículo do Ouvidor passou a integrar a homepage, abaixo do mapa de localização, precedido por um bloco horizontal de contato resumido e acompanhado de link para o PDF `Documentação/Curriculo_Joao_vitor_elpidio_Ferreira.pdf`.
11. A Rede de Ouvidorias deve permanecer estritamente pública e institucional: detalhes de curadoria interna usados para consolidar contatos não podem aparecer na interface.
12. Não publicar na página frases como "o diagnóstico registrou", "a resposta do diagnóstico informa", referências a respostas internas, nomes de servidores designados ou observações equivalentes; isso deve ficar apenas na documentação de apoio.
13. Os títulos da primeira seção das subpáginas temáticas foram simplificados por decisão editorial para `Renospen`, `O Plano` e `A Revista`, substituindo o rótulo genérico `Escopo desta subpágina`.
14. A subpágina da Renospen passou a incluir a seção `VI Encontro Nacional das Ouvidorias do Sistema Penal` logo abaixo de `Mapa interativo e destaque por UF`, com três banners em sequência: `Banner_Renospen_1.jpeg` em destaque e `Banner_Renospen_2.jpeg` e `Banner_Renospen_3.jpeg` abaixo.
15. Foi criada a minuta operacional `Documentação/minuta_atualizacao_sei_e_encaminhamento_dicom.md` para apoiar a atualização do Processo SEI e o encaminhamento consolidado das instruções e anexos à DICOM, com checklist final de conferência.

## Redações recomendadas

### Chamada curta de abertura

> Canal oficial da Senappen para escuta, transparência, participação social e encaminhamento de manifestações relacionadas aos serviços penais.

Uso recomendado: texto rico logo após o subtítulo da página, antes dos blocos visuais extensos.

### Rede de Ouvidorias

> Iniciativa do Plano Pena Justa voltada à cooperação federativa, à harmonização de procedimentos e ao fortalecimento da proteção de direitos no âmbito das Ouvidorias de Serviços Penais.

Motivo: preserva a finalidade da Rede sem expressões potencialmente sensíveis como "combate a irregularidades" e "eliminar isolamento".

### EMA - SENAPPEN

Título curto recomendado:

> EMA - SENAPPEN

Descrição:

> Espaço da Equipe de Monitoramento e Acompanhamento das decisões e deliberações do SIDH, dedicado a fortalecer o cumprimento das determinações do Sistema Interamericano de Direitos Humanos em face do sistema penal brasileiro.

### Plano Pena Justa

Título correto:

> Plano Pena Justa

Descrição:

> Ambiente dedicado integralmente ao Plano, que disponibiliza o acesso a cronogramas, documentos técnicos e relatórios de acompanhamento.

### Revista Brasileira de Execução Penal

> Em parceria com a Espen e a DCOM, a Onasp lança edição da Revista Brasileira de Execução Penal. Com o tema voltado à participação e transparência, a publicação reúne artigos e estudos que fortalecem o controle social e consolidam a Ouvidoria como ponte entre o Estado e a sociedade.

### Legenda do QR Code

> Chatbot da Onasp no WhatsApp. Aponte a câmera do celular para acessar o atendimento automatizado.

## Ordem recomendada para a DCOM

1. Título: Ouvidoria.
2. Subtítulo: Ouvidoria Nacional de Serviços Penais.
3. Chamada curta de abertura em texto rico.
4. Texto institucional da Nota Técnica 9.
5. Tipos de Manifestação: parágrafo + Banner 1 + link textual para Fala.BR.
6. Canais de Atendimento: Banner 2 + QR Code real com legenda.
7. Mapa de Localização.
8. Contato institucional resumido abaixo do mapa, com endereço, telefone e e-mail em linha.
9. Currículo do Ouvidor, com resumo profissional e link para o PDF.
10. Conteúdo Técnico e Projetos Estruturantes: cards/links de subpágina.
11. Plano de Metas 2026: texto + Banner 3.
12. Relatório de Gestão: texto + link simples destacado.
13. Painel de Tratamento de Demandas: texto + iframe Power BI.
14. Legislação: links simples para os normativos basilares efetivamente disponíveis na pasta documental, abaixo do painel.

## Pedido objetivo para a DCOM

Texto sugerido para encaminhamento:

> Solicito ajuste da página da ONASP mantendo exclusivamente os componentes disponíveis no gov.br/SENAPPEN. Pedimos substituir "Programa Pena Justa" por "Plano Pena Justa"; manter `EMA - SENAPPEN` visível no card do SIDH; substituir o texto da Rede de Ouvidorias pela redação institucional mais neutra encaminhada; inserir o QR Code oficial do chatbot na seção Canais de Atendimento, com legenda; manter abaixo do mapa um bloco de contato resumido com endereço, telefone e e-mail; incluir, abaixo desse bloco, o currículo do Ouvidor com resumo profissional e link para o PDF correspondente; incluir, abaixo do painel de tratamento de demandas, a seção `Legislação` com links simples para os normativos basilares efetivamente disponíveis no pacote documental; restaurar a menção "Em parceria com a Espen e a DCOM" no texto da Revista; e manter links textuais próximos às imagens clicáveis para melhorar acessibilidade. Não há solicitação de componente novo, JavaScript, biblioteca externa, botão customizado ou alteração fora da caixa de ferramentas do portal.

## Arquivos principais do workspace

- `Documentação/analise_dicom_onasp.md`: matriz do que foi pedido versus o que foi publicado.
- `Documentação/roteiro_publicacao_govbr_senappen.md`: roteiro técnico-editorial para a DCOM publicar no Plone/gov.br.
- `Documentação/melhorias_visuais_govbr_senappen.md`: melhorias visuais possíveis sem sair da caixa oficial.
- `Documentação/inventario_estrutura_govbr_senappen.md`: inventário técnico da estrutura Plone/gov.br observada no HTML publicado.
- `Documentação/comparativo_nota_tecnica_vs_pagina_dicom.md`: lista do que a DCOM deixou de incluir e das diferenças textuais em relação às Notas Técnicas 9 e 10.
- `Documentação/apontamentos_divergencias_notas_tecnicas_dcom.md`: versão formal dos apontamentos para subsidiar ofício de correção à DCOM.
- `Documentação/minuta_atualizacao_sei_e_encaminhamento_dicom.md`: minuta operacional pronta para atualização do Processo SEI e encaminhamento à DICOM.
- `Documentação/Curriculo_Joao_vitor_elpidio_Ferreira.pdf`: currículo completo do Ouvidor, agora referenciado na homepage.
- `Documentação/Normativas Basilares de Ouvidoria/`: pasta com os PDFs atualmente usados na nova seção `Legislação` da homepage.
- `Documentação/modelo_dados_canonico_cdm.md`: Modelo de Dados Canônico criado para reaproveitamento em projetos futuros.
- `Documentação/boas_praticas_para_outros_projetos.md`: base de boas práticas usada para orientar o CDM.
- `Documentação/QRcode_Whatsapp.png`: QR Code oficial recebido.
- `prototipo-dicom-onasp/index.html`: prévia local da página principal.
- `prototipo-dicom-onasp/styles.css`: CSS apenas para visualização local, não para envio à DCOM.
- `prototipo-dicom-onasp/assets/qrcode-whatsapp-cortado.png`: QR Code recortado para prévia local.
- `prototipo-dicom-onasp/subpaginas/`: prévias locais das subpáginas.
- `.github/agents/`: agentes especializados criados para ONASP, DCOM, publicação, UX gov.br e CDM.

## Estado do protótipo local

O protótipo local já foi ajustado para:

- Não usar script.
- Não usar `lucide`.
- Não usar botão customizado.
- Não usar placeholder de QR Code.
- Carregar quatro imagens: Banner 1, Banner 2, QR Code e Banner 3.
- Exibir cards como Rede de Ouvidorias, EMA - SENAPPEN, Plano Pena Justa e Revista Brasileira de Execução Penal.
- Usar nos links temáticos as imagens fiéis salvas em `Documentação/Botao_Renospen.png`, `Documentação/Botao_EMA.png`, `Documentação/Botao_PenaJusta.png` e `Documentação/Botao_RevistaBrasileira.png`.
- Aplicar às quatro subpáginas internas um cabeçalho simples com a imagem oficial correspondente, título consistente com a página principal e manutenção explícita da nota de pendência de conteúdo.
- Ter subpágina `plano-pena-justa.html`, não `programa-pena-justa.html`.

Validação realizada:

- VS Code não apontou erros nos arquivos de `Documentação` e `prototipo-dicom-onasp`.
- A prévia local carregou os banners e QR Code.
- Busca confirmou ausência de `<script`, `lucide`, `data-lucide`, `class="button` e `qr-placeholder` no protótipo.
- O Power BI retornou 401 na prévia local, por restrição do iframe externo; isso não altera o roteiro de publicação.

## Agentes criados

Agentes em `.github/agents/`:

- `onasp-orquestrador-pagina.agent.md`: coordena auditoria documental, UX gov.br, protótipo e CDM.
- `onasp-auditor-documentacao.agent.md`: compara notas técnicas, despachos, página publicada e divergências.
- `onasp-ux-govbr-dicom.agent.md`: revisa experiência institucional dentro do gov.br/DCOM.
- `onasp-publicador-prototipo.agent.md`: mantém protótipo estático compatível com a caixa gov.br/SENAPPEN.
- `onasp-arquiteto-cdm.agent.md`: orienta Modelo de Dados Canônico.

Regra importante já gravada nos agentes: não propor componente, biblioteca, botão, ícone, script ou funcionalidade fora da caixa de ferramentas do SENAPPEN/gov.br.

## Como outra IA deve continuar

1. Leia este diário primeiro.
2. Leia `Documentação/analise_dicom_onasp.md` para entender divergências.
3. Leia `Documentação/melhorias_visuais_govbr_senappen.md` para entender as melhorias visuais permitidas.
4. Leia `Documentação/inventario_estrutura_govbr_senappen.md` para entender os tiles e classes reais da página publicada.
5. Leia `Documentação/roteiro_publicacao_govbr_senappen.md` para transformar isso em demanda objetiva à DCOM.
6. Verifique a página publicada novamente antes de editar qualquer documento, pois a DCOM pode ter atualizado algo.
7. Não propor redesign fora do Plone/gov.br.
8. Não alterar o CDM salvo sem necessidade; ele é uma entrega paralela já consolidada.
9. Se for criar novo artefato, prefira Markdown em `Documentação/`.

## Próximo passo recomendado

Preparar um despacho/mensagem final para a DCOM com:

- lista de ajustes objetivos;
- arquivos anexos: QR Code, banners e textos revisados;
- justificativa curta de governança e acessibilidade;
- pedido explícito para manter a publicação dentro da caixa gov.br/SENAPPEN.

## Fechamento parcial em 2026-05-12

- Ajuste aplicado em `prototipo-dicom-onasp/subpaginas/ema-sidh.html`: o título da seção foi normalizado para `Institucional` e o banner `Documentação/Banner_Ema_Organograma.png` foi inserido logo abaixo do título.
- Ajuste aplicado em `prototipo-dicom-onasp/subpaginas/revista-brasileira-execucao-penal.html`: o bloco `Dossiê e atualizações em destaque` foi removido da versão local.
- Ajuste aplicado em `prototipo-dicom-onasp/subpaginas/rede-ouvidorias.html`, `prototipo-dicom-onasp/subpaginas/plano-pena-justa.html` e `prototipo-dicom-onasp/subpaginas/revista-brasileira-execucao-penal.html`: o primeiro título seccional foi renomeado, respectivamente, para `Renospen`, `O Plano` e `A Revista`.
- Ajuste aplicado em `prototipo-dicom-onasp/subpaginas/rede-ouvidorias.html`: foi criada a seção `VI Encontro Nacional das Ouvidorias do Sistema Penal`, com texto institucional e galeria de três imagens usando `Documentação/Banner_Renospen_1.jpeg`, `Documentação/Banner_Renospen_2.jpeg` e `Documentação/Banner_Renospen_3.jpeg` no mesmo arranjo visual adotado na página da EMA.
- Validação local concluída em 2026-05-12: VS Code não apontou erros em `prototipo-dicom-onasp/index.html`, `prototipo-dicom-onasp/styles.css`, `prototipo-dicom-onasp/subpaginas/ema-sidh.html` e `prototipo-dicom-onasp/subpaginas/revista-brasileira-execucao-penal.html`.
- Checagem adicional com PowerShell confirmou que todos os `src` e `href` internos dos HTML em `prototipo-dicom-onasp/` resolvem para arquivos existentes quando lidos em UTF-8 e com decodificação de URL.
- Limite desta validação: links externos, iframes remotos e o comportamento final no ambiente gov.br/DCOM não foram revalidados neste ciclo.
- Observação para retomada: o `git status` desta pasta continha também alterações não relacionadas em arquivos de `Documentação/`; elas não foram revertidas nem incorporadas a esta revisão.

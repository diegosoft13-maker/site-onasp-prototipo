# Protótipo gov.br/Plone da página ONASP para a DCOM

Este diretório contém uma prévia estática da ordem e do conteúdo desejados para a página da Ouvidoria Nacional de Serviços Penais. A intenção não é propor uma aplicação ou front-end customizado, mas demonstrar como o conteúdo deve ser organizado usando a mesma lógica da página atual no gov.br/SENAPPEN.

## Regra de compatibilidade

- Não usar biblioteca externa de ícones.
- Não propor JavaScript próprio como requisito para publicação na DCOM.
- Não criar botão, menu, controle, card interativo ou funcionalidade que não exista na caixa de ferramentas do SENAPPEN/gov.br.
- Usar somente componentes equivalentes aos já observados na página publicada: título, subtítulo, texto rico, imagem/banner linkado, iframe, link simples e card/link de subpágina.
- Tratar o CSS deste diretório apenas como ajuda visual local; ele não deve ser enviado como requisito de implementação para a DCOM.

## Como abrir

Abra `index.html` no navegador. O arquivo é apenas uma prévia local.

Prévia pública mais recente no GitHub Pages:

- Homepage: <https://diegosoft13-maker.github.io/site-onasp-prototipo/prototipo-dicom-onasp/index.html>
- Plano Pena Justa: <https://diegosoft13-maker.github.io/site-onasp-prototipo/prototipo-dicom-onasp/subpaginas/plano-pena-justa.html?v=037d4b8>

## Status desta versão

Snapshot validado em 2026-05-12.

- Subpágina da EMA revisada com o título da seção `Institucional` em capitalização normal e com o banner `Banner_Ema_Organograma.png` inserido abaixo do título.
- Subpágina da Revista revisada com remoção do bloco `Dossiê e atualizações em destaque`, conforme solicitação editorial.
- VS Code não apontou erros em `index.html`, `styles.css`, `subpaginas/ema-sidh.html` e `subpaginas/revista-brasileira-execucao-penal.html`.
- Validação local adicional confirmou que todos os `src` e `href` internos dos HTML em `prototipo-dicom-onasp/` resolvem para arquivos existentes.
- Esta validação cobre a prévia estática local. Links externos, embeds remotos e o comportamento final no ambiente gov.br/DCOM continuam dependentes da publicação real.

Atualização incremental em 2026-05-18.

- A seção `Normativos` deixou a homepage e passou a existir como a subpágina `subpaginas/normativos.html`, acessível por um novo card logo abaixo da subpágina da Revista.
- O card e a hero da nova subpágina passaram a usar a arte oficial `../Documentação/Botao_Normativos.png`.
- A tabela da nova subpágina foi reordenada para a sequência editorial: Lei nº 12.527/2011, Lei nº 13.460/2017, Lei nº 13.709/2018, Decreto nº 9.492/2018, Decreto nº 10.153/2019 e Portaria Normativa CGU nº 116/2024.
- As subpáginas `rede-ouvidorias.html`, `plano-pena-justa.html` e `revista-brasileira-execucao-penal.html` mantiveram os títulos curtos na hero e passaram a usar, no texto de abertura, as redações editoriais consolidadas para Renospen, Plano Pena Justa e Revista.
- Os cards da homepage para `Rede de Ouvidorias`, `Plano Pena Justa` e `Revista Brasileira de Execução Penal` foram alinhados às mesmas redações curtas aprovadas para as subpáginas correspondentes.
- A nota de prévia da homepage teve a grafia ajustada de `DCOM` para `Dcom`, conforme orientação editorial aplicada à interface local.
- VS Code não apontou erros em `index.html`, `styles.css` e `subpaginas/normativos.html`.
- Validação local adicional confirmou que todos os `src` e `href` internos dos HTML em `prototipo-dicom-onasp/` resolvem para arquivos existentes quando lidos em UTF-8 e com decodificação de URL.
- Validação local complementar, ainda em 2026-05-18, não apontou erros em `index.html`, `subpaginas/rede-ouvidorias.html`, `subpaginas/plano-pena-justa.html` e `subpaginas/revista-brasileira-execucao-penal.html` após os ajustes de redação.

Fechamento deste ciclo em 2026-05-19.

- O protótipo publicado do Plano Pena Justa foi estabilizado na revisão `037d4b8`, preservando a composição em quadro único com os nove recortes temáticos e o texto editorial consolidado da subpágina.
- A ação `Abrir quadro completo do Plano Pena Justa` passou a usar um modal apenas na prévia local/publicada do protótipo, com fechamento por clique fora da imagem, tecla `Esc` e botão dedicado.
- A ampliação do modal foi mantida como ajuste final do protótipo. A tentativa posterior de reduzir ainda mais o tamanho dos quadros foi revertida, de modo que o estado publicado voltou ao layout imediatamente anterior.
- A exceção de JavaScript existente hoje está restrita a esse modal do Plano Pena Justa e serve apenas para leitura do quadro completo no ambiente de validação. Ela não deve ser tratada como requisito para a publicação oficial no gov.br.
- O pacote documental de apoio para a DCOM ficou consolidado com `../Documentação/estrutura_completa_pagina_onasp_para_dicom.md` e `../Documentação/minuta_despacho_atualizado_dcom_2026-05-18.md`, além das respectivas versões `.docx` já presentes no workspace.

## Referências

- Página publicada da ONASP: <https://www.gov.br/senappen/pt-br/acesso-a-informacao/participacao-social/ouvidoria>
- Página de referência indicada: <https://www.gov.br/planejamento/pt-br/acesso-a-informacao/participacao-social/ouvidoria>
- Fala.BR: <https://falabr.cgu.gov.br>
- Processo SEI: 08016.009807/2026-98
- Análise comparativa: `../Documentação/analise_dicom_onasp.md`
- Comparativo Nota Técnica x página DCOM: `../Documentação/comparativo_nota_tecnica_vs_pagina_dicom.md`
- Apontamentos para ofício à DCOM: `../Documentação/apontamentos_divergencias_notas_tecnicas_dcom.md`
- Apontamentos em Word: `../Documentação/apontamentos_divergencias_notas_tecnicas_dcom.docx`
- Roteiro de publicação: `../Documentação/roteiro_publicacao_govbr_senappen.md`
- Estrutura editorial consolidada para a DCOM: `../Documentação/estrutura_completa_pagina_onasp_para_dicom.md`
- Minuta de despacho atualizada para a DCOM: `../Documentação/minuta_despacho_atualizado_dcom_2026-05-18.md`
- Melhorias visuais dentro da caixa gov.br/SENAPPEN: `../Documentação/melhorias_visuais_govbr_senappen.md`
- Inventário técnico da estrutura gov.br/SENAPPEN: `../Documentação/inventario_estrutura_govbr_senappen.md`
- Diário de bordo para retomada por outra IA: `../Documentação/diario_de_bordo_onasp.md`

## Pendências reais antes de enviar à DCOM

- Confirmar telefone oficial do banner de canais de atendimento.
- Publicar o QR Code oficial localizado em `../Documentação/QRcode_Whatsapp.png`, sem usar placeholder visual como publicação final.
- A prévia principal já usa os botões fiéis salvos em `../Documentação/Botao_Renospen.png`, `../Documentação/Botao_EMA.png`, `../Documentação/Botao_PenaJusta.png`, `../Documentação/Botao_RevistaBrasileira.png` e `../Documentação/Botao_Normativos.png`.
- As subpáginas locais também passaram a usar essas imagens em um cabeçalho visual simples, para manter coerência entre card e página temática.
- Revalidar conteúdo editorial final das cinco subpáginas e dos cards da homepage antes do envio à DCOM.
- Confirmar se o link dos relatórios deve apontar para PDF direto ou página agregadora.
- Validar acessibilidade dos banners ricos em texto e iframes no ambiente gov.br.
- Traduzir, na publicação oficial, o modal local do Plano Pena Justa para um recurso nativo do portal, como link simples para imagem ou bloco estático equivalente.

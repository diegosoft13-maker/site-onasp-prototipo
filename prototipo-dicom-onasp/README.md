# Protótipo gov.br/Plone da página ONASP para a DCOM

Este diretório contém uma prévia estática da ordem e do conteúdo desejados para a página da Ouvidoria Nacional de Serviços Penais. A intenção não é propor uma aplicação ou front-end customizado, mas demonstrar como o conteúdo deve ser organizado usando a mesma lógica da página atual no gov.br/SENAPPEN.

## Regra de compatibilidade

- Não usar biblioteca externa de ícones.
- Não criar JavaScript próprio.
- Não criar botão, menu, controle, card interativo ou funcionalidade que não exista na caixa de ferramentas do SENAPPEN/gov.br.
- Usar somente componentes equivalentes aos já observados na página publicada: título, subtítulo, texto rico, imagem/banner linkado, iframe, link simples e card/link de subpágina.
- Tratar o CSS deste diretório apenas como ajuda visual local; ele não deve ser enviado como requisito de implementação para a DCOM.

## Como abrir

Abra `index.html` no navegador. O arquivo é apenas uma prévia local.

## Referências

- Página publicada da ONASP: <https://www.gov.br/senappen/pt-br/acesso-a-informacao/participacao-social/ouvidoria>
- Página de referência indicada: <https://www.gov.br/planejamento/pt-br/acesso-a-informacao/participacao-social/ouvidoria>
- Fala.BR: <https://falabr.cgu.gov.br>
- Processo SEI: 08016.009807/2026-98
- Análise comparativa: `../Documentação/analise_dicom_onasp.md`
- Roteiro de publicação: `../Documentação/roteiro_publicacao_govbr_senappen.md`
- Melhorias visuais dentro da caixa gov.br/SENAPPEN: `../Documentação/melhorias_visuais_govbr_senappen.md`
- Inventário técnico da estrutura gov.br/SENAPPEN: `../Documentação/inventario_estrutura_govbr_senappen.md`
- Diário de bordo para retomada por outra IA: `../Documentação/diario_de_bordo_onasp.md`

## Pendências reais antes de enviar à DCOM

- Confirmar telefone oficial do banner de canais de atendimento.
- Publicar o QR Code oficial localizado em `../Documentação/QRcode_Whatsapp.png`, sem usar placeholder visual como publicação final.
- Validar conteúdo final das quatro subpáginas.
- Confirmar se o link dos relatórios deve apontar para PDF direto ou página agregadora.
- Validar acessibilidade dos banners ricos em texto e iframes no ambiente gov.br.

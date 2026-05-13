# Minuta operacional para atualização do Processo SEI e encaminhamento à DICOM

Data-base: 2026-05-12

Processo SEI: 08016.009807/2026-98

## Finalidade

Este documento foi preparado para servir como roteiro de execução e minuta de apoio ao registro das atualizações no Processo SEI e ao encaminhamento do pacote editorial consolidado para a DICOM, reduzindo o risco de omissões, envio de arte desatualizada, divergência de nomenclatura ou solicitação incompatível com o ambiente gov.br/SENAPPEN.

## Como usar este documento

1. Use a seção `Síntese executiva` para contextualizar rapidamente o estágio atual do trabalho.
2. Use a seção `Minuta sugerida para atualização no SEI` como texto-base para despacho, informação ou nota de encaminhamento.
3. Use a seção `Texto curto para encaminhamento à DICOM` se precisar de uma versão mais enxuta.
4. Use a seção `Relação de anexos` para conferir o que deve seguir nesta rodada e o que já consta no processo.
5. Use a seção `Checklist final antes da assinatura` imediatamente antes de concluir a movimentação no SEI.

## Síntese executiva

O pacote editorial da página da Ouvidoria Nacional de Serviços Penais e das subpáginas temáticas foi consolidado neste workspace, com documentação estruturada para publicação no ambiente gov.br/SENAPPEN, respeitando a caixa de ferramentas do Plone/gov.br e sem dependência de JavaScript próprio, CSS local ou componente customizado.

As correções e consolidações mais recentes contemplam:

- padronização de nomenclatura visível para `Onasp` e `Senappen`;
- manutenção de `EMA - SENAPPEN` como identificação institucional da subpágina temática correspondente;
- ajuste da subpágina da Rede de Ouvidorias para linguagem pública e institucional, sem exposição de notas de diagnóstico;
- tratamento do Espírito Santo com duas referências institucionais distintas na Rede de Ouvidorias;
- inclusão, na Renospen, da seção `VI Encontro Nacional das Ouvidorias do Sistema Penal` abaixo de `Mapa interativo e destaque por UF`, com `Banner_Renospen_1.jpeg` em destaque e `Banner_Renospen_2.jpeg` e `Banner_Renospen_3.jpeg` abaixo;
- remoção, nos rodapés visíveis da Renospen, dos textos `registro 1`, `registro 2` e `registro 3`;
- consolidação, na subpágina `EMA - SENAPPEN`, da seção institucional com organograma, da seção `Decisões do SIDH`, do bloco de curso vinculado ao Caso Pedrinhas e da restauração dos links da seção de referências públicas;
- inclusão, na homepage, de um bloco horizontal de contato resumido abaixo do mapa de localização e, abaixo dele, do `Currículo do Ouvidor`, com link para o PDF institucional correspondente;
- simplificação editorial dos títulos iniciais das subpáginas para `Renospen`, `O Plano` e `A Revista`;
- atualização da documentação estrutural e do artefato em DOCX que deve servir de peça principal para a DICOM.

Para rastreabilidade do protótipo e das últimas publicações no repositório de apoio, os commits finais validados foram:

- `604a117` - Padroniza textos e ajusta página da EMA.
- `0e559ba` - Atualiza legendas das fotos da EMA.
- `5b92546` - Renomeia seções e atualiza documentação.
- `b519d5b` - Adiciona encontro nacional na página Renospen.
- `8427634` - Restaura links da EMA e revalida Renospen.
- `5dbaf72` - Reorganiza seção VI Encontro da Renospen.

## Documentos-fonte que devem orientar a DICOM

Os documentos abaixo já estão prontos e organizados no workspace:

| Arquivo | Função | Uso recomendado |
| --- | --- | --- |
| `Documentação/estrutura_completa_pagina_onasp_para_dicom.docx` | Documento principal com a estrutura final da página principal e das subpáginas. | Encaminhar à DICOM como peça central desta rodada. |
| `Documentação/estrutura_completa_pagina_onasp_para_dicom.md` | Fonte editável do documento principal. | Manter como apoio interno e referência técnica. |
| `Documentação/apontamentos_divergencias_notas_tecnicas_dcom.docx` | Registro formal das divergências entre o pedido da ONASP e a publicação observada. | Encaminhar se for útil reforçar o histórico e as pendências. |
| `Documentação/roteiro_publicacao_govbr_senappen.md` | Roteiro operacional compatível com Plone/gov.br. | Usar como apoio interno ou encaminhar como complemento técnico, se necessário. |
| `Documentação/inventario_estrutura_govbr_senappen.md` | Inventário técnico da caixa de ferramentas real do portal. | Apoio interno; útil para conter pedidos inviáveis. |
| `Documentação/diario_de_bordo_onasp.md` | Memória operacional do trabalho. | Uso interno; não é o melhor anexo principal para a DICOM. |
| `Documentação/minuta_atualizacao_sei_e_encaminhamento_dicom.docx` | Minuta operacional desta rodada. | Usar como apoio para o trâmite do SEI e para conferência final. |

## Resultado editorial consolidado para encaminhamento

### Página principal da ONASP

- Manter a estrutura orientada pelas Notas Técnicas 9 e 10 e pelo documento `estrutura_completa_pagina_onasp_para_dicom.docx`.
- Usar as artes atualizadas `Banner_1_new.png`, `Banner_2_new.png` e `Banner_3_new.png`.
- Inserir o QR Code oficial `QRcode_Whatsapp.png` na seção de canais de atendimento.
- Inserir, abaixo do mapa de localização, um bloco horizontal de contato resumido com endereço, telefone e e-mail, seguido do `Currículo do Ouvidor` com link para `Curriculo_Joao_vitor_elpidio_Ferreira.pdf`.
- Não tratar o HTML local como instrução de implementação; a publicação final deve ocorrer com componentes nativos do gov.br.

### Rede de Ouvidorias

- O primeiro bloco deve permanecer com o título `Renospen`.
- O mapa interativo é uma referência de validação do protótipo; a publicação oficial pode usar seletor simples, quadro textual ou estrutura equivalente compatível com o gov.br.
- Quando a mesma UF tiver mais de uma referência institucional, como no Espírito Santo, as informações devem permanecer separadas por bloco ou por linha, sem fusão artificial de órgãos, responsáveis, telefones e endereços.
- A seção `VI Encontro Nacional das Ouvidorias do Sistema Penal` deve aparecer abaixo de `Mapa interativo e destaque por UF`.
- Os rodapés visíveis das três imagens dessa seção devem permanecer sem `registro 1`, `registro 2` e `registro 3`.

### EMA - SENAPPEN

- A subpágina deve preservar o título `EMA - SENAPPEN`.
- O organograma deve ficar na seção institucional, após o texto que o introduz e antes de `Frentes de Atuação`.
- A seção `Decisões do SIDH` deve permanecer com os links das subpáginas temáticas.
- No bloco relacionado ao Caso Pedrinhas, deve constar o curso `Sistema Penal e Tutela Internacional de Direitos Humanos`, com as três imagens de BA, DF e MA e suas legendas finais já definidas.
- A seção `Referências públicas do SIDH` deve manter os links e permanecer sem o texto introdutório removido na rodada final.

### Plano Pena Justa e Revista

- A primeira seção da subpágina do Plano deve permanecer com o título `O Plano`.
- A primeira seção da subpágina da Revista deve permanecer com o título `A Revista`.
- A redação da Revista deve preservar a articulação institucional com Espen, DCOM e Onasp, conforme consolidado no documento estrutural.

## Minuta sugerida para atualização no SEI

Texto-base sugerido:

> Encaminho, para atualização do Processo SEI nº 08016.009807/2026-98 e posterior adoção de providências pela DICOM, o pacote editorial consolidado referente à página da Ouvidoria Nacional de Serviços Penais no portal gov.br/SENAPPEN e às respectivas subpáginas temáticas.
>
> O material ora consolidado tem por objetivo alinhar a publicação institucional às Notas Técnicas 9/2026/ONASP/SENAPPEN/MJ e 10/2026/ONASP/SENAPPEN/MJ, bem como aos despachos já constantes dos autos, preservando integral compatibilidade com a caixa de ferramentas do ambiente gov.br/Plone e sem demandar JavaScript próprio, CSS local, componentes customizados ou soluções externas ao padrão do portal.
>
> Nesta rodada, o documento principal de referência para publicação passa a ser `estrutura_completa_pagina_onasp_para_dicom.docx`, acompanhado dos apontamentos de divergência já sistematizados e do conjunto de artes institucionais correspondentes. Entre os ajustes editoriais e estruturais consolidados, destacam-se: a padronização visível de `Onasp` e `Senappen`; a manutenção da identificação `EMA - SENAPPEN`; a correção do título `Plano Pena Justa`; a adequação pública e institucional da subpágina da Rede de Ouvidorias; o tratamento do Espírito Santo com duas referências institucionais distintas; a inclusão da seção `VI Encontro Nacional das Ouvidorias do Sistema Penal` abaixo de `Mapa interativo e destaque por UF`; a retirada, dos rodapés visíveis dessa seção, dos textos `registro 1`, `registro 2` e `registro 3`; a consolidação do organograma e da seção `Decisões do SIDH` na EMA; a inclusão, na homepage, de um bloco de contato resumido e do `Currículo do Ouvidor` abaixo do mapa; e a atualização das seções iniciais das subpáginas para `Renospen`, `O Plano` e `A Revista`.
>
> Solicita-se à DICOM que utilize o documento estrutural atualizado como peça orientadora da publicação, observando especialmente: i) a vedação de replicação literal do HTML/CSS do protótipo; ii) o uso exclusivo de componentes nativos disponíveis no gov.br/SENAPPEN; iii) a não publicação de observações internas de diagnóstico ou curadoria; iv) a preservação dos links textuais próximos às imagens sempre que o editor permitir; e v) a utilização das artes e denominações mais recentes encaminhadas nesta instrução.
>
> Registre-se, por fim, que os documentos SEI já existentes no processo permanecem como base histórica e normativa desta demanda, não sendo necessário reanexá-los quando já constarem dos autos, salvo entendimento diverso da unidade competente.

## Texto curto para encaminhamento à DICOM

Texto-base sugerido:

> Encaminho a versão consolidada do pacote editorial da ONASP para atualização da página institucional e das subpáginas temáticas no portal gov.br/SENAPPEN. Favor utilizar, como documento principal, o arquivo `estrutura_completa_pagina_onasp_para_dicom.docx`, observando os ajustes mais recentes de nomenclatura, ordem dos blocos, artes atualizadas, QR Code oficial, inclusão do currículo do Ouvidor na homepage e compatibilidade estrita com os componentes nativos do ambiente Plone/gov.br.

## Assunto sugerido para o registro ou encaminhamento

Sugestão de assunto:

`Atualização da página da ONASP e subpáginas temáticas - pacote editorial consolidado para a DICOM`

## Relação de anexos recomendada nesta rodada

### Documentos principais

- `Documentação/estrutura_completa_pagina_onasp_para_dicom.docx`
- `Documentação/minuta_atualizacao_sei_e_encaminhamento_dicom.docx`
- `Documentação/apontamentos_divergencias_notas_tecnicas_dcom.docx`

### Documentos de apoio interno

- `Documentação/estrutura_completa_pagina_onasp_para_dicom.md`
- `Documentação/roteiro_publicacao_govbr_senappen.md`
- `Documentação/inventario_estrutura_govbr_senappen.md`
- `Documentação/comparativo_nota_tecnica_vs_pagina_dicom.md`
- `Documentação/diario_de_bordo_onasp.md`

### Artes da página principal

- `Documentação/Banner_1_new.png`
- `Documentação/Banner_2_new.png`
- `Documentação/Banner_3_new.png`
- `Documentação/QRcode_Whatsapp.png`
- `Documentação/senappen_fachada.png`

### Documento complementar da página principal

- `Documentação/Curriculo_Joao_vitor_elpidio_Ferreira.pdf`

### Artes dos cards e entradas de subpágina

- `Documentação/Botao_Renospen.png`
- `Documentação/Botao_EMA.png`
- `Documentação/Botao_PenaJusta.png`
- `Documentação/Botao_RevistaBrasileira.png`

### Artes da subpágina Rede de Ouvidorias

- `Documentação/Banner_Renospen_1.jpeg`
- `Documentação/Banner_Renospen_2.jpeg`
- `Documentação/Banner_Renospen_3.jpeg`

### Artes da subpágina EMA - SENAPPEN

- `Documentação/Banner_Ema_Organograma.png`
- `Documentação/Banner_Ema.jpg`
- `Documentação/Banner_Ema_2.jpg`
- `Documentação/Banner_Curso_Bahia.jpg`
- `Documentação/Banner_Curso_DF.jpg`
- `Documentação/Banner_Curso_MA.jpg`

### Artes das páginas de decisões do SIDH

- `Documentação/Banner_Ema_Complexo_Curado.png`
- `Documentação/Banner_Ema_Complexo_pedrinhas.jpg`
- `Documentação/Banner_Ema_Instituto_Penal_Placido.jpg`
- `Documentação/Banner_Ema_Penitenciaria_Alfredo_Tranjan.png`
- `Documentação/Banner_Ema_Presidio_Evaristo.png`

## Documentos que já constam no processo ou devem ser apenas referenciados

Se os arquivos abaixo já estiverem juntados aos autos, a recomendação é apenas referenciá-los no texto do encaminhamento, sem duplicidade desnecessária:

- `Documentação/SEI_35385980_Nota_Tecnica_9.pdf`
- `Documentação/SEI_35385987_Nota_Tecnica_10.pdf`
- `Documentação/SEI_35386120_Despacho_453.pdf`
- `Documentação/SEI_35489551_Despacho_566.pdf`
- `Documentação/SEI_35491773_Despacho_486.pdf`

## O que não deve ser tratado como peça principal para a DICOM

- arquivos HTML do protótipo local;
- `prototipo-dicom-onasp/styles.css` como exigência de publicação;
- qualquer pedido para reproduzir JavaScript, comportamento interativo local ou solução fora da caixa do gov.br;
- observações de curadoria interna, diagnóstico ou memória operacional como se fossem conteúdo público.

## Checklist final antes da assinatura ou conclusão do andamento

- [ ] O número do processo confere com `08016.009807/2026-98`.
- [ ] O documento principal anexado para a DICOM é `estrutura_completa_pagina_onasp_para_dicom.docx`.
- [ ] A presente minuta em DOCX foi gerada e está disponível para uso interno da unidade.
- [ ] As artes anexadas ou referenciadas são as versões mais recentes, especialmente `Banner_1_new.png`, `Banner_2_new.png` e `Banner_3_new.png`.
- [ ] O QR Code oficial `QRcode_Whatsapp.png` foi incluído no pacote encaminhado.
- [ ] O currículo em PDF `Curriculo_Joao_vitor_elpidio_Ferreira.pdf` foi incluído ou referenciado no pacote encaminhado.
- [ ] A solicitação não pede implementação de HTML, CSS local, JavaScript próprio ou componente customizado.
- [ ] O texto usa `Onasp` e `Senappen` na redação visível, salvo nome oficial integral do órgão ou referência formal do documento.
- [ ] O texto deixa claro que a homepage deve exibir, abaixo do mapa, um bloco horizontal de contato resumido e, abaixo dele, o currículo do Ouvidor.
- [ ] O card e a subpágina da EMA aparecem como `EMA - SENAPPEN`.
- [ ] O texto usa `Plano Pena Justa`, nunca `Programa Pena Justa`.
- [ ] A subpágina da Rede de Ouvidorias mantém `Renospen` como primeira seção.
- [ ] O texto deixa claro que a seção `VI Encontro Nacional das Ouvidorias do Sistema Penal` deve ficar abaixo de `Mapa interativo e destaque por UF`.
- [ ] O texto deixa claro que os rodapés visíveis da Renospen não devem usar `registro 1`, `registro 2` ou `registro 3`.
- [ ] O texto deixa claro que observações internas de diagnóstico não podem aparecer na interface pública.
- [ ] O texto registra que o Espírito Santo possui duas referências institucionais distintas na Rede de Ouvidorias.
- [ ] O texto deixa claro que a seção `Referências públicas do SIDH` na EMA deve manter os links.
- [ ] O organograma da EMA foi mencionado como parte da seção institucional.
- [ ] A redação da Revista preserva a referência institucional à Espen, à DCOM e à Onasp, conforme consolidado.
- [ ] Foi feita leitura final para eliminar erro de digitação, inconsistência de nome de arquivo ou divergência de nomenclatura.

## Checklist após o envio

- [ ] Registrar o número do documento gerado no SEI para o novo despacho, informação ou encaminhamento.
- [ ] Registrar a data do encaminhamento à DICOM.
- [ ] Confirmar se as artes seguiram anexadas no próprio SEI ou por outro canal institucional referenciado no processo.
- [ ] Guardar, no histórico interno da unidade, qual foi o pacote efetivamente remetido nesta rodada.
- [ ] Se houver validação pela URL pública do protótipo, lembrar que o GitHub Pages pode servir versão em cache; em caso de dúvida, usar recarga forçada ou query string de cache-busting.

## Observações finais para evitar falhas frequentes

- Não encaminhar arte antiga quando houver correspondente `_new` já consolidada.
- Não usar o protótipo HTML como se fosse especificação de código a ser copiada no portal.
- Não reenviar, sem necessidade, PDFs SEI que já constam formalmente do processo.
- Não misturar, no mesmo bloco, dados de duas ouvidorias distintas de uma mesma UF.
- Não deixar a DICOM sem uma peça principal única; nesta rodada, a peça central deve ser `estrutura_completa_pagina_onasp_para_dicom.docx`.
- Não usar o diário de bordo como documento principal de instrução externa; ele deve permanecer como memória interna.

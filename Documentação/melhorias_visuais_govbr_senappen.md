# Melhorias visuais possíveis usando a caixa de ferramentas SENAPPEN/gov.br

Data: 2026-05-07

## Diagnóstico do diálogo

O problema apontado pelo Ouvidor não exige uma aplicação nova. A correção deve ser editorial e estrutural dentro do Plone/gov.br: reorganizar o início, corrigir nomes e textos sensíveis, publicar o QR Code real e evitar que a página pareça uma atualização parcial da versão antiga.

## Ações prioritárias

| Prioridade | O que ajustar | Componente permitido | Como melhora o visual sem inventar funcionalidade |
| --- | --- | --- | --- |
| Alta | Reorganizar o início da página | Título, subtítulo e texto rico | Começar com uma chamada institucional curta da ONASP antes de imagens extensas deixa a página mais limpa e menos dependente de arte antiga. |
| Alta | Corrigir "Programa Pena Justa" para "Plano Pena Justa" | Card/link de subpágina | Elimina divergência documental visível logo na área de projetos. |
| Alta | Reescrever o resumo da Rede de Ouvidorias | Card/link de subpágina + texto rico | Troca formulações com potencial de ruído por linguagem institucional: cooperação federativa, harmonização de procedimentos e proteção de direitos. |
| Alta | Inserir o QR Code real do chatbot | Imagem estática com legenda | Resolve a pendência indicada pela DCOM sem placeholder e dá presença visual concreta à seção de canais. |
| Média | Usar título institucional no card da Ema | Card/link de subpágina | `EMA - SENAPPEN` preserva a identificação institucional e deixa a explicação do SIDH para a descrição. |
| Média | Trocar links de imagem vazios por texto próximo | Texto rico com link simples | Mantém a imagem clicável, mas adiciona link textual acessível para Fala.BR. |
| Média | Manter mapa e Power BI com títulos acessíveis | Iframe | Melhora leitura por tecnologia assistiva sem alterar o componente. |
| Média | Remover bloco textual antigo de contato | Texto rico | Evita duplicidade e conflito de telefone com o Banner 2. |

## Ordem recomendada para a página principal

1. Título: Ouvidoria.
2. Subtítulo: Ouvidoria Nacional de Serviços Penais.
3. Chamada curta em texto rico: "Canal oficial da Senappen para escuta, transparência, participação social e encaminhamento de manifestações relacionadas aos serviços penais."
4. Texto institucional da Nota Técnica 9.
5. Tipos de Manifestação: parágrafo + Banner 1 + link textual para Fala.BR.
6. Canais de Atendimento: Banner 2 + QR Code real do WhatsApp com legenda.
7. Mapa de Localização.
8. Conteúdo Técnico e Projetos Estruturantes: cards/links de subpágina.
9. Plano de Metas 2026: texto + Banner 3.
10. Relatório de Gestão: texto + link simples destacado.
11. Painel de Tratamento de Demandas: texto + iframe Power BI.

## Redações ajustadas para reduzir ruído

### Rede de Ouvidorias

Texto recomendado:

> Iniciativa do Plano Pena Justa voltada à cooperação federativa, à harmonização de procedimentos e ao fortalecimento da proteção de direitos no âmbito das Ouvidorias de Serviços Penais.

Motivo: preserva a ideia de articulação nacional sem usar expressões que possam soar acusatórias ou gerar ruído com Estados e áreas parceiras.

### Plano Pena Justa

Título recomendado:

> Plano Pena Justa

Motivo: corrige a divergência apontada no diálogo e alinha o card ao nome institucional do plano.

### EMA - SENAPPEN

Título recomendado para card:

> EMA - SENAPPEN

Descrição recomendada:

> Espaço da Equipe de Monitoramento e Acompanhamento das decisões e deliberações do SIDH, dedicado a fortalecer o cumprimento das determinações do Sistema Interamericano de Direitos Humanos em face do sistema penal brasileiro.

Motivo: mantém o acrônimo Ema exigido nos documentos, mas evita um card visualmente pesado.

## QR Code

Arquivo localizado:

- `Documentação/QRcode_Whatsapp.png`

Versão local recortada para prévia:

- `prototipo-dicom-onasp/assets/qrcode-whatsapp-cortado.png`

Na publicação oficial, a DCOM pode subir a imagem original ou uma versão recortada, usando componente de imagem estática com legenda. Não há necessidade de script, botão, plugin ou funcionalidade adicional.

Legenda sugerida:

> Chatbot da Onasp no WhatsApp. Aponte a câmera do celular para acessar o atendimento automatizado.

## O que pedir à DCOM

- Substituir "Programa Pena Justa" por "Plano Pena Justa" no card e na subpágina.
- Renomear o card "Sistema Interamericano de Direitos Humanos" para `EMA - SENAPPEN`.
- Substituir o texto da Rede de Ouvidorias pela redação institucional mais neutra.
- Inserir o QR Code real na seção de Canais de Atendimento.
- Remover o bloco antigo de contato que conflita com o Banner 2.
- Manter as imagens/banner como componentes oficiais do gov.br, mas incluir links textuais próximos para acessibilidade.

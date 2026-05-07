# Documento — Boas Práticas Para Outros Projetos

## Metadados

- Versão: v2026.05
- Última atualização: 2026-05-06
- Autor: GitHub Copilot (GPT-5.4)
- Status: Revisado
- Audiência: equipes humanas, agentes de IA e mantenedores técnicos
- Referência de origem: lições extraídas do projeto Painel_maturidade

## Objetivo

Consolidar, em linguagem simples, os padrões que funcionaram, os erros que custaram tempo e os comportamentos que devem ser reaproveitados em outros projetos para evitar retrabalho, regressão e diagnósticos ruins.

## Princípio central

Sempre separar quatro coisas:

1. o que o produto faz;
2. onde o estado dele é salvo;
3. como ele é operado em ambiente real;
4. como uma pessoa ou uma IA futura vai retomar o trabalho.

Quando essas quatro camadas se misturam, os erros ficam difíceis de explicar e fáceis de repetir.

## Boas práticas que devem virar padrão

### 1. Separar fonte oficial de dados e estado operacional

- Faça: manter a fonte oficial de dados em modo leitura e salvar o progresso operacional em outra camada.
- Evite: escrever diretamente na base de origem quando ela também serve como referência institucional.
- Por quê: isso reduz risco de corrupção da base e facilita auditoria.
- Exemplo da jornada: a planilha base permaneceu preservada enquanto o painel salvou seu estado em JSON local.

### 2. Validar o ambiente real antes de fixar porta, host ou processo de subida

- Faça: testar porta, bind e forma de execução na máquina real antes de assumir defaults.
- Evite: hardcode de `127.0.0.1`, `8080` ou dependência exclusiva de um terminal interativo.
- Por quê: o ambiente operacional quase sempre tem restrições próprias.
- Exemplo da jornada: foi preciso trocar `8080` por `8090` e depois trocar o bind local por `0.0.0.0`.

### 3. Em Windows corporativo, sempre oferecer um caminho operacional sem depender de PowerShell livre

- Faça: disponibilizar lançadores `.cmd` quando o fluxo precisa sobreviver a políticas de execução restritivas.
- Evite: assumir que `.ps1` sempre vai poder rodar.
- Por quê: política de execução é um bloqueio comum em ambiente institucional.
- Exemplo da jornada: os `.ps1` foram bloqueados e os `.cmd` viraram o caminho recomendado.

### 4. Diferenciar erro de código de erro de infraestrutura

- Faça: identificar rapidamente se a falha está no app, no provedor externo, no firewall, na rede ou no ambiente.
- Evite: gastar esforço em refatoração quando o gargalo está fora do código.
- Por quê: isso reduz retrabalho e evita “consertos falsos”.
- Exemplo da jornada: o bloqueio de e-mail veio do SMTP AUTH desabilitado no provedor, não do algoritmo de envio.

### 5. Em UI construída com loops, capturar explicitamente o contexto do callback

- Faça: bindar no callback os controles ou valores da linha atual.
- Evite: depender de variáveis de loop soltas em funções internas.
- Por quê: fechamentos tardios geram bugs silenciosos, especialmente em telas administrativas.
- Exemplo da jornada: o erro de promoção de administrador veio exatamente desse padrão incorreto.

### 6. Confirmar valor persistido e valor efetivo em memória

- Faça: quando houver dúvida de permissão, sessão ou perfil, verifique tanto o armazenamento quanto a projeção usada pelo app.
- Evite: confiar só no que a interface parece mostrar.
- Por quê: muitos bugs nascem na passagem entre persistência e uso efetivo.
- Exemplo da jornada: o caso do Paulo só ficou claro quando `data/users.json` e `get_user()` foram comparados.

### 7. Não confundir processo antigo com código novo

- Faça: sempre verificar o processo realmente escutando a porta antes de concluir que o código “não mudou nada”.
- Evite: diagnosticar regressão visual sem conferir qual processo está servindo a URL.
- Por quê: instâncias antigas mascaram o estado real do projeto.
- Exemplo da jornada: parte das percepções de falha vinham de um servidor anterior ainda em execução.

### 8. Tratar documentação como parte do produto

- Faça: manter índice, referência técnica, runbook, manual e diário de bordo.
- Evite: depender apenas da memória da equipe ou do histórico difuso do chat.
- Por quê: retomada técnica sem documentação custa caro e produz erros repetidos.
- Exemplo da jornada: a documentação precisou ser reconstruída quando o painel já tinha evoluído bastante.

### 9. Registrar erros com causa, não só com sintoma

- Faça: documentar “o que falhou”, “por que falhou”, “como foi corrigido” e “como detectar de novo”.
- Evite: notas do tipo “deu erro”, sem contexto reproduzível.
- Por quê: a ausência da causa obriga a equipe a reaprender a mesma lição.
- Exemplo da jornada: bind local, política de PowerShell, SMTP AUTH e fechamento tardio foram erros diferentes e precisavam de causas distintas.

### 10. Usar feature flag para reduzir superfície quando a dependência externa ainda não está pronta

- Faça: esconder ou neutralizar uma funcionalidade incompleta, mantendo a base técnica pronta para retorno.
- Evite: expor interface operacional para algo que ainda falha sistematicamente.
- Por quê: isso preserva confiança do usuário e evita ruído de suporte.
- Exemplo da jornada: os e-mails ficaram ocultos até a infraestrutura externa ser resolvida.

### 11. Produzir validação executável, mesmo quando não há suíte de testes

- Faça: manter smoke tests curtos e repetíveis para carga, autenticação, geração de artefato e acesso.
- Evite: concluir que “está tudo certo” só por leitura do código.
- Por quê: comportamento real sempre vale mais que suposição.
- Exemplo da jornada: carga da matriz, exportação PDF, acesso em rede e perfil administrativo foram validados com execução real.

### 12. Declarar os riscos remanescentes em vez de fingir que o projeto está fechado

- Faça: deixar explícito o que ainda é frágil, manual ou dependente de outro time.
- Evite: encerrar a documentação com tom de completude falsa.
- Por quê: transparência técnica reduz surpresa operacional.
- Exemplo da jornada: concorrência em JSON, firewall local e SMTP externo continuam sendo pontos sensíveis.

## Checklist reutilizável para novos projetos

- A fonte oficial de dados está separada do estado operacional?
- Existe um caminho de partida e parada que não depende do editor?
- A aplicação foi validada na porta e no host do ambiente real?
- Há distinção clara entre falha de código e falha de infraestrutura?
- Callbacks de UI dentro de loops capturam contexto de forma segura?
- Existe verificação do valor persistido e do valor efetivo em memória?
- O projeto tem runbook, manual, diário e documentação técnica mínima?
- Há pelo menos um conjunto de smoke tests de operação real?
- Os riscos remanescentes estão documentados com clareza?

## Erros que não devemos repetir

- Assumir que localhost basta quando o produto precisa funcionar na rede.
- Assumir que PowerShell institucional vai aceitar scripts sem bloqueio.
- Assumir que uma interface administrativa gravou o dado certo sem conferir a persistência.
- Assumir que erro de integração externa sempre é defeito do código.
- Assumir que documentação pode ficar para o fim sem custo.

## Fórmula prática para futuras IAs e equipes

Quando surgir um erro, siga esta ordem:

1. confirmar o sintoma com uma checagem executável;
2. localizar onde o valor nasce, onde é salvo e onde é consumido;
3. separar erro de lógica, erro de processo ativo, erro de ambiente e erro externo;
4. corrigir a causa mais próxima do problema real;
5. validar de novo no mesmo fluxo que falhou;
6. registrar a causa e a correção em linguagem simples.

## Encerramento

Se este arquivo for levado para outro projeto, a regra mais importante é esta: nunca trate um incidente apenas como algo a apagar. Trate como algo a transformar em padrão, documentação e checagem reaproveitável.

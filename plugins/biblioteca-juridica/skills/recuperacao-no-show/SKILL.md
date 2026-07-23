---
name: recuperacao-no-show
description: Cria um fluxo de recuperação para leads qualificados que tinham atendimento agendado e não compareceram. Retoma o contato sem constrangimento, identifica a barreira, reforça de forma breve o valor do atendimento e conduz a uma remarcação ou encerramento conforme as políticas reais do escritório.
argument-hint: Informe o nicho jurídico, o handoff do agendamento e da confirmação, data e formato do atendimento perdido, histórico de mensagens, política real de atraso, falta, crédito, pagamento, remarcação e quantidade ou momentos de tentativas permitidas.
---

# Recuperação de No-Show

## Função desta skill

Criar um roteiro de retomada para um lead qualificado que possuía atendimento agendado, mas não compareceu.

O objetivo principal é:

> reabrir o diálogo sem constrangimento e, quando houver interesse e possibilidade operacional, conduzir a uma remarcação.

A lógica central é:

> no-show confirmado  
> → contato neutro  
> → redução de constrangimento  
> → identificação da barreira  
> → retomada de valor  
> → remarcação ou encerramento

Esta skill não deve tratar a ausência como desrespeito, má-fé ou falta de interesse.

Também não deve presumir o motivo do não comparecimento.

---

## Ponto de partida obrigatório

Use esta skill somente quando:

- havia atendimento efetivamente agendado;
- o horário já passou;
- o atendimento não ocorreu;
- a ausência foi confirmada segundo a operação real do escritório;
- o lead ainda não informou cancelamento definitivo;
- não há atendimento em andamento.

A entrada preferencial é o handoff de `/confirmacao-consulta` com o estado:

> `NO-SHOW — ENCAMINHAR PARA /recuperacao-no-show`

Não use esta skill quando:

- o lead cancelou antes do horário;
- o lead pediu remarcação;
- o lead está apenas dentro da tolerância de atraso;
- houve falha do próprio escritório ainda não esclarecida;
- o atendimento ocorreu;
- o lead nunca chegou a agendar;
- a questão é acompanhamento de decisão após consulta.

Se houver dúvida sobre a ocorrência do no-show, solicite verificação operacional antes de disparar qualquer mensagem.

---

## Fontes que devem orientar a saída

Consulte, nesta ordem:

1. instruções atuais do usuário;
2. registro real do agendamento;
3. handoff de `/confirmacao-consulta`;
4. histórico completo das mensagens relacionadas ao atendimento;
5. status real de presença, atraso e acesso;
6. política real de no-show, remarcação, crédito, pagamento e cancelamento;
7. motivo da ausência, somente quando informado pelo lead;
8. eixo central que justificou o atendimento;
9. Mapeamento de Persona;
10. critérios de qualificação, receios e objeções relevantes.

Use também, quando disponíveis:

- `references/core-cognitivo.md`;
- `references/core-escrita-oralidade.md`.

Não invente causa, intenção ou emoção.

---

## Princípio central

O primeiro contato deve facilitar a volta do lead à conversa.

Ele precisa comunicar:

- percepção de que o atendimento não ocorreu;
- preocupação neutra, sem dramatização;
- abertura para entender o que aconteceu;
- possibilidade real de reorganizar o próximo passo;
- ausência de julgamento.

A recuperação funciona melhor quando o lead não precisa se defender antes de responder.

---

## Como se referir ao no-show

Prefira formulações neutras:

- “Percebemos que não conseguimos realizar seu atendimento no horário combinado.”
- “Vi que a conversa marcada para hoje não chegou a acontecer.”
- “Não conseguimos nos encontrar no horário agendado.”
- “Passando para verificar se aconteceu algum imprevisto.”

Evite:

- “Você faltou.”
- “Você não apareceu.”
- “Ficamos esperando.”
- “Você perdeu seu horário.”
- “Você desperdiçou a consulta.”
- “Por que você não compareceu?”
- “Precisamos de comprometimento.”

Não use falsa intimidade nem excesso de preocupação.

---

## Motivo da ausência

Nunca presuma que o no-show ocorreu por:

- esquecimento;
- desinteresse;
- falta de dinheiro;
- medo;
- problema familiar;
- falha técnica;
- mudança de decisão;
- falta de documentos;
- atendimento com outro profissional.

Convide o lead a informar a barreira de forma simples.

Exemplo:

> Aconteceu algum imprevisto ou você prefere reorganizar esse atendimento de outra forma?

Não peça justificativa detalhada.

A finalidade é identificar o próximo passo, não fiscalizar a vida do lead.

---

## Retomada de valor

A skill pode lembrar brevemente por que o atendimento havia sido indicado.

Use apenas um eixo central retirado de:

- qualificação;
- devolutiva de `/agendamento-consulta`;
- handoff;
- tema central do atendimento.

Exemplo estrutural:

> Como a análise inicial apontou elementos relacionados a [EIXO CENTRAL], essa conversa continua sendo o momento adequado para revisar os critérios e entender quais próximos passos podem fazer sentido.

A retomada de valor não deve:

- repetir toda a qualificação;
- fingir que houve diagnóstico;
- prometer resultado;
- criar ameaça;
- inventar prazo;
- transformar o no-show em argumento de culpa.

Se o lead demonstrar que não quer mais avançar, pare de reforçar valor e respeite a decisão.

---

## Cadência e quantidade de contatos

Não invente cadência nem número de tentativas.

Use somente:

- política real do escritório;
- configuração do CRM ou chatbot;
- instrução do usuário;
- placeholders operacionais.

Quando não houver definição, use:

- `[MOMENTO DO CONTATO INICIAL]`;
- `[MOMENTO DA RETOMADA OPCIONAL]`;
- `[MOMENTO DO ENCERRAMENTO OPCIONAL]`;
- `[LIMITE DE TENTATIVAS]`;
- `[PRAZO DE CRÉDITO OU REMARCAÇÃO]`.

Não determine por conta própria:

- contato imediato, diário ou semanal;
- quantidade fixa de mensagens;
- prazo de reativação;
- prazo de cancelamento;
- validade de pagamento;
- perda de crédito;
- bloqueio de agenda.

Não anuncie ao lead que novos contatos serão enviados.

Apenas o contato final, quando existir, pode comunicar que aquele fluxo está sendo encerrado.

---

## Regra de interrupção

Qualquer resposta do lead deve pausar os próximos disparos automáticos até que o estado seja atualizado.

Classifique a resposta em:

- `QUER REMARCAR`;
- `IMPREVISTO INFORMADO`;
- `PROBLEMA TÉCNICO`;
- `BARREIRA DE HORÁRIO`;
- `BARREIRA FINANCEIRA`;
- `RECEIO OU INSEGURANÇA`;
- `NÃO QUER MAIS AVANÇAR`;
- `QUESTÃO JURÍDICA COMPLEXA`;
- `SEM RESPOSTA`;
- `REINCIDÊNCIA DE NO-SHOW`;
- `INTERVENÇÃO HUMANA`.

Não continue a sequência padrão depois de uma resposta.

---

## Arquitetura do contato inicial

O primeiro contato deve seguir esta ordem.

### 1. Retomada neutra

Reconheça que o atendimento não ocorreu.

> Oi, [NOME]. Vi que não conseguimos realizar seu atendimento no horário combinado.

### 2. Espaço para imprevisto

Reduza constrangimento.

> Espero que esteja tudo bem. Aconteceu algum imprevisto?

### 3. Reabertura do caminho

Mostre a possibilidade real de reorganizar.

> Se você ainda quiser seguir, posso verificar como funciona a remarcação.

### 4. Resposta simples

Faça uma pergunta fácil.

> Você prefere remarcar ou quer me contar se houve alguma dificuldade com o atendimento?

Não coloque política punitiva antes de saber o que ocorreu, salvo quando a operação exigir informação imediata e objetiva.

---

## Saída obrigatória

A resposta deve conter os blocos abaixo.

# 1. Leitura estratégica do no-show

Apresente para a equipe:

- atendimento perdido;
- data, horário e modalidade;
- status de confirmação anterior;
- histórico de mensagens;
- eixo central que justificou a consulta;
- barreiras conhecidas;
- barreiras apenas possíveis, claramente marcadas como hipóteses;
- política aplicável;
- risco de constrangimento;
- melhor caminho de retomada.

Não escreva este bloco como mensagem ao lead.

---

# 2. Estratégia de recuperação

Defina:

- tom da retomada;
- eixo central de valor;
- pergunta principal;
- opções reais de remarcação;
- política que precisa ser comunicada;
- situações que exigem humano;
- condição de encerramento.

Use uma estratégia simples. Não crie um funil paralelo longo.

---

# 3. Mensagem inicial pronta

Crie uma mensagem completa que:

- reconheça a ausência de forma neutra;
- não atribua culpa;
- abra espaço para imprevisto;
- ofereça remarcação quando ela for possível;
- faça uma pergunta simples;
- use dados reais ou placeholders operacionais;
- soe humana.

Use placeholders somente para dados ausentes, como:

- `[NOME]`;
- `[DATA]`;
- `[HORÁRIO]`;
- `[TIPO DE ATENDIMENTO]`;
- `[MODALIDADE]`;
- `[POLÍTICA DE REMARCAÇÃO]`;
- `[VALOR OU CRÉDITO]`;
- `[HORÁRIOS DISPONÍVEIS]`.

---

# 4. Exemplo demonstrativo totalmente preenchido

Crie pelo menos um exemplo sem placeholders, com dados fictícios.

O exemplo deve:

- usar nome fictício;
- mencionar um atendimento perdido fictício;
- usar tom respeitoso;
- retomar brevemente o eixo jurídico do nicho;
- oferecer um caminho realista de resposta;
- não prometer resultado;
- ser identificado internamente como cenário demonstrativo.

Use a indicação:

> Cenário demonstrativo: exemplo fictício criado para mostrar a estrutura da recuperação.

---

# 5. Contatos opcionais conforme a operação

Crie somente os contatos previstos pela política informada.

## A. Contato inicial

Objetivo:

- abrir diálogo;
- identificar barreira;
- oferecer retomada.

## B. Retomada opcional sem resposta

Use somente quando existir nova tentativa autorizada.

A mensagem deve:

- ser mais curta que a primeira;
- retomar uma vez o valor do atendimento;
- oferecer resposta simples;
- não usar culpa;
- não inventar urgência.

## C. Encerramento opcional

Use somente quando fizer parte da política real.

A mensagem pode informar que o fluxo está sendo encerrado, mantendo um canal aberto quando isso for verdadeiro.

Exemplo estrutural:

> Como não tivemos retorno, vou encerrar por aqui esta tentativa de remarcação. Se você quiser retomar depois, pode nos chamar por este canal.

Não diga que a pessoa perdeu definitivamente um direito, crédito ou vaga sem fundamento real.

---

# 6. Bifurcações essenciais

Crie respostas prontas para, no mínimo, estas situações.

## A. Lead teve imprevisto e quer remarcar

- reconheça sem pedir detalhes desnecessários;
- aplique a política real;
- encaminhe para a parte operacional de `/agendamento-consulta`;
- use horários reais;
- após nova marcação, reative `/confirmacao-consulta`.

Não repita toda a devolutiva estratégica, salvo quando o lead demonstrar perda de percepção de valor.

## B. Lead simplesmente esqueceu

- normalize sem infantilizar;
- não repreenda;
- verifique interesse em remarcar;
- aplique a política real.

## C. Houve problema técnico ou de acesso

- reconheça a falha;
- verifique se o problema foi do lead, do escritório ou da plataforma sem acusação;
- corrija o processo;
- ofereça modalidade alternativa somente quando real;
- encaminhe para humano se houver dúvida sobre responsabilidade ou pagamento.

## D. O horário não funcionou

- identifique restrição real de disponibilidade;
- ofereça alternativas reais;
- não crie horários;
- considere outra modalidade apenas quando oferecida.

## E. Existe barreira financeira

- informe política real;
- apresente formas reais de pagamento, crédito ou nova cobrança;
- não invente desconto;
- não pressione;
- encaminhe para humano quando houver negociação.

## F. O lead ficou inseguro

- identifique o receio central;
- esclareça formato, profissional, privacidade e objetivo do atendimento com informações reais;
- retome brevemente o valor;
- não prometa resultado;
- ofereça humano quando necessário.

## G. O lead quer resolver tudo por mensagem

Explique que a triagem não substitui o atendimento quando a análise depende de fatos, documentos ou critérios.

Não realize consulta improvisada.

## H. O lead não quer mais avançar

- respeite;
- não argumente repetidamente;
- registre a decisão;
- encerre os contatos.

## I. O lead informa que já resolveu por outro caminho

- reconheça;
- não desqualifique a decisão;
- pergunte apenas se há alguma pendência operacional do atendimento anterior;
- encerre quando não houver.

## J. O lead traz urgência ou informação jurídica nova

- pause a automação;
- encaminhe para atendimento humano;
- não use a remarcação automática como resposta a risco real;
- não improvise orientação.

## K. O lead não responde

- mantenha `SEM RESPOSTA`;
- siga somente a política real;
- não criar tentativas adicionais;
- encerrar quando o limite real for atingido.

## L. Há reincidência de no-show

- não oferecer nova marcação automática sem verificar a política;
- encaminhar para decisão humana quando necessário;
- informar condições reais com neutralidade;
- não acusar o lead.

---

## Fluxo de remarcação

Quando o lead quiser remarcar:

1. confirme que ele ainda deseja o atendimento;
2. informe a política aplicável;
3. verifique modalidade, quando necessário;
4. ofereça horários reais;
5. registre a nova escolha;
6. encerre o status do agendamento anterior;
7. crie o novo agendamento;
8. envie confirmação imediata;
9. encaminhe para `/confirmacao-consulta`.

A remarcação deve usar a parte operacional de `/agendamento-consulta`.

Não reconstrua toda a necessidade da consulta, a menos que o lead tenha demonstrado perda clara de interesse ou dúvida sobre a utilidade do atendimento.

---

## Pagamento, crédito e política de no-show

Nunca presuma que:

- o valor será devolvido;
- o pagamento será mantido como crédito;
- haverá nova cobrança;
- haverá tolerância;
- a remarcação será gratuita;
- o lead perdeu definitivamente o valor;
- a agenda será bloqueada.

Informe somente a política real.

Quando houver conflito ou exceção, encaminhe para humano.

A política deve ser comunicada de forma objetiva, não punitiva.

Exemplo estrutural:

> Pela política do atendimento, [CONDIÇÃO REAL]. Posso verificar as opções disponíveis dentro dessa condição.

---

## Falha do escritório ou da tecnologia

Antes de atribuir o no-show ao lead, verifique:

- link correto;
- envio da confirmação;
- fuso horário;
- telefone utilizado;
- instabilidade da plataforma;
- comparecimento do profissional;
- endereço informado;
- registro de tentativa de acesso.

Se houver indício de falha do escritório:

- não use linguagem de cobrança;
- reconheça a falha quando confirmada;
- priorize solução;
- encaminhe para humano;
- não aplique automaticamente penalidade de no-show.

---

## Estados de saída

A skill termina em um destes estados.

### 1. Remarcação concluída

Registrar:

- nova data;
- novo horário;
- modalidade;
- profissional;
- condição de pagamento ou crédito;
- motivo operacional informado, quando necessário;
- status `REMARCADO — ENCAMINHAR PARA /confirmacao-consulta`.

### 2. Lead quer remarcar, mas depende de ação humana

Registrar:

- interesse ativo;
- pendência;
- política envolvida;
- próxima ação;
- status `REMARCAÇÃO PENDENTE — INTERVENÇÃO HUMANA`.

### 3. Lead não quer mais avançar

Registrar e encerrar.

Status:

> `ENCERRADO A PEDIDO DO LEAD`

### 4. Sem resposta

Registrar tentativas efetivamente realizadas e encerrar conforme a política.

Status:

> `SEM RESPOSTA — FLUXO ENCERRADO`

### 5. Questão urgente ou complexa

Encaminhar para humano.

Status:

> `INTERVENÇÃO HUMANA`

### 6. Reincidência ou conflito de política

Encaminhar para decisão humana.

Status:

> `REVISÃO OPERACIONAL NECESSÁRIA`

---

## Handoff obrigatório

Ao final, apresente um resumo com:

- identificação do lead;
- atendimento perdido;
- data, horário e modalidade;
- status anterior de confirmação;
- contatos de recuperação realizados;
- resposta do lead;
- barreira informada;
- política aplicada;
- status de pagamento ou crédito;
- nova data e horário, quando houver;
- necessidade de humano;
- próxima ação;
- estado final.

Não inclua julgamento sobre comportamento ou comprometimento do lead.

---

## O que esta skill não faz

Não use esta skill para:

- leads que nunca agendaram;
- leads frios;
- nutrição;
- pré-qualificação;
- confirmação anterior ao atendimento;
- atraso ainda dentro da tolerância;
- cancelamento comunicado antes do horário;
- consulta jurídica;
- parecer;
- fechamento de contrato;
- cobrança agressiva;
- negociação complexa de valores;
- acompanhamento após consulta;
- follow-up de decisão;
- contatos indefinidos;
- reativação futura sem política definida.

---

## Regras de escrita

As mensagens devem:

- ser curtas;
- ser respeitosas;
- soar humanas;
- reduzir constrangimento;
- permitir resposta simples;
- usar linguagem compatível com a persona;
- evitar juridiquês;
- evitar tom de cobrança;
- evitar excesso de emojis;
- evitar dramatização.

Prefira:

- “Não conseguimos realizar seu atendimento no horário combinado.”
- “Aconteceu algum imprevisto?”
- “Se você ainda quiser seguir, posso verificar a remarcação.”
- “Teve alguma dificuldade com o acesso ou com o horário?”
- “Posso te mostrar as opções disponíveis?”

Evite:

- “Você faltou.”
- “Você nos deixou esperando.”
- “Seu horário foi perdido.”
- “Precisamos que você tenha responsabilidade.”
- “Essa é sua última oportunidade.”
- “Você perderá seu direito.”
- “Depois não diga que não avisamos.”

---

## Validação interna obrigatória

Antes de concluir, verifique:

### Escopo

- O no-show foi realmente confirmado?
- O horário já passou?
- O atendimento não ocorreu?
- Não se trata de cancelamento, remarcação ou atraso em tolerância?

### Integridade

- O motivo da ausência não foi inventado?
- A mensagem não atribui culpa?
- A mensagem não simula informação inexistente?
- O eixo de valor vem do histórico, handoff ou qualificação?
- Não há promessa de resultado?
- Não há urgência artificial?

### Operação

- A política informada é real?
- Nenhum valor, crédito, desconto, prazo ou penalidade foi inventado?
- A falha do escritório foi considerada?
- A remarcação usa horários reais?
- Reincidência foi tratada conforme a política?

### Fluxo

- Qualquer resposta interrompe os próximos disparos?
- O contato inicial é neutro?
- A retomada opcional é mais curta?
- O encerramento só existe quando autorizado?
- Não há número ou cadência inventados?
- O lead pode recusar sem pressão?

### Handoff

- O estado final está claro?
- A barreira informada foi registrada sem julgamento?
- A próxima ação está definida?
- A nova marcação retorna para `/confirmacao-consulta`?

---

## Critérios de conclusão

A saída está completa somente quando:

- parte de um no-show confirmado;
- retoma o contato sem acusação;
- não presume o motivo da ausência;
- abre espaço para uma resposta simples;
- retoma brevemente um eixo real de valor;
- aplica somente políticas reais;
- cria contatos apenas para os momentos autorizados;
- cobre as principais barreiras;
- conduz a remarcação quando houver interesse;
- respeita recusa e silêncio;
- encerra em um estado objetivo;
- prepara o handoff correto.

A skill não existe para cobrar explicações.

Ela existe para tornar possível uma retomada digna, clara e operacional.


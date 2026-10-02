---
name: follow-up
description: Cria fluxos de follow-up para recuperar movimento em oportunidades que travaram entre a pré-qualificação e o fechamento. Parte do ponto exato de travamento, verifica se a ação pendente ainda é necessária e constrói a menor intervenção útil para devolver o lead à etapa correta, com cadência mínima, ângulos condicionais, bifurcações, saídas e encerramento, sem reiniciar o funil, inventar objeções ou criar pressão artificial.
argument-hint: [etapa atual, ponto de travamento, ação pendente, histórico da conversa, motivo conhecido ou objeção, próximo passo esperado, duração/quantidade/intervalos quando definidos, canal, mapeamento de persona e regras operacionais]
---

# Follow-up Jurídico — Construtor de Cadências de Recuperação Comercial

## Objetivo

Criar fluxos de follow-up contextualizados para leads que já ingressaram no processo comercial jurídico, mas interromperam o avanço antes da próxima etapa esperada.

A função da skill é **recuperar movimento**, não repetir o funil. Ela identifica o ponto exato de travamento, confirma se ainda existe uma ação realmente necessária e usa o mínimo de interações úteis para devolver o lead à etapa em que deve continuar.

A skill atua entre:

- pré-qualificação;
- qualificação;
- coleta de informações realmente necessária;
- etapa documental já existente na operação, quando expressamente definida;
- agendamento;
- preparação operacional para atendimento, quando existir;
- devolutiva;
- negociação;
- proposta;
- decisão;
- formalização;
- assinatura;
- pagamento inicial, quando houver;
- fechamento.

A skill não cria a etapa principal.

Ela entra quando:

1. já existe um processo em andamento;
2. já existe contexto suficiente;
3. existe um ponto de travamento claro;
4. existe uma ação pendente observável;
5. essa ação **ainda é necessária** para a próxima decisão ou etapa;
6. o lead ainda não executou essa ação ou parou de responder;
7. é útil construir uma recuperação para destravar o avanço.

Exemplos:

- parou no meio da pré-qualificação e ainda falta um fato essencial para classificá-lo;
- foi qualificado, recebeu horários e não escolheu;
- recebeu a proposta e não decidiu;
- disse que falaria com um terceiro e combinou retorno;
- aceitou contratar, recebeu o contrato e não assinou;
- iniciou uma etapa documental já definida pela operação e não concluiu;
- recebeu orientação de pagamento inicial real e não concluiu.

Não crie follow-up apenas para completar um questionário, obter informação complementar ou coletar documento que poderia ser tratado em etapa posterior.

A skill deve transformar um problema genérico como:

> "o lead sumiu"

em um problema operacional claro:

> "o lead está na etapa X, ficou pendente a ação Y e a cadência precisa remover os obstáculos que podem estar impedindo Y."

---

## Referências obrigatórias

Antes de produzir a saída:

1. leia `${CLAUDE_PLUGIN_ROOT}/references/core-cognitivo.md`;
2. leia `${CLAUDE_PLUGIN_ROOT}/references/core-escrita-oralidade.md`;
3. utilize o Mapeamento de Persona Jurídica fornecido pelo usuário ou disponível na conversa, quando houver;
4. utilize o histórico real da conversa ou do processo comercial, quando fornecido;
5. utilize somente condições, políticas, procedimentos, prazos, provas e dados efetivamente informados;
6. preserve as fronteiras das demais skills da biblioteca.

Não execute novamente o Mapeamento de Persona.

Não reconstrua todo o processo comercial.

Use somente o contexto necessário para construir a recuperação do ponto travado.

---

## Princípio central

> O tempo organiza a cadência. O obstáculo organiza o conteúdo. A necessidade atual organiza se a cadência deve existir.

Antes de qualquer cadência, verifique:

1. por que o lead entrou em follow-up;
2. qual é a única ação pendente que destrava a próxima etapa;
3. se essa ação ainda é necessária;
4. se existe motivo conhecido, objeção declarada ou apenas hipótese;
5. qual é a menor intervenção capaz de destravar;
6. para qual etapa o lead volta quando responder.

Se a ação deixou de ser necessária, **não crie a cadência**. Siga para a próxima etapa adequada.

A skill não deve produzir uma sequência de lembretes repetidos.

Ela deve investigar ou trabalhar, ao longo da cadência, os possíveis obstáculos que impedem a ação pendente.

Cada contato deve cumprir uma função diferente.

Exemplos de funções:

- esclarecer o que precisa ser feito;
- explicar por que a ação é necessária;
- reduzir esforço;
- eliminar dúvida operacional;
- corrigir crença;
- trabalhar objeção declarada;
- testar uma hipótese de travamento;
- oferecer alternativa operacional real;
- verificar mudança de contexto;
- facilitar decisão;
- retomar um compromisso anterior;
- lembrar sem pressionar;
- permitir encerramento.

Não use:

- "viu minha mensagem?";
- "alguma novidade?";
- "ainda tem interesse?";
- "estou aguardando";
- "só passando para cobrar";
- "última chance";
- mensagens sucessivas com o mesmo pedido apenas reescrito.

---

## Natureza da skill

Esta skill produz um **fluxo de cadência**.

A saída principal deve combinar:

- estratégia;
- linha do tempo;
- função de cada contato;
- mensagens prontas;
- hipóteses de travamento;
- bifurcações, quando necessárias;
- respostas possíveis;
- regras de continuidade;
- regras de saída;
- pontos de intervenção humana;
- critérios de encerramento.

A skill pode criar:

- uma cadência curta;
- uma cadência média;
- uma cadência longa;
- um único follow-up;
- vários blocos de contatos;
- trilhas distintas;
- fluxo manual;
- fluxo automatizável;
- fluxo híbrido.

A quantidade de contatos não é fixa.

A duração não é fixa.

A frequência não é fixa.

A estrutura deve ser adaptada ao contexto informado.

Quando houver mais de um contato possível, diferencie duas camadas:

### Cadência mínima recomendada

É o menor conjunto de contatos prioritários normalmente suficiente para recuperar movimento. Deve ser o ponto de partida padrão quando o escritório não tiver definido uma sequência fixa.

### Banco de ângulos de recuperação

São abordagens adicionais disponíveis somente quando houver gatilho real, como:

- sinal do lead;
- obstáculo identificado;
- objeção declarada;
- motivo conhecido;
- política do escritório;
- necessidade operacional concreta.

Ângulos não devem ser disparados automaticamente em sequência apenas porque existem.

A lógica é: **ter várias formas de recuperar uma oportunidade, e não obrigação de usar todas**.

---

## Escopo comercial

A skill pode ser usada em qualquer ponto entre a pré-qualificação e o fechamento, desde que exista uma ação pendente concreta.

### Exemplos de uso permitidos

#### Pré-qualificação

- fato essencial sem resposta e que ainda impede classificar;
- esclarecimento indispensável para decidir entre avanço, revisão, roteamento ou não aderência;
- retorno combinado.

Antes de criar follow-up nesta etapa, verifique se o lead já pode ser classificado com o que respondeu. Se puder, classifique e avance.

Informação complementar, data exata não essencial, existência de documento, detalhe de handoff ou dado que pode ser obtido na reunião **não geram cadência por si só**.

#### Qualificação

- pendência factual indispensável para uma decisão objetiva da etapa;
- confirmação de titularidade ou outro fato realmente necessário;
- ação documental somente quando a própria operação já tiver definido expressamente essa etapa como necessária.

#### Agendamento

- lead qualificado que não concluiu a escolha de data;
- lead que demonstrou intenção de agendar e travou;
- ação operacional necessária antes da confirmação.

Não substitua `/agendamento` nem `/confirmacao-agendamento`.

#### Consulta e devolutiva

- silêncio depois de devolutiva;
- esclarecimento pendente;
- documento complementar solicitado;
- retorno combinado.

#### Negociação e fechamento

- silêncio depois da apresentação do serviço;
- silêncio depois dos honorários;
- proposta enviada sem resposta;
- objeção declarada;
- decisão pendente;
- consulta com cônjuge ou terceiro decisor;
- contrato não assinado;
- pagamento inicial não concluído;
- formalização incompleta.

---

## Casos fora do escopo

Não use esta skill para:

- lead frio que nunca iniciou conversa;
- sequência de aquecimento anterior à pré-qualificação;
- recuperação de no-show;
- confirmação de consulta;
- campanha de marketing;
- nutrição genérica;
- remarketing amplo;
- reativação de base sem contexto;
- leads antigos sem ponto de travamento identificado;
- pós-venda;
- acompanhamento processual;
- relacionamento com cliente já contratado;
- cobrança financeira de cliente inadimplente, salvo se o usuário pedir expressamente uma adaptação e fornecer a política real aplicável.

Use `/funil-nutricao` para lead frio anterior à conversa.

Use `/recuperacao-no-show` para ausência confirmada em consulta.

Use outras skills específicas quando a etapa principal ainda estiver sendo construída.

---

## Ponto de partida obrigatório

Antes de construir a cadência, identifique:

1. **etapa atual**;
2. **ponto exato de travamento**;
3. **ação pendente**;
4. **se essa ação ainda é necessária** para a próxima decisão ou etapa;
5. **próximo passo esperado**;
6. **o que aconteceu antes do silêncio**;
7. **o que já foi dito ou enviado**;
8. **se existe objeção declarada**;
9. **se existe motivo conhecido para o travamento**;
10. **se houve retorno combinado**;
11. **qual é o limite operacional da equipe**;
12. **qual é a duração ou estrutura desejada, quando informada**;
13. **qual evento encerra ou altera a cadência**.

### Checagem de necessidade

Antes de prosseguir, responda:

- sem essa ação, o lead realmente não pode avançar?
- a etapa anterior já permite classificação ou encaminhamento?
- a pendência é essencial ou apenas complementar?
- essa informação pode ser obtida na reunião ou depois sem prejuízo à decisão atual?

Se a resposta indicar que a ação não é mais necessária, não crie follow-up. Registre a ausência, quando útil, e siga para a próxima etapa.

Defina a ação pendente de forma observável.

Boas ações pendentes:

- responder uma pergunta essencial;
- confirmar uma informação indispensável;
- escolher uma data ou horário;
- retornar uma decisão;
- esclarecer uma objeção real;
- assinar contrato;
- efetuar pagamento inicial, quando existir;
- concluir uma etapa documental já configurada pela operação;
- informar se deseja continuar.

Evite objetivos vagos:

- recuperar o lead;
- fazê-lo voltar;
- aumentar interesse;
- convencer;
- aquecer;
- gerar urgência.

---

## Hierarquia do contexto

Quando houver conflito entre sinais, siga esta ordem:

1. fatos concretos da conversa;
2. resposta explícita do lead;
3. ação pendente confirmada;
4. histórico operacional;
5. regras do escritório;
6. Mapeamento de Persona;
7. hipótese estratégica.

O Mapeamento de Persona orienta.

O histórico real prevalece.

Exemplo:

Se a persona costuma demonstrar medo de golpe, mas o lead disse:

> "não consegui ir ao médico buscar o laudo"

não use medo de golpe como barreira principal.

Trabalhe o obstáculo real.

---

## Fato conhecido, objeção declarada e hipótese de travamento

A skill deve separar explicitamente três categorias.

### 1. Motivo conhecido

O lead explicou por que não avançou.

Exemplos:

- "o documento está com meu médico";
- "vou falar com meu marido";
- "não consegui pagar ainda";
- "não achei o contrato";
- "estou esperando um exame".

Pode ser tratado diretamente.

### 2. Objeção declarada

O lead verbalizou uma resistência.

Exemplos:

- preço;
- medo;
- desconfiança;
- insegurança;
- dúvida sobre o serviço;
- receio de processo;
- dificuldade com contrato.

Pode ser trabalhada diretamente, dentro do limite real do escritório.

### 3. Hipótese de travamento

O lead não explicou o silêncio.

Nesse caso:

- não afirme a causa;
- não personalize a hipótese como fato;
- não escreva "sei que você está...";
- não invente objeção;
- use mensagens que testem ou removam obstáculos possíveis sem atribuí-los ao lead.

Exemplo adequado:

> Se a dificuldade for localizar o documento, pode mandar primeiro o que já tiver em mãos.

Exemplo inadequado:

> Sei que você está com dificuldade para achar seus documentos.

### Hipótese interna não é automaticamente tema da mensagem

Uma hipótese pode orientar a estratégia sem ser verbalizada ao lead. Antes de mencionar diretamente uma possível objeção ou receio, verifique se:

1. existe sinal concreto do lead que sustente o tema; ou
2. a mensagem possui valor independente e não corre o risco de criar uma nova objeção.

Sem sinal, não introduza espontaneamente temas como:

- medo ou desconfiança;
- necessidade de documentos;
- preço;
- receio de contratar;
- medo de exposição;
- intenção de tentar sozinho.

Prefira mensagens neutras que removam atrito sem atribuir uma causa ao silêncio.

---

## Mapeamento de obstáculos

Quando o motivo não estiver conhecido, identifique hipóteses plausíveis relacionadas à ação pendente.

As hipóteses devem vir de:

- histórico da operação;
- etapa comercial;
- processo necessário;
- Mapeamento de Persona;
- comportamento já observado;
- dificuldades operacionais típicas efetivamente informadas pelo usuário;
- contexto do caso.

Não invente uma lista genérica apenas para preencher a cadência.

Para cada hipótese, avalie:

- o que o obstáculo impede;
- como ele poderia aparecer;
- que tipo de mensagem pode removê-lo;
- se exige automação ou humano;
- se pode ser tratado sem presumir que se aplica ao lead.

A cadência pode ser organizada como um processo de eliminação de obstáculos.

Cada novo contato deve:

- atacar uma hipótese diferente; ou
- avançar a função estratégica da cadência.

Não repita o mesmo obstáculo com palavras diferentes.

---

## Estratégia da cadência

Antes de escrever mensagens, construa a lógica.

Considere:

- urgência real;
- dificuldade da ação;
- esforço exigido;
- valor percebido;
- risco de desgaste;
- estágio comercial;
- nível de envolvimento anterior;
- histórico de respostas;
- tamanho da pendência;
- necessidade de intervenção humana;
- duração solicitada;
- quantidade de contatos solicitada.

A cadência pode ser estruturada em blocos.

Exemplos abstratos:

### Etapa documental já existente

Use somente quando o escritório já tiver definido essa etapa ou quando um documento específico for realmente necessário para a ação atual. Não crie coleta documental apenas para enriquecer a qualificação.

Possíveis funções:

1. clareza sobre o que realmente é necessário;
2. instrução de envio;
3. redução de esforço;
4. remoção de barreira operacional;
5. alternativa permitida;
6. encerramento.

### Agendamento travado

1. retomada;
2. facilitação;
3. redução de esforço;
4. verificação de impedimento;
5. saída respeitosa.

### Proposta

1. retomada contextual;
2. abertura para dúvida;
3. objeção real;
4. valor e clareza;
5. decisão;
6. encerramento.

### Contrato não assinado

1. retomada;
2. verificação de impedimento operacional;
3. ajuda concreta;
4. confirmação de intenção;
5. encerramento.

Esses exemplos são estruturas possíveis.

Não os aplique mecanicamente.

### Argumentos sobre o serviço

Não invente argumentos de venda para preencher a cadência. Toda mensagem sobre:

- benefícios da contratação;
- diferencial do escritório;
- riscos evitados;
- etapas do trabalho;
- documentos que o escritório organiza;
- atividades realizadas;
- consequências de fazer sozinho;

deve estar ancorada em pelo menos uma destas fontes:

1. serviço efetivamente oferecido pelo escritório;
2. procedimento real informado;
3. proposta apresentada ao lead;
4. conteúdo efetivamente tratado na reunião ou conversa anterior.

Sem confirmação, use campo configurável ou marque `[VALIDAR COM O ESCRITÓRIO]`.

---

## Blocos estratégicos

Quando a cadência tiver vários contatos, agrupe-os por função quando isso melhorar a compreensão.

Exemplos:

- remoção de obstáculos;
- persistência com variação;
- facilitação de ação;
- tratamento de objeção;
- decisão;
- presença residual;
- encerramento.

Não crie blocos artificiais apenas para organizar visualmente.

Cada bloco deve representar uma mudança real de estratégia.

---

## Mensagens leves e densas

A cadência pode alternar contatos de diferentes níveis de profundidade.

### Mensagem leve

Serve para:

- lembrar;
- retomar;
- reduzir pressão;
- testar canal;
- pedir resposta simples;
- manter presença;
- confirmar pendência.

Deve exigir pouco esforço.

### Mensagem densa

Serve para:

- ensinar algo necessário;
- esclarecer uma dúvida;
- reduzir obstáculo;
- apresentar orientação operacional;
- corrigir crença;
- explicar por que a ação importa;
- responder objeção.

Uma mensagem não é densa apenas por ser longa.

Critério:

> Se esta mensagem for retirada da cadência, o lead deixa de receber alguma informação necessária para avançar?

Se não, provavelmente ela apenas está comprida.

Não imponha uma regra fixa de alternância.

Use a profundidade conforme a função.

---

## Cadência, duração e frequência

Não invente:

- duração total;
- número de contatos;
- intervalo;
- dia da semana;
- horário;
- limite diário;
- janela de disparo;
- frequência ideal;
- prazo de reativação.

Quando o usuário informar:

- duração;
- número de contatos;
- intervalo;
- datas;
- dias específicos;

respeite.

Quando não informar e isso não impedir a arquitetura, use placeholders:

- `[DURAÇÃO DEFINIDA PELO ESCRITÓRIO]`;
- `[QUANTIDADE DE CONTATOS]`;
- `[INTERVALO DEFINIDO PELO ESCRITÓRIO]`;
- `[DATA DE RETORNO]`;
- `[PRAZO COMBINADO]`.

Quando a ausência desses dados impedir a construção solicitada, faça uma pergunta objetiva.

Se o usuário pedir recomendação de cadência, diferencie claramente:

- regra do escritório;
- hipótese estratégica;
- recomendação.

Não apresente recomendação como fato ou padrão universal.

Quando o usuário não definir a quantidade de contatos, não preencha automaticamente uma sequência longa. Comece pela **Cadência mínima recomendada** e apresente os demais caminhos como **Banco de ângulos de recuperação**.

Quando o usuário definir uma quantidade específica, respeite-a, mas ainda assim diferencie quais contatos são prioritários e quais dependem de gatilho sempre que isso melhorar a operação.

---

## Linha do tempo

Quando houver cadência temporal definida, entregue uma linha do tempo.

Exemplo:

| Momento | Obstáculo/função | Tipo | Mensagem | Respostas possíveis | Ação |
|---|---|---|---|---|---|

Use:

- D+1;
- D+3;
- D+7;
- data real;
- prazo combinado;
- intervalo definido;

somente quando fornecidos ou recomendados de forma explicitamente identificada.

Quando não houver tempo definido, use:

- Contato 1;
- Contato 2;
- Contato 3;

 e placeholders de intervalo.

---

## Bifurcações e trilhas

A skill pode criar trilhas diferentes quando existir uma diferença objetiva de estado.

Exemplos:

- nunca respondeu;
- respondeu, mas não concluiu a ação;
- declarou objeção;
- informou dificuldade operacional;
- informou que depende de terceiro;
- solicitou tempo;
- combinou uma data;
- informou mudança de contexto.

Não crie bifurcação apenas porque seria possível.

Crie somente quando:

1. a mensagem necessária muda;
2. o próximo passo muda;
3. o estado operacional muda;
4. a diferença pode ser identificada objetivamente.

Evite árvores complexas.

Prefira poucas trilhas claras.

---

## Regra sobre respostas durante a cadência

Qualquer mensagem do lead deve pausar o próximo disparo automático até que a resposta seja classificada. Não mantenha uma sequência ativa enquanto houver mensagem aguardando tratamento.


Diferentemente do `/funil-nutricao`, qualquer resposta do lead **não encerra automaticamente** esta skill.

A resposta pode:

- encerrar;
- pausar;
- alterar;
- redirecionar;
- manter a cadência;
- registrar pendência;
- exigir intervenção humana.

Analise o evento operacional.

Exemplos:

### Pode encerrar a cadência

- executou a ação pendente;
- informou que não deseja continuar;
- pediu interrupção;
- concluiu contratação;
- concluiu assinatura;
- efetuou pagamento, quando esse era o objetivo.

### Pode manter a cadência

- informou que o documento está com terceiro;
- disse que pretende enviar depois;
- explicou um obstáculo ainda não resolvido;
- pediu prazo;
- informou dificuldade operacional.

### Pode pausar e exigir humano

- objeção complexa;
- situação jurídica nova;
- alteração de qualificação;
- informação contraditória;
- documento ilegível;
- pedido de orientação específica;
- situação não prevista;
- reclamação;
- pedido expresso de atendimento.

Não trate qualquer resposta como sucesso.

Não trate qualquer silêncio como recusa.

---

## Saídas objetivas

Toda cadência deve definir:

- evento de sucesso;
- evento de pausa;
- evento de intervenção humana;
- evento de abandono;
- pedido de opt-out;
- mudança de estágio;
- mudança de qualificação;
- encerramento natural.

Exemplo:

| Gatilho | Destino | Regra |
|---|---|---|
| Executou a ação pendente | Próxima etapa | Encerrar cadência |
| Informou impedimento real | Manter/ajustar | Registrar pendência |
| Pediu humano | Atendimento | Pausar automação |
| Não quer continuar | Encerramento | Não insistir |
| Pediu interrupção | Opt-out | Bloquear novos contatos |
| Mudança relevante | Revisão humana | Pausar até revisão |

Adapte ao caso.

---

## Handoff entre etapas

Quando a ação pendente for concluída, indique claramente a próxima etapa.

Exemplos:

- documento enviado → análise;
- qualificação concluída → `/agendamento`;
- agendamento concluído → `/confirmacao-agendamento`;
- comparecimento → `/roteiro-consulta`;
- proposta aceita → formalização;
- contrato assinado → procedimento real do escritório.

Não invente uma etapa que não existe.

Não execute automaticamente a próxima skill.

Apenas sinalize o handoff.

---

## Follow-up na pré-qualificação

Quando a cadência estiver ligada à pré-qualificação, a primeira tarefa é verificar se ela ainda é necessária.

Antes de iniciar:

1. identifique qual informação ficou faltando;
2. verifique se ela é essencial para classificação, roteamento, prioridade ou próximo passo;
3. verifique se, com o que já existe, o lead pode ser classificado como avanço, avanço com pendência, revisão profissional, roteamento, não aderência ou outro status previsto;
4. se já for possível classificar, **não crie cadência** apenas para completar o questionário;
5. se realmente faltar um fato essencial, recupere somente esse ponto.

Regras:

- preserve as perguntas já respondidas;
- não reinicie a triagem;
- não repita coleta;
- não persiga informação complementar;
- aceite resposta aproximada ou `não sei` quando a política da pré-qualificação permitir;
- diferencie ausência de informação de não aderência;
- existência de documentos não é, por padrão, critério de qualificação;
- ausência de documento não gera follow-up por si só;
- não crie etapa documental que não existia.

Informações que normalmente **não** justificam uma cadência sozinhas:

- data exata quando estimativa já basta;
- existência de documento;
- detalhe de handoff;
- informação complementar para o profissional;
- dado que pode ser obtido na reunião ou depois.

Se a operação tiver definido expressamente uma etapa documental após a classificação, o follow-up pode recuperar essa ação operacional, mas ela não deve ser apresentada como requisito genérico de aderência.

---

## Follow-up de agendamento

Quando o lead já estiver qualificado e travar no agendamento:

- não refaça pré-qualificação;
- não crie necessidade jurídica novamente;
- não repita toda a devolutiva;
- preserve os fatos e a qualificação já obtidos;
- a ação pendente principal é **escolher um horário** ou resolver um impedimento operacional diretamente ligado a isso;
- reduza a fricção operacional;
- use apenas horários, canais e políticas reais;
- não invente agenda;
- não crie preparação documental como condição para marcar, salvo regra expressa da operação;
- não substitua `/agendamento`;
- não envie confirmação antes de existir atendimento marcado.

Se o motivo conhecido for horário, resolva horário. Se houver dúvida sobre a reunião, responda a dúvida. Se houver custo declarado, trate a condição real. Não introduza espontaneamente objeções que o lead não demonstrou.

---

## Follow-up de proposta e decisão

Quando a proposta já tiver sido apresentada:

- retome o contexto real;
- não reapresente toda a proposta em cada contato;
- não presuma que preço é a objeção;
- motivo conhecido e objeção declarada prevalecem sobre hipótese;
- trate somente o ponto real quando ele estiver declarado;
- reforce valor apenas com base no serviço efetivamente explicado;
- não invente desconto;
- não invente prazo;
- não invente condição;
- não use urgência jurídica para pressionar decisão comercial;
- não crie novos argumentos de venda apenas para preencher a cadência.

Mensagens sobre valor do serviço, próximos passos, documentos, diferenciais ou consequências de fazer sozinho devem estar apoiadas na proposta, no procedimento real ou no que foi efetivamente tratado na reunião.

Quando houver retorno combinado:

- registre a data;
- respeite a data;
- não cobre antes do prazo combinado;
- retome exatamente o ponto pendente.

A ação pendente pode ser:

- decidir seguir;
- decidir não seguir;
- informar quando decidirá;
- esclarecer uma objeção real.

---

## Follow-up de contrato e formalização

Quando houver aceite, mas a formalização não tiver sido concluída:

- preserve a decisão já tomada;
- não volte a vender;
- não repita argumentos comerciais;
- trate primeiro impedimentos operacionais;
- verifique se o contrato foi recebido;
- facilite assinatura apenas dentro do procedimento real;
- explique documento quando necessário;
- não trate silêncio como desistência;
- diferencie obstáculo operacional de mudança de decisão;
- se o lead disser que mudou de ideia, registre a nova situação e encaminhe conforme a operação, sem reabrir pressão comercial.

A ação pendente é concluir a formalização. Se houver pagamento inicial, trate-o como ação separada e somente quando a operação realmente exigir.

---

## Persona orienta; histórico prevalece

O Mapeamento de Persona pode orientar:

- linguagem;
- formalidade;
- fricção percebida;
- medo de golpe;
- dificuldade tecnológica;
- papel do cônjuge;
- sensibilidade financeira;
- confiança;
- formato;
- nível de detalhamento.

Mas não autoriza afirmar que o lead:

- sente medo;
- está sem dinheiro;
- esqueceu;
- está inseguro;
- depende do cônjuge;
- não sabe usar o celular;
- não encontrou documento;
- está desconfiado.

Use formulações hipotéticas quando necessário:

- "Se a dificuldade for...";
- "Caso tenha ficado alguma dúvida...";
- "Se você ainda não conseguiu...";
- "Se o documento estiver com...";
- "Se preferir...".

Não escreva:

- "sei que você está...";
- "você deve estar...";
- "imagino que o problema seja...";
- "percebi que você...";

sem base real.

---

## Objeções

Quando a objeção for declarada:

1. reconheça;
2. investigue quando necessário;
3. responda ao ponto real;
4. verifique se esclareceu;
5. retome o próximo passo.

Não invente objeção.

Não responda a várias objeções ao mesmo tempo.

Não use objeções como desculpa para escrever textos longos.

Não trabalhe preço, honorários ou condição comercial se isso ainda não apareceu naquela etapa.

---

## Utilidade obrigatória

Uma cadência longa não pode ser composta apenas por cobranças.

Quando houver vários contatos, distribua utilidade.

Utilidade pode ser:

- explicar o que serve;
- mostrar como executar;
- reduzir exigência;
- orientar uma ação;
- responder dúvida;
- esclarecer o próximo passo;
- remover crença;
- facilitar decisão;
- oferecer alternativa permitida;
- resumir ponto importante.

Não crie conteúdo só para preencher o calendário.

Pergunte:

> Este contato ajuda a pessoa a executar a ação pendente ou apenas lembra que ela ainda não executou?

Se apenas lembra, avalie se ele é realmente necessário.

---

## Encerramento

Toda cadência deve ter critério de encerramento.

O último contato deve:

- deixar claro que a cadência ativa está terminando;
- evitar culpa;
- evitar ameaça;
- evitar pressão;
- não inventar prazo;
- não criar "última chance";
- permitir retorno futuro quando a política permitir;
- explicar o que acontece depois, se houver regra real.

Não escreva automaticamente:

- "vou encerrar seu caso";
- "você perderá o direito";
- "esta é sua última oportunidade";
- "se não responder hoje...";
- "não poderemos mais ajudar";

sem fundamento real.

---

## Automação e intervenção humana

Quando o fluxo for automatizável, defina:

- estados;
- gatilhos;
- saídas;
- bloqueios;
- intervenção humana;
- eventos que interrompem disparos;
- migração entre trilhas.

A automação não deve continuar quando:

- existe mensagem do lead aguardando resposta humana;
- houve pedido de interrupção;
- houve opt-out;
- surgiu situação não classificada;
- surgiu mudança relevante;
- houve conclusão da ação pendente;
- a política real exigir análise humana.

Não invente:

- janela de horário;
- dias proibidos;
- prazo de resposta;
- SLA;
- regra de CRM;
- política de opt-out;
- nome de tag.

Use placeholders ou marque `[VALIDAR COM O ESCRITÓRIO]`.

---

## Não invenção

Não invente:

- motivo do silêncio;
- objeção;
- dificuldade;
- urgência;
- prazo legal;
- prazo comercial;
- escassez;
- desconto;
- bônus;
- condição especial;
- agenda;
- canal alternativo;
- possibilidade de parcelamento;
- gratuidade;
- política de documentos;
- política de assinatura;
- política de retorno;
- tempo de análise;
- disponibilidade do profissional;
- SLA;
- resultado provável;
- chance de êxito;
- estatística;
- case;
- experiência institucional;
- promessa de resultado;
- regra de automação não fornecida;
- prazo de cadência;
- frequência de contatos.

Use placeholders quando necessário:

- `[NOME]`;
- `[ETAPA ATUAL]`;
- `[AÇÃO PENDENTE]`;
- `[PRÓXIMO PASSO]`;
- `[DOCUMENTO]`;
- `[DURAÇÃO DA CADÊNCIA]`;
- `[INTERVALO DEFINIDO PELO ESCRITÓRIO]`;
- `[QUANTIDADE DE CONTATOS]`;
- `[DATA DE RETORNO]`;
- `[PRAZO COMBINADO]`;
- `[CANAL]`;
- `[RESPONSÁVEL]`;
- `[POLÍTICA DE ENCERRAMENTO]`;
- `[CONDIÇÃO COMERCIAL REAL]`;
- `[PROCEDIMENTO REAL]`;
- `[VALIDAR COM O ESCRITÓRIO]`.

---

## Perguntas ao usuário

Não transforme a ativação em formulário.

Use tudo o que já estiver disponível.

Pergunte apenas quando a ausência impedir a construção.

As perguntas prioritárias são:

1. Em que etapa o lead travou?
2. Qual ação está pendente?
3. O que aconteceu imediatamente antes do silêncio?
4. Existe motivo conhecido ou objeção declarada?
5. Qual duração, quantidade ou intervalo você quer?
6. O que encerra a cadência?
7. Existe alguma regra operacional que precisa ser respeitada?

Se o usuário fornecer um contexto como:

> "Lead recebeu os horários depois da pré-qualificação e não escolheu. Quero uma cadência de 10 dias com 3 contatos."

execute diretamente.

Se o usuário disser que precisa de documento para `confirmar a qualificação`, verifique primeiro se isso é uma regra expressa da operação ou uma necessidade profissional real. Não assuma automaticamente que a falta do documento impede a classificação.

---

## Formato por canal

### WhatsApp

Use:

- mensagens confortáveis em tela pequena;
- uma função principal por contato;
- parágrafos curtos;
- linguagem natural;
- pouca burocracia;
- CTA simples;
- poucos emojis, quando adequados.

### E-mail

Inclua:

- assunto;
- retomada;
- utilidade;
- ação esperada;
- fechamento.

Não copie mecanicamente o WhatsApp.

### Áudio

Use somente quando houver ganho real.

Quando sugerir áudio:

- escreva o texto integral;
- não presuma preferência;
- use somente quando permitido;
- não use áudio para pressionar.

---

## Formato da entrega

Entregue nesta ordem.

# 0. CHECAGEM DE NECESSIDADE DA CADÊNCIA

Antes de desenhar qualquer contato, responda internamente e mostre de forma breve:

- por que esse lead entrou em follow-up;
- qual é a única ação pendente;
- se essa ação ainda é necessária;
- se o motivo é conhecido, objeção declarada ou hipótese;
- qual é a menor intervenção capaz de destravar;
- para qual etapa o lead volta quando responder.

Se a ação não for necessária, encerre a construção e indique a próxima etapa adequada.

# 1. CONTEXTO E PONTO DE TRAVAMENTO

Apresente:

- etapa atual;
- ponto exato de travamento;
- ação pendente;
- próximo passo esperado;
- histórico relevante;
- última ação do escritório;
- última manifestação do lead, quando houver;
- motivo conhecido, se houver;
- objeção declarada, se houver;
- canal;
- responsável;
- duração;
- quantidade de contatos;
- intervalos;
- condições já definidas.

Diferencie:

- fato;
- informação ausente;
- hipótese.

# 2. OBJETIVO DA CADÊNCIA

Declare uma única ação observável.

Exemplos:

> Fazer o lead responder a informação essencial que ainda impede a classificação.

> Fazer o lead escolher um horário para a reunião.

> Obter uma decisão sobre a proposta ou uma data real de retorno.

> Concluir a assinatura do contrato e da procuração.

Não use objetivo abstrato. Não misture duas ações principais na mesma cadência.

# 3. MOTIVO, OBJEÇÃO E HIPÓTESES DE TRAVAMENTO

Separe explicitamente:

- motivo conhecido;
- objeção declarada;
- hipótese interna.

Quando o motivo não for conhecido, apresente somente hipóteses estratégicas relevantes.

Use tabela:

| Hipótese | Sinal possível | Como remover/testar | Pode ser dita sem sinal? | Status |
|---|---|---|---|---|

Em `Status`, use:

- confirmado;
- declarado;
- hipótese;
- não aplicável.

Não trate hipótese como diagnóstico nem transforme hipótese interna em assunto obrigatório da mensagem.

# 4. ESTRATÉGIA DA CADÊNCIA

Explique de forma curta:

- lógica;
- progressão;
- nível de insistência;
- quando bifurca;
- quando encerra.

Depois separe:

## Cadência mínima recomendada

Liste os contatos prioritários normalmente suficientes para recuperar movimento.

## Banco de ângulos de recuperação

Liste abordagens adicionais com o gatilho de uso. Elas não são sequência obrigatória.

Quando o escritório tiver uma cadência fixa informada, preserve-a, mas identifique os contatos condicionais quando houver.

Não transforme em teoria excessiva.

# 5. LINHA DO TEMPO

Use tabela:

| Momento | Camada | Função/obstáculo | Tipo | Contato | Respostas possíveis | Ação operacional |
|---|---|---|---|---|---|---|

Use datas e intervalos reais ou placeholders.

# 6. MENSAGENS PRONTAS

Para cada contato da cadência mínima e para cada ângulo realmente útil:

## CONTATO [NÚMERO] — [FUNÇÃO] [MÍNIMA]

ou

## ÂNGULO [CÓDIGO] — [FUNÇÃO] [CONDICIONAL]

**Quando enviar:** [condição]

**Objetivo interno:** [função]

**Mensagem pronta:**

> [mensagem]

**Se responder:** [regra operacional]

Não escreva notas internas dentro da mensagem ao lead.

# 7. BIFURCAÇÕES OU TRILHAS

Somente quando necessárias.

Explique:

- condição de entrada;
- diferença de mensagem;
- diferença de ação;
- migração entre trilhas.

Se não houver necessidade, diga:

> Não há bifurcação necessária nesta cadência.

# 8. REGRAS DE SAÍDA E CONTINUIDADE

Inclua:

- sucesso;
- resposta parcial;
- obstáculo declarado;
- pedido de humano;
- mudança de contexto;
- falta de interesse;
- opt-out;
- silêncio até o final;
- encerramento.

# 9. REGRAS DE AUTOMAÇÃO OU OPERAÇÃO

Quando aplicável:

- condição de disparo;
- bloqueios;
- intervenção humana;
- alteração de estado;
- registro de pendência;
- pausa;
- encerramento.

Regras transversais:

- qualquer mensagem do lead pausa os próximos disparos até classificação;
- uma oportunidade fica em apenas uma cadência por vez;
- ação concluída encerra a cadência atual antes da próxima etapa;
- retorno combinado suspende contatos até a data;
- opt-out bloqueia novos contatos conforme política real;
- fim da cadência não reinicia automaticamente.

Não invente regras da operação.

# 10. PONTOS A VALIDAR COM O ESCRITÓRIO

Liste somente lacunas reais, como:

- duração;
- intervalo;
- dias/horários;
- responsável;
- canal;
- política de encerramento;
- prazo;
- condição comercial;
- regra documental;
- automação;
- etapa posterior.

---

## Revisão interna obrigatória

Antes de entregar, verifique silenciosamente:

### Escopo

- existe uma etapa comercial já iniciada?
- existe ação pendente clara?
- essa ação ainda é necessária?
- seria possível avançar sem recuperar essa informação?
- a skill está recuperando continuidade e não recriando a etapa?
- houve invasão de nutrição, no-show ou pós-venda?
- o objetivo é observável?

### Contexto

- o ponto de travamento foi identificado?
- o histórico real foi aproveitado?
- perguntas já respondidas foram repetidas?
- o lead recebeu novamente informação que já tinha?
- o próximo passo está claro?

### Obstáculos

- motivos conhecidos foram tratados como fatos?
- hipóteses foram tratadas como hipóteses?
- alguma hipótese virou afirmação sobre o lead?
- alguma objeção foi introduzida sem sinal ou sem valor independente?
- os contatos trabalham obstáculos diferentes?
- houve repetição de cobrança?

### Cadência

- a lógica é estratégica e não apenas cronológica?
- o tempo organiza, o obstáculo orienta o conteúdo e a necessidade atual define se a cadência existe?
- existe uma cadência mínima claramente identificada?
- os ângulos condicionais estão separados e possuem gatilho?
- a duração foi fornecida ou marcada como placeholder?
- a frequência foi inventada?
- cada contato possui função distinta?
- contatos vazios foram usados para preencher calendário?
- a profundidade é proporcional?

### Bifurcações

- cada trilha tem condição objetiva?
- a bifurcação realmente muda mensagem ou ação?
- a árvore ficou mais complexa do que precisa?
- respostas podem alterar a cadência quando necessário?

### Persona

- o histórico real prevaleceu?
- medo, renda, cônjuge, dificuldade tecnológica ou desconfiança foram presumidos?
- o Mapeamento serviu como orientação, não como fato individual?

### Comercial

- objeção declarada foi tratada?
- argumentos sobre o serviço vêm do que o escritório realmente oferece, da proposta ou da reunião?
- objeção não declarada foi inventada?
- houve pressão?
- houve urgência comercial artificial?
- desconto ou condição foram inventados?
- silêncio foi tratado como desinteresse?
- decisão já tomada foi reaberta sem motivo?

### Jurídico

- houve promessa?
- documento foi tratado como barreira automática ou como requisito de qualificação sem base operacional?
- houve direito individual afirmado?
- prazo jurídico foi inventado?
- consequência jurídica foi usada para pressionar?
- pedido documental virou parecer?
- informação sensível foi tratada com proporcionalidade?

### Operação

- regras de CRM foram inventadas?
- horário foi inventado?
- opt-out foi respeitado?
- existe intervenção humana quando necessária?
- o evento de sucesso encerra ou redireciona corretamente?
- mensagens do lead aguardando humano bloqueiam automação, quando aplicável?

### Escrita

- as mensagens são naturais?
- parecem conversa real?
- cada uma tem uma função?
- o CTA é simples?
- há excesso de formalidade?
- há cobrança vazia?
- o último contato encerra sem pressão?

Corrija silenciosamente o que falhar.

---

## Critério de conclusão

A cadência está pronta quando:

1. identifica claramente a etapa atual;
2. identifica o ponto de travamento;
3. define uma única ação pendente observável;
4. confirma que essa ação ainda é necessária;
5. não cria follow-up para completar questionário ou informação complementar;
6. utiliza o histórico real;
7. separa motivo conhecido, objeção declarada e hipótese;
8. não inventa o motivo do silêncio;
9. não transforma hipótese interna em assunto obrigatório da mensagem;
10. identifica uma cadência mínima recomendada;
11. separa ângulos condicionais com gatilhos claros;
12. organiza contatos por função estratégica;
13. não repete cobrança;
14. respeita duração e frequência fornecidas;
15. não inventa cadência ausente;
16. admite fluxos curtos ou longos;
17. admite bifurcações quando objetivamente necessárias;
18. permite que respostas alterem a rota;
19. define saídas claras;
20. define intervenção humana quando necessária;
21. preserva fronteiras das outras skills;
22. usa a persona sem transformá-la em fato individual;
23. ancora argumentos comerciais no serviço real, na proposta ou no histórico;
24. não inventa condição comercial ou operacional;
25. não cria pressão artificial;
26. não usa urgência jurídica como ferramenta comercial;
27. não cria barreira documental que não existia na jornada;
28. mantém mensagens proporcionais ao canal;
29. encerra de forma respeitosa;
30. conduz o lead exatamente à etapa correta quando a ação pendente for concluída.

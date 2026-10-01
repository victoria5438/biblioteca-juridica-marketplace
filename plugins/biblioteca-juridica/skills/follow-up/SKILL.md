---
name: follow-up
description: Cria fluxos de cadência de follow-up para recuperar leads que interromperam alguma etapa do processo comercial jurídico entre a pré-qualificação e o fechamento. Parte do ponto exato de travamento, da ação pendente e do histórico real para estruturar contatos progressivos, mensagens, bifurcações, regras de continuidade, saídas e encerramento, sem repetir cobrança, inventar o motivo do silêncio ou criar pressão artificial.
argument-hint: [etapa atual, ponto de travamento, ação pendente, histórico da conversa, duração desejada, quantidade de contatos, intervalos, canal, mapeamento de persona, regras operacionais e próximo passo esperado]
---

# Follow-up Jurídico — Construtor de Cadências de Recuperação Comercial

## Objetivo

Criar fluxos de cadência de follow-up contextualizados para leads que já ingressaram no processo comercial jurídico, mas interromperam o avanço antes da próxima etapa esperada.

A skill atua entre:

- pré-qualificação;
- qualificação;
- coleta de informações;
- coleta de documentação prévia;
- agendamento;
- preparação para consulta;
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
3. existe uma ação pendente clara;
4. o lead ainda não executou essa ação ou parou de responder;
5. é necessário construir uma cadência para recuperar o avanço.

Exemplos:

- respondeu a pré-qualificação, mas não enviou os laudos necessários;
- iniciou a coleta documental, mas não concluiu;
- foi qualificado, mas não avançou para o agendamento;
- recebeu a devolutiva e ficou de verificar um ponto;
- recebeu a proposta e parou de responder;
- disse que falaria com o cônjuge e não retornou;
- recebeu o contrato e não assinou;
- recebeu a orientação para pagamento inicial e não concluiu.

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

> O tempo organiza a cadência. O obstáculo organiza o conteúdo.

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

---

## Escopo comercial

A skill pode ser usada em qualquer ponto entre a pré-qualificação e o fechamento, desde que exista uma ação pendente concreta.

### Exemplos de uso permitidos

#### Pré-qualificação

- pergunta relevante sem resposta;
- informação indispensável incompleta;
- documento prévio necessário para concluir aderência;
- laudo, relatório, contrato, comprovante ou outro material necessário;
- retorno combinado.

#### Qualificação

- pendência que impede confirmar MQL ou SQL;
- documento necessário para análise preliminar;
- confirmação de titularidade ou outro fato indispensável.

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
4. **próximo passo esperado**;
5. **o que aconteceu antes do silêncio**;
6. **o que já foi dito ou enviado**;
7. **se existe objeção declarada**;
8. **se existe motivo conhecido para o travamento**;
9. **se houve retorno combinado**;
10. **qual é o limite operacional da equipe**;
11. **qual é a duração ou estrutura desejada, quando informada**;
12. **qual evento encerra ou altera a cadência**.

Defina a ação pendente de forma observável.

Boas ações pendentes:

- enviar laudo;
- enviar documento;
- responder uma pergunta;
- confirmar uma informação;
- escolher uma data;
- retornar uma decisão;
- esclarecer uma objeção;
- assinar contrato;
- efetuar pagamento;
- comparecer a uma ação combinada;
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

### Coleta documental

1. clareza;
2. instrução;
3. redução de exigência;
4. remoção de barreira;
5. correção de crença;
6. alternativa operacional;
7. encerramento.

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

Quando a cadência estiver ligada à pré-qualificação:

- preserve as perguntas já respondidas;
- não reinicie a triagem;
- não repita coleta;
- trabalhe apenas o ponto que impede concluir a qualificação;
- diferencie ausência de informação de não aderência;
- não transforme falta documental em desqualificação automática;
- não prometa que o documento confirmará direito.

Se a pendência for documental:

- diga por que o documento é necessário, quando isso puder ser explicado;
- aceite envio parcial quando a política permitir;
- não rejeite automaticamente documento de menor utilidade;
- não peça lista maior do que o necessário;
- defina quando a automação deve parar e a análise humana assumir.

---

## Follow-up de agendamento

Quando o lead já estiver qualificado e travar no agendamento:

- não refaça pré-qualificação;
- não crie necessidade jurídica novamente;
- retome o motivo pelo qual o agendamento foi indicado;
- reduza a fricção operacional;
- use apenas horários, canais e políticas reais;
- não invente agenda;
- não substitua `/agendamento`;
- não envie confirmação de consulta antes de existir consulta marcada.

---

## Follow-up de proposta e decisão

Quando a proposta já tiver sido apresentada:

- retome o contexto real;
- não reapresente toda a proposta em cada contato;
- não presuma que preço é a objeção;
- pergunte quando o impedimento não estiver claro;
- trate somente objeções declaradas;
- reforce valor com base no serviço já explicado;
- não invente desconto;
- não invente prazo;
- não invente condição;
- não use urgência jurídica para pressionar decisão comercial.

Quando houver retorno combinado:

- registre a data;
- respeite a data;
- não cobre antes do prazo combinado;
- retome exatamente o ponto pendente.

---

## Follow-up de contrato e formalização

Quando houver aceite, mas a formalização não tiver sido concluída:

- trate primeiro impedimentos operacionais;
- verifique se o contrato foi recebido;
- facilite assinatura apenas dentro do procedimento real;
- explique documento quando necessário;
- não comemore decisão excessivamente;
- não trate silêncio como desistência;
- não repita argumentos comerciais se a decisão já foi tomada;
- diferencie obstáculo operacional de nova objeção.

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

> "Lead respondeu a pré-qualificação, preciso dos laudos para confirmar a qualificação, já solicitei, ele sumiu, quero uma cadência de 15 dias com 5 contatos"

execute diretamente.

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

Declare uma ação observável.

Exemplo:

> Fazer com que o lead envie os documentos médicos necessários para concluir a análise preliminar.

Não use objetivo abstrato.

# 3. HIPÓTESES DE TRAVAMENTO

Quando o motivo não for conhecido, apresente somente hipóteses estratégicas relevantes.

Use tabela:

| Hipótese | Sinal possível | Como a cadência pode remover/testar | Status |
|---|---|---|---|

Em `Status`, use:

- confirmado;
- declarado;
- hipótese;
- não aplicável.

Não trate hipótese como diagnóstico.

# 4. ESTRATÉGIA DA CADÊNCIA

Explique:

- lógica;
- blocos;
- progressão;
- nível de insistência;
- alternância de profundidade;
- por que cada fase existe;
- quando bifurca;
- quando encerra.

Não transforme em teoria excessiva.

# 5. LINHA DO TEMPO

Use tabela:

| Momento | Função/obstáculo | Tipo | Contato | Respostas possíveis | Ação operacional |
|---|---|---|---|---|---|

Use datas e intervalos reais ou placeholders.

# 6. MENSAGENS PRONTAS

Para cada contato:

## CONTATO [NÚMERO] — [FUNÇÃO]

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
- os contatos trabalham obstáculos diferentes?
- houve repetição de cobrança?

### Cadência

- a lógica é estratégica e não apenas cronológica?
- o tempo organiza e o obstáculo orienta o conteúdo?
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
- objeção não declarada foi inventada?
- houve pressão?
- houve urgência comercial artificial?
- desconto ou condição foram inventados?
- silêncio foi tratado como desinteresse?
- decisão já tomada foi reaberta sem motivo?

### Jurídico

- houve promessa?
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
3. define uma ação pendente observável;
4. utiliza o histórico real;
5. separa fato, objeção e hipótese;
6. não inventa o motivo do silêncio;
7. organiza contatos por função estratégica;
8. não repete cobrança;
9. trabalha obstáculos diferentes;
10. respeita duração e frequência fornecidas;
11. não inventa cadência ausente;
12. admite fluxos curtos ou longos;
13. admite bifurcações quando objetivamente necessárias;
14. permite que respostas alterem a rota;
15. define saídas claras;
16. define intervenção humana quando necessária;
17. preserva fronteiras das outras skills;
18. usa a persona sem transformá-la em fato individual;
19. não inventa condição comercial ou operacional;
20. não cria pressão artificial;
21. não usa urgência jurídica como ferramenta comercial;
22. mantém mensagens proporcionais ao canal;
23. distribui utilidade ao longo da cadência;
24. encerra de forma respeitosa;
25. conduz o lead à próxima etapa real quando a ação pendente for concluída.

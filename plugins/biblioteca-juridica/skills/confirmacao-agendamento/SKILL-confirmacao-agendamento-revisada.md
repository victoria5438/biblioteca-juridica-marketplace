---
name: confirmacao-agendamento
description: Cria um fluxo de confirmação para atendimentos já agendados, com foco em comparecimento. Reforça data, horário e acesso, reduz barreiras práticas, obtém microcompromisso de presença e conduz remarcações, cancelamentos ou intervenções conforme as regras reais do escritório. Documentos e preparo só entram quando houver necessidade operacional configurada.
argument-hint: Informe o nicho jurídico, o handoff de /agendamento, o tipo de atendimento, data, horário, modalidade, profissional, duração, acesso, valor ou pagamento quando houver, política documental e políticas reais de confirmação, remarcação, cancelamento e atraso.
---

# Confirmação de Agendamento

## Função desta skill

Criar um roteiro de confirmação para um atendimento que já foi efetivamente agendado.

O atendimento pode ser:

- consulta jurídica;
- ligação;
- reunião;
- entrevista;
- análise inicial;
- conversa com especialista;
- reunião de fechamento;
- outro formato definido pelo escritório.

Adapte a nomenclatura ao formato real.

O objetivo desta skill é um só:

> fazer com que o atendimento já marcado aconteça com o mínimo de atrito possível.

A lógica central é:

> atendimento agendado  
> → data, horário e acesso claros  
> → barreiras práticas reduzidas  
> → microcompromisso de presença  
> → comparecimento, remarcação ou cancelamento corretamente tratados

Esta skill não deve:

- reabrir a venda;
- requalificar o lead;
- reconstruir a necessidade do atendimento;
- transformar confirmação em preparação técnica extensa;
- criar tarefas prévias que a operação não exige.

---

# Referências obrigatórias

Antes de produzir a saída:

1. leia `${CLAUDE_PLUGIN_ROOT}/references/core-cognitivo.md`;
2. leia `${CLAUDE_PLUGIN_ROOT}/references/core-escrita-oralidade.md`;
3. utilize o handoff produzido por `/agendamento`, quando disponível;
4. utilize os dados reais registrados na agenda, CRM ou histórico;
5. utilize somente políticas e condições efetivamente informadas pelo escritório;
6. preserve as fronteiras de `/agendamento`, `/recuperacao-no-show`, `/roteiro-consulta` e `/follow-up`.

O Mapeamento de Persona, quando disponível, pode orientar linguagem, receios e percepção de valor.

Ele não substitui os dados reais do agendamento.

Não execute novamente `/mapear-persona`.

---

# Ponto de partida obrigatório

Use esta skill somente quando já existir um agendamento efetivamente registrado.

No mínimo, deve haver:

- identificação do lead;
- tipo de atendimento;
- data;
- horário;
- modalidade;
- canal de contato.

Sempre que aplicável, use também:

- profissional responsável;
- duração;
- endereço, telefone ou link;
- fuso horário;
- valor;
- forma ou status de pagamento;
- política documental;
- política de remarcação e cancelamento;
- tolerância de atraso;
- instrução operacional de acesso.

A entrada preferencial é o handoff de `/agendamento`.

Se faltar dado indispensável para confirmar o atendimento, não invente.

Indique pendência operacional ou intervenção humana.

---

# Hierarquia das fontes

Consulte, nesta ordem:

1. instruções atuais do usuário;
2. handoff do agendamento;
3. agenda, CRM ou registro operacional real;
4. histórico real com o lead;
5. políticas reais do escritório;
6. características reais do atendimento;
7. Mapeamento de Persona;
8. critérios que justificaram o atendimento, apenas para um reforço de valor breve.

Quando houver conflito, o registro operacional atual prevalece sobre exemplos genéricos.

Nunca invente:

- data;
- horário;
- modalidade;
- profissional;
- duração;
- link;
- endereço;
- valor;
- pagamento;
- política documental;
- política de remarcação;
- política de cancelamento;
- tolerância de atraso;
- consequência de ausência ou não pagamento.

---

# Princípio central: confirmação cuida do comparecimento

A confirmação existe para responder, de forma simples:

- quando é o atendimento;
- como participar;
- com quem será, quando relevante;
- qual é o objetivo geral da conversa;
- como confirmar presença;
- o que fazer se precisar remarcar ou cancelar.

Somente acrescente preparo, documento, pagamento ou outra tarefa quando isso realmente existir na operação.

A regra é:

> não confunda melhorar a qualidade do atendimento com aumentar a fricção antes do atendimento.

A confirmação não deve espontaneamente transformar-se em:

- lista de documentos;
- segunda triagem;
- checklist jurídico;
- coleta de prova;
- nova venda;
- mini-consulta por WhatsApp.

---

# Regra de documentação

A política documental desta skill deve ser a mesma aplicada em `/agendamento`.

Use uma das três situações.

## Situação 1 — documento não necessário antes do atendimento

É o padrão quando o escritório não definiu outra regra.

Efeito:

- não mencionar documentos espontaneamente;
- não criar tarefa prévia;
- não registrar pendência documental;
- confirmar normalmente o atendimento.

Se o lead perguntar se precisa levar algo, responda de forma específica:

> Você não precisa preparar nenhum documento para essa conversa. Se algum documento for necessário depois, a equipe te orienta.

Adapte ao serviço e não use essa frase se existir regra diferente.

## Situação 2 — documento útil, mas não obrigatório

Use somente quando o escritório quiser que o lead tenha determinado documento em mãos, sem condicionar o atendimento.

Efeito:

- mencionar no máximo uma vez;
- usar linguagem leve;
- não cobrar novamente;
- não transformar em pendência;
- a ausência do documento não altera a confirmação nem impede o atendimento.

Exemplo estrutural:

> Se você já tiver [DOCUMENTO ÚTIL], pode deixar em mãos. Se não tiver, tudo bem.

## Situação 3 — documento obrigatório antes do atendimento

Use somente quando houver regra expressa do escritório para documento específico.

Efeito:

- informar a exigência de forma objetiva;
- explicar como obter ou enviar, quando houver procedimento real;
- se o lead tiver dificuldade, aplicar a regra real do escritório;
- não transformar a exigência em conclusão jurídica;
- não pedir ao SDR para validar tecnicamente o documento.

Se o documento não for obtido, seguir a regra real:

- manter o atendimento;
- remarcar;
- ou encaminhar à equipe.

Nunca:

- generalize a situação 3;
- peça senha de gov.br;
- trate a ausência de documento nas situações 1 ou 2 como impeditivo;
- lembre repetidamente documento útil;
- crie exigência que não veio da operação.

---

# Pagamento

Pagamento só entra na confirmação quando houver condição real relacionada ao atendimento.

Quando houver pagamento prévio, use somente:

- valor real;
- forma real;
- status real;
- instrução real;
- prazo real;
- consequência real do não pagamento.

Não invente:

- desconto;
- parcelamento;
- tolerância;
- reembolso;
- prazo;
- cobrança;
- cancelamento automático.

Não use tom acusatório.

Pagamento não deve dominar a mensagem de confirmação quando não for a barreira principal de comparecimento.

---

# Reforço de valor sem reabrir a venda

A confirmação pode lembrar, em uma frase, o que a pessoa obterá da conversa.

Use um eixo amplo e real.

Exemplos estruturais:

- “Na conversa, [PROFISSIONAL] vai entender melhor a sua situação, tirar suas dúvidas e orientar os próximos passos.”
- “O encontro será para aprofundar os pontos que apareceram na triagem e explicar o que faz sentido fazer depois.”
- “O objetivo da conversa é compreender melhor o caso e orientar os próximos passos.”

Não transforme esse trecho em:

- nova devolutiva jurídica;
- lista de benefícios;
- explicação de todos os critérios;
- demonstração de tudo que ainda precisa ser provado;
- argumento de pressão para comparecer.

Não repita toda a mensagem de `/agendamento`.

---

# Cadência e momentos de contato

Não invente cadência.

Use somente:

- momentos definidos pelo usuário;
- política real do escritório;
- configuração real da agenda, CRM ou automação;
- placeholders operacionais claros.

Quando o momento não estiver definido, use:

- `[MOMENTO DA CONFIRMAÇÃO]`;
- `[MOMENTO DO LEMBRETE]`;
- `[MOMENTO DO CONTATO FINAL]`;
- `[LIMITE PARA REMARCAÇÃO]`.

Não determine por conta própria:

- quantidade de lembretes;
- intervalo;
- horário de disparo;
- prazo de resposta;
- tolerância de atraso;
- cancelamento automático;
- encerramento por silêncio.

A skill cria a arquitetura das mensagens.

O escritório define a política operacional.

Não anuncie ao lead que novas mensagens virão.

Evite:

- “Amanhã vamos te lembrar novamente.”
- “Você receberá outro lembrete.”
- “Mais perto do horário enviaremos nova mensagem.”

---

# Regra de reação a respostas

Qualquer resposta do lead deve pausar o próximo disparo automático até que a resposta seja classificada e o estado atualizado.

A resposta pode:

- confirmar presença;
- abrir dúvida operacional;
- pedir remarcação;
- pedir cancelamento;
- revelar problema de acesso;
- revelar dificuldade com pagamento;
- revelar dificuldade com documento obrigatório;
- trazer informação jurídica nova;
- exigir intervenção humana.

Não continue enviando mensagens incompatíveis com o novo estado.

Silêncio não é confirmação.

---

# Arquitetura da confirmação principal

A mensagem principal deve ser curta e priorizar comparecimento.

## 1. Data e horário

Comece pelo compromisso marcado.

> Sua conversa está marcada para [DATA], às [HORÁRIO].

Inclua fuso quando necessário.

## 2. Modalidade e acesso

Informe como participar.

> Será [MODALIDADE], por [LINK / TELEFONE / ENDEREÇO].

## 3. Profissional e duração

Inclua somente quando forem informações reais e úteis.

> O atendimento será com [PROFISSIONAL] e dura cerca de [DURAÇÃO].

## 4. Valor da conversa

Use uma frase ampla.

> Na conversa, [PROFISSIONAL] vai entender melhor a sua situação, tirar suas dúvidas e orientar os próximos passos.

## 5. Documento ou preparo

Não inclua por padrão.

Aplique apenas:

- situação 2: uma linha leve, uma vez;
- situação 3: regra obrigatória real;
- outra orientação operacional indispensável.

## 6. Microcompromisso

Finalize com resposta simples.

> Pode me confirmar sua presença com um “confirmo”?

---

# Informações por camadas

Não coloque tudo na mesma mensagem se isso prejudicar leitura.

## Camada essencial

- data;
- horário;
- modalidade;
- acesso, quando necessário;
- resposta solicitada.

## Camada operacional

- profissional;
- duração;
- endereço;
- link;
- telefone;
- pagamento, quando aplicável;
- regra de remarcação, quando necessária.

## Camada condicional

Só existe quando aplicável:

- documento útil da situação 2;
- documento obrigatório da situação 3;
- instrução técnica de acesso;
- outra preparação realmente necessária.

A camada condicional não deve aparecer apenas porque “seria bom chegar preparado”.

---

# Estrutura obrigatória da saída

A entrega deve conter os blocos abaixo.

## 1. Leitura operacional do agendamento

Apresente para a equipe:

- tipo de atendimento;
- data e horário;
- fuso, quando necessário;
- modalidade e acesso;
- responsável;
- duração;
- eixo geral da conversa;
- status de pagamento, quando houver;
- política documental aplicada: situação 1, 2 ou 3;
- políticas de remarcação, cancelamento e atraso;
- possíveis barreiras práticas de comparecimento;
- dados ausentes que impedem a confirmação;
- status atual.

Não escreva esse bloco como mensagem ao lead.

## 2. Estratégia de confirmação

Explique brevemente:

- qual informação aparece primeiro;
- qual frase de valor será usada;
- qual microcompromisso será solicitado;
- quais barreiras práticas precisam ser reduzidas;
- se existe alguma orientação condicional real;
- quais respostas exigem handoff.

Não transforme em aula extensa.

## 3. Mensagem principal pronta

Crie a mensagem completa para o canal informado.

Ela deve:

- priorizar data e horário;
- informar acesso;
- reforçar o valor em uma frase;
- solicitar confirmação simples;
- usar política documental corretamente;
- ter parágrafos curtos;
- soar humana;
- não reabrir a venda.

Use placeholders apenas para dados ausentes, como:

- `[NOME]`;
- `[DATA]`;
- `[HORÁRIO]`;
- `[FUSO HORÁRIO]`;
- `[MODALIDADE]`;
- `[PROFISSIONAL]`;
- `[DURAÇÃO]`;
- `[LINK]`;
- `[TELEFONE]`;
- `[ENDEREÇO]`;
- `[VALOR]`;
- `[FORMA DE PAGAMENTO]`;
- `[DOCUMENTO ÚTIL]`;
- `[DOCUMENTO OBRIGATÓRIO]`.

Não invente esses dados.

## 4. Exemplo demonstrativo totalmente preenchido

Crie pelo menos um cenário fictício sem placeholders operacionais.

O exemplo deve:

- usar nome fictício;
- usar data, horário e modalidade fictícios;
- ter profissional fictício;
- demonstrar a política documental escolhida;
- reforçar o objetivo da conversa em uma frase;
- solicitar confirmação;
- ser explicitamente identificado como exemplo.

Use:

> Cenário demonstrativo: exemplo fictício criado para mostrar a estrutura da confirmação.

Não apresente como agendamento real.

## 5. Mensagens por momento configurado

Crie apenas mensagens para os momentos que existirem na operação.

### A. Confirmação após o agendamento

Use quando a confirmação imediata ainda não tiver sido enviada.

Se `/agendamento` já enviou a confirmação imediata e o próximo contato estiver próximo, não repita a mesma mensagem sem necessidade.

### B. Lembrete de acesso e preparo

Use somente se houver algo útil a transmitir.

Priorize:

- data e horário;
- link, endereço ou telefone;
- orientação técnica de acesso;
- pagamento real, quando necessário;
- documento apenas nas situações 2 ou 3.

Na situação 1, não crie lembrete documental.

### C. Confirmação de presença

Use no momento configurado.

Peça resposta simples.

### D. Contato próximo ao atendimento

Use somente se fizer parte da operação.

Seja breve.

Priorize:

- horário;
- acesso;
- localização;
- eventual instrução operacional imediata.

Não repita a explicação jurídica nem crie novas tarefas.

## 6. Bifurcações essenciais

Crie respostas prontas para as situações aplicáveis abaixo.

### A. Lead confirma

- agradeça;
- registre `CONFIRMADO`;
- repita apenas o indispensável;
- não reinicie venda ou qualificação.

### B. Lead pergunta como funciona

Explique objetivamente:

- formato;
- duração, quando conhecida;
- profissional;
- objetivo geral;
- acesso;
- preparo somente se houver algo real.

Não execute a consulta por mensagem.

### C. Lead pede remarcação

- reconheça o pedido;
- interrompa os lembretes do horário anterior;
- aplique a política real;
- retorne ao fluxo operacional de `/agendamento`;
- use apenas horários reais.

Depois da nova marcação, esta skill passa a usar os novos dados.

### D. Lead pede cancelamento

- confirme o pedido;
- informe política real quando aplicável;
- não pressione;
- registre `CANCELADO`;
- encerre os lembretes.

### E. Lead está em dúvida se poderá comparecer

- identifique a barreira prática;
- ofereça solução real;
- não trate incerteza como confirmação;
- registre o estado correto.

### F. Lead informa problema com link, telefone ou endereço

- corrija com dado real;
- envie acesso correto;
- se não puder resolver, encaminhe para humano;
- não invente alternativa.

### G. Lead pergunta sobre documentos

Aplique a política documental.

Situação 1:

- informar que não precisa preparar documento para participar;
- dizer que a equipe orientará depois se algo for necessário.

Situação 2:

- informar que o documento pode ajudar, mas não é obrigatório;
- não cobrar depois.

Situação 3:

- explicar a exigência real;
- explicar como obter ou enviar;
- se houver dificuldade, aplicar a regra real do escritório.

### H. Lead pergunta sobre pagamento

Informe somente:

- valor real;
- forma real;
- prazo real;
- status real;
- consequência real.

Não invente condição.

### I. Lead tenta antecipar a consulta pelo chat

Responda de forma útil sem substituir o atendimento.

Estrutura:

> Esse é um dos pontos que [PROFISSIONAL] vai avaliar na conversa, porque depende de [PONTO RELEVANTE].

Não improvise diagnóstico.

### J. Lead não responde

- mantenha `SEM RESPOSTA`;
- siga somente a cadência real configurada;
- não trate silêncio como confirmação;
- não crie disparos adicionais;
- não cancele automaticamente sem política expressa.

### K. Lead traz informação nova, urgente ou contraditória

- pause automação;
- registre a informação;
- encaminhe para humano ou profissional;
- não requalifique por conta própria;
- não improvise orientação jurídica.

### L. Documento obrigatório não foi obtido

Use somente na situação 3.

- não trate como falta de interesse;
- aplique a regra real do escritório;
- manter, remarcar ou encaminhar para equipe conforme configuração;
- se a regra não estiver definida, usar `INTERVENÇÃO HUMANA`.

---

# Modalidade online

Quando o atendimento for online, considere apenas informações úteis e reais:

- link;
- plataforma;
- necessidade de aplicativo;
- câmera ou áudio, quando realmente necessário;
- conexão;
- fuso horário;
- contato alternativo para falha técnica.

Não sobrecarregue com instruções óbvias.

---

# Modalidade presencial

Quando o atendimento for presencial, considere:

- endereço completo;
- sala, andar ou referência;
- acesso, quando relevante;
- estacionamento, quando informado;
- acessibilidade;
- documento de identificação somente quando realmente necessário.

Não invente informações logísticas.

---

# Estados de saída

A skill termina em um dos estados abaixo.

## 1. `CONFIRMADO`

Registrar:

- data;
- horário;
- modalidade;
- profissional;
- acesso;
- mensagens enviadas;
- orientações realmente aplicáveis.

## 2. `REMARCAÇÃO SOLICITADA`

Encerrar os lembretes do horário anterior e retornar ao fluxo operacional de `/agendamento`.

## 3. `CANCELADO`

Registrar cancelamento e encerrar os lembretes.

## 4. `SEM RESPOSTA`

Manter conforme a política real.

Se o horário passar e o atendimento não ocorrer, só encaminhar para `/recuperacao-no-show` depois de a falta estar operacionalmente confirmada.

## 5. `INTERVENÇÃO HUMANA`

Use quando houver:

- questão jurídica complexa;
- inconsistência de dados;
- urgência real;
- problema de acesso não resolvido;
- conflito sobre pagamento;
- documento obrigatório não obtido sem regra definida;
- nova informação que possa alterar o caso;
- necessidade de decisão profissional.

## 6. `ATENDIMENTO INICIADO`

Encerrar a automação de confirmação.

Não enviar lembretes durante ou depois do atendimento.

## 7. `NO-SHOW — ENCAMINHAR PARA /recuperacao-no-show`

Use somente após confirmação operacional da ausência.

A falta de documento nas situações 1 e 2 nunca altera o estado de confirmação.

---

# Handoff obrigatório

Ao final, apresente um resumo operacional com:

- identificação do lead;
- tipo de atendimento;
- data;
- horário;
- fuso, quando aplicável;
- modalidade;
- acesso;
- profissional;
- status de confirmação;
- status de pagamento, quando aplicável;
- política documental aplicada: situação 1, 2 ou 3;
- documento obrigatório recebido: somente na situação 3;
- dúvidas pendentes;
- mensagens enviadas;
- informação nova trazida pelo lead;
- próxima ação;
- status final.

Não registre documento útil da situação 2 como pendência.

Não inclua conclusão jurídica definitiva.

---

# O que esta skill não faz

Não use esta skill para:

- nutrir lead frio;
- pré-qualificar;
- qualificar;
- criar necessidade inicial do atendimento;
- realizar agendamento do zero;
- reabrir venda;
- executar consulta jurídica;
- produzir parecer;
- negociar honorários do caso;
- fazer fechamento de contrato;
- recuperar no-show antes de confirmar a ausência;
- acompanhar decisão depois do atendimento;
- criar follow-up comercial;
- inventar cadência;
- criar coleta documental extensa;
- validar documentos tecnicamente.

---

# Regras de escrita

As mensagens devem:

- ser breves;
- soar humanas;
- facilitar resposta;
- usar linguagem compatível com a persona;
- apresentar uma ação por vez;
- usar parágrafos curtos;
- evitar excesso de emojis;
- evitar juridiquês;
- evitar tom de cobrança;
- evitar tom de call center;
- priorizar informação operacional.

Prefira:

- “Sua conversa está marcada para...”;
- “Na conversa, [PROFISSIONAL] vai...”;
- “Pode me confirmar sua presença com um ‘confirmo’?”;
- “Se precisar remarcar, me avise por aqui.”;
- “Se já tiver [DOCUMENTO ÚTIL], pode deixar em mãos. Se não tiver, tudo bem.”, somente na situação 2.

Evite:

- “Não falte.”;
- “Contamos com sua pontualidade obrigatória.”;
- “Essa é sua última chance.”;
- “Se não responder, perderá a vaga.”;
- “Seu caso depende dessa consulta.”;
- “Precisamos que você se comprometa.”;
- “Prepare toda a documentação do caso.”;
- “Sem os documentos não conseguiremos conversar.”, salvo quando isso for literalmente a regra real da situação 3.

Use consequências de ausência, cancelamento, pagamento ou documento somente quando forem políticas reais e necessárias.

---

# Validação interna obrigatória

Antes de concluir, verifique:

## Escopo

- O atendimento já está agendado?
- A skill está cuidando de comparecimento?
- A skill não refez a qualificação?
- A skill não voltou a vender?
- A skill não antecipou a consulta?

## Dados

- Data, horário, modalidade e acesso são reais ou placeholders claros?
- Nenhum valor, link, endereço, profissional ou política foi inventado?
- O fuso foi considerado quando necessário?
- A política documental veio do handoff ou da operação?

## Documentação

- Na situação 1, documentos ficaram fora das mensagens, salvo pergunta do lead?
- Na situação 2, houve no máximo uma menção leve?
- Na situação 2, ausência de documento não virou pendência?
- Na situação 3, a exigência é realmente expressa e específica?
- A skill não pediu senha de gov.br?
- O SDR não foi instruído a validar documento?

## Mensagem

- Data e horário aparecem cedo?
- O valor da conversa está resumido em uma frase?
- O pedido de confirmação é simples?
- Não foram criadas tarefas desnecessárias?
- O texto reduz atrito?
- Não anuncia contatos futuros?
- Não cria culpa ou medo?

## Fluxo

- Qualquer resposta pausa o próximo disparo?
- Remarcação encerra o horário anterior?
- Cancelamento encerra os lembretes?
- Silêncio não foi tratado como confirmação?
- No-show só foi acionado depois de confirmado?
- Informação nova relevante leva a humano/profissional?

## Handoff

- O status final está claro?
- A política documental aplicada foi registrada?
- Só a situação 3 pode registrar documento obrigatório pendente?
- A próxima ação está definida?
- Os nomes das skills estão padronizados como `/agendamento` e `/confirmacao-agendamento`?

---

# Critérios de conclusão

A saída está completa somente quando:

- parte de um atendimento efetivamente agendado;
- organiza data, horário e acesso;
- reduz barreiras práticas;
- reforça o valor da conversa em uma frase;
- solicita microcompromisso simples;
- usa somente os momentos de contato existentes na operação;
- trata documentação conforme situação 1, 2 ou 3;
- não transforma preparo em barreira padrão;
- cobre confirmação, dúvida, remarcação, cancelamento e silêncio;
- não inventa política nem logística;
- pausa automação diante de resposta;
- prepara handoff objetivo;
- encaminha no-show somente após ausência confirmada.

A skill não existe para pressionar o lead.

Ela existe para tornar o comparecimento fácil, claro e previsível.

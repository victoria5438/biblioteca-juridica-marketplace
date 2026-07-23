---
name: confirmacao-agendamento
description: Cria um fluxo de confirmação e preparação para atendimentos já agendados. Reduz dúvidas e barreiras de comparecimento, reforça de forma breve o valor do encontro, organiza informações práticas e conduz confirmações, remarcações ou cancelamentos conforme as condições reais do escritório.
argument-hint: Informe o nicho jurídico, o handoff do agendamento, o tipo de atendimento, data, horário, modalidade, profissional, duração, valor ou pagamento, orientações necessárias e políticas reais de confirmação, remarcação e cancelamento.
---

# Confirmação de Consulta

## Função desta skill

Criar um roteiro de confirmação e preparação para um atendimento que já foi efetivamente agendado.

O atendimento pode ser:

- consulta jurídica;
- ligação;
- reunião;
- entrevista;
- análise inicial;
- conversa com especialista;
- outro formato definido pelo escritório.

“Consulta” é o nome guarda-chuva da etapa. Adapte a nomenclatura ao formato real.

Esta skill deve aumentar a probabilidade de comparecimento por meio de quatro movimentos:

1. confirmar com clareza o que foi marcado;
2. reduzir dúvidas e barreiras práticas;
3. reforçar de forma breve o valor do atendimento;
4. obter uma resposta operacional simples do lead.

A lógica central é:

> atendimento agendado  
> → informações organizadas  
> → expectativa clara  
> → barreiras reduzidas  
> → presença confirmada  
> → atendimento realizado

Esta skill não deve reabrir toda a venda nem reconstruir a necessidade da consulta desde o início.

---

## Ponto de partida obrigatório

Use esta skill somente quando já houver um agendamento registrado com, no mínimo:

- tipo de atendimento;
- data;
- horário;
- modalidade;
- identificação do lead;
- canal de contato.

Sempre que aplicável, use também:

- profissional responsável;
- duração;
- endereço ou link;
- fuso horário;
- valor;
- forma ou status de pagamento;
- orientações prévias;
- política de remarcação e cancelamento.

A entrada preferencial é o handoff produzido por `/agendamento-consulta`.

Se faltarem dados indispensáveis, não invente. Indique a pendência operacional ou solicite intervenção humana.

---

## Fontes que devem orientar a saída

Consulte, nesta ordem:

1. instruções atuais do usuário;
2. handoff do agendamento;
3. dados reais registrados na agenda ou no CRM;
4. histórico de mensagens com o lead;
5. condições reais do atendimento;
6. políticas reais de confirmação, atraso, remarcação e cancelamento;
7. orientações reais sobre documentos, acesso, endereço ou pagamento;
8. Mapeamento de Persona;
9. critérios de qualificação e eixo central que justificaram o atendimento.

Use também, quando disponíveis:

- `references/core-cognitivo.md`;
- `references/core-escrita-oralidade.md`.

O Mapeamento de Persona deve orientar linguagem, receios e percepção de valor. Ele não substitui os dados reais do agendamento.

---

## Princípio central

A confirmação deve remover atrito, não criar uma nova etapa comercial.

O lead precisa saber, com facilidade:

- quando será o atendimento;
- onde ou por qual canal ele acontecerá;
- com quem será;
- como participar;
- o que precisa preparar;
- o que acontecerá durante o encontro;
- como confirmar, remarcar ou cancelar.

A mensagem deve responder ao maior número possível dessas dúvidas sem ficar longa ou burocrática.

---

## Reforço de valor sem reabrir a venda

A skill pode lembrar brevemente por que o atendimento é relevante.

Use apenas um eixo central, retirado do handoff ou da qualificação.

Exemplos estruturais:

- “Nesse atendimento, serão revisados os pontos que apareceram na análise inicial sobre [EIXO CENTRAL].”
- “A conversa será voltada a esclarecer [QUESTÃO CENTRAL] e organizar os próximos passos.”
- “O objetivo é avaliar com mais cuidado [PONTO PRINCIPAL] e orientar quais caminhos podem ser considerados.”

Não repita toda a devolutiva da skill `/agendamento-consulta`.

Não use o lembrete para:

- pressionar;
- requalificar;
- prometer resultado;
- acrescentar urgência artificial;
- criar medo;
- iniciar consulta jurídica por mensagem.

---

## Cadência e momentos de contato

Não invente cadência.

Use somente:

- horários definidos pelo usuário;
- política real do escritório;
- configuração real do CRM, chatbot ou agenda;
- placeholders operacionais claros.

Quando o momento não estiver definido, use:

- `[MOMENTO DA CONFIRMAÇÃO]`;
- `[MOMENTO DO LEMBRETE]`;
- `[MOMENTO DO CONTATO FINAL]`;
- `[LIMITE PARA REMARCAÇÃO]`.

Não determine por conta própria:

- quantidade de lembretes;
- intervalo entre mensagens;
- horário de disparo;
- prazo de resposta;
- janela de tolerância;
- momento de cancelamento automático.

A skill deve criar a arquitetura das mensagens, não uma política operacional fictícia.

Não anuncie ao lead que outras mensagens serão enviadas.

Evite:

- “Amanhã vamos te lembrar novamente.”
- “Mais perto do horário enviaremos outra mensagem.”
- “Você receberá novos lembretes.”

---

## Estado e reação a respostas

Qualquer resposta do lead deve pausar o próximo disparo automático até que o estado seja atualizado.

Classifique a resposta em um destes estados:

- `CONFIRMADO`;
- `DÚVIDA OPERACIONAL`;
- `DÚVIDA SOBRE O ATENDIMENTO`;
- `REMARCAÇÃO SOLICITADA`;
- `CANCELAMENTO SOLICITADO`;
- `PAGAMENTO PENDENTE`;
- `DOCUMENTO OU PREPARO PENDENTE`;
- `PROBLEMA DE ACESSO`;
- `QUESTÃO JURÍDICA COMPLEXA`;
- `SEM RESPOSTA`;
- `INTERVENÇÃO HUMANA`.

Não continue enviando lembretes incompatíveis com o novo estado.

---

## Arquitetura da confirmação principal

A mensagem de confirmação deve conter, de forma natural, os elementos aplicáveis.

### 1. Identificação do atendimento

Informe o que foi marcado.

> Seu atendimento está marcado para [DATA], às [HORÁRIO].

### 2. Modalidade e acesso

Informe onde ou como ocorrerá.

> O atendimento será [ONLINE/PRESENCIAL/POR TELEFONE], por [LINK/CANAL/ENDEREÇO].

### 3. Profissional e duração

Inclua somente quando forem informações reais e úteis.

> Você será atendido por [PROFISSIONAL], e a previsão de duração é de [DURAÇÃO].

### 4. Expectativa clara

Explique brevemente o objetivo do encontro.

> A conversa será voltada a revisar [EIXO CENTRAL] e orientar os próximos passos possíveis.

### 5. Preparo necessário

Peça apenas o que for indispensável.

> Para o atendimento, tenha em mãos [DOCUMENTOS OU INFORMAÇÕES NECESSÁRIAS].

Não transforme a confirmação em coleta extensa de documentos.

### 6. Confirmação simples

Finalize com uma resposta fácil.

> Pode me confirmar sua presença com um “confirmo”?

Adapte ao canal e à operação real.

---

## Informações por camadas

Não coloque todas as informações em uma única mensagem quando isso prejudicar a leitura.

Organize em camadas:

### Camada essencial

- data;
- horário;
- modalidade;
- resposta solicitada.

### Camada operacional

- endereço ou link;
- profissional;
- duração;
- pagamento;
- instrução de acesso.

### Camada de preparo

- documentos;
- informações necessárias;
- orientações específicas.

A saída pode dividir essas camadas em mensagens curtas, desde que a sequência continue clara.

---

## Saída obrigatória

A resposta deve conter os blocos abaixo.

# 1. Leitura operacional do agendamento

Apresente para a equipe:

- tipo de atendimento;
- data e horário;
- modalidade;
- responsável;
- eixo central do atendimento;
- dados já disponíveis;
- dados ainda ausentes;
- possíveis barreiras de comparecimento;
- políticas aplicáveis;
- status atual.

Não escreva este bloco como mensagem ao lead.

---

# 2. Estratégia de confirmação

Explique brevemente:

- qual informação deve aparecer primeiro;
- qual eixo de valor será retomado;
- quais dúvidas práticas precisam ser eliminadas;
- qual microcompromisso será solicitado;
- quais bifurcações exigem resposta ou handoff.

Use um eixo central. Não crie um catálogo de benefícios ou riscos.

---

# 3. Mensagem principal pronta

Crie uma mensagem completa e adequada ao canal informado.

A mensagem deve:

- identificar o atendimento;
- trazer dados reais ou placeholders operacionais;
- reforçar brevemente o objetivo do encontro;
- reduzir incerteza;
- solicitar confirmação simples;
- ter parágrafos curtos;
- soar humana.

Use placeholders somente para dados ausentes, como:

- `[NOME]`;
- `[DATA]`;
- `[HORÁRIO]`;
- `[FUSO HORÁRIO]`;
- `[MODALIDADE]`;
- `[PROFISSIONAL]`;
- `[DURAÇÃO]`;
- `[LINK]`;
- `[ENDEREÇO]`;
- `[VALOR]`;
- `[FORMA DE PAGAMENTO]`;
- `[DOCUMENTOS NECESSÁRIOS]`.

Não invente esses dados.

---

# 4. Exemplo demonstrativo totalmente preenchido

Crie pelo menos um exemplo sem placeholders, usando dados fictícios e plausíveis.

O exemplo deve:

- usar nome fictício;
- informar data, horário e modalidade fictícios;
- retomar um eixo jurídico coerente com o nicho;
- solicitar confirmação;
- ser identificado internamente como cenário demonstrativo.

Use a indicação:

> Cenário demonstrativo: exemplo fictício criado para mostrar a estrutura da confirmação.

Não apresente o exemplo como agendamento real.

---

# 5. Mensagens por momento configurado

Crie mensagens para os momentos que existirem na operação informada.

## A. Confirmação após o agendamento

Use quando a confirmação imediata ainda não tiver sido enviada.

Se `/agendamento-consulta` já registrou e confirmou o horário, não repita a mesma mensagem sem necessidade.

## B. Lembrete de preparação

Use quando houver orientação útil a transmitir.

Pode incluir:

- documentos;
- endereço;
- link;
- instruções de acesso;
- pagamento;
- duração;
- pontualidade.

Não invente o momento do disparo.

## C. Confirmação de presença

Use no momento configurado pelo escritório.

Peça uma resposta simples.

## D. Contato próximo ao atendimento

Use somente se fizer parte da operação real.

Seja breve e priorize acesso, localização e horário.

Não repita toda a explicação jurídica.

---

# 6. Bifurcações essenciais

Crie respostas prontas para, no mínimo, estas situações.

## A. Lead confirma

- agradeça;
- atualize o estado para `CONFIRMADO`;
- repita apenas a informação operacional indispensável;
- não reinicie a venda.

## B. Lead pergunta como funciona

Explique objetivamente:

- formato;
- duração, quando conhecida;
- profissional;
- objetivo;
- como acessar;
- o que preparar.

Não realize a consulta por mensagem.

## C. Lead pede remarcação

- reconheça o pedido;
- interrompa os lembretes do horário anterior;
- aplique a política real;
- encaminhe para a parte operacional de `/agendamento-consulta`;
- use apenas horários reais.

Depois da nova marcação, reinicie esta skill com os novos dados.

## D. Lead pede cancelamento

- confirme o pedido;
- informe a política real, quando aplicável;
- não pressione;
- atualize o status para `CANCELADO`;
- encerre os lembretes.

## E. Lead está em dúvida se poderá comparecer

- identifique a barreira prática;
- ofereça solução real;
- não trate incerteza como confirmação;
- registre o status correto.

## F. Lead informa problema com link, telefone ou endereço

- corrija a informação;
- envie o acesso real;
- encaminhe para humano quando não puder resolver;
- não invente alternativa.

## G. Lead pergunta sobre documentos

Informe apenas o preparo realmente exigido.

Diferencie:

- documento obrigatório para participar;
- documento útil para análise;
- documento que poderá ser enviado depois.

Não crie exigências inexistentes.

## H. Lead pergunta sobre pagamento

Informe apenas:

- valor real;
- forma real de pagamento;
- prazo real;
- status conhecido;
- política real.

Não invente desconto, parcelamento, reembolso ou tolerância.

## I. Lead tenta antecipar a consulta pelo chat

Responda de forma útil, mas preserve a fronteira:

> Essa é uma das questões que o profissional vai analisar no atendimento, porque a resposta depende de [PONTO RELEVANTE].

Não dê diagnóstico improvisado.

## J. Lead não responde

- mantenha o estado `SEM RESPOSTA`;
- siga somente a cadência real configurada;
- não trate silêncio como confirmação;
- não crie disparos adicionais;
- não cancele automaticamente sem política expressa.

## K. Lead traz situação urgente ou informação que altera o caso

- pause a automação;
- encaminhe para atendimento humano;
- não espere o horário agendado quando houver risco real que exija análise imediata;
- não improvise orientação jurídica.

---

## Pagamento e documentos

Pagamento e documentos podem afetar o comparecimento, mas não devem dominar a comunicação.

### Quando houver pagamento prévio

Informe:

- condição real;
- status real;
- instrução de pagamento real;
- prazo real;
- consequência real do não pagamento.

Não use “pagamento pendente” como acusação.

### Quando houver documentos necessários

Explique:

- quais documentos;
- por qual canal;
- até quando, se houver prazo real;
- se o envio é obrigatório ou apenas recomendado.

Não presuma que o lead não possui ou não enviou determinado documento.

---

## Modalidade online

Quando o atendimento for online, considere:

- link real;
- plataforma;
- necessidade de aplicativo;
- câmera ou áudio, quando aplicável;
- conexão;
- ambiente reservado;
- fuso horário;
- contato alternativo para falha técnica.

Não sobrecarregue a mensagem com instruções óbvias.

---

## Modalidade presencial

Quando o atendimento for presencial, considere:

- endereço completo;
- sala, andar ou referência;
- estacionamento ou acesso, quando relevante e real;
- documento de identificação, quando necessário;
- orientação de chegada;
- acessibilidade.

Não invente informações logísticas.

---

## Estados de saída

A skill termina em um destes estados.

### 1. Presença confirmada

Registrar:

- status `CONFIRMADO`;
- data e horário;
- modalidade;
- profissional;
- orientações enviadas;
- pendências existentes.

### 2. Remarcação solicitada

Interromper o fluxo atual e encaminhar para a parte operacional de `/agendamento-consulta`.

### 3. Atendimento cancelado

Registrar o cancelamento e encerrar os lembretes.

### 4. Sem resposta

Manter o status conforme a política real.

Se o horário passar e o atendimento não ocorrer, encaminhar para `/recuperacao-no-show` somente depois de o no-show estar operacionalmente confirmado.

### 5. Intervenção humana

Encaminhar quando houver:

- questão jurídica complexa;
- inconsistência de dados;
- problema operacional não resolvido;
- urgência real;
- conflito sobre pagamento ou política;
- necessidade de decisão profissional.

### 6. Atendimento iniciado

Encerrar a automação de confirmação.

Não enviar lembretes durante ou depois do atendimento.

---

## Handoff obrigatório

Ao final, apresente um resumo operacional com:

- identificação do lead;
- tipo de atendimento;
- data;
- horário;
- fuso, quando aplicável;
- modalidade;
- profissional;
- status de confirmação;
- status de pagamento;
- documentos ou preparo;
- dúvidas pendentes;
- orientações enviadas;
- próxima ação;
- status final.

Use um dos estados:

- `CONFIRMADO`;
- `REMARCAÇÃO SOLICITADA`;
- `CANCELADO`;
- `SEM RESPOSTA`;
- `INTERVENÇÃO HUMANA`;
- `ATENDIMENTO INICIADO`;
- `NO-SHOW — ENCAMINHAR PARA /recuperacao-no-show`.

---

## O que esta skill não faz

Não use esta skill para:

- nutrir lead frio;
- qualificar lead;
- criar a necessidade inicial do atendimento;
- realizar novo agendamento do zero;
- executar consulta jurídica;
- produzir parecer;
- negociar honorários do caso;
- fazer fechamento de contrato;
- recuperar no-show antes de a ausência estar confirmada;
- acompanhar decisão depois do atendimento;
- enviar mensagens depois de cancelamento;
- criar cadência não informada.

---

## Regras de escrita

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
- evitar tom de call center.

Prefira:

- “Seu atendimento está marcado para...”
- “O objetivo da conversa é...”
- “Para participar, basta...”
- “Pode me confirmar sua presença?”
- “Caso precise remarcar, me avise por aqui.”

Evite:

- “Não falte.”
- “Contamos com sua pontualidade obrigatória.”
- “Essa é sua última chance.”
- “Se você não responder, perderá a vaga.”
- “Seu caso depende dessa consulta.”
- “Precisamos que você se comprometa.”

Use consequências de ausência ou cancelamento apenas quando forem políticas reais e necessárias.

---

## Validação interna obrigatória

Antes de concluir, verifique:

### Escopo

- O atendimento já está agendado?
- A skill não refez a qualificação?
- A skill não tentou vender novamente a consulta?
- A skill não executou orientação jurídica individual?

### Dados

- Data, horário, modalidade e acesso são reais ou placeholders claros?
- Nenhum valor, link, endereço, profissional ou política foi inventado?
- O fuso foi considerado quando necessário?
- Não foi presumida ausência de pagamento ou documento?

### Mensagem

- A informação essencial aparece primeiro?
- Há apenas um eixo central de valor?
- A resposta solicitada é simples?
- O texto reduz dúvidas práticas?
- A mensagem não anuncia contatos futuros?
- A mensagem não cria culpa ou medo?

### Fluxo

- Qualquer resposta pausa o próximo disparo?
- Os estados são objetivos?
- Remarcação interrompe o horário anterior?
- Cancelamento encerra os lembretes?
- Silêncio não foi tratado como confirmação?
- No-show só é acionado depois de confirmado?

### Handoff

- O status final está claro?
- As pendências estão registradas?
- A próxima ação está definida?

---

## Critérios de conclusão

A saída está completa somente quando:

- parte de um atendimento efetivamente agendado;
- organiza os dados essenciais;
- reduz barreiras práticas;
- reforça brevemente o valor do encontro;
- solicita confirmação simples;
- cria mensagens para os momentos reais da operação;
- cobre confirmação, dúvida, remarcação, cancelamento e silêncio;
- não inventa cadência nem informações operacionais;
- encerra mensagens incompatíveis com o novo estado;
- prepara handoff objetivo;
- encaminha no-show somente quando a ausência estiver confirmada.

A skill não existe para pressionar o lead.

Ela existe para tornar o comparecimento fácil, claro e previsível.


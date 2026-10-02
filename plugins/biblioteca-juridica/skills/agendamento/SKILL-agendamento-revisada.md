---
name: agendamento
description: Cria um roteiro de conversão para transformar um lead previamente qualificado em um atendimento efetivamente agendado, com devolutiva curta, valor claro da próxima conversa e mínimo de fricção. Parte do relato já coletado, respeita a classificação anterior, evita segunda pré-qualificação e trata documentação prévia apenas conforme regra expressa da operação.
argument-hint: Informe o nicho jurídico, o Mapeamento de Persona, o handoff da pré-qualificação, o tipo de atendimento oferecido, a política documental e as condições reais de agenda. Inclua as respostas individuais da pré-qualificação quando estiverem disponíveis.
---

# Agendamento

## Função desta skill

Transformar um lead que já possui elementos suficientes para avançar em um atendimento efetivamente agendado.

O atendimento pode assumir diferentes formatos:

- consulta jurídica;
- ligação;
- reunião;
- entrevista;
- análise inicial;
- conversa com especialista;
- reunião de fechamento;
- outro formato definido pelo escritório.

“Consulta” ou “reunião” são nomes possíveis da etapa. Adapte a nomenclatura ao formato real.

O objetivo desta skill é um só:

> converter um lead suficientemente qualificado em um atendimento marcado, com o mínimo de atrito necessário.

A lógica central é:

> lead qualificado  
> → devolutiva curta  
> → valor da conversa  
> → horários reais  
> → escolha  
> → agendamento registrado  
> → handoff para `/confirmacao-agendamento`

A skill não deve criar uma segunda pré-qualificação antes de permitir que o lead converse com o profissional.

---

# Referências obrigatórias

Antes de produzir a saída:

1. leia `${CLAUDE_PLUGIN_ROOT}/references/core-cognitivo.md`;
2. leia `${CLAUDE_PLUGIN_ROOT}/references/core-escrita-oralidade.md`;
3. utilize o Mapeamento de Persona Jurídica fornecido pelo usuário ou disponível na conversa;
4. utilize o handoff da pré-qualificação, quando disponível;
5. priorize informações reais do escritório, do atendimento e da agenda;
6. preserve as fronteiras das skills `/pre-qualificacao` e `/confirmacao-agendamento`.

Não execute novamente a skill `/mapear-persona`.

Não refaça a pré-qualificação.

---

# Princípio central: qualificação comercial não é prova

A etapa de agendamento responde:

> Há elementos suficientes para justificar a conversa e marcar o próximo passo?

A resposta pode se apoiar no relato do lead e na classificação produzida pela pré-qualificação.

A etapa de prova ou validação responde outra pergunta:

> As informações estão demonstradas e o caso se confirma após análise profissional?

Essas duas decisões não devem ser confundidas.

Portanto:

- fato relatado não precisa estar documentalmente comprovado para justificar o agendamento;
- pendência de prova não é, por si só, pendência de qualificação;
- o SDR não deve conferir documentos para decidir se oferece horário;
- a reunião pode existir justamente para aprofundar fatos, esclarecer dúvidas, identificar provas necessárias e definir próximos passos;
- o nível de evidência exigido deve ser proporcional à decisão desta etapa.

Se a operação do escritório exigir determinado documento antes do atendimento, respeite essa regra. Não generalize essa exigência para outros escritórios, serviços ou leads.

---

# Ponto de partida obrigatório

Use esta skill somente quando:

- o lead já passou pela pré-qualificação ou por processo equivalente;
- há elementos suficientes para justificar o atendimento;
- a classificação permite avanço, mesmo que existam pontos a aprofundar;
- ainda não há data e horário efetivamente marcados.

Podem entrar nesta skill, conforme a nomenclatura da operação:

- `AVANÇA`;
- `AVANÇA COM PENDÊNCIAS`;
- `QUALIFICADO`;
- `APTO PARA AGENDAMENTO`;
- outro status equivalente informado pelo escritório.

Considere como premissa:

> A decisão de que vale conversar com esse lead já foi tomada.

Não reabra essa decisão sem fato novo relevante.

Faça pergunta adicional somente quando ela for indispensável para:

- escolher o formato correto do atendimento;
- resolver inconsistência que impeça o agendamento;
- identificar urgência ou necessidade de intervenção humana;
- concluir uma ação operacional necessária para registrar o horário.

Não pergunte apenas porque seria útil saber mais sobre o caso.

---

# Hierarquia das fontes

Consulte, nesta ordem:

1. instruções atuais do usuário;
2. regras e políticas reais do escritório;
3. handoff da pré-qualificação;
4. respostas individuais do lead;
5. características reais do atendimento;
6. condições reais de agenda;
7. Mapeamento de Persona;
8. histórico relevante da conversa.

O Mapeamento de Persona orienta a estratégia e a linguagem.

O relato individual do lead e as regras reais da operação prevalecem sobre exemplos genéricos.

Não invente:

- fatos individuais;
- horários;
- datas;
- duração;
- profissional;
- valor;
- modalidade;
- política documental;
- política de pagamento;
- política de cancelamento ou remarcação.

---

# Quando as respostas individuais não estiverem disponíveis

A ausência das respostas literais não impede a criação do roteiro.

Nesse caso:

1. utilize apenas os critérios mínimos que, segundo o Mapeamento, sustentam o avanço;
2. escreva a mensagem principal de forma aplicável ao nicho, sem atribuir falas específicas ao lead;
3. crie um cenário demonstrativo separado, claramente fictício;
4. não simule que houve análise de documento ou conversa que não foi fornecida.

Evite:

- “Você disse que...”;
- “Como você contou...”;
- “Pelo documento que você enviou...”;
- “Como conversamos...”.

Quando não houver histórico individual, prefira construções como:

- “Pelos critérios avaliados até aqui...”;
- “A triagem inicial indicou elementos que justificam uma conversa...”;
- “Os elementos iniciais apontam que vale aprofundar a situação...”.

Não invente fatos adicionais para tornar a mensagem mais persuasiva.

---

# Regra de documentação

Documentação não é barreira padrão para o agendamento.

A skill deve trabalhar com uma das três situações abaixo.

## Situação 1 — documento não necessário antes do atendimento

É o padrão quando o escritório não definiu outra regra.

Efeito:

- agendar normalmente;
- não criar tarefa documental;
- não mencionar documento espontaneamente;
- se algum documento for necessário, ele pode ser solicitado no atendimento ou em etapa posterior.

## Situação 2 — documento útil, mas não obrigatório

Use somente quando o escritório quiser que o lead tenha determinado documento em mãos, sem condicionar o atendimento.

Efeito:

- agendar normalmente;
- mencionar no máximo uma vez e de forma leve;
- não transformar em pendência;
- não cobrar novamente;
- a ausência do documento não altera a classificação nem impede o atendimento.

Exemplo estrutural:

> Se você já tiver [DOCUMENTO ÚTIL], pode deixar em mãos. Se não tiver, tudo bem.

## Situação 3 — documento obrigatório antes do atendimento

Use somente por regra expressa do escritório e para documento específico.

Efeito:

- o convite e a escolha de horário continuam podendo acontecer;
- após a escolha, informe a exigência real;
- explique o procedimento real de obtenção ou envio, se houver;
- se o documento não puder ser obtido, aplique a regra real do escritório: manter, remarcar ou levar à equipe.

Nunca:

- generalize a situação 3;
- invente exigência documental;
- peça senha de gov.br;
- peça ao SDR para validar o conteúdo do documento;
- trate falta de documento como “lead não está pronto”, salvo se houver regra operacional específica e o registro deixar claro que é impedimento operacional, não desqualificação.

---

# Objetivo estratégico da devolutiva

A devolutiva existe para responder apenas ao necessário antes da escolha de horário.

Ela deve mostrar:

1. por que faz sentido conversar;
2. o que a pessoa pode obter da conversa;
3. como avançar agora.

Não transforme a devolutiva em aula, parecer ou lista de tudo que ainda precisa ser provado.

## 1. Por que faz sentido conversar

Use um ou dois fatos relevantes do relato, quando disponíveis.

Exemplo estrutural:

> Pelo que você contou, [FATO 1] e [FATO 2]. Esses pontos fazem sentido serem avaliados com mais profundidade.

Se a operação permitir e for útil, traduza isso para uma possibilidade geral, sempre em linguagem condicional.

## 2. Valor da conversa

Descreva a reunião de forma ampla e concreta.

Ela pode servir para:

- entender melhor a situação;
- aprofundar os pontos relevantes da triagem;
- esclarecer dúvidas;
- avaliar se o caso se encaixa;
- explicar próximos passos;
- identificar quais documentos ou provas serão necessários, se forem;
- apresentar como o escritório pode atuar, quando aplicável;
- conduzir contratação ou fechamento, quando essa for a função real da reunião.

Não trate análise documental como valor central da reunião, salvo quando esse for efetivamente o formato contratado ou definido pela operação.

## 3. Convite com próximo passo concreto

Quando horários reais estiverem disponíveis, ofereça-os na própria mensagem.

Padrão preferido:

> Tenho estes horários: [HORÁRIOS DISPONÍVEIS]. Qual fica melhor para você?

Evite criar uma etapa intermediária desnecessária como:

> “Posso te mostrar os horários?”

Use esse tipo de CTA somente quando não houver disponibilidade real para apresentar ou quando a operação tiver razão específica para fazê-lo.

---

# Pendências da pré-qualificação

Pendência não é sinônimo de tarefa para o lead resolver antes da reunião.

Se o lead avançou com algum ponto em aberto:

- agende normalmente;
- registre o ponto para aprofundamento;
- quando útil, diga que ele será esclarecido na conversa;
- não mande o lead buscar prova ou resposta antes do agendamento, salvo regra operacional expressa.

Exemplo estrutural:

> Alguns detalhes, como [PONTO EM ABERTO], podem ser esclarecidos com [PROFISSIONAL] na conversa.

Não use um parágrafo obrigatório de “limite da triagem”.

A cautela jurídica pode aparecer em palavras como:

- “pode”;
- “faz sentido avaliar”;
- “há elementos que justificam conversar”;
- “vale aprofundar”.

Não precisa aparecer como uma lista do que ainda não está comprovado.

---

# Urgência real

Urgência pode alterar prioridade, mas não deve ser fabricada para conversão.

Use somente quando houver fato concreto e registrado.

Exemplos genéricos:

- prazo real;
- audiência próxima;
- perícia marcada;
- negativa recente;
- risco de perda de oportunidade processual;
- outro marco objetivo informado no Mapeamento ou pelo usuário.

Quando houver urgência real:

- sinalize prioridade;
- não invente prazo;
- não use medo;
- não transforme urgência jurídica em pressão comercial.

---

# Estrutura obrigatória da saída

A entrega deve conter oito blocos:

1. leitura estratégica do momento do lead;
2. política documental aplicável;
3. estrutura da devolutiva e convite;
4. mensagem principal pronta;
5. exemplo demonstrativo;
6. bifurcações essenciais;
7. fluxo operacional e estados de saída;
8. handoff.

---

# 1. Leitura estratégica do momento do lead

Apresente de forma interna e objetiva:

- condição de entrada;
- status de qualificação;
- um ou dois fatos que sustentam o avanço, quando disponíveis;
- possibilidade que pode ser mencionada, se aplicável;
- valor real do atendimento;
- pontos a aprofundar na reunião;
- urgência real registrada, se houver;
- receios ou objeções declaradas, se houver;
- melhor ângulo de convite;
- política documental do escritório;
- informações operacionais ainda ausentes.

Não trate “pontos a aprofundar” como tarefas prévias do lead.

Não transforme esse bloco em nova triagem.

---

# 2. Política documental aplicável

Declare qual das três situações está sendo usada:

- situação 1 — documento não necessário antes do atendimento;
- situação 2 — documento útil, mas não obrigatório;
- situação 3 — documento obrigatório por regra expressa.

Se a política não tiver sido informada, use:

> `[POLÍTICA DOCUMENTAL A DEFINIR COM O ESCRITÓRIO]`

Não presuma situação 2 ou 3.

---

# 3. Estrutura da devolutiva e convite

Mostre a lógica aplicada:

> retomada curta  
> → um ou dois fatos relevantes  
> → valor da reunião  
> → horários reais

Quando não houver respostas individuais:

> contextualização genérica  
> → razão para conversar  
> → valor da reunião  
> → horários reais

Não inclua como etapa obrigatória:

- “o que ainda precisa ser confirmado”;
- “documentos que faltam”;
- “provas que o lead precisa obter”;
- nova rodada de qualificação.

---

# 4. Mensagem principal pronta

Crie uma mensagem curta, natural e específica para o nicho.

Quando houver relato individual, a mensagem deve:

1. agradecer ou retomar brevemente;
2. mencionar um ou dois fatos relevantes do relato;
3. dizer por que faz sentido conversar, sem concluir direito;
4. explicar em uma ou duas frases o valor da reunião;
5. oferecer horários reais na mesma mensagem, quando disponíveis.

Exemplo estrutural:

> [NOME], obrigado por responder.  
> Pelo que você contou, [FATO 1] e [FATO 2]. Esses pontos fazem sentido serem avaliados com mais profundidade.  
>  
> O próximo passo é uma conversa [MODALIDADE] com [PROFISSIONAL]. [ELE/ELA] vai entender melhor a sua situação, esclarecer suas dúvidas e te orientar sobre os próximos passos.  
>  
> Tenho estes horários: [HORÁRIOS DISPONÍVEIS]. Qual fica melhor para você?

Se o nicho permitir uma explicação breve e útil sobre o serviço, inclua-a sem transformar a mensagem em aula.

Não use placeholders jurídicos vagos quando o Mapeamento permitir escrever o conteúdo real.

Use placeholders para dados operacionais ausentes:

- `[NOME]`;
- `[PROFISSIONAL]`;
- `[MODALIDADE]`;
- `[DURAÇÃO]`;
- `[VALOR]`;
- `[FORMA DE PAGAMENTO]`;
- `[ENDEREÇO]`;
- `[LINK]`;
- `[HORÁRIOS DISPONÍVEIS]`.

Não deixe comandos internos na mensagem final.

---

# 5. Exemplo demonstrativo

Crie pelo menos um cenário totalmente fictício para demonstrar a estrutura.

Identifique:

> Cenário demonstrativo: exemplo fictício criado a partir dos critérios de qualificação do nicho.

O exemplo deve:

- usar fatos fictícios coerentes com o Mapeamento;
- mostrar um lead suficientemente qualificado;
- evitar prova documental inventada;
- explicar o valor da conversa;
- oferecer horários fictícios claramente demonstrativos;
- terminar com escolha simples.

Não apresente o cenário como caso real.

---

# 6. Bifurcações essenciais

Crie respostas prontas para, no mínimo, as situações abaixo.

## A. Lead escolhe um horário

Siga direto para o fluxo operacional.

Não repita a devolutiva.

## B. Lead pergunta como funciona

Explique objetivamente:

- formato;
- duração, quando conhecida;
- profissional;
- objetivo;
- o que a pessoa poderá obter da conversa;
- como acessar, quando aplicável.

Depois, ofereça horários reais.

Não realize a consulta por mensagem.

## C. Lead pergunta o valor

Informe apenas a condição real.

Depois, recoloque o valor no contexto da entrega da reunião.

Não esconda preço conhecido.

Não invente desconto, parcelamento ou gratuidade.

## D. Lead pede para resolver tudo pelo WhatsApp

Explique que a etapa atual foi suficiente para triagem, mas que a conversa permite aprofundar e orientar com mais segurança.

Não use superioridade.

Não transforme a resposta em nova triagem.

## E. Lead demonstra receio ou insegurança

Primeiro identifique o receio real quando ele não estiver claro.

Responda somente ao ponto indicado.

Não introduza espontaneamente medo de empresa, golpe, preço ou documentos sem sinal do lead.

## F. Lead diz que precisa pensar

Pergunte brevemente qual é o ponto que ele quer avaliar, quando isso ajudar.

Responda uma vez ao motivo real.

Se não quiser avançar agora:

- registre o motivo;
- respeite;
- não inicie sequência de pressão.

Falta de documento, isoladamente, não deve gerar “não está pronto”.

## G. Lead não pode nos horários oferecidos

Pergunte qual período funciona melhor.

Ofereça apenas horários reais.

Se não houver disponibilidade compatível, registre indisponibilidade operacional e encaminhe à equipe.

## H. Lead prefere outro formato

Adapte somente se o escritório realmente oferecer.

## I. Lead recusa

Respeite e encerre.

Não pressione.

## J. Lead traz informação jurídica nova, contraditória ou urgente

Pause o fluxo.

Encaminhe para revisão humana.

Não improvise diagnóstico.

## K. Lead pergunta se precisa levar ou enviar algo

Aplique a política documental.

Situação 1:

> Não precisa preparar nenhum documento para essa conversa. Se algum for útil depois, [PROFISSIONAL] te orienta.

Situação 2:

> Não é obrigatório. Se você já tiver [DOCUMENTO ÚTIL], pode deixar em mãos. Se não tiver, tudo bem.

Situação 3:

> Para essa conversa, o escritório pede [DOCUMENTO OBRIGATÓRIO], porque [MOTIVO REAL]. [INSTRUÇÃO REAL]. Se tiver dificuldade, me avise que eu vejo com a equipe.

Nunca invente a situação 3.

---

# 7. Fluxo operacional do agendamento

Quando horários reais já estiverem disponíveis, a mensagem principal deve oferecê-los.

A sequência padrão é:

1. enviar devolutiva curta com horários;
2. receber a escolha;
3. confirmar modalidade, quando ainda necessário;
4. informar condição real do atendimento, quando aplicável;
5. coletar somente dados operacionais indispensáveis;
6. registrar o agendamento;
7. enviar confirmação imediata do que foi combinado;
8. aplicar orientação documental somente conforme a situação 2 ou 3;
9. preparar handoff para `/confirmacao-agendamento`.

A confirmação imediata desta skill serve apenas para registrar o combinado.

Exemplo:

> Combinado, [NOME]. Seu atendimento ficou marcado para [DATA], às [HORÁRIO], [MODALIDADE], com [PROFISSIONAL].

Inclua link, endereço ou instrução de acesso somente quando forem reais e já estiverem disponíveis.

Lembretes posteriores, confirmação de presença e preparação pertencem à skill `/confirmacao-agendamento`.

## Quando os horários ainda não estiverem disponíveis

Não invente agenda.

Use um CTA operacional simples, por exemplo:

> Qual período costuma funcionar melhor para você?

ou

> Vou verificar os horários disponíveis e te apresentar as opções reais.

Não crie disponibilidade fictícia.

---

# Dados que podem ser coletados

Colete somente o necessário para registrar o atendimento.

Exemplos:

- nome;
- telefone;
- e-mail, se necessário;
- modalidade;
- data;
- horário;
- informação operacional indispensável.

Não use esta etapa para:

- coletar relato completo;
- pedir novamente informações já registradas;
- solicitar documentação extensa;
- validar prova;
- realizar segunda triagem;
- pedir dados sensíveis sem necessidade;
- montar estratégia jurídica;
- antecipar a consulta.

---

# Estados de saída

A skill termina em um estado claro.

## 1. `AGENDADO — ENCAMINHAR PARA /confirmacao-agendamento`

Há definição de:

- tipo de atendimento;
- modalidade;
- data;
- horário;
- profissional, quando aplicável;
- condição de pagamento, quando aplicável;
- registro operacional.

## 2. `RECUSOU`

Registrar e encerrar.

## 3. `NÃO ESTÁ PRONTO`

Use somente quando o lead expressar que não quer ou não consegue avançar agora por motivo comercial ou operacional real, como:

- horário;
- custo;
- quer pensar;
- precisa consultar terceiro;
- outro impedimento declarado.

Não use “falta de documento” como motivo padrão.

## 4. `INDISPONIBILIDADE OPERACIONAL`

Não há opção real compatível com o pedido do lead.

Encaminhar à equipe.

## 5. `INTERVENÇÃO HUMANA`

Use quando houver questão complexa, urgência real, problema operacional não resolvido ou necessidade de decisão profissional.

## 6. `NOVA INFORMAÇÃO — REVISÃO`

Fato novo pode alterar a classificação anterior.

Pause e encaminhe para revisão.

## 7. `PENDÊNCIA OPERACIONAL DOCUMENTAL`

Use somente na situação 3, se a operação exigir determinado documento e houver impedimento para obtê-lo.

Esse status não equivale a desqualificação.

O agendamento pode continuar registrado conforme a política real do escritório.

---

# Handoff obrigatório

Quando houver agendamento, apresente resumo operacional com:

- identificação do lead;
- nicho ou assunto;
- status vindo da pré-qualificação;
- relato relevante do lead, marcado como não validado quando aplicável;
- pontos a aprofundar no atendimento;
- urgência real registrada, se houver;
- receios ou objeções declaradas, se houver;
- tipo de atendimento;
- modalidade;
- data;
- horário;
- profissional;
- duração;
- valor e pagamento, quando aplicável;
- política documental aplicada: situação 1, 2 ou 3;
- documento mencionado espontaneamente pelo lead, se houver, apenas como informação;
- observação operacional relevante;
- status: `AGENDADO — ENCAMINHAR PARA /confirmacao-agendamento`.

Não inclua conclusão jurídica definitiva.

Não transforme documento mencionado espontaneamente em requisito.

---

# O que esta skill não faz

Não use esta skill para:

- captar lead frio;
- nutrir lead sem interação;
- realizar pré-qualificação completa;
- criar segunda qualificação;
- convencer lead claramente não aderente;
- executar consulta jurídica;
- produzir parecer;
- montar estratégia jurídica completa;
- negociar honorários do caso fora das condições reais informadas;
- realizar fechamento de contrato, salvo quando a própria reunião agendada for definida pelo escritório como reunião de fechamento;
- solicitar documentação extensa;
- validar documentos;
- enviar lembretes posteriores;
- confirmar presença em momento futuro;
- recuperar no-show;
- criar follow-up indefinido.

Ela termina no agendamento concluído ou em estado claro de encerramento, revisão ou handoff.

---

# Regras de escrita

As mensagens devem:

- parecer escritas por uma pessoa;
- ser claras e diretas;
- usar linguagem compatível com a persona;
- evitar juridiquês desnecessário;
- usar parágrafos curtos;
- fazer uma ação por vez;
- facilitar a escolha de horário;
- evitar excesso de emojis;
- evitar texto promocional;
- evitar tom de call center;
- evitar pressão.

Prefira:

- “Pelo que você contou...”;
- “Esses pontos fazem sentido serem avaliados com mais profundidade.”;
- “O próximo passo é uma conversa com...”;
- “Na conversa, [PROFISSIONAL] vai entender melhor a sua situação, tirar suas dúvidas e orientar os próximos passos.”;
- “Tenho estes horários: [HORÁRIOS]. Qual fica melhor para você?”.

Evite como padrão:

- “Para confirmar, ainda precisamos analisar...”;
- “Você precisa enviar os documentos antes...”;
- “Só depois de verificar os documentos conseguimos marcar...”;
- “Posso te mostrar os horários?” quando os horários já estão disponíveis;
- “Parabéns, você foi aprovado!”;
- “Seu caso é perfeito.”;
- “Você não pode perder essa oportunidade.”;
- “Últimas vagas.”;
- “Garanta já seus direitos.”;
- “Seu benefício está praticamente certo.”

---

# Validação interna obrigatória

Antes de concluir, verifique:

## Escopo

- O lead já foi suficientemente qualificado?
- A skill evitou refazer a triagem?
- Alguma pergunta adicional é realmente indispensável?
- A consulta não foi realizada por mensagem?

## Fricção

- A mensagem vai direto da devolutiva curta para o próximo passo?
- Se houver horários reais, eles já aparecem na mensagem principal?
- Foi evitada uma etapa intermediária de “posso mostrar os horários?” sem necessidade?
- Alguma pendência foi transformada indevidamente em tarefa prévia?

## Documentação

- A política documental foi identificada?
- A ausência de documento foi tratada como não aderência ou “não está pronto” sem regra expressa?
- A situação 3 foi usada somente quando configurada pelo escritório?
- O SDR foi impedido de validar documentos?

## Valor da reunião

- O valor foi explicado de forma ampla e concreta?
- Documento não virou o eixo central sem motivo?
- A reunião foi apresentada como espaço para compreender, esclarecer, avaliar e orientar?
- Quando aplicável, a função comercial/fechamento real da reunião foi preservada?

## Integridade

- Nenhum fato individual foi inventado?
- O exemplo está identificado como fictício?
- Não há promessa de direito ou resultado?
- Não há urgência artificial?
- Não há contradição entre leitura interna e mensagem ao lead?

## Operação

- Horários, valores, modalidade, links e políticas são reais ou placeholders claros?
- O agendamento pode ser registrado?
- A confirmação imediata é apenas do que foi combinado?
- O handoff usa `/confirmacao-agendamento`?

---

# Critérios de conclusão

A saída está completa somente quando:

- parte de um lead suficientemente qualificado;
- utiliza o Mapeamento e o handoff sem refazer a pré-qualificação;
- apresenta devolutiva curta e contextualizada;
- explica o valor real do atendimento;
- não transforma prova ou documento em barreira padrão;
- oferece horários diretamente quando eles estiverem disponíveis;
- cobre as bifurcações essenciais;
- conduz o lead até data e horário definidos;
- usa somente dados reais ou placeholders claros;
- registra estados de saída;
- prepara handoff para `/confirmacao-agendamento`.

A skill não vende um horário.

Ela transforma uma decisão já tomada — “vale conversar com este lead” — em uma reunião marcada com o mínimo de fricção necessário.

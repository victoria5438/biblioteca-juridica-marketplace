---
name: agendamento
description: Cria um roteiro de conversão para transformar um lead previamente qualificado em um atendimento efetivamente agendado. Usa os critérios de qualificação do Mapeamento de Persona para construir uma devolutiva contextualizada, demonstrar por que o aprofundamento profissional é relevante, fazer o convite e conduzir o lead até a definição do formato, da data e do horário.
argument-hint: Informe o nicho jurídico, o Mapeamento de Persona, o tipo de atendimento oferecido e as condições reais de agendamento. Inclua as respostas individuais da pré-qualificação quando estiverem disponíveis.
---

# Agendamento de Consulta

## Função desta skill

Transformar um lead previamente qualificado em um atendimento efetivamente agendado.

O atendimento pode assumir diferentes formatos:

- consulta jurídica;
- ligação;
- reunião;
- entrevista;
- análise inicial;
- conversa com especialista;
- outro formato definido pelo escritório.

“Consulta” é o nome guarda-chuva da etapa. Adapte a nomenclatura ao serviço real.

Esta skill não deve começar com um convite isolado para marcar horário. Antes do convite, deve construir uma devolutiva que ajude o lead a compreender:

1. o que foi identificado na análise inicial;
2. o que isso pode representar;
3. o que ainda precisa ser verificado;
4. por que o próximo atendimento é útil;
5. qual avanço concreto esse atendimento pode proporcionar.

A lógica central é:

> lead qualificado  
> → devolutiva contextualizada  
> → percepção de relevância  
> → necessidade de aprofundamento  
> → convite  
> → agendamento concluído

---

## Ponto de partida obrigatório

Use esta skill somente quando o lead:

- já passou pela pré-qualificação;
- atende aos critérios mínimos de viabilidade definidos no Mapeamento de Persona;
- está apto a avançar para um atendimento;
- ainda não possui data e horário efetivamente marcados.

Considere como premissa operacional:

> O lead foi classificado como qualificado segundo os critérios objetivos do nicho.

Não refaça toda a pré-qualificação.

Faça apenas uma pergunta adicional quando a informação for indispensável para:

- escolher o formato correto do atendimento;
- resolver uma inconsistência relevante;
- identificar necessidade de intervenção humana;
- concluir o agendamento.

---

## Fontes que devem orientar a saída

Consulte, nesta ordem:

1. instruções atuais do usuário;
2. particularidades reais do escritório;
3. respostas individuais da pré-qualificação, quando fornecidas;
4. critérios de MQL e SQL do Mapeamento de Persona;
5. respostas que indicam lead quente;
6. critérios de desqualificação e sinais de risco;
7. dores, desejos, receios e objeções da persona;
8. mecanismo jurídico, benefício, risco ou solução relacionados ao nicho;
9. características reais do atendimento;
10. condições operacionais reais de agenda.

Use também, quando disponíveis:

- `references/core-cognitivo.md`;
- `references/core-escrita-oralidade.md`.

O Mapeamento de Persona é uma base estratégica. Ele não é uma ficha individual do lead.

---

## Quando as respostas individuais não estiverem disponíveis

A ausência das respostas literais não impede a criação do roteiro.

Nesse caso:

1. identifique os critérios mínimos que necessariamente justificam a qualificação;
2. escolha os critérios mais representativos para construir a devolutiva;
3. apresente a mensagem principal de forma aplicável ao nicho;
4. crie um exemplo demonstrativo com um lead hipotético;
5. deixe explícito, na parte interna do roteiro, quais fatos foram presumidos apenas para exemplificação.

Não atribua ao lead uma fala específica que não foi fornecida.

Evite:

- “Você disse que...”
- “Como você contou...”
- “Pelo documento que você enviou...”
- “Como conversamos...”

Quando não houver histórico individual, prefira:

- “Na análise inicial, foram identificados...”
- “Os elementos avaliados indicam...”
- “Pelos critérios observados até aqui...”
- “A triagem inicial apontou...”

A skill pode presumir apenas os critérios mínimos de qualificação definidos no mapa. Não invente fatos adicionais.

---

## Objetivo estratégico da devolutiva

A devolutiva deve responder a quatro perguntas.

### 1. O que tornou esse lead qualificado?

Selecione dois ou três critérios centrais.

Não despeje uma lista completa de requisitos.

### 2. O que esses critérios podem representar?

Traduza os critérios em uma possibilidade compreensível:

- possível direito;
- possível benefício;
- possível medida;
- possível risco;
- possível solução;
- possível necessidade de proteção;
- possível caminho de regularização.

Use linguagem condicional.

### 3. O que ainda não pode ser concluído?

Mostre os pontos que dependem de análise mais aprofundada.

A necessidade do atendimento deve nascer da diferença entre:

- o que a triagem já indica;
- o que ainda precisa ser confirmado.

### 4. O que o atendimento entregará?

Explique o valor concreto da consulta, ligação ou reunião.

Exemplos de entrega:

- revisar os critérios;
- analisar documentos;
- verificar riscos;
- identificar o caminho aplicável;
- esclarecer alternativas;
- definir próximos passos;
- avaliar viabilidade;
- organizar uma estratégia inicial.

Não use frases vazias como:

- “É importante falar com um advogado.”
- “Seu caso parece interessante.”
- “Uma consulta pode ajudar.”
- “Vamos conversar melhor.”

Explique por que o atendimento é relevante naquele nicho.

---

## Arquitetura obrigatória da mensagem principal

A mensagem principal deve seguir esta ordem.

### 1. Retomada contextual

Demonstre que houve análise inicial.

Exemplo estrutural:

> Oi, [NOME]. Analisei as informações iniciais encaminhadas para a equipe.

### 2. Devolutiva seletiva

Apresente os critérios mais importantes.

Exemplo estrutural:

> Foram identificados elementos relevantes, especialmente [CRITÉRIO CENTRAL 1] e [CRITÉRIO CENTRAL 2].

### 3. Possibilidade relacionada

Traduza os critérios em uma possibilidade.

Exemplo estrutural:

> Esses pontos podem estar relacionados a [DIREITO, BENEFÍCIO, RISCO OU SOLUÇÃO].

### 4. Limite da análise inicial

Explique o que ainda precisa ser verificado.

Exemplo estrutural:

> Para entender se esse caminho realmente se aplica, ainda é necessário avaliar [PONTOS PENDENTES].

### 5. Valor concreto do atendimento

Explique o que acontecerá no próximo passo.

Exemplo estrutural:

> Nesse atendimento, [RESPONSÁVEL] poderá revisar esses pontos, esclarecer as possibilidades e orientar os próximos passos.

### 6. Convite claro

Somente agora faça o convite.

Exemplo estrutural:

> Posso te apresentar as opções de horário?

O convite deve ser simples, específico e fácil de responder.

---

## Linguagem jurídica e promessa de resultado

A skill pode afirmar regras gerais com segurança quando elas estiverem consolidadas e forem relevantes.

A skill pode dizer:

- “Esse benefício depende da análise de critérios de saúde e da situação socioeconômica.”
- “Esse tipo de medida costuma exigir a verificação de documentos e da sequência dos fatos.”
- “Há elementos que justificam uma análise mais aprofundada.”

A skill não pode concluir, sem análise individual suficiente:

- “Você tem direito.”
- “Seu benefício será aprovado.”
- “Sua ação está ganha.”
- “O escritório conseguirá resolver.”
- “Você certamente receberá.”
- “Esse é o melhor caminho para o seu caso.”

Use construções como:

- “pode haver direito”;
- “há indícios que justificam análise”;
- “existe uma possibilidade a ser verificada”;
- “os elementos iniciais são compatíveis com uma análise de”;
- “a confirmação depende de”.

Não enfraqueça tanto a mensagem a ponto de ela parecer evasiva. Equilibre clareza com prudência.

---

## Criação ética da necessidade

Criar necessidade não significa criar medo.

A necessidade deve ser construída a partir de:

- relevância real dos critérios;
- lacuna entre triagem e conclusão;
- risco concreto de interpretar o caso de forma incompleta;
- valor real do atendimento;
- necessidade de verificar fatos, documentos ou critérios;
- existência de decisões ou próximos passos que dependem de análise.

Não use:

- urgência inventada;
- ameaça;
- culpa;
- pressão emocional;
- escassez falsa;
- prazo inexistente;
- promessa de perda automática de direito;
- linguagem que explore vulnerabilidade.

Use urgência jurídica somente quando ela estiver:

- ligada ao tema do caso;
- sustentada pelas informações disponíveis;
- coerente com a regra jurídica aplicável;
- necessária para orientar o próximo passo.

---

## Saída obrigatória

A resposta deve conter os blocos abaixo.

# 1. Leitura estratégica do momento do lead

Apresente de forma interna e objetiva:

- condição de entrada;
- critérios que sustentam a qualificação;
- possibilidade que pode ser mencionada;
- pontos que ainda exigem análise;
- valor concreto do atendimento;
- objeções mais prováveis;
- melhor ângulo de convite.

Este bloco é voltado ao advogado ou à equipe.

Não escreva como se estivesse falando com o lead.

---

# 2. Estrutura da devolutiva

Mostre a lógica aplicada:

> retomada  
> → critérios relevantes  
> → possibilidade  
> → limite da triagem  
> → valor do atendimento  
> → convite

Explique em uma ou duas frases o papel de cada etapa.

Evite transformar este bloco em aula extensa.

---

# 3. Mensagem principal pronta

Crie uma mensagem completa e específica para o nicho.

A mensagem deve:

- soar natural;
- demonstrar análise;
- selecionar os critérios relevantes;
- apresentar uma possibilidade compreensível;
- explicar o limite da triagem;
- demonstrar o valor do atendimento;
- fazer o convite;
- ser adequada ao canal informado.

Não use placeholders jurídicos vagos quando o Mapeamento de Persona permitir escrever o conteúdo.

Use placeholders apenas para dados realmente ausentes, principalmente:

- `[NOME]`;
- `[NOME DO ESCRITÓRIO]`;
- `[PROFISSIONAL]`;
- `[FORMATO DO ATENDIMENTO]`;
- `[DURAÇÃO]`;
- `[VALOR]`;
- `[FORMA DE PAGAMENTO]`;
- `[ENDEREÇO]`;
- `[LINK]`;
- `[HORÁRIOS DISPONÍVEIS]`.

Não deixe comandos internos dentro da mensagem, como:

- “[explique o direito aqui]”;
- “[crie necessidade]”;
- “[fale da dor]”.

A skill deve escrever essas partes.

---

# 4. Exemplo demonstrativo totalmente preenchido

Crie pelo menos um exemplo de mensagem sem placeholders jurídicos.

Simule um lead hipotético que atenda a uma combinação representativa dos critérios de qualificação.

O exemplo deve:

- ter nome fictício;
- refletir o nicho;
- utilizar critérios presentes no mapa;
- apresentar possibilidade sem prometer resultado;
- explicar o que ainda precisa ser analisado;
- terminar com convite claro;
- soar como mensagem real.

Identifique internamente:

> Cenário demonstrativo: exemplo fictício criado a partir dos critérios de qualificação do nicho.

Não apresente o cenário como se fosse um caso real fornecido pelo usuário.

---

# 5. Bifurcações essenciais da conversa

Crie respostas prontas para, no mínimo, estas situações.

## A. Lead aceita o convite

Avance para a etapa operacional.

Não repita toda a devolutiva.

## B. Lead pergunta como funciona

Explique:

- formato;
- objetivo;
- responsável;
- duração, quando conhecida;
- o que será analisado;
- o que o lead poderá obter ao final.

Não realize a consulta dentro da mensagem.

## C. Lead pergunta o valor

Informe apenas a condição real.

Depois, recoloque o valor no contexto da entrega.

Estrutura:

> condição objetiva  
> + o que o atendimento inclui  
> + convite para escolher horário

Não esconda preço quando ele estiver disponível.

Não invente desconto, parcelamento ou gratuidade.

## D. Lead pede para resolver tudo pelo WhatsApp

Explique por que a triagem não substitui o atendimento.

Não use superioridade ou rigidez.

Mostre quais pontos dependem de análise mais aprofundada.

## E. Lead demonstra receio ou insegurança

Reconheça o receio.

Explique como o atendimento funciona.

Reduza incerteza com informações reais.

Não prometa resultado.

## F. Lead diz que precisa pensar

Identifique brevemente qual é a dúvida central.

Responda uma vez de forma útil.

Evite sequência de pressão.

## G. Lead não pode nos horários oferecidos

Ofereça alternativas reais ou encaminhe para a equipe.

Não invente disponibilidade.

## H. Lead prefere outro formato

Adapte apenas quando o escritório realmente oferecer a modalidade.

## I. Lead recusa

Respeite a decisão.

Não discuta.

Não pressione.

Encerre de forma profissional.

## J. Lead traz questão jurídica complexa, contraditória ou urgente

Interrompa o roteiro automático.

Encaminhe para atendimento humano.

Não improvise diagnóstico.

---

# 6. Fluxo operacional do agendamento

Depois do aceite, conduza até o agendamento efetivo.

A sequência padrão é:

1. confirmar o tipo de atendimento;
2. informar modalidade disponível;
3. apresentar condições relevantes;
4. oferecer horários reais;
5. receber a escolha;
6. coletar apenas os dados necessários;
7. registrar o agendamento;
8. enviar confirmação imediata do que foi marcado;
9. preparar handoff para `/confirmacao-consulta`.

A confirmação imediata desta skill serve apenas para registrar o que acabou de ser combinado.

Exemplo:

> Perfeito. Seu atendimento ficou marcado para [DATA], às [HORÁRIO], no formato [MODALIDADE], com [PROFISSIONAL].

Lembretes posteriores, confirmação de presença e orientações prévias pertencem à skill `/confirmacao-consulta`.

---

## Uso de agenda, links e horários

Quando houver integração com agenda:

- use somente horários realmente disponíveis;
- registre a escolha;
- evite dupla reserva;
- confirme fuso horário quando necessário;
- registre modalidade e responsável.

Quando não houver integração:

- use placeholders operacionais;
- entregue ao advogado a estrutura pronta;
- indique claramente onde inserir a disponibilidade real.

Nunca invente:

- datas;
- horários;
- profissional;
- endereço;
- link;
- duração;
- valor;
- política de pagamento;
- política de cancelamento;
- disponibilidade.

Não trate um link de agenda como substituto automático da conversa estratégica.

A devolutiva e o convite devem vir antes do link, salvo instrução expressa do escritório.

---

## Dados que podem ser coletados

Colete somente o necessário para concluir o agendamento.

Exemplos:

- nome;
- telefone;
- e-mail;
- modalidade;
- data;
- horário;
- informação operacional indispensável.

Não use esta etapa para:

- coletar relato completo;
- solicitar todos os documentos;
- realizar nova triagem extensa;
- pedir dados sensíveis sem necessidade;
- montar estratégia jurídica;
- antecipar a consulta.

---

## Estados de saída

A skill termina em um destes estados.

### 1. Agendamento concluído

Há definição de:

- tipo de atendimento;
- modalidade;
- data;
- horário;
- responsável, quando aplicável;
- condição de pagamento, quando aplicável;
- registro operacional.

Encaminhar para `/confirmacao-consulta`.

### 2. Lead recusou

Registrar a recusa e encerrar.

### 3. Lead não está pronto

Registrar a objeção ou pendência.

Não iniciar automaticamente um fluxo longo de follow-up.

### 4. Indisponibilidade operacional

Encaminhar à equipe.

### 5. Necessidade de intervenção humana

Interromper automação e encaminhar.

### 6. Nova informação desqualifica o lead

Não force o agendamento.

Encaminhe para revisão humana ou retorne ao fluxo adequado.

---

## Handoff obrigatório

Quando o agendamento for concluído, apresente um resumo operacional com:

- identificação do lead;
- nicho ou assunto;
- tipo de atendimento;
- modalidade;
- data;
- horário;
- profissional;
- duração;
- valor e pagamento, quando aplicável;
- observação operacional relevante;
- origem da qualificação;
- pontos que justificaram o atendimento;
- status: `AGENDADO — ENCAMINHAR PARA /confirmacao-consulta`.

Não inclua conclusões jurídicas definitivas no handoff.

---

## O que esta skill não faz

Não use esta skill para:

- captar lead frio;
- nutrir lead sem interação;
- realizar pré-qualificação completa;
- convencer um lead claramente desqualificado;
- executar consulta jurídica;
- produzir parecer;
- elaborar estratégia jurídica completa;
- negociar honorários do caso;
- realizar fechamento de contrato;
- solicitar documentação extensa;
- enviar lembretes posteriores;
- confirmar presença em momento futuro;
- recuperar no-show;
- acompanhar decisão após consulta;
- criar follow-up indefinido.

Ela termina no agendamento efetivamente concluído ou em um estado claro de encerramento ou handoff.

---

## Regras de escrita

As mensagens devem:

- parecer escritas por uma pessoa;
- ser claras e diretas;
- usar linguagem compatível com a persona;
- evitar juridiquês desnecessário;
- usar parágrafos curtos;
- criar progressão natural;
- fazer uma pergunta por vez quando estiver conduzindo escolha;
- evitar excesso de emojis;
- evitar texto promocional;
- evitar tom de call center;
- evitar pressão.

Prefira:

- “Pelos elementos avaliados até aqui...”
- “Isso pode indicar...”
- “Para confirmar, ainda precisamos analisar...”
- “Nesse atendimento será possível...”
- “Posso te mostrar os horários disponíveis?”

Evite:

- “Parabéns, você foi aprovado!”
- “Seu caso é perfeito.”
- “Você não pode perder essa oportunidade.”
- “Últimas vagas.”
- “Garanta já seus direitos.”
- “Seu benefício está praticamente certo.”

---

## Validação interna obrigatória

Antes de concluir, verifique:

### Escopo

- O lead já está qualificado?
- A skill não refez a triagem?
- A saída permanece entre qualificação e agendamento?
- A consulta não foi realizada por mensagem?

### Devolutiva

- A mensagem mostra o que foi identificado?
- Os critérios vêm do mapa ou das respostas reais?
- Há no máximo dois ou três eixos centrais?
- A possibilidade está compreensível?
- O limite da análise inicial está claro?
- O valor do atendimento é concreto?

### Integridade

- Nenhum fato individual foi inventado?
- O exemplo está identificado como fictício?
- A mensagem não simula conversa inexistente?
- Não há promessa de direito ou resultado?
- Não há urgência artificial?
- Não há contradição entre a análise interna e a mensagem enviada?

### Conversão

- O convite aparece depois da contextualização?
- O CTA é simples?
- As objeções principais estão cobertas?
- O fluxo continua até data e horário definidos?
- Não há insistência excessiva?

### Operação

- Os dados operacionais são reais ou placeholders claros?
- Nenhum horário, valor, link ou política foi inventado?
- O agendamento pode ser registrado?
- O handoff contém o necessário?
- A próxima etapa correta é `/confirmacao-consulta`?

---

## Critérios de conclusão

A saída está completa somente quando:

- parte de um lead previamente qualificado;
- utiliza o Mapeamento de Persona como base estratégica;
- cria uma devolutiva coerente com os critérios de qualificação;
- demonstra por que o aprofundamento é relevante;
- não promete resultado;
- apresenta mensagem principal pronta;
- apresenta exemplo demonstrativo completo;
- cobre as bifurcações essenciais;
- conduz o aceite até o agendamento efetivo;
- usa apenas dados operacionais reais ou placeholders;
- registra estados de saída;
- prepara o handoff para `/confirmacao-consulta`.

A skill não vende um horário.

Ela transforma a qualificação em percepção de valor, e a percepção de valor em um atendimento marcado.


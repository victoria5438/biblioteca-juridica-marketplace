---
name: pre-qualificacao
description: Cria um roteiro humano de pré-qualificação jurídica para decidir, com o mínimo de interações necessárias, qual deve ser o próximo passo do lead. Usa o Mapeamento de Persona Jurídica para transformar critérios objetivos de aderência, revisão, roteamento, urgência, maturidade e prontidão em um Fluxo Mínimo Viável de até 5 perguntas e em um Banco Estratégico de apoio, sem antecipar a análise jurídica nem transformar prova documental em requisito automático de avanço.
argument-hint: Informe o nicho jurídico, forneça o Mapeamento de Persona e acrescente dados reais do escritório, do canal e da próxima etapa.
---

# Pré-qualificação

## Objetivo

Criar um roteiro humano e reutilizável de pré-qualificação jurídica para uso pela equipe do escritório.

A pré-qualificação é uma **etapa comercial de decisão**. Seu objetivo não é esgotar a análise jurídica, coletar tudo o que possa ser útil nem antecipar o trabalho do profissional.

Ela deve obter informação suficiente para responder:

> **Qual é o próximo passo adequado para este lead?**

O roteiro deve cumprir, nesta ordem:

1. receber o lead e contextualizar a etapa;
2. identificar a situação objetiva que motivou o contato;
3. testar os requisitos mínimos de aderência ao serviço;
4. aprofundar somente fatos que ainda sejam necessários para decidir o próximo passo;
5. reconhecer urgência, pendências, necessidade de revisão ou roteamento;
6. classificar e direcionar assim que houver informação suficiente;
7. registrar maturidade comercial e prontidão operacional separadamente, quando isso for útil;
8. preparar um handoff factual para a próxima etapa.

Princípio central:

> **Cada pergunta tem custo. Ela só permanece no fluxo principal se sua resposta puder mudar a classificação, o roteamento, a prioridade ou o próximo passo.**

Estrutura central:

> boas-vindas e contextualização  
> → Fluxo Mínimo Viável  
> → complementos condicionais somente quando necessários  
> → classificação e direcionamento  
> → handoff  
> → Banco Estratégico de apoio

A skill deve produzir um roteiro que uma pessoa do escritório consiga utilizar em conversa real.

Ela não cria automações, chatbot, árvore técnica de decisões, lógica de CRM, gatilhos, integrações, código ou instruções de sistema.

---

# Referências obrigatórias

Antes de produzir a saída:

1. leia `${CLAUDE_PLUGIN_ROOT}/references/core-cognitivo.md`;
2. leia `${CLAUDE_PLUGIN_ROOT}/references/core-escrita-oralidade.md`;
3. utilize o Mapeamento de Persona Jurídica fornecido pelo usuário ou disponível na conversa;
4. priorize informações reais do escritório, do serviço, do canal e da operação;
5. não execute novamente a skill `/mapear-persona`.

Use especialmente as seguintes partes do Mapeamento de Persona:

- situação qualificadora central;
- natureza do serviço;
- requisitos materiais ou condições objetivas de aderência;
- critérios de MQL jurídico;
- elementos de SQL jurídico;
- fatores de complexidade;
- fatores de prioridade e urgência;
- condições operacionais e informações pendentes;
- critérios de exclusão e roteamento;
- perguntas principais, condicionais e de esclarecimento;
- critérios de avanço;
- linguagem, medos, objeções e nível de compreensão da persona;
- dados relevantes para handoff.

Não reproduza o Mapeamento inteiro.

Converta-o em decisões concretas de:

- quais informações são realmente essenciais;
- quais perguntas entram no Fluxo Mínimo Viável;
- quais perguntas ficam apenas no Banco Estratégico;
- ordem e linguagem das perguntas;
- condições que justificam aprofundamento;
- momento de parar de perguntar;
- classificação interna;
- direcionamento;
- dados de repasse.

## Quando o Mapeamento não estiver disponível

Solicite o documento.

Somente prossiga sem ele quando o usuário fornecer, no mínimo:

- natureza do serviço;
- situação qualificadora central;
- requisitos de aderência;
- causas de não aderência ou roteamento;
- situações que exigem revisão profissional;
- urgências reais;
- próxima etapa;
- perfil de linguagem do público.

Não invente esses critérios.

---

# Delimitação do produto

Esta skill produz um **roteiro humano de pré-qualificação**.

Use quando:

- o lead iniciou contato;
- ainda não passou por triagem inicial;
- o escritório precisa compreender fatos básicos;
- existe critério objetivo de aderência ao serviço;
- o objetivo é decidir o próximo atendimento adequado.

A skill pode criar:

- saudação e contextualização;
- Fluxo Mínimo Viável;
- perguntas condicionais;
- perguntas de esclarecimento;
- Banco Estratégico de perguntas;
- orientações breves para o atendente;
- critérios de parada;
- classificação interna;
- mensagens de agradecimento e direcionamento;
- modelo de handoff;
- roteiro final limpo.

A skill não deve:

- realizar consulta jurídica;
- emitir parecer;
- afirmar definitivamente que existe ou não direito;
- prometer resultado;
- calcular chance de êxito;
- transformar coleta de prova em requisito automático de qualificação;
- pedir documentação extensa;
- montar estratégia jurídica;
- negociar honorários do caso;
- agendar;
- confirmar presença;
- recuperar no-show;
- criar follow-up;
- criar sequência de nutrição;
- adaptar o material para automação;
- simular respostas completas do lead sem pedido expresso.

## Simulação

Crie conversa fictícia ou role-play somente quando o usuário pedir expressamente.

A ausência de simulação não torna a saída incompleta.

---

# Objetivo, produto e canal

Antes de escrever, determine:

- **objetivo:** pré-qualificar e direcionar;
- **produto:** roteiro humano reutilizável;
- **canal:** WhatsApp, ligação, recepção, formulário assistido ou outro informado.

Adapte a distribuição das perguntas ao canal.

- No WhatsApp, escreva mensagens curtas, faça uma pergunta por vez e indique quando aguardar.
- Em ligação ou recepção, use perguntas faláveis e transições naturais.
- Não transforme WhatsApp em interrogatório enviado de uma vez.
- Não transforme ligação em formulário lido mecanicamente.

Se o canal não estiver informado, use WhatsApp como `[PREMISSA OPERACIONAL]` somente quando o contexto indicar atendimento por mensagem. Caso contrário, escreva um roteiro neutro e falável.

---

# Princípios de qualificação

## 1. Qualificação comercial não é prova

A pré-qualificação responde:

> **Há elementos suficientes, principalmente pelo relato, para justificar o próximo passo?**

A validação profissional responde, em etapa posterior:

> **Os fatos estão comprovados, juridicamente confirmados e suficientes para a medida pretendida?**

Não misture as duas decisões.

O nível de evidência exigido deve ser proporcional à decisão tomada naquela etapa do funil.

Para fins de pré-qualificação, o relato pode ser suficiente para sustentar avanço, pendência, revisão, roteamento ou não aderência preliminar.

## 2. Fato, prova e coleta são coisas diferentes

Diferencie sempre:

- **fato:** o que o lead relata ter acontecido;
- **prova:** o que pode demonstrar esse fato;
- **coleta:** o momento em que essa prova é solicitada ou recebida.

A ausência de prova não significa automaticamente ausência do fato.

Perguntar se existe um documento não equivale a exigir seu envio.

A coleta documental pode acontecer na próxima etapa ou depois, conforme a operação do escritório.

Se a próxima etapa definida pelo escritório for análise documental, preserve essa operação. A solicitação deve aparecer como orientação da próxima etapa, não como requisito artificial de qualificação, salvo quando o documento for realmente indispensável para decidir um fato essencial ou houver regra operacional expressa.

## 3. MQL jurídico

Use o MQL para identificar se o relato apresenta os requisitos materiais ou as condições objetivas mínimas que tornam a situação pertinente ao serviço.

A pré-qualificação pode identificar:

- requisito indicado pelo relato;
- indício;
- ausência aparente;
- informação desconhecida;
- contradição;
- necessidade de revisão profissional.

Não transforme relato em confirmação documental.

## 4. SQL jurídico

Use o SQL somente para fatos ou elementos adicionais que sejam realmente necessários para uma decisão comercial ou para preparar a próxima etapa.

Não presuma que todo elemento de SQL precisa ser perguntado na pré-qualificação.

Um dado de SQL pode ficar apenas no Banco Estratégico ou no handoff quando sua ausência não muda a decisão atual.

Documentos, datas, históricos, vínculos ou elementos técnicos só entram no fluxo principal quando sua resposta ainda puder mudar:

- aderência;
- classificação;
- roteamento;
- prioridade;
- necessidade de revisão;
- próximo passo.

Se o Mapeamento tratar um documento como SQL, verifique se ele é:

- um **fato qualificador em si**; ou
- apenas um **meio de prova** de fato que já pode ser relatado.

Não transforme meio de prova em requisito de avanço por padrão.

SQL jurídico não inclui:

- disponibilidade de agenda;
- comparecimento;
- rapidez de resposta;
- intenção imediata de contratar;
- aceitação de proposta;
- disposição atual para enviar documentos;
- participação de cônjuge ou terceiro.

Esses elementos pertencem à maturidade comercial ou à prontidão operacional.

## 5. Maturidade comercial e prontidão operacional

Registre separadamente, quando isso for útil à operação:

- reconhecimento da necessidade;
- interesse em conhecer o próximo passo;
- intenção de avançar;
- disponibilidade;
- preferência de canal;
- necessidade de consultar terceiro;
- objeção ou impedimento operacional.

Capacidade de reunir documentos pode ser registrada quando tiver utilidade operacional, mas não deve rebaixar aderência por si só.

Um lead pode ser juridicamente aderente e ainda não estar pronto para avançar.

Um lead também pode querer contratar e não apresentar aderência suficiente.

## 6. Informação ausente

“Não sei”, “não lembro” ou “não tenho o documento agora” não equivalem automaticamente a não aderência.

Quando faltar um **fato essencial**, classifique conforme o caso como:

- informação pendente;
- elemento a confirmar;
- necessidade de revisão profissional;
- informação insuficiente.

Quando faltar apenas **prova documental**, registre a situação probatória ou operacional sem alterar automaticamente o status.

## 7. Não aderência e roteamento

Diferencie:

- ausência aparente de requisito essencial;
- situação pertencente a outro serviço;
- caso fora do escopo do escritório;
- caso que exige análise profissional;
- impossibilidade operacional confirmada;
- informação realmente insuficiente;
- falta de prontidão comercial.

Nunca agrupe tudo como “desqualificado”.

---

# Regra obrigatória: Fluxo Mínimo Viável

Toda saída deve conter uma seção claramente identificada como **Fluxo Mínimo Viável**.

Esse é o fluxo recomendado para execução padrão.

Regras:

- no máximo **5 perguntas principais** de qualificação;
- pode haver menos de 5;
- se o relato inicial já respondeu uma pergunta, considere o objetivo cumprido e pule;
- uma pergunta por mensagem ou turno;
- perguntas curtas, claras e objetivas;
- preferir resposta fechada, objetiva ou curta quando isso não prejudicar a informação;
- usar pergunta aberta somente quando realmente necessária;
- escolher perguntas pelo poder de decisão, não pela quantidade de informação que coletam;
- não perguntar apenas porque a informação “seria útil”;
- não antecipar investigação que pode acontecer depois;
- condicionais não contam como licença para criar uma segunda entrevista;
- complemento condicional só deve existir quando a resposta deixou a decisão em aberto.

Princípio de parada:

> **Assim que houver informação suficiente para classificar e direcionar, pare de perguntar.**

Não complete o questionário por completude.

Não exija que o lead responda cinco perguntas se duas ou três já forem suficientes ou se parte delas já estiver respondida no relato.

---

# Estrutura obrigatória da saída

A entrega deve conter cinco blocos:

1. leitura estratégica;
2. Fluxo Mínimo Viável comentado;
3. classificação e direcionamento;
4. handoff e roteiro final limpo;
5. Banco Estratégico de perguntas.

---

# 1. Leitura estratégica

Apresente uma síntese interna curta com:

- nicho e serviço;
- natureza da etapa: comercial e de decisão;
- canal utilizado;
- situação qualificadora central;
- critérios principais de aderência por relato;
- fatos essenciais que realmente precisam ser conhecidos antes do próximo passo;
- informações úteis para handoff, mas não obrigatórias na triagem;
- urgências reais;
- principais causas de revisão ou roteamento;
- causas claras de não aderência;
- temas sensíveis;
- tom recomendado;
- próxima etapa esperada;
- informações operacionais ainda não confirmadas;
- política documental relevante, quando informada.

Inclua uma nota de uso que deixe claro:

> O Fluxo Mínimo Viável é a sequência operacional recomendada. O Banco Estratégico é material de consulta e não deve ser executado automaticamente.

Não reproduza o Mapeamento.

---

# 2. Fluxo Mínimo Viável comentado

## 2.1. Saudação e contextualização

Crie uma única abertura recomendada.

Somente apresente alternativas quando o usuário pedir opções.

A abertura deve, conforme as informações disponíveis:

1. cumprimentar;
2. identificar o escritório;
3. indicar a área ou o serviço;
4. mencionar autoridade real, quando houver;
5. explicar de forma breve a finalidade das perguntas;
6. preparar o lead para responder uma pergunta de cada vez.

Evite criar uma interação extra apenas para pedir permissão para começar.

No WhatsApp, prefira contextualizar e seguir diretamente para a primeira pergunta ainda em aberto, salvo quando a marca ou a operação exigir outra abordagem.

Exemplo estrutural:

> Olá, [NOME]. Aqui é [ATENDENTE], do [ESCRITÓRIO]. Recebemos seu contato sobre [TEMA].  
> Para direcionar seu atendimento, vou fazer algumas perguntas rápidas, uma de cada vez. Se não souber alguma, sem problema, é só me dizer.

Se o lead já abriu contando a história, reconheça brevemente o relato e vá para a primeira informação essencial ainda não respondida.

### Tom, emojis e sinais visuais

Não inclua emojis, símbolos afetivos ou marcas de informalidade na versão padrão sem que o tom da marca, o usuário ou o Mapeamento indiquem esse uso.

Quando não houver informação:

- prefira uma abertura neutra, humana e profissional;
- não presuma que emojis combinam com o escritório;
- não use emoji apenas para tornar a mensagem “mais acolhedora”.

### Prova de autoridade

Use somente fatos fornecidos ou confirmados.

Não invente:

- número de clientes;
- anos de atuação;
- casos vencidos;
- taxa de êxito;
- títulos;
- prêmios;
- certificações;
- presença nacional;
- depoimentos;
- resultados.

Quando não houver prova de autoridade, omita.

Não transforme a saudação em anúncio.

## 2.2. Seleção das até 5 perguntas

Escolha as perguntas de maior poder de decisão.

Priorize as que ajudam a responder:

- há aderência suficiente para avançar?;
- existe causa clara de não aderência?;
- o caso pertence a outro serviço?;
- há ponto técnico que exige revisão profissional?;
- existe prioridade ou urgência real?;
- falta um fato essencial sem o qual não é possível classificar?

As perguntas principais devem:

- testar um critério real por vez, sempre que possível;
- ser específicas para o nicho;
- usar linguagem simples;
- permitir resposta “não sei”;
- evitar narrativa extensa;
- não antecipar a consulta;
- não pedir todos os documentos;
- não introduzir preço ou contratação antes da aderência;
- não repetir informação já fornecida.

Organize na ordem mais natural, não necessariamente na ordem jurídica abstrata.

## 2.3. Ficha obrigatória de cada pergunta

Para **cada pergunta principal**, apresente internamente:

### [NOME DO OBJETIVO]

**Objetivo:** o que se pretende descobrir.

**Critério relacionado:** qual critério de aderência, roteamento, prioridade, revisão ou prontidão aquela informação ajuda a avaliar.

**Relevância:** por que essa informação importa para a decisão desta etapa.

**Prioridade:** Essencial / Complementar / Condicional.

**Quando perguntar:** em quais situações a pergunta deve ser feita.

**Pergunta sugerida:** uma formulação simples, natural e adequada ao canal.

**Complemento condicional:** pergunta adicional somente se determinada resposta exigir esclarecimento. Em WhatsApp, enviar em mensagem separada.

**Quando não perguntar:** quando o relato anterior já resolveu o objetivo ou quando a informação não é necessária para a decisão atual.

**Tratamento:** como registrar ou interpretar operacionalmente a resposta sem extrapolar para conclusão jurídica.

Quando aplicável, indique quais respostas:

- favorecem avanço;
- geram pendência de fato essencial;
- exigem revisão profissional;
- geram roteamento;
- afastam aderência;
- indicam prioridade ou urgência.

Não force essas categorias quando não fizerem sentido.

## 2.4. Perguntas condicionais e de esclarecimento

Inclua somente quando uma resposta alterar:

- aderência;
- subperfil;
- classificação;
- urgência;
- revisão profissional;
- roteamento;
- próximo passo.

Não inclua condicionais apenas para enriquecer o histórico.

Pergunte fatos, não enquadramentos jurídicos.

Não peça que o lead classifique juridicamente a própria situação.

Para respostas ambíguas, proponha uma pergunta curta.

Exemplos estruturais:

> Só para eu entender: isso aconteceu antes ou depois de [MARCO]?

> Quando você diz que não recebeu, está falando de [OPÇÃO A] ou de [OPÇÃO B]?

> Você consegue estimar, mesmo que aproximadamente?

Faça apenas o esclarecimento necessário.

Se a pessoa não souber:

- registre a pendência quando o fato for essencial;
- prossiga quando possível;
- não force resposta;
- não conclua ausência do requisito.

## 2.5. Quando parar de perguntar

Inclua uma seção objetiva com stop rules.

Considere, conforme o nicho:

- critérios suficientes para avanço → parar e direcionar;
- fato essencial incerto, mas sem sinal contrário → parar e usar “Avança com pendências”, quando adequado;
- ponto técnico que o atendente não deve decidir → parar ou concluir apenas as perguntas que ainda possam mudar claramente o direcionamento, depois encaminhar para revisão;
- causa clara de não aderência → parar; não completar perguntas restantes;
- necessidade clara de outro serviço → parar e rotear;
- informação realmente insuficiente → registrar o que falta;
- urgência/prioridade → sinalizar sem criar interrogatório paralelo.

Não prolongue o fluxo apenas para preencher handoff.

---

# 3. Classificação e direcionamento

A classificação é interna. Não mostre os rótulos ao lead.

## A. Avança

Use quando:

- há aderência preliminar suficiente pelo relato;
- os fatos essenciais foram suficientemente delimitados para o próximo passo;
- não apareceu causa objetiva de roteamento.

Mensagem estrutural:

> Obrigado por responder, [NOME].  
> Pelo que você contou, faz sentido seguir com o seu caso.  
> O próximo passo será [PRÓXIMA ETAPA REAL]. [ORIENTAÇÃO OPERACIONAL CONFIRMADA.]

Não diga que o lead “tem direito”.

## B. Avança com pendências

Use quando:

- há aderência provável pelo relato;
- **um fato essencial** ficou incerto;
- essa incerteza não impede a continuidade.

A simples ausência de documento, sozinha, não deve levar a este status.

Mensagem estrutural:

> Obrigado pelas informações, [NOME]. Pelo que você contou, faz sentido seguir. Alguns detalhes, como [PONTO EM LINGUAGEM SIMPLES], podem ser esclarecidos na próxima etapa.  
> O próximo passo será [PRÓXIMA ETAPA REAL].

## C. Revisão profissional

Use quando:

- existe ambiguidade técnica relevante;
- há contradição;
- o enquadramento é controvertido;
- a equipe de atendimento não deve decidir sozinha.

Mensagem estrutural:

> Obrigado pelas informações, [NOME]. Alguns pontos da sua situação precisam ser avaliados com mais cuidado antes de qualquer direcionamento. Vou repassar o seu relato para a equipe responsável.

Não prometa prazo de resposta não informado.

## D. Prioridade ou urgência

Use quando houver sinal objetivo de prazo ou risco real.

Mensagem estrutural:

> Entendi. Como você mencionou [FATO COM DATA OU RISCO], vou sinalizar essa informação para a equipe responsável.

Não prometa atendimento imediato.

A prioridade pode coexistir com qualquer outro status.

## E. Roteamento

Use quando a necessidade pertence a outro serviço, área ou profissional.

Mensagem estrutural:

> Obrigado por explicar, [NOME]. Pelo que você contou, o atendimento que você precisa agora parece estar mais ligado a [OUTRO SERVIÇO OU ÁREA] do que a [SERVIÇO INICIAL].

Indique outro caminho somente quando ele for real e confirmado.

## F. Não aparenta aderência

Use quando o relato não apresenta requisito essencial e não há fato pendente capaz de alterar isso.

Mensagem estrutural:

> Obrigado por responder às perguntas, [NOME]. Pelas informações iniciais, sua situação não parece apresentar um dos pontos necessários para este serviço: [PONTO EM LINGUAGEM SIMPLES].  
> Essa é uma avaliação inicial e não representa uma conclusão definitiva sobre todos os seus direitos.

## G. Informação insuficiente

Use somente quando faltam fatos centrais a ponto de não ser possível classificar.

Não use quando faltam apenas:

- documentos;
- datas exatas que podem ser aproximadas;
- informações complementares de handoff.

Mensagem estrutural:

> Obrigado pelas informações, [NOME]. Para eu conseguir direcionar, ainda preciso entender melhor [FATO ESSENCIAL]. Quando conseguir me dizer isso, seguimos por aqui.

## H. Sem prontidão para avançar

Use quando há aderência, mas a pessoa não deseja ou não consegue continuar agora.

Mensagem estrutural:

> Sem problema, [NOME]. Obrigado pelo contato. Quando quiser retomar, é só falar com a gente por aqui.

Não altere a classificação de aderência por causa disso.

---

# 4. Handoff e roteiro final

## 4.1. Resumo para o próximo profissional

Crie um modelo de repasse com esta estrutura:

```text
STATUS DA PRÉ-QUALIFICAÇÃO:
[Avança / Avança com pendências / Revisão profissional / Roteamento / Não aparenta aderência / Informação insuficiente / Sem prontidão]

PRIORIDADE OU URGÊNCIA:
[Não identificada / Identificada — descrever fato e data]

Nome:
Nicho ou serviço:
Motivo principal do contato:

FATOS RELATADOS:
[resumo objetivo, usando “relata” quando necessário]

CRITÉRIOS INDICADOS PELO RELATO:
[critério → indicado / não indicado / incerto / revisão]

INFORMAÇÕES ADICIONAIS:
[registrar somente se surgiram; não obrigatórias]

Provas ou documentos mencionados pelo lead:
[informação de contexto, não requisito automático]

PONTOS A APROFUNDAR NA PRÓXIMA ETAPA:
[fatos essenciais incertos, contradições, pontos técnicos]

Contradições ou dúvidas:
Critério de roteamento, se houver:

Maturidade comercial:
Prontidão operacional:
Receios ou objeções:

Próximo passo recomendado:
Observação importante:
```

Regras:

- diferencie relato de confirmação;
- use “indicado pelo relato”, não “direito confirmado”;
- não registre chance de êxito;
- não declare culpa, fraude ou resultado;
- ausência de documento não muda o status por si só;
- falta de disponibilidade não muda o status;
- indique `/agendamento` somente quando essa for a próxima skill real;
- registre fatos, datas e falas relevantes sem exagero interpretativo.

## 4.2. Roteiro final limpo

Ao final, entregue uma versão pronta para utilização.

Inclua apenas:

1. saudação/contextualização;
2. Fluxo Mínimo Viável com até 5 perguntas;
3. complementos condicionais indispensáveis, ligados aos respectivos gatilhos;
4. indicação de aguardar resposta quando o canal for WhatsApp;
5. mensagens de direcionamento por status.

Não inclua:

- todas as perguntas do Banco Estratégico;
- explicações teóricas;
- objetivos internos;
- classificação MQL ou SQL;
- tabela estratégica;
- análise jurídica;
- código;
- instruções de automação;
- conversa fictícia não solicitada.

No WhatsApp:

- uma pergunta por mensagem;
- indicação de `Aguarde a resposta.` quando útil ao material;
- não envie todos os ramos ao lead;
- não apresente mensagens de encerramento antes de saber o status;
- pule qualquer pergunta que o lead já respondeu.

---

# 5. Banco Estratégico de Perguntas

O Banco Estratégico é material de apoio.

Ele pode conter mais perguntas do que o Fluxo Mínimo Viável, mas **não deve ser executado automaticamente em sequência**.

Use-o quando:

- uma informação importante não surgiu;
- uma resposta foi ambígua;
- determinado ramo condicional foi aberto;
- há uma situação excepcional;
- a equipe profissional pediu um dado específico;
- a operação exige informação adicional para o próximo passo.

Para cada pergunta do Banco, use a mesma ficha:

- Objetivo;
- Critério relacionado;
- Relevância;
- Prioridade: Complementar ou Condicional;
- Quando perguntar;
- Pergunta sugerida;
- Complemento condicional, se houver;
- Quando não perguntar;
- Tratamento.

Não use prioridade “Essencial” no Banco para uma pergunta que deveria estar no Fluxo Mínimo Viável.

## Perguntas sobre documentos

Perguntas sobre existência de prova documental podem aparecer no Banco quando tiverem utilidade real.

Regra padrão:

- se a existência do documento não muda a classificação, trate como informação de handoff;
- não pergunte no fluxo padrão só para “deixar o caso completo”;
- não transforme “não tenho” em pendência de aderência;
- não solicite envio antes da classificação, salvo necessidade real ou regra expressa da operação.

Quando a próxima etapa for análise documental, a solicitação pode vir **depois da classificação**, como instrução da próxima etapa.

Exemplo estrutural:

> O próximo passo é [ANÁLISE DOCUMENTAL]. Para isso, a equipe precisa de [DOCUMENTOS DEFINIDOS PELO ESCRITÓRIO]. [COMO ENVIAR.]

Nunca pedir senha do gov.br.

---

# Perguntas sensíveis

Contextualize perguntas sobre:

- renda;
- saúde;
- deficiência;
- violência;
- morte;
- dependência;
- separação;
- demissão;
- discriminação;
- dívida;
- situação migratória;
- acusação criminal;
- patrimônio;
- composição familiar.

A pergunta sensível só deve existir quando estiver ligada a um requisito, bifurcação ou decisão real.

Não peça desculpas excessivamente.

---

# Quantidade e profundidade

Como regra:

- Fluxo Mínimo Viável: no máximo 5 perguntas principais;
- Banco Estratégico: pode ser mais amplo, mas é consultivo;
- elimine redundâncias;
- faça uma pergunta por envio ou turno;
- não substitua consulta por triagem;
- não solicite narrativa completa;
- não peça documentação extensa;
- não investigue objeção comercial antes de saber se há aderência;
- não crie perguntas apenas para deixar o roteiro “completo”;
- não prolongue a conversa para preencher handoff;
- pare assim que a decisão da etapa puder ser tomada.

---

# Regras de linguagem

O roteiro deve:

- soar humano;
- ser específico para o nicho;
- preservar autoridade profissional;
- usar linguagem simples;
- fazer uma pergunta por vez;
- usar parágrafos curtos;
- evitar intimidade forçada;
- evitar frieza burocrática;
- explicar perguntas sensíveis quando necessário;
- permitir “não sei”;
- acolher sem dramatizar;
- reagir ao que já foi informado;
- não obrigar a pessoa a repetir dados.

Evite:

- “Seu caso foi aprovado.”
- “Você está qualificado.”
- “Você é um SQL.”
- “Temos certeza de que você tem direito.”
- “Parabéns, seu caso se enquadra.”
- “Caso ganho.”
- “Alta chance de êxito.”
- “Última oportunidade.”
- “Responda obrigatoriamente.”
- “Envie todos os documentos agora.”
- “Nossa taxa de sucesso é de 100%.”
- “Um especialista falará com você em breve”, quando isso não estiver confirmado.

---

# Validação interna obrigatória

Antes de concluir, verifique:

## Referências

- O Mapeamento de Persona foi consultado?
- A situação qualificadora veio do mapa?
- Os critérios de aderência vieram do mapa?
- Nenhum critério jurídico foi inventado?
- O Core Cognitivo e o Core de Escrita foram aplicados?

## Arquitetura

- O produto é um roteiro humano de pré-qualificação?
- O canal foi identificado?
- A pré-qualificação foi tratada como etapa comercial de decisão?
- Existe um Fluxo Mínimo Viável claramente separado do Banco Estratégico?
- O Fluxo Mínimo Viável tem no máximo 5 perguntas principais?
- O material não virou chatbot ou lógica de automação?
- Não houve simulação sem pedido expresso?

## Perguntas

- Cada pergunta do fluxo pode mudar classificação, roteamento, prioridade ou próximo passo?
- Perguntas já respondidas pelo relato foram puladas?
- As perguntas solicitam fatos, e não enquadramentos jurídicos?
- Há uma pergunta por vez?
- Complementos condicionais só aparecem quando necessários?
- O fluxo para assim que existe informação suficiente?
- O Banco Estratégico não foi transformado em sequência obrigatória?
- Informação ausente virou pendência somente quando o fato é essencial?
- Ausência de documento foi tratada separadamente de ausência do fato?
- Não há pedido documental excessivo?
- Urgência foi baseada em fato real?

## Classificação

- Avanço com pendência foi reservado para fato essencial incerto, e não mera falta de documento?
- Revisão foi diferenciada de pendência?
- Roteamento foi diferenciado de não aderência?
- Informação insuficiente foi usada apenas quando realmente não é possível classificar?
- Baixa prontidão não alterou a aderência?
- Nenhuma conclusão definitiva foi apresentada ao lead?

## Direcionamento

- O próximo passo é real?
- Consulta, reunião, análise documental ou outro formato foram preservados quando definidos pelo escritório?
- A skill não impôs nem suprimiu análise documental como próxima etapa?
- Não há promessa de prazo?
- Não há promessa de contato não confirmado?
- As mensagens são respeitosas?

## Entrega

- Há leitura estratégica?
- Há Fluxo Mínimo Viável comentado?
- Há stop rules?
- Há classificação e mensagens de direcionamento?
- Há handoff?
- Há roteiro final limpo?
- Há Banco Estratégico?
- Cada pergunta relevante tem objetivo, critério, relevância, prioridade, quando perguntar, pergunta sugerida, complemento condicional, quando não perguntar e tratamento?
- Não há conteúdo duplicado sem função?

Corrija silenciosamente.

---

# Critérios de conclusão

A saída está completa quando:

- utiliza o Mapeamento de Persona;
- identifica corretamente a natureza do serviço;
- trata a pré-qualificação como etapa comercial de decisão;
- produz um Fluxo Mínimo Viável com no máximo 5 perguntas principais;
- pula perguntas já respondidas pelo relato;
- pergunta uma coisa por vez;
- para assim que houver informação suficiente para classificar e direcionar;
- separa fato, prova e coleta;
- não transforma ausência documental em pendência de aderência por padrão;
- preserva análise documental como possível próxima etapa quando definida pelo escritório;
- cria Banco Estratégico separado e não automático;
- estrutura cada pergunta com objetivo, relevância, uso e tratamento claros;
- reconhece urgência sem criá-la;
- diferencia avanço, pendência, revisão, roteamento, não aderência, informação insuficiente e sem prontidão;
- cria handoff baseado em fatos e níveis de certeza;
- entrega roteiro final limpo;
- não realiza consulta;
- não cria automação;
- não inclui simulação sem pedido expresso.

A skill deve ajudar o escritório a **perguntar menos, perguntar melhor, decidir mais cedo e encaminhar com clareza**.

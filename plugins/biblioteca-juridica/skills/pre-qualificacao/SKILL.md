---
name: pre-qualificacao
description: Cria um roteiro humano de pré-qualificação jurídica para identificar aderência preliminar, reunir informações essenciais, reconhecer urgência, registrar pendências e direcionar o lead à próxima etapa adequada. Usa o Mapeamento de Persona Jurídica para transformar requisitos de MQL, elementos de SQL, critérios de revisão, roteamento, maturidade e prontidão operacional em uma conversa clara, ética e específica para o nicho.
argument-hint: Informe o nicho jurídico, forneça o Mapeamento de Persona e acrescente dados reais do escritório, do canal e da próxima etapa.
---

# Pré-qualificação

## Objetivo

Criar um roteiro humano e reutilizável de pré-qualificação jurídica para uso pela equipe do escritório.

O roteiro deve cumprir, nesta ordem:

1. receber o lead e contextualizar a etapa;
2. identificar a situação objetiva que motivou o contato;
3. testar os requisitos preliminares de aderência ao serviço;
4. aprofundar somente os fatos necessários à próxima etapa;
5. reconhecer urgência, pendências, necessidade de revisão ou roteamento;
6. registrar maturidade comercial e prontidão operacional separadamente;
7. agradecer e direcionar o lead de forma adequada.

Estrutura central:

> boas-vindas  
> → contextualização  
> → perguntas principais  
> → perguntas condicionais ou de esclarecimento  
> → classificação interna  
> → agradecimento e direcionamento  
> → handoff

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
- dados obrigatórios para handoff.

Não reproduza o Mapeamento inteiro.

Converta-o em decisões concretas de:

- ordem das perguntas;
- linguagem;
- quantidade;
- profundidade;
- bifurcações;
- pontos de esclarecimento;
- classificação interna;
- direcionamento;
- dados de repasse.

## Quando o Mapeamento não estiver disponível

Solicite o documento.

Somente prossiga sem ele quando o usuário fornecer, no mínimo:

- natureza do serviço;
- situação qualificadora central;
- requisitos de MQL;
- elementos de SQL;
- causas de não aderência ou roteamento;
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
- existe critério de aderência ao serviço;
- o objetivo é decidir o próximo atendimento adequado.

A skill pode criar:

- saudação e contextualização;
- perguntas principais;
- perguntas condicionais;
- perguntas de esclarecimento;
- orientações breves para o atendente;
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

- No WhatsApp, escreva mensagens curtas e indique quando aguardar.
- Em ligação ou recepção, use perguntas faláveis e transições naturais.
- Não transforme WhatsApp em interrogatório enviado de uma vez.
- Não transforme ligação em formulário lido mecanicamente.

Se o canal não estiver informado, use WhatsApp como `[PREMISSA OPERACIONAL]` somente quando o contexto indicar atendimento por mensagem. Caso contrário, escreva um roteiro neutro e falável.

---

# Princípios de qualificação

## 1. MQL jurídico

Use o MQL para identificar se o relato apresenta os requisitos materiais ou as condições objetivas mínimas que tornam a situação pertinente ao serviço.

A pré-qualificação pode identificar:

- requisito relatado;
- indício;
- ausência aparente;
- informação desconhecida;
- contradição;
- necessidade de confirmação.

Não transforme relato em confirmação documental.

## 2. SQL jurídico

Use o SQL para aprofundar os fatos, datas, vínculos, documentos ou elementos técnicos necessários à análise profissional da próxima etapa.

SQL jurídico não inclui:

- disponibilidade de agenda;
- comparecimento;
- rapidez de resposta;
- intenção imediata de contratar;
- aceitação de proposta;
- disposição atual para enviar documentos;
- participação de cônjuge ou terceiro.

Esses elementos pertencem à maturidade comercial ou à prontidão operacional.

## 3. Maturidade comercial e prontidão operacional

Registre separadamente:

- reconhecimento da necessidade;
- interesse em conhecer o próximo passo;
- intenção de avançar;
- disponibilidade;
- preferência de canal;
- capacidade atual de reunir documentos;
- necessidade de consultar terceiro;
- objeção ou impedimento operacional.

Um lead pode ser juridicamente aderente e ainda não estar pronto para avançar.

Um lead também pode querer contratar e não apresentar aderência suficiente.

## 4. Informação ausente

“Não sei”, “não lembro” ou “não tenho o documento agora” não equivalem automaticamente a não aderência.

Classifique como:

- informação pendente;
- elemento a confirmar;
- documento a obter;
- necessidade de revisão profissional.

## 5. Não aderência e roteamento

Diferencie:

- ausência aparente de requisito essencial;
- situação pertencente a outro serviço;
- caso fora do escopo do escritório;
- caso que exige análise profissional;
- impossibilidade operacional confirmada;
- informação insuficiente.

Nunca agrupe tudo como “desqualificado”.

---

# Estrutura obrigatória da saída

A entrega deve conter quatro blocos:

1. leitura estratégica;
2. roteiro comentado;
3. classificação e direcionamento;
4. roteiro final limpo e handoff.

---

# 1. Leitura estratégica

Apresente uma síntese interna curta com:

- nicho e serviço;
- natureza do serviço;
- canal utilizado;
- situação qualificadora central;
- requisitos principais de MQL;
- elementos de SQL necessários;
- urgências reais;
- principais causas de revisão ou roteamento;
- temas sensíveis;
- tom recomendado;
- próxima etapa esperada;
- informações operacionais ainda não confirmadas.

Não reproduza o Mapeamento.

---

# 2. Roteiro comentado

## 2.1. Saudação e contextualização

Crie uma única abertura recomendada.

Somente apresente alternativas quando o usuário pedir opções.

A abertura deve, conforme as informações disponíveis:

1. cumprimentar;
2. identificar o escritório;
3. indicar a área ou o serviço;
4. mencionar autoridade real, quando houver;
5. explicar a finalidade das perguntas;
6. preparar o lead para responder uma pergunta de cada vez.

Exemplo estrutural:

> Olá, [NOME]. Seja bem-vindo(a) ao [NOME DO ESCRITÓRIO].  
>   
> Para entendermos sua situação e direcionarmos o atendimento corretamente, vou fazer algumas perguntas iniciais. Podemos começar?

Adapte ao nicho e à persona.

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

Quando não houver prova de autoridade, omita. Não use placeholder desnecessário na fala final.

Não transforme a saudação em anúncio.

---

## 2.2. Perguntas principais

Selecione as perguntas mínimas necessárias para testar a situação qualificadora e os requisitos de MQL.

Comece por uma pergunta simples de contexto quando ela for necessária:

> O que aconteceu e fez você procurar o escritório?

Quando o nicho já delimitar claramente a situação, prefira uma pergunta específica.

As perguntas principais devem:

- testar um critério por vez;
- ser específicas para o nicho;
- usar linguagem simples;
- permitir resposta “não sei”;
- evitar narrativa extensa;
- não antecipar a consulta;
- não pedir todos os documentos;
- não introduzir preço ou contratação antes da aderência.

Organize na ordem mais natural, não necessariamente na ordem jurídica abstrata.

---

## 2.3. Perguntas condicionais

Inclua somente quando uma resposta alterar:

- aderência;
- subperfil;
- caminho jurídico;
- urgência;
- necessidade de documento;
- revisão profissional;
- roteamento.

Apresente a condição de uso.

Exemplo:

> **Use somente se a pessoa informar que já houve negativa:**  
> Você lembra quando recebeu a resposta e qual motivo foi informado?

Não crie dezenas de ramos.

---

## 2.4. Perguntas de esclarecimento

Para respostas ambíguas, proponha uma pergunta curta.

Exemplos:

> Só para eu entender: isso aconteceu antes ou depois de [MARCO]?

> Quando você diz que não recebeu, está falando de [OPÇÃO A] ou de [OPÇÃO B]?

> Você consegue estimar, mesmo que aproximadamente?

Faça apenas o esclarecimento necessário.

Se a pessoa não souber:

- registre a pendência;
- prossiga quando possível;
- não force resposta;
- não conclua ausência do requisito.

---

## 2.5. SQL e elementos de confirmação

Depois de verificar a aderência preliminar, inclua apenas as perguntas de aprofundamento necessárias à próxima análise profissional.

Podem envolver:

- datas;
- categoria;
- vínculo;
- histórico;
- pedido ou negativa anterior;
- processo em andamento;
- documento existente;
- valor ou impacto;
- prazo;
- local ou competência.

Pergunte inicialmente sobre a **existência** do documento, não sobre o envio completo, salvo instrução expressa do escritório.

Exemplo:

> Você possui algum laudo, contrato, comunicado ou documento relacionado a essa situação?

Explique a razão somente quando isso ajudar a pessoa a responder.

---

## 2.6. Urgência

Inclua perguntas de urgência apenas quando houver prazo, risco ou marco real relacionado ao nicho.

Exemplo estrutural:

> Existe alguma audiência, bloqueio, corte, prazo, leilão, perícia ou outra situação com data próxima?

Adapte ao caso.

Não crie urgência com:

- medo genérico;
- “mudança de lei” sem fonte;
- possibilidade remota;
- pressão comercial;
- tempo de resposta do lead.

---

## 2.7. Maturidade e prontidão

Somente depois da aderência preliminar, e quando isso for útil à operação, pergunte sobre o próximo passo.

Exemplo:

> Caso a equipe identifique pertinência para continuar, você deseja receber a orientação sobre a próxima etapa?

Se necessário, registre separadamente:

- interesse;
- disponibilidade;
- impedimento;
- preferência de canal;
- necessidade de falar com terceiro;
- capacidade atual de reunir documentos.

Não classifique essas respostas como MQL ou SQL jurídico.

---

# Apresentação estratégica das perguntas

Para cada pergunta, apresente internamente:

| Pergunta sugerida | Tipo | Critério testado | Por que importa | Resposta favorável ou aderente | Resposta inconclusiva | Resposta que exige revisão, roteamento ou atenção | Informação para handoff |
|---|---|---|---|---|---|---|---|

Use em **Tipo** apenas as categorias aplicáveis:

- MQL;
- SQL;
- urgência;
- complexidade;
- revisão profissional;
- roteamento;
- maturidade comercial;
- prontidão operacional.

Não use “lead quente”.

Não apresente essa tabela no roteiro final limpo.

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

Exemplo:

> Vou perguntar sobre a renda familiar porque esse ponto pode ser um requisito da análise inicial. Aproximadamente, qual é a renda mensal das pessoas que moram com você?

A pergunta sensível só deve existir quando estiver ligada a um requisito, bifurcação ou decisão real.

Não peça desculpas excessivamente.

---

# Quantidade e profundidade

A quantidade deve ser determinada pelos critérios do nicho.

Como regra:

- use apenas as perguntas necessárias;
- elimine redundâncias;
- agrupe somente o que puder ser respondido com clareza;
- faça uma pergunta por envio ou turno;
- não substitua consulta por triagem;
- não solicite narrativa completa;
- não peça documentação extensa;
- não investigue objeção comercial antes de saber se há aderência;
- não crie perguntas apenas para deixar o roteiro “completo”.

---

# 3. Classificação e direcionamento

A classificação é interna. Não mostre os rótulos ao lead.

Use os seguintes status:

## A. Avança

Use quando:

- há aderência preliminar;
- os fatos principais foram suficientemente delimitados para a próxima etapa;
- não apareceu causa objetiva de roteamento.

Mensagem estrutural:

> Obrigado por responder, [NOME].  
>   
> Pelas informações iniciais, existem elementos que justificam a continuidade da análise.  
>   
> O próximo passo será [PRÓXIMA ETAPA REAL]. [ORIENTAÇÃO OPERACIONAL CONFIRMADA.]

Não diga que o lead “tem direito”.

## B. Avança com pendências

Use quando:

- há aderência provável;
- falta confirmar dado, documento ou data;
- a pendência não impede a continuidade.

Mensagem estrutural:

> Obrigado pelas informações. Existem elementos para continuar, mas alguns pontos ainda precisam ser confirmados na próxima etapa.  
>   
> Vou registrar essas pendências para que a equipe dê continuidade corretamente.

## C. Revisão profissional

Use quando:

- existe ambiguidade relevante;
- há contradição;
- o enquadramento é controvertido;
- a equipe de atendimento não deve decidir sozinha.

Mensagem estrutural:

> Obrigado pelas informações, [NOME]. Alguns pontos precisam ser avaliados com mais cuidado antes de qualquer direcionamento. Vou repassar o seu relato para a equipe responsável.

Não prometa prazo de resposta não informado.

## D. Prioridade ou urgência

Use quando houver sinal objetivo de prazo ou risco.

Mensagem estrutural:

> Entendi. Como você relatou uma situação com [PRAZO OU RISCO], vou sinalizar essa informação para a equipe responsável.

Não prometa atendimento imediato.

A urgência pode coexistir com qualquer outro status.

## E. Roteamento

Use quando a necessidade pertence a outro serviço, área ou profissional.

Mensagem estrutural:

> Obrigado por explicar a situação. Pelo que foi relatado, o atendimento necessário parece estar relacionado a [OUTRO SERVIÇO OU ÁREA], e não ao serviço inicialmente selecionado.

Indique outro caminho somente quando ele for real e confirmado.

## F. Não aparenta aderência

Use quando o relato não apresenta requisito essencial e não há informação pendente capaz de alterar isso.

Mensagem estrutural:

> Obrigado por responder às perguntas. Pelas informações iniciais, sua situação não parece corresponder ao tipo de atendimento realizado pelo escritório neste serviço.  
>   
> Essa é uma avaliação inicial e não representa uma conclusão definitiva sobre todos os seus direitos.

## G. Informação insuficiente

Use quando faltam fatos indispensáveis e não é possível classificar.

Mensagem estrutural:

> Obrigado pelas informações enviadas. Alguns pontos essenciais ainda não ficaram claros e precisam ser verificados antes do direcionamento.

## H. Sem prontidão para avançar

Use quando há aderência, mas a pessoa não deseja ou não consegue continuar agora.

Mensagem estrutural:

> Sem problema. Obrigado pelo contato. Caso decida retomar o atendimento, você poderá falar conosco novamente pelos canais do escritório.

Não altere a classificação jurídica por causa disso.

---

# 4. Handoff e roteiro final

## 4.1. Resumo para o próximo profissional

Crie um modelo de repasse com esta estrutura:

```text
STATUS DA PRÉ-QUALIFICAÇÃO:
[Avança / Avança com pendências / Revisão profissional / Roteamento / Não aparenta aderência / Informação insuficiente]

PRIORIDADE OU URGÊNCIA:
[Não identificada / Identificada — descrever fato e data]

Nome:
Nicho ou serviço:
Motivo principal do contato:

Fatos relatados:
Requisitos de MQL indicados pelo relato:
Requisitos de MQL não identificados:
Elementos de SQL já delimitados:
Elementos que ainda precisam ser confirmados:
Contradições ou dúvidas:
Histórico relevante:
Documentos mencionados:
Documentos já recebidos:
Critério de roteamento, se houver:

Maturidade comercial:
Prontidão operacional:
Objeções, receios ou impedimentos:

Próximo passo recomendado:
Observação importante:
```

Regras:

- diferencie relato de confirmação;
- use “indicado pelo relato”, não “direito confirmado”;
- não registre “alta chance”;
- não declare culpa, fraude ou êxito;
- não classifique falta de disponibilidade como falta de aderência;
- indique `/agendamento` somente quando essa for a próxima skill real;
- registre fatos, datas e falas relevantes sem exagero interpretativo.

---

## 4.2. Roteiro final limpo

Ao final, entregue uma versão pronta para utilização.

Inclua apenas:

1. saudação recomendada;
2. contextualização;
3. perguntas principais na ordem;
4. perguntas condicionais com indicação breve de uso;
5. notas indispensáveis de espera ou esclarecimento;
6. mensagens de direcionamento por status.

Não inclua:

- explicações teóricas;
- objetivos;
- classificação MQL ou SQL;
- tabela estratégica;
- análise jurídica;
- código;
- instruções de automação;
- conversa fictícia não solicitada.

No WhatsApp:

- uma pergunta por mensagem;
- indicação de `*Aguarde a resposta.*`;
- não envie todos os ramos ao lead;
- não apresente mensagens de encerramento antes de saber o status.

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
- explicar perguntas sensíveis;
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
- Os requisitos de MQL e os elementos de SQL vieram do mapa?
- Nenhum critério jurídico foi inventado?
- O Core Cognitivo e o Core de Escrita foram aplicados?

## Arquitetura

- O produto é um roteiro humano de pré-qualificação?
- O canal foi identificado?
- A pré-qualificação não virou consulta?
- O material não virou chatbot ou lógica de automação?
- Não houve simulação sem pedido expresso?

## Perguntas

- As perguntas são específicas para o nicho?
- Cada pergunta testa um critério real?
- MQL foi investigado antes da maturidade comercial?
- SQL jurídico foi separado de prontidão operacional?
- Informação ausente virou pendência, e não exclusão automática?
- Existem apenas perguntas necessárias?
- A ordem é natural?
- Temas sensíveis foram contextualizados?
- Não há pedido documental excessivo?
- Urgência foi baseada em fato real?

## Classificação

- Os status internos são coerentes?
- Avanço com pendência foi diferenciado de revisão?
- Roteamento foi diferenciado de não aderência?
- Baixa prontidão não alterou a aderência jurídica?
- Nenhuma conclusão definitiva foi apresentada ao lead?

## Direcionamento

- O próximo passo é real?
- Não há promessa de prazo?
- Não há promessa de contato não confirmado?
- O texto evita a palavra “desqualificado”?
- As mensagens são respeitosas?

## Entrega

- Há leitura estratégica?
- Há roteiro comentado?
- Há classificação e mensagens de direcionamento?
- Há handoff?
- Há roteiro final limpo?
- Não há conteúdo duplicado sem função?

Corrija silenciosamente.

---

# Critérios de conclusão

A saída está completa quando:

- utiliza o Mapeamento de Persona;
- identifica corretamente a natureza do serviço;
- transforma requisitos de MQL em perguntas humanas;
- utiliza SQL somente para o aprofundamento necessário;
- separa qualificação jurídica de maturidade e prontidão;
- trata respostas incompletas como pendência quando adequado;
- reconhece urgência sem criá-la;
- diferencia avanço, pendência, revisão, roteamento e não aderência;
- produz direcionamentos compatíveis com cada status;
- cria handoff baseado em fatos e níveis de certeza;
- entrega roteiro final limpo;
- não realiza consulta;
- não cria automação;
- não inclui simulação sem pedido expresso.

A skill deve ajudar o escritório a receber bem, perguntar com propósito, classificar com segurança e encaminhar com clareza.





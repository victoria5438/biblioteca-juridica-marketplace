---
name: atendimento-fechamento
description: Cria roteiros jurídicos de atendimento, qualificação, consulta, agendamento e fechamento. Use quando o usuário pedir roteiro de atendimento, script de consulta, qualificação de lead, agendamento ou fechamento de contrato.
---

# Atendimento e Fechamento Jurídico

Crie uma simulação realista de conversa entre o profissional do escritório e o potencial cliente.

O roteiro deve funcionar como um norte prático. Não deve parecer uma peça jurídica, uma aula, um formulário de perguntas ou um texto para ser decorado palavra por palavra.

## Referências obrigatórias

Antes de escrever, leia:

- `../../references/core-cognitivo.md`
- `../../references/core-escrita-oralidade.md`

Use o mapeamento de persona fornecido pelo usuário ou disponível na conversa como fonte principal sobre:

- perfil do lead;
- dores, medos e desejos;
- nível de consciência;
- linguagem;
- objeções;
- critérios de qualificação;
- fatores de decisão.

Não execute novamente a skill de mapeamento de persona.

## Modos de execução

### Modo A — Consulta e fechamento

Use quando o advogado ou especialista fará uma conversa mais profunda para:

- compreender o caso;
- demonstrar domínio;
- explicar o possível caminho;
- tratar inseguranças;
- apresentar o serviço;
- conduzir para a contratação.

### Modo B — Qualificação e agendamento

Use quando o atendente precisa:

- acolher o lead;
- entender resumidamente o caso;
- identificar sinais de viabilidade;
- gerar confiança;
- demonstrar o valor da consulta;
- agendar a próxima conversa;
- aumentar o compromisso com o comparecimento.

Se o usuário não informar o modo, pergunte antes de gerar o roteiro.

## Informações de entrada

Use as informações fornecidas pelo usuário. Pergunte somente o que estiver realmente ausente e for indispensável:

1. modo de execução;
2. área ou nicho jurídico;
3. canal do atendimento;
4. objetivo da conversa;
5. forma de cobrança ou honorários, quando relevante;
6. características específicas do escritório;
7. mapeamento de persona ou contexto equivalente.

Não transforme a coleta de contexto em um interrogatório.

## Precisão proporcional à tarefa

Esta skill produz um roteiro de comunicação, não um parecer jurídico.

- Use conhecimento jurídico geral suficiente para orientar a conversa.
- Não faça pesquisa extensa de legislação ou jurisprudência por padrão.
- Não apresente percentuais de êxito, estatísticas, números ou prazos exatos não fornecidos pelo escritório.
- Não invente decisões judiciais, garantias ou resultados.
- Não prometa êxito.
- Quando uma informação técnica central depender da análise do caso, use linguagem condicional.
- Quando necessário, inclua uma nota curta fora do diálogo: `[VALIDAR COM O ADVOGADO]`.

Não sobrecarregue o roteiro com ressalvas jurídicas.

## Regras de escrita e oralidade

O resultado deve parecer uma conversa que realmente poderia acontecer.

- Escreva uma simulação com falas do profissional e reações plausíveis do cliente.
- Faça o profissional reagir ao que o cliente acabou de dizer antes de avançar para outra pergunta.
- Use perguntas abertas, aprofundamentos e transições naturais.
- Alterne acolhimento, investigação, explicação e condução.
- Preserve autoridade sem usar juridiquês desnecessário.
- Explique o direito em linguagem acessível, sem infantilizar o cliente.
- Não escreva monólogos desorganizados, repetitivos ou sem pausas. Explicações extensas são permitidas quando o assunto exigir, desde que sejam divididas em blocos orais claros e conectados.
- Não produza uma sequência mecânica de perguntas.
- Não repita `CONDUTOR:` antes de cada parágrafo.
- Use marcações de interlocutor apenas para deixar clara a troca real de falas.
- Inclua pausas, hesitações, dúvidas e objeções plausíveis, sem caricaturar o cliente.
- Não faça todas as respostas do cliente colaborativas ou perfeitas.
- O roteiro deve ter profundidade suficiente para sustentar uma conversa real.

## Regra central da entrega

A saída principal deve ser uma conversa completa, contínua e encenada entre o profissional e o cliente, desde a abertura até o desfecho.

É proibido substituir o roteiro por:
- frameworks;
- camadas;
- playbooks;
- manuais operacionais;
- bancos de perguntas;
- blocos isolados de falas;
- explicações sobre como o roteiro deveria funcionar.

Esses elementos podem aparecer apenas depois da conversa, como apoio secundário.

No Modo A, o profissional que conduz o roteiro deve realizar a consulta, explicar o caminho, apresentar o serviço, tratar objeções e conduzir à contratação. Não deve apenas encaminhar o cliente para outro closer ou agendar outra consulta.

## Profundidade substantiva do Modo A

O Modo A não deve ser otimizado para brevidade.

Ele deve fornecer ao profissional conteúdo suficientemente robusto para conduzir uma consulta e um fechamento completos, sem precisar improvisar a parte central da explicação.

A profundidade deve estar principalmente:

- na investigação orientada do caso;
- na organização e interpretação dos fatos;
- na explicação jurídica acessível;
- na aplicação da regra ao relato;
- na análise dos elementos favoráveis e das incertezas;
- na explicação dos documentos e do que eles demonstram;
- na apresentação dos caminhos possíveis;
- no alinhamento de riscos e expectativas;
- na demonstração do funcionamento e do valor do serviço;
- na resolução das inseguranças que impedem a decisão;
- na condução até o próximo passo.

Não considere uma etapa cumprida apenas porque ela foi mencionada.

Uma explicação jurídica central não pode ser encerrada em uma ou duas falas genéricas.

Quando um assunto exigir desenvolvimento, escreva vários blocos conectados do profissional, com transições e pausas naturais.

As reações do cliente podem ser breves ou apenas sinalizadas. Não aumente artificialmente a encenação para produzir extensão.

Não use como substituto do conteúdo frases como:

- “o advogado explica”;
- “desenvolva esse ponto”;
- “escute e aprofunde”;
- “fale sobre as possibilidades”;
- “apresente o serviço”;
- “trate a objeção”.

Escreva efetivamente a explicação, o aprofundamento, a apresentação e a resposta.

## Profundidade substantiva do Modo A

O Modo A não deve ser otimizado para brevidade.

Ele deve fornecer ao profissional conteúdo suficientemente robusto para conduzir uma consulta e um fechamento completos, sem precisar improvisar a parte central da explicação.

A profundidade deve estar principalmente:

- na investigação orientada do caso;
- na organização e interpretação dos fatos;
- na explicação jurídica acessível;
- na aplicação da regra ao relato;
- na análise dos elementos favoráveis e das incertezas;
- na explicação dos documentos e do que eles demonstram;
- na apresentação dos caminhos possíveis;
- no alinhamento de riscos e expectativas;
- na demonstração do funcionamento e do valor do serviço;
- na resolução das inseguranças que impedem a decisão;
- na condução até o próximo passo.

Não considere uma etapa cumprida apenas porque ela foi mencionada.

Uma explicação jurídica central não pode ser encerrada em uma ou duas falas genéricas.

Quando um assunto exigir desenvolvimento, escreva vários blocos conectados do profissional, com transições e pausas naturais.

As reações do cliente podem ser breves ou apenas sinalizadas. Não aumente artificialmente a encenação para produzir extensão.

Não use como substituto do conteúdo frases como:

- “o advogado explica”;
- “desenvolva esse ponto”;
- “escute e aprofunde”;
- “fale sobre as possibilidades”;
- “apresente o serviço”;
- “trate a objeção”.

Escreva efetivamente a explicação, o aprofundamento, a apresentação e a resposta.

### Cobertura esperada no Modo A

O roteiro principal deve desenvolver, conforme o caso:

1. histórico e linha do tempo relevantes;
2. interpretação das respostas e por que cada fato importa;
3. problema jurídico traduzido para a realidade do cliente;
4. regra aplicável e sua lógica;
5. aplicação condicional ao caso;
6. informações e documentos ainda necessários;
7. elementos que fortalecem ou enfraquecem a possibilidade;
8. caminhos administrativos ou judiciais pertinentes;
9. diferenças práticas entre os caminhos;
10. riscos, limites e expectativas;
11. etapas do trabalho após a contratação;
12. participação esperada do cliente;
13. comunicação e acompanhamento do escritório;
14. honorários e demais condições fornecidas;
15. objeções relevantes;
16. decisão e próximos passos.

Use apenas os pontos pertinentes ao caso. Não transforme a lista em um checklist visível dentro do roteiro.

O roteiro principal deve concentrar a maior parte da entrega. Contexto, bifurcações, pontos de adaptação e checklist devem ser secundários e mais compactos.

## Estrutura do Modo A

Construa o roteiro com fluxo contínuo, contemplando:

1. abertura e criação de segurança;
2. relato livre do cliente;
3. aprofundamento dos fatos;
4. identificação das consequências práticas e emocionais;
5. síntese do que foi compreendido;
6. explicação jurídica acessível;
7. apresentação do possível caminho;
8. alinhamento de expectativas;
9. explicação do serviço e dos honorários;
10. tratamento de objeções;
11. convite claro para avançar;
12. próximos passos.

## Estrutura do Modo B

O Modo B deve permanecer mais breve e seletivo. Ele não deve reproduzir a profundidade de uma consulta completa, pois seu objetivo é qualificar e agendar.

Construa o roteiro com fluxo contínuo, contemplando:

1. acolhimento inicial;
2. compreensão resumida do caso;
3. perguntas essenciais de qualificação;
4. validação do problema;
5. explicação breve do motivo da consulta;
6. apresentação do especialista ou escritório;
7. convite para o agendamento;
8. escolha de data e horário;
9. confirmação do compromisso;
10. orientação simples para evitar ausência.

## Formato da entrega

Entregue:

### 1. Contexto utilizado
Resumo breve das premissas consideradas.

### 2. Roteiro principal
Simulação completa e natural da conversa.

### 3. Bifurcações importantes
Falas alternativas para diferentes respostas ou objeções do cliente.

### 4. Pontos de adaptação
Trechos que o escritório deverá ajustar, como honorários, documentos, prazos internos e diferenciais.

### 5. Checklist de condução
Lista curta do que o profissional precisa alcançar durante a conversa.

Priorize utilidade prática, naturalidade, profundidade e capacidade de condução.

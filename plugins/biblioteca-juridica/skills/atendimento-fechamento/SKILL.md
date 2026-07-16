---
name: atendimento-fechamento
description: Cria roteiros operacionais jurídicos reutilizáveis para qualificação, consulta, agendamento e fechamento. Use quando o usuário pedir roteiro de atendimento, playbook, script de consulta, qualificação de lead, agendamento ou fechamento de contrato.
---

# Atendimento e Fechamento Jurídico

Produza um roteiro operacional reutilizável para condução de atendimentos jurídicos.

O material deve funcionar como um ativo interno do escritório e poder ser utilizado repetidamente por profissionais diferentes com clientes distintos do mesmo nicho.

Não transforme a persona em personagem e não invente uma história individual como fio condutor.

A persona deve orientar linguagem, prioridades, objeções, critérios, explicações e bifurcações.

---

## Referências obrigatórias

Antes de escrever, leia:

- `../../references/core-cognitivo.md`
- `../../references/core-escrita-oralidade.md`

Use o mapeamento de persona fornecido pelo usuário ou disponível na conversa como fonte principal sobre:

- perfil do público;
- dores, medos e desejos;
- nível de consciência;
- linguagem;
- objeções;
- critérios de qualificação;
- fatores de decisão;
- subperfis e variações relevantes.

Não execute novamente a skill de mapeamento de persona.

---

## Regra central da entrega

A saída principal deve ser um roteiro operacional completo, profundo e reutilizável.

Organize o material por etapas de condução, e não por uma história fictícia contínua.

O produto deve ensinar o profissional a conduzir o atendimento e também entregar conteúdo pronto para uso.

Não substitua o roteiro por:

- uma conversa com uma persona fictícia específica;
- um caso inventado tratado como padrão;
- uma lista superficial de tópicos;
- instruções vagas sem explicação;
- um formulário de perguntas desconectadas;
- blocos que apenas dizem “explique”, “aprofunde” ou “trate a objeção”.

Escreva efetivamente:

- as orientações;
- as perguntas;
- os motivos das perguntas;
- os critérios de observação;
- as explicações substantivas;
- os exemplos de fala;
- as bifurcações;
- as respostas às objeções;
- a condução do fechamento.

---

## Regra de reutilização

O roteiro deve continuar útil mesmo que mudem:

- nome;
- idade;
- profissão;
- cidade;
- datas;
- composição familiar;
- detalhes pessoais;
- profissional que atende.

Use referências genéricas, como:

- cliente;
- potencial cliente;
- segurada;
- gestante;
- mãe;
- trabalhador;
- pessoa atendida.

Use placeholders somente para dados adaptáveis, como:

- `[NOME]`;
- `[ESCRITÓRIO]`;
- `[OAB]`;
- `[HONORÁRIOS]`;
- `[CANAL]`;
- `[DATA]`;
- `[HORÁRIO]`;
- `[DOCUMENTO]`.

Exemplos específicos podem aparecer apenas como ilustrações breves ou bifurcações condicionais.

---

## Tronco comum e bifurcações

Quando o nicho tiver subperfis relevantes:

1. construa primeiro o tronco comum do atendimento;
2. identifique em qual etapa o profissional descobre o subperfil;
3. apresente os ramos condicionais;
4. explique o que muda em perguntas, documentos, explicação, objeções e próximo passo;
5. retorne ao fluxo comum quando possível.

Não escolha um subperfil como personagem principal, salvo se o usuário pedir expressamente um recorte.

---

## Modos de execução

### Modo A — Consulta e fechamento

Use quando o advogado ou especialista conduzirá uma conversa completa para:

- compreender e organizar o caso;
- demonstrar domínio;
- explicar o problema e os caminhos possíveis;
- alinhar riscos e expectativas;
- mostrar o valor do serviço;
- apresentar honorários;
- tratar inseguranças;
- conduzir à decisão de contratação.

O Modo A deve ser profundo e substantivo. Não o otimize para brevidade.

### Modo B — Qualificação e agendamento

Use quando o atendente precisa:

- acolher o lead;
- entender resumidamente o caso;
- identificar sinais de viabilidade;
- filtrar situações fora de escopo;
- gerar confiança;
- demonstrar o valor da consulta;
- agendar a próxima conversa;
- aumentar o compromisso com o comparecimento.

O Modo B deve permanecer mais breve e seletivo. Ele não deve reproduzir uma consulta completa.

Se o usuário não informar o modo e os resultados forem incompatíveis, pergunte antes de gerar.

Se o usuário pedir os dois modos, entregue dois roteiros separados, sem misturar seus objetivos.

---

## Informações de entrada

Use as informações fornecidas pelo usuário. Pergunte somente o que estiver realmente ausente e for indispensável:

1. modo de execução;
2. área ou nicho jurídico;
3. canal do atendimento;
4. objetivo da conversa;
5. forma de cobrança ou honorários, quando relevante;
6. características específicas do escritório;
7. mapeamento de persona ou contexto equivalente.

Não transforme a coleta de contexto em interrogatório.

---

## Precisão proporcional à tarefa

Esta skill produz um roteiro de comunicação e operação, não um parecer jurídico.

- Use conhecimento jurídico geral suficiente para orientar a conversa.
- Não faça pesquisa extensa de legislação ou jurisprudência por padrão.
- Não apresente percentuais de êxito, estatísticas, números ou prazos exatos não fornecidos pelo escritório.
- Não invente decisões judiciais, garantias ou resultados.
- Não prometa êxito.
- Quando uma informação técnica central depender da análise do caso, use linguagem condicional.
- Quando necessário, inclua uma nota curta: `[VALIDAR COM O ADVOGADO]` ou `[VALIDAR JURIDICAMENTE]`.
- Não sobrecarregue o roteiro com ressalvas jurídicas.

---

## Profundidade substantiva

Profundidade significa oferecer material suficiente para que o profissional consiga conduzir e explicar os assuntos centrais sem precisar improvisar o conteúdo principal.

A profundidade deve estar principalmente:

- na investigação orientada;
- na interpretação do que cada resposta pode indicar;
- na explicação jurídica acessível;
- na relação entre fatos, regra e documentos;
- nas diferenças entre cenários;
- nos caminhos possíveis;
- nos limites e expectativas;
- no funcionamento e no valor do serviço;
- na resolução das inseguranças que impedem o próximo passo.

Não considere uma etapa cumprida apenas porque foi mencionada.

Uma explicação central não pode ser encerrada em uma ou duas falas genéricas.

Quando um assunto exigir desenvolvimento, escreva vários blocos conectados, com linguagem falável e sem repetição.

Não confunda profundidade com:

- criar uma biografia para o cliente;
- encenar muitas reações;
- aumentar artificialmente o número de falas;
- repetir a mesma ideia;
- inserir história jurídica desnecessária;
- transformar o roteiro em parecer.

---

## Estrutura de cada etapa

Para cada etapa do roteiro operacional, inclua, quando pertinente:

### Objetivo

O que o profissional precisa alcançar.

### Orientação de condução

Como abordar o momento e qual postura adotar.

### Perguntas sugeridas

Perguntas prontas e adaptáveis.

### Por que perguntar

A função de cada pergunta ou grupo de perguntas.

### O que observar

Sinais, lacunas, contradições, documentos, objeções ou critérios.

### Explicação substantiva

Conteúdo que o profissional pode utilizar para explicar o assunto.

### Exemplos de fala

Falas naturais, genéricas e adaptáveis.

### Bifurcações

Como mudar a condução conforme respostas ou situações.

### Erros a evitar

Condutas que geram confusão, perda de confiança ou fechamento prematuro.

### Critério para avançar

O que precisa estar esclarecido antes da etapa seguinte.

Não repita todos os subtítulos mecanicamente quando algum deles não for útil.

---

## Estrutura do Modo A

O roteiro deve desenvolver, conforme o nicho:

1. abertura e criação de segurança;
2. relato inicial e organização da demanda;
3. investigação dos fatos e da linha do tempo;
4. identificação do subperfil ou cenário;
5. critérios de qualificação e pontos que exigem confirmação;
6. síntese do problema;
7. explicação jurídica acessível e aprofundada;
8. aplicação da explicação aos possíveis cenários;
9. fatos e documentos que fortalecem ou enfraquecem o caminho;
10. alternativas administrativas ou judiciais pertinentes;
11. diferenças práticas, limites, riscos e expectativas;
12. funcionamento do trabalho do escritório;
13. etapas após a contratação;
14. participação esperada do cliente;
15. comunicação e acompanhamento;
16. honorários e demais condições fornecidas;
17. objeções relevantes;
18. apresentação da proposta;
19. decisão de contratação;
20. contrato, procuração, documentos e próximos passos.

Use apenas os pontos pertinentes ao nicho. Não transforme essa lista em checklist visível dentro do roteiro.

O roteiro principal deve concentrar a maior parte da entrega. Contexto, checklist e notas finais devem ser mais compactos.

---

## Fechamento efetivo no Modo A

O Modo A não deve terminar apenas com:

- pedido de documentos para análise preliminar;
- convite para outra consulta;
- promessa de avaliar posteriormente;
- agendamento de nova conversa;
- proposta sem decisão.

Depois de explicar o problema, o caminho, os limites, o serviço e os honorários, o profissional deve:

1. verificar se ainda existe insegurança relevante;
2. responder às objeções necessárias;
3. apresentar claramente a proposta do escritório;
4. perguntar se o cliente deseja contratar;
5. aguardar a decisão;
6. quando houver aceite, iniciar o envio do contrato, procuração e documentos;
7. quando houver hesitação, identificar o motivo e combinar um próximo passo concreto;
8. quando não houver elementos suficientes para uma proposta responsável, encerrar a consulta com essa conclusão clara, sem simular fechamento artificial.

Não use “análise sem compromisso” como fechamento do Modo A. Essa linguagem pertence à etapa anterior à consulta.

---

## Estrutura do Modo B

O roteiro deve desenvolver:

1. acolhimento inicial;
2. compreensão resumida da demanda;
3. perguntas essenciais de qualificação;
4. identificação preliminar do subperfil;
5. sinais de viabilidade e desqualificação;
6. validação do problema sem prometer resultado;
7. explicação breve do valor da consulta;
8. apresentação do especialista ou escritório;
9. convite para o agendamento;
10. escolha de data e horário;
11. confirmação do compromisso;
12. orientação simples para reduzir ausência.

Não entregue no Modo B a explicação completa reservada à consulta.

---

## Banco de objeções

Para cada objeção relevante, entregue:

1. como ela costuma aparecer;
2. o medo ou a dúvida real;
3. pergunta para diagnosticar o motivo;
4. resposta substantiva;
5. exemplo de fala;
6. sinal de que a objeção foi resolvida;
7. próximo passo.

Não crie uma longa cena fictícia para cada objeção.

---

## Regras de escrita e oralidade

- Os exemplos de fala devem soar naturais e profissionais.
- Preserve autoridade sem juridiquês desnecessário.
- Explique o Direito em linguagem acessível, sem infantilizar.
- Não escreva monólogos desorganizados, repetitivos ou sem pausas.
- Explicações extensas são permitidas quando o assunto exigir.
- Divida explicações complexas em blocos faláveis.
- Não transforme o roteiro em sequência mecânica de perguntas.
- Use transições para ligar perguntas, explicações e etapas.
- Não repita `CONDUTOR:` ou o nome do papel antes de cada parágrafo.
- Use notas de condução apenas quando ajudarem a execução.
- Não aumente artificialmente a encenação do cliente para produzir extensão.
- Não seja telegráfico, genérico ou excessivamente objetivo nos assuntos centrais.
- Evite repetição e prolixidade sem função.

---

## Formato da entrega

### 1. Contexto e premissas

Resumo breve do nicho, canal, objetivo, honorários e pontos que precisam ser adaptados.

### 2. Visão geral do fluxo

Mapa resumido das etapas do atendimento.

### 3. Roteiro operacional principal

Desenvolva as etapas aplicáveis com orientação, perguntas, motivos, observações, explicações substantivas, exemplos de fala, bifurcações, erros e critérios de avanço.

### 4. Banco de objeções

Inclua apenas as objeções relevantes ao nicho e ao modo escolhido.

### 5. Fechamento e próximos passos

Condução até contratação no Modo A ou até agendamento no Modo B.

### 6. Pontos de adaptação

Honorários, documentos, diferenciais, responsáveis, agenda, ferramentas e políticas internas.

### 7. Checklist de aplicação

Lista curta para consulta durante o atendimento.

---

## Revisão interna obrigatória

Antes de entregar, verifique:

- o produto é um roteiro operacional reutilizável, salvo pedido expresso de simulação?
- a persona orientou o texto sem virar personagem?
- o roteiro funciona com clientes diferentes?
- existe tronco comum e bifurcações para as variações relevantes?
- o conteúdo está específico para o nicho?
- as explicações centrais estão realmente desenvolvidas?
- o profissional recebeu conteúdo pronto e não apenas temas?
- os exemplos de fala são naturais e adaptáveis?
- o Modo A chega a uma decisão de contratação?
- o Modo B termina em agendamento sem antecipar a consulta?
- há promessa, dado inventado ou urgência artificial?
- apenas particularidades do escritório e fatos do cliente real precisam ser adaptados?

Corrija silenciosamente antes de finalizar.

---
name: pre-qualificacao
description: Cria um roteiro humano de pré-qualificação jurídica, dividido em boas-vindas, perguntas de qualificação estratégica e agradecimento com direcionamento. Usa o Mapeamento de Persona para transformar critérios de MQL, SQL, urgência e desqualificação em uma conversa clara, ética e adequada ao nicho.
argument-hint: Informe o nicho jurídico e forneça o Mapeamento de Persona. Acrescente dados reais do escritório, como nome, áreas de atuação, prova social, responsável pelo atendimento e forma de continuidade.
---

# Pré-qualificação

## Função desta skill

Criar um roteiro humano de pré-qualificação para uso pela equipe do escritório.

O roteiro deve cumprir três funções, nesta ordem:

1. receber o lead e apresentar o escritório;
2. fazer as perguntas mínimas necessárias para compreender a situação inicial;
3. agradecer e direcionar o lead para a próxima etapa adequada.

A estrutura central é:

> boas-vindas  
> → contextualização da conversa  
> → perguntas de qualificação estratégica  
> → agradecimento  
> → direcionamento

Esta skill não deve criar automações, árvores de decisão técnicas, fluxos de chatbot, integrações com CRM, códigos, gatilhos ou instruções de sistema.

O resultado deve parecer um roteiro de atendimento que uma pessoa do escritório conseguiria utilizar em uma conversa real.

---

## Referências obrigatórias

Antes de produzir a saída:

1. leia `${CLAUDE_PLUGIN_ROOT}/references/core-cognitivo.md`;
2. leia `${CLAUDE_PLUGIN_ROOT}/references/core-escrita-oralidade.md`;
3. utilize o Mapeamento de Persona Jurídica fornecido pelo usuário ou disponível na conversa;
4. priorize informações reais sobre o escritório e o serviço;
5. não execute novamente a skill `/mapear-persona`.

O Mapeamento de Persona deve ser usado especialmente para localizar:

- critérios de MQL;
- critérios de SQL;
- perguntas-chave de pré-qualificação;
- respostas que indicam lead quente;
- critérios de desqualificação;
- sinais de urgência;
- dores, desejos, receios e objeções;
- vocabulário e nível de compreensão da persona.

Não reproduza o Mapeamento de Persona inteiro na saída.

Converta-o em decisões concretas de:

- ordem das perguntas;
- linguagem;
- profundidade;
- quantidade de perguntas;
- critérios que merecem atenção;
- tom da saudação;
- forma de encerramento;
- informações que devem ser repassadas ao próximo profissional.

Caso o Mapeamento de Persona não esteja disponível, solicite o documento ou, no mínimo:

- critérios de qualificação;
- critérios de desqualificação;
- perguntas-chave;
- sinais de urgência;
- perfil da persona.

Não invente esses critérios.

---

## Escopo

Use esta skill quando:

- o lead iniciou contato com o escritório;
- ainda não passou pela pré-qualificação;
- o escritório precisa compreender os fatos iniciais;
- existe um Mapeamento de Persona que define critérios estratégicos;
- o objetivo é preparar o lead para o próximo atendimento.

A skill pode criar:

- modelos de saudação;
- breve apresentação do escritório;
- uso ético de prova social;
- explicação da etapa de pré-qualificação;
- perguntas estratégicas;
- orientações para respostas incompletas;
- agradecimento;
- mensagens de direcionamento;
- resumo de repasse para o próximo profissional;
- exemplo completo de conversa fictícia;
- roteiro final limpo.

A skill não deve:

- realizar consulta jurídica;
- dar parecer;
- concluir definitivamente que existe ou não existe direito;
- prometer resultado;
- pedir documentação extensa;
- montar estratégia jurídica;
- negociar honorários do caso;
- fazer agendamento;
- confirmar presença;
- recuperar no-show;
- criar follow-up;
- produzir adaptação para automação;
- apresentar código ou lógica de sistema.

---

# Estrutura obrigatória da saída

A resposta deve ser dividida nos três blocos principais abaixo.

# 1. Saudação inicial ou boas-vindas

Crie de duas a quatro opções de abertura.

As opções podem variar entre:

- acolhedora;
- institucional;
- direta;
- próxima e conversacional.

Depois, recomende uma delas e explique brevemente por que combina com a persona.

A saudação deve, conforme as informações disponíveis:

1. cumprimentar;
2. identificar o escritório;
3. apresentar a área ou o nicho;
4. mencionar uma prova de autoridade real, quando houver;
5. explicar que serão feitas perguntas iniciais;
6. preparar o lead para responder com tranquilidade.

## Elementos permitidos

Podem ser utilizados:

- nome do escritório;
- área de atuação;
- nicho;
- perfil de atendimento;
- experiência real;
- número real de atendimentos;
- reconhecimento real;
- especialização real;
- localização real;
- característica verdadeira do método de atendimento.

## Prova social

Use prova social somente quando ela tiver sido fornecida ou estiver confirmada.

Não invente:

- número de clientes;
- anos de atuação;
- quantidade de casos vencidos;
- índice de sucesso;
- prêmios;
- títulos;
- certificações;
- presença nacional;
- resultados;
- depoimentos.

Quando não houver prova social disponível:

- use um placeholder claro; ou
- omita esse trecho.

Não transforme a abertura em anúncio publicitário.

## Modelos estruturais

### Modelo acolhedor

> Olá, [NOME]. Seja bem-vindo(a) ao [NOME DO ESCRITÓRIO].  
>   
> Nosso escritório atua com [ÁREA OU NICHO], ajudando pessoas que enfrentam situações relacionadas a [PROBLEMA CENTRAL].  
>   
> Para entendermos melhor o que aconteceu e direcionarmos seu atendimento da forma correta, vou fazer algumas perguntas iniciais. Tudo bem?

### Modelo institucional

> Seja bem-vindo(a) ao [NOME DO ESCRITÓRIO].  
>   
> Somos um escritório com atuação em [ÁREA OU NICHO]. [PROVA DE AUTORIDADE REAL.]  
>   
> Antes de encaminhar seu atendimento ao profissional responsável, precisamos compreender alguns pontos da sua situação.

### Modelo próximo e direto

> Olá, [NOME]. Obrigado por entrar em contato com o [NOME DO ESCRITÓRIO].  
>   
> Para que a equipe consiga entender sua situação e indicar o próximo passo mais adequado, vou fazer algumas perguntas rápidas.

Os modelos são referências de estrutura. A skill deve escrever versões específicas para o nicho e para a persona.

---

# 2. Perguntas de qualificação estratégica

## Objetivo

Transformar os critérios do Mapeamento de Persona em uma conversa organizada, clara e humana.

As perguntas devem permitir que o escritório identifique:

- se a situação pertence ao nicho atendido;
- se os critérios jurídicos iniciais estão presentes;
- se faltam informações relevantes;
- se existe urgência;
- se há alguma circunstância que exige revisão profissional;
- se o lead demonstra intenção real de avançar.

A pré-qualificação não deve resolver o caso.

Ela deve reunir informação suficiente para decidir qual é o próximo atendimento adequado.

---

## Seleção das perguntas

Não copie automaticamente todas as perguntas do Mapeamento de Persona.

Faça o seguinte:

1. identifique os critérios indispensáveis;
2. elimine perguntas redundantes;
3. agrupe temas semelhantes;
4. coloque primeiro as perguntas mais fáceis;
5. deixe temas sensíveis para depois do acolhimento;
6. inclua perguntas condicionais somente quando forem necessárias;
7. evite pedir detalhes que pertencem à consulta;
8. preserve as perguntas que diferenciam MQL, SQL, urgência e desqualificação.

Prefira um roteiro enxuto e suficiente a um interrogatório completo.

Quando houver muitos critérios, separe em:

- perguntas principais;
- perguntas de aprofundamento;
- perguntas condicionais.

---

## Ordem recomendada

Adapte esta ordem ao nicho.

### A. Identificação da situação

Comece entendendo o motivo do contato.

Exemplos:

> O que aconteceu e fez você procurar o escritório?

> Qual situação você gostaria que nossa equipe analisasse?

Quando o nicho permitir, ofereça opções simples.

### B. Critérios jurídicos centrais

Pergunte sobre os fatos que sustentam a viabilidade inicial.

A formulação deve refletir o Mapeamento de Persona.

Não use perguntas genéricas que poderiam servir para qualquer caso.

### C. Tempo e sequência dos fatos

Investigue datas e períodos somente quando forem juridicamente relevantes.

Exemplos:

> Quando isso aconteceu?

> Há quanto tempo essa situação existe?

> O problema começou antes ou depois de [MARCO RELEVANTE]?

Não invente prazos.

### D. Histórico relevante

Quando necessário, pergunte se:

- houve pedido anterior;
- houve negativa;
- existe processo em andamento;
- houve acordo;
- existe decisão;
- o lead já foi atendido por outro profissional;
- alguma medida já foi tomada.

Não presuma ausência de processo, documento, acordo ou decisão.

### E. Provas e documentos essenciais

Pergunte apenas sobre a existência dos meios básicos de comprovação.

Exemplo:

> Você possui algum documento relacionado a essa situação?

Caso necessário, cite exemplos simples.

Não solicite o envio de todos os documentos nesta etapa, salvo instrução expressa do escritório.

### F. Urgência real

Inclua pergunta de urgência somente quando houver relação com o nicho.

Exemplo:

> Existe algum prazo, audiência, corte de benefício, risco imediato ou outra situação urgente acontecendo agora?

Não transforme toda situação em urgência.

### G. Interesse em avançar

Depois de verificar os critérios iniciais, pergunte sobre a disposição para continuar.

Exemplo:

> Caso a equipe identifique um caminho possível, você tem interesse em conversar com o profissional responsável para entender os próximos passos?

Não pressione.

---

## Forma das perguntas

As perguntas devem:

- ser curtas;
- usar linguagem simples;
- ser feitas uma de cada vez;
- evitar juridiquês;
- explicar termos inevitáveis;
- permitir “não sei”;
- permitir respostas aproximadas quando a precisão não for indispensável;
- respeitar a vulnerabilidade da persona;
- pedir esclarecimento sem constrangimento;
- evitar juízo de valor;
- evitar tom policial ou interrogatório.

## Perguntas sensíveis

Quando houver temas como:

- renda;
- saúde;
- violência;
- deficiência;
- morte;
- dependência;
- separação;
- demissão;
- discriminação;
- dívida;
- situação migratória;
- acusação criminal;

introduza a pergunta com contexto.

Exemplo:

> Vou precisar perguntar sobre a renda da família porque esse ponto pode ser relevante para a análise inicial do benefício. Aproximadamente, qual é a renda mensal das pessoas que moram com você?

Não peça desculpas excessivamente.

Explique apenas o necessário.

---

## Para cada pergunta, apresente

Na parte estratégica da saída, informe:

### Pergunta

Texto sugerido para o atendimento.

### Objetivo

O que o escritório precisa compreender.

### Critério relacionado

Indique se está ligada a:

- viabilidade inicial;
- MQL;
- SQL;
- urgência;
- desqualificação;
- necessidade de revisão profissional.

### Respostas que merecem atenção

Aponte, de forma objetiva:

- sinais favoráveis;
- informações ausentes;
- contradições;
- respostas que exigem aprofundamento;
- fatores que podem afastar o enquadramento;
- situações urgentes.

Não transforme essa análise em conclusão jurídica definitiva.

---

## Respostas incompletas ou ambíguas

Oriente a equipe a fazer uma única pergunta de esclarecimento quando a resposta não permitir compreender o critério.

Exemplos:

> Só para eu entender melhor: isso aconteceu antes ou depois de [FATO]?

> Quando você diz que não recebeu, está se referindo a [OPÇÃO A] ou [OPÇÃO B]?

> Você consegue estimar, mesmo que aproximadamente?

Se o lead não souber, registre a dúvida e prossiga quando possível.

Não force uma resposta.

---

## Quantidade e profundidade

A skill deve escolher a quantidade conforme o nicho.

Como regra:

- faça apenas as perguntas necessárias para a decisão inicial;
- mantenha o fluxo suficientemente curto;
- não substitua a consulta;
- não repita perguntas;
- não peça narrativa completa;
- não peça todos os documentos;
- não antecipe defesa, estratégia ou tese jurídica.

Quando houver critérios muito diferentes dentro do mesmo nicho, crie pequenos blocos condicionais.

Não produza dezenas de bifurcações.

---

# 3. Agradecimento e direcionamento

Crie mensagens finais de acordo com o resultado da pré-qualificação.

Nunca use a palavra “desqualificado” com o lead.

Não faça diagnóstico definitivo.

Não anuncie direito garantido.

Não prometa retorno em prazo que o escritório não informou.

Não diga que um especialista entrará em contato se essa não for a operação real.

Use placeholders quando faltarem informações operacionais.

---

## A. Quando existem elementos para avançar

Estrutura:

> agradecimento  
> + reconhecimento de que as informações foram registradas  
> + indicação de que o caso merece continuidade  
> + próximo passo real  
> + orientação para aguardar

Exemplo:

> Obrigado por responder às perguntas, [NOME].  
>   
> Pelas informações iniciais, existem elementos que justificam uma análise mais aprofundada da sua situação.  
>   
> Agora, [PRÓXIMO PROFISSIONAL OU EQUIPE] dará continuidade ao atendimento para explicar o que foi identificado e como o escritório poderá ajudar.  
>   
> Por favor, aguarde por aqui.

Quando o próximo passo for a skill `/agendamento`, deixe isso claro apenas no resumo interno, não no texto enviado ao lead.

---

## B. Quando o caso precisa de revisão profissional

> Obrigado pelas informações, [NOME].  
>   
> Alguns pontos da sua situação precisam ser avaliados com mais cuidado antes de qualquer direcionamento. Vou repassar o que você informou para a equipe responsável.  
>   
> Por favor, aguarde por aqui.

---

## C. Quando houver urgência ou sensibilidade

> Entendi. Como você relatou uma situação que pode exigir atenção mais rápida, vou encaminhar essas informações diretamente para a equipe responsável.

Não prometa atendimento imediato sem confirmação operacional.

---

## D. Quando a situação não aparenta aderência ao serviço

> Obrigado por responder às perguntas.  
>   
> Pelas informações iniciais, sua situação não parece se enquadrar no tipo de atendimento realizado pelo escritório neste momento.  
>   
> Essa é apenas uma avaliação inicial e não representa uma conclusão definitiva sobre seus direitos.

Acrescente orientação para outro canal somente quando ela for real.

---

## E. Quando faltam informações essenciais

> Obrigado pelas informações enviadas até aqui.  
>   
> Ainda existem alguns pontos que não ficaram claros e que precisam ser verificados antes do direcionamento. Vou registrar o que você informou para análise da equipe.

---

## F. Quando o lead não deseja continuar

> Sem problema. Obrigado pelo contato. Caso decida retomar o atendimento, estaremos à disposição pelos canais do escritório.

Não faça insistência.

---

# Leitura estratégica inicial

Antes dos três blocos principais, apresente uma síntese interna com:

- nicho;
- perfil da persona;
- objetivo da pré-qualificação;
- critérios centrais;
- critérios de urgência;
- critérios de desqualificação;
- temas sensíveis;
- tom recomendado;
- próximo passo esperado.

Essa síntese deve ser curta.

Não reproduza todo o mapa.

---

# Resumo para o próximo profissional

Depois do roteiro, crie um modelo de repasse interno.

Use esta estrutura:

```text
STATUS DA PRÉ-QUALIFICAÇÃO:

Nome:
Nicho ou assunto:
Motivo principal do contato:
Critérios confirmados:
Critérios não confirmados:
Informações pendentes:
Histórico relevante:
Documentos mencionados:
Sinal de urgência:
Objeções, receios ou dúvidas:
Interesse em avançar:
Observação importante:
Próximo passo recomendado:
```

O resumo deve registrar fatos, não interpretações exageradas.

Evite conclusões como:

- “tem direito”;
- “caso ganho”;
- “alta chance”;
- “fraude evidente”;
- “empresa culpada”;
- “benefício garantido”.

Quando o lead estiver apto a avançar, indique internamente:

```text
Próximo passo recomendado: /agendamento
```

---

# Exemplo demonstrativo

Crie uma conversa fictícia completa, adaptada ao nicho.

O exemplo deve conter:

1. saudação;
2. apresentação;
3. explicação da etapa;
4. perguntas em sequência;
5. respostas fictícias;
6. ao menos um esclarecimento natural;
7. agradecimento;
8. direcionamento.

Identifique:

> Cenário demonstrativo: conversa fictícia criada a partir dos critérios do Mapeamento de Persona.

Não apresente a simulação como caso real.

O exemplo não deve ser muito mais longo que o roteiro utilizável.

---

# Roteiro final limpo

Ao final, entregue uma versão pronta para copiar e utilizar.

Ela deve conter apenas:

1. saudação recomendada;
2. perguntas na ordem;
3. observações curtas para o atendente, somente quando indispensáveis;
4. mensagens de agradecimento e direcionamento.

Não inclua nessa versão:

- explicações teóricas;
- objetivos estratégicos;
- classificação MQL ou SQL;
- análise técnica;
- códigos;
- instruções de automação;
- tabelas complexas.

---

## Regras de escrita

O roteiro deve:

- soar humano;
- ser adequado ao WhatsApp ou ao canal informado;
- usar parágrafos curtos;
- fazer uma pergunta de cada vez;
- evitar excesso de formalidade;
- evitar excesso de intimidade;
- respeitar a persona;
- evitar mensagens longas;
- manter ritmo conversacional;
- usar linguagem compatível com o nível de compreensão do lead;
- explicar o motivo de perguntas sensíveis;
- demonstrar atenção sem teatralidade.

Evite:

- “Seu caso foi aprovado.”
- “Você está qualificado.”
- “Temos certeza de que você tem direito.”
- “Parabéns, seu caso se enquadra.”
- “Última oportunidade.”
- “Responda obrigatoriamente.”
- “Envie todos os seus documentos agora.”
- “Nossa taxa de sucesso é de 100%.”
- “Um especialista falará com você em breve”, quando isso não estiver confirmado.

---

## Validação interna obrigatória

Antes de concluir, verifique:

### Referências

- O Mapeamento de Persona foi consultado?
- Os critérios vêm do mapa ou de informações fornecidas?
- As referências obrigatórias foram lidas?
- Nenhum critério jurídico foi inventado?

### Saudação

- O escritório foi apresentado de forma verdadeira?
- A prova social é real ou está marcada como placeholder?
- A abertura explica a finalidade das perguntas?
- O tom combina com a persona?
- A abertura não parece propaganda exagerada?

### Perguntas

- As perguntas são específicas para o nicho?
- Cada pergunta possui função clara?
- Há apenas perguntas necessárias?
- A ordem é natural?
- A linguagem é simples?
- Temas sensíveis foram contextualizados?
- Não há repetição?
- A consulta não foi antecipada?
- A skill não solicitou documentação extensa?

### Direcionamento

- Existem encerramentos adequados aos resultados mais relevantes?
- O texto evita “desqualificado”?
- Não há conclusão definitiva sobre direitos?
- O próximo passo é real?
- Não há prazo ou promessa inventada?

### Escopo

- A saída é um roteiro humano?
- Não há adaptação para automação?
- Não há chatbot, CRM, código, gatilho ou máquina de estados?
- Não houve agendamento?
- Não houve consulta?
- Não houve follow-up?

### Entrega

- Há leitura estratégica?
- Há modelos de saudação?
- Há recomendação de abertura?
- Há perguntas com objetivo e sinais de atenção?
- Há mensagens de agradecimento e direcionamento?
- Há resumo de repasse?
- Há exemplo fictício?
- Há roteiro final limpo?

---

## Critérios de conclusão

A saída está completa somente quando:

- utiliza o Mapeamento de Persona;
- apresenta modelos de boas-vindas;
- recomenda uma abertura;
- transforma critérios estratégicos em perguntas humanas;
- explica a função prática das perguntas;
- trata respostas incompletas;
- apresenta agradecimento e direcionamento;
- diferencia avanço, revisão, urgência e não aderência;
- cria resumo para o próximo profissional;
- inclui exemplo fictício;
- entrega roteiro final limpo;
- não contém modelos ou adaptações para automação.

A skill deve ajudar o escritório a receber bem, perguntar com propósito e encaminhar com clareza.


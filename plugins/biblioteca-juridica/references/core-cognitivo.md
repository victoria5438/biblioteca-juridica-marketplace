# CORE COGNITIVO — BIBLIOTECA JURÍDICA

## Função

Este documento define como todas as skills do plugin raciocinam, selecionam contexto, preenchem lacunas, controlam a segurança das saídas e escolhem o tipo de produto a ser entregue.

Ele não determina a estrutura de uma peça específica. Cada `SKILL.md` continua responsável por:

- objetivo;
- entradas;
- etapas;
- formato de saída;
- limites próprios da tarefa.

O Core Cognitivo deve ser aplicado antes das regras específicas da skill.

---

# 1. HIERARQUIA DAS FONTES

Use as fontes nesta ordem:

1. instrução expressa do usuário no pedido atual;
2. particularidades expressas do escritório;
3. fatos confirmados do lead ou do caso;
4. Mapeamento de Persona Jurídica;
5. materiais e exemplos fornecidos para a skill;
6. conhecimento jurídico consolidado;
7. boas práticas de atendimento e operação jurídica;
8. presunções inteligentes e adaptáveis.

Uma fonte inferior não pode contradizer uma fonte superior.

Exemplo: se a prática comum for cobrar por êxito, mas o escritório informar honorários fixos, use honorários fixos.

---

# 2. DEFINIÇÃO DO TIPO DE PRODUTO

Antes de escrever, determine separadamente:

1. qual é o objetivo da comunicação;
2. qual é o produto solicitado;
3. qual é o canal utilizado.

O objetivo define o que a comunicação precisa alcançar.

O produto define a arquitetura da entrega.

O canal define como o conteúdo será distribuído e utilizado.

Não trate objetivo, produto e canal como se fossem a mesma coisa.

## 2.1. Playbook operacional reutilizável

Use quando o usuário pedir:

- playbook;
- manual de condução;
- fluxo interno;
- material para treinamento;
- padronização do escritório;
- orientação para equipe;
- roteiro operacional;
- documento que ensine o profissional a conduzir.

Esse produto deve explicar:

- o que fazer;
- por que fazer;
- o que perguntar;
- o que observar;
- como interpretar respostas;
- quais bifurcações existem;
- quais erros evitar;
- como avançar.

A saída pode conter objetivos, orientações, critérios, notas, exemplos de fala e checklists.

## 2.2. Roteiro falado fluido e reutilizável

Use quando o usuário pedir:

- roteiro integral de consulta;
- script falado;
- roteiro para ligação;
- roteiro para videoconferência;
- roteiro para reunião presencial;
- conversa pronta para o profissional conduzir;
- versão fluida de um atendimento ou fechamento.

Esse produto deve fornecer a condução praticamente pronta para ser falada.

A maior parte da entrega deve ser composta por:

- falas do profissional;
- perguntas;
- explicações;
- transições;
- pausas;
- bifurcações indispensáveis;
- respostas a objeções;
- fechamento e próximos passos.

Não transforme esse produto em manual operacional.

Não apresente repetidamente:

- objetivo;
- por que perguntar;
- o que observar;
- erros a evitar;
- critério para avançar.

Notas internas podem aparecer apenas quando forem indispensáveis para usar corretamente uma fala ou bifurcação.

O roteiro deve ser reutilizável para clientes diferentes do mesmo nicho. Não invente uma pessoa ou uma história específica como fio condutor.

## 2.3. Fluxo conversacional reutilizável de WhatsApp

Use quando o usuário pedir:

- roteiro de WhatsApp;
- fluxo de mensagens;
- sequência de atendimento pelo WhatsApp;
- script de qualificação por mensagem;
- conversa escrita de fechamento;
- follow-up;
- recuperação de silêncio;
- confirmação;
- convite;
- nutrição pelo WhatsApp.

Esse produto deve entregar mensagens prontas ou quase prontas para envio, organizadas conforme a progressão real da conversa.

A estrutura pode conter:

- mensagem inicial;
- pergunta;
- momento de aguardar resposta;
- continuação conforme a resposta;
- bifurcações;
- retomada de contexto;
- mensagens de áudio sugeridas;
- envio de documentos ou links;
- CTA da etapa;
- follow-up quando não houver resposta.

Não transforme o fluxo em:

- transcrição de uma ligação;
- manual cheio de explicações internas;
- texto corrido para ser enviado de uma vez;
- coleção de frases soltas sem progressão.

A profundidade deve aparecer no conjunto da conversa, distribuída em mensagens adequadas ao canal.

## 2.4. Simulação de caso ou role-play

Use somente quando o usuário pedir expressamente:

- conversa encenada;
- role-play;
- exemplo de atendimento com personagem;
- treinamento baseado em caso fictício;
- simulação de uma reunião específica;
- representação das respostas completas do cliente.

Nesse formato, podem existir personagens e respostas encenadas, desde que o usuário tenha pedido essa experiência.

## 2.5. Material para caso individual

Use quando o usuário fornecer fatos de uma pessoa real ou pedir preparação para um atendimento concreto.

Personalize somente com:

- fatos confirmados;
- documentos fornecidos;
- respostas da pessoa;
- particularidades expressamente informadas.

Não complete lacunas pessoais com características da persona.

## 2.6. Canal não define sozinho o objetivo

O WhatsApp pode ser utilizado para:

- qualificação;
- agendamento;
- consulta;
- apresentação de proposta;
- fechamento;
- envio de documentos;
- follow-up;
- nutrição.

Ligação, videoconferência ou reunião presencial também podem ter objetivos diferentes.

Não presuma que:

- todo WhatsApp deve ser superficial;
- toda ligação deve realizar consulta completa;
- todo roteiro falado deve fechar contrato;
- toda mensagem curta deve perder profundidade.

O objetivo da conversa continua controlando a profundidade e o próximo passo.

## 2.7. Regra de desempate

Quando uma skill específica for invocada, a missão declarada naquela skill define o produto.

Na ausência de skill específica:

- “playbook”, “manual”, “treinamento” ou “processo da equipe” indicam playbook operacional;
- “roteiro falado”, “ligação”, “videoconferência”, “reunião” ou “consulta integral” indicam roteiro falado fluido;
- “WhatsApp”, “mensagens”, “sequência de mensagens” ou “fluxo escrito” indicam fluxo conversacional de WhatsApp;
- “simule”, “encene” ou “faça um role-play” indicam simulação;
- fatos concretos de uma pessoa indicam material para caso individual.

Pergunte ao usuário somente quando os produtos possíveis forem incompatíveis e o pedido não permitir identificar qual deles foi solicitado.

---

# 3. REGRA DA HERANÇA

O Mapeamento de Persona Jurídica é o banco de contexto compartilhado do plugin.

Quando a informação já estiver nele, utilize-a automaticamente. Não peça ao usuário para preencher novamente:

- dores;
- desejos;
- crenças;
- medos;
- objeções;
- linguagem;
- nível de consciência;
- contexto jurídico;
- requisitos;
- prazos;
- documentos;
- riscos;
- ganhos;
- âncoras concretas;
- critérios preliminares;
- sinais de validação;
- transformação desejada.

A skill deve selecionar apenas as partes relevantes para sua tarefa.

Não copie o mapeamento inteiro para a saída. Converta o contexto em decisões de estratégia, linguagem, explicação e condução.

---

# 4. PERSONA NÃO É PERSONAGEM NEM FICHA INDIVIDUAL

O mapeamento descreve padrões prováveis. Ele não confirma fatos sobre uma pessoa específica e não deve virar automaticamente o personagem do material final.

A persona pode orientar:

- tom;
- ritmo;
- vocabulário;
- perguntas;
- acolhimento;
- objeções esperadas;
- nível de explicação;
- ordem dos assuntos;
- bifurcações relevantes;
- fatores de decisão.

Ela não autoriza inventar, como fio condutor:

- nome;
- idade;
- profissão;
- cidade;
- empresa;
- datas;
- composição familiar;
- histórico contributivo;
- motivo de desligamento;
- negativa;
- documentos;
- impacto emocional específico.

Use a hipótese para formular perguntas, caminhos e bifurcações. Não use a hipótese para criar uma biografia.

Em materiais reutilizáveis, prefira referências como:

- cliente;
- potencial cliente;
- segurada;
- gestante;
- mãe;
- trabalhador;
- contratante;
- pessoa atendida.

Detalhes específicos podem aparecer apenas:

1. quando forem fornecidos pelo usuário para um caso individual;
2. em exemplos breves claramente identificados;
3. em bifurcações condicionais, como “se a cliente informar que...”.

---

# 5. REUTILIZAÇÃO E GENERALIZAÇÃO OPERACIONAL

Um ativo operacional deve continuar útil quando mudarem:

- nomes;
- datas;
- profissões;
- cidades;
- composição familiar;
- detalhes da história;
- profissional que conduz o atendimento.

Ser reutilizável não significa ser genérico no conteúdo.

O material deve continuar:

- específico para o nicho;
- profundo nas explicações;
- claro sobre o que perguntar e observar;
- preparado para as principais variações do público;
- adaptável às particularidades do escritório.

Quando houver subperfis relevantes, construa:

1. um tronco comum de atendimento;
2. bifurcações por resposta, categoria ou situação;
3. critérios claros para escolher cada ramo.

Não eleja um subperfil como história principal, salvo se o usuário pedir esse recorte.

# 5-A. NEUTRALIDADE DE NICHO E NÃO CONTAMINAÇÃO

Os cores compartilhados são universais e devem funcionar para qualquer área ou nicho do Direito.

Exemplos presentes nos cores servem apenas para demonstrar um princípio de raciocínio ou escrita.

Eles não podem determinar automaticamente:

- o público;
- o problema jurídico;
- os documentos;
- as perguntas;
- os prazos;
- as objeções;
- as categorias de cliente;
- os caminhos administrativos ou judiciais;
- o modelo de contratação;
- o fechamento.

A cada execução, derive esses elementos exclusivamente do:

1. pedido atual;
2. nicho jurídico atual;
3. mapeamento de persona atual;
4. contexto do escritório;
5. conhecimento jurídico pertinente àquela área.

Não reutilize automaticamente categorias, termos, documentos ou estruturas jurídicas de uma execução anterior.

Salário-maternidade, INSS, relações trabalhistas, divórcio, fraude bancária ou qualquer outro tema utilizado em testes são apenas exemplos de aplicação.

Antes de finalizar, verifique se algum trecho da saída só faz sentido para outro nicho que não o solicitado. Se fizer, reescreva.

---

# 6. PRINCÍPIO DA PRESUNÇÃO INTELIGENTE

A IA deve realizar o trabalho intelectual e criativo da skill.

Não transforme a saída em formulário e não substitua blocos inteiros por `[PREENCHER]`.

## 6.1. Desenvolva automaticamente

Quando houver base suficiente no mapeamento, nos materiais ou no conhecimento consolidado, desenvolva:

- estratégia;
- perguntas;
- motivos das perguntas;
- critérios de observação;
- explicações jurídicas;
- traduções de termos;
- ganhos condicionados;
- objeções;
- respostas;
- documentos normalmente relevantes;
- fluxo operacional plausível;
- participação provável do cliente;
- próximos passos;
- mensagens;
- transições;
- CTAs.

## 6.2. Presuma de forma adaptável

Quando não houver particularidade do escritório, use uma prática plausível e registre-a brevemente como premissa adaptável.

Exemplos:

- envio de resumo e retorno para quem quer pensar;
- oferta de duas opções de horário;
- confirmação pelo canal de contato;
- contrato escrito;
- procuração quando necessária;
- envio e conferência de documentos;
- explicação transparente dos honorários;
- participação do cliente com documentos, informações e assinaturas.

A premissa deve produzir conteúdo pronto. Não deve esvaziar o roteiro.

## 6.3. Use placeholders apenas para dados exatos

Reserve placeholders principalmente para:

- nome;
- marca;
- OAB;
- endereço;
- data;
- horário;
- link;
- canal oficial;
- preço exato;
- percentual exato;
- duração exata;
- ferramenta específica.

Mesmo quando faltar um valor exato, escreva toda a orientação e a fala ao redor dele.

Exemplo adequado:

> O escritório recebe `[X%]` sobre o valor efetivamente recebido, conforme o contrato.

Exemplo inadequado:

> `[PREENCHER MODELO DE HONORÁRIOS]`

---

# 7. AUTONOMIA JURÍDICA CONTROLADA

A skill deve explicar o Direito quando essa explicação fizer parte da tarefa.

Não deixe a explicação jurídica inteira para o usuário preencher.

## 7.1. Pode desenvolver

- conceitos jurídicos consolidados;
- requisitos gerais;
- consequências práticas;
- documentos normalmente relevantes;
- possibilidades jurídicas;
- prazos consolidados;
- diferenças entre cenários;
- ganhos condicionados.

## 7.2. Deve condicionar

Use formulações como:

- “pelo que foi relatado...”;
- “isso pode indicar...”;
- “se os documentos confirmarem...”;
- “dependendo das datas...”;
- “essa possibilidade precisa ser analisada no caso concreto...”.

## 7.3. Marque apenas a dúvida específica

Quando um ponto for controvertido, recente ou altamente dependente do caso, use `[VALIDAR JURIDICAMENTE]` apenas naquele ponto.

Não esvazie o bloco inteiro porque uma frase exige validação.

## 7.4. Nunca invente

- promessa;
- garantia;
- percentual de chance;
- estatística;
- jurisprudência inexistente;
- caso de sucesso;
- prazo artificial;
- urgência criada;
- comparação não comprovada com outros casos;
- afirmação categórica sobre fatos ainda não analisados.

---

# 8. RÉGUA DE CERTEZA

Separe quatro níveis:

1. **Relato** — o que a pessoa disse.
2. **Indício** — o que o relato sugere.
3. **Confirmação** — o que depende de documentos ou análise.
4. **Resultado** — o que depende da atuação e da decisão competente.

O modelo não deve saltar do relato para o resultado.

Exemplo:

> O fato relatado é relevante e pode indicar um caminho jurídico. Antes de concluir, é necessário confirmar as datas, os documentos e os demais requisitos aplicáveis. Se esses elementos forem confirmados, será possível avaliar a medida adequada, sempre sujeita à análise técnica e à decisão competente.

---

# 9. TRADUÇÃO DO DIREITO

Toda skill de comunicação deve realizar duas traduções.

## 9.1. Tradução jurídica

Explique o termo técnico em linguagem cotidiana.

> Prescrição é o limite de tempo que pode restringir ou impedir a cobrança de determinado direito.

## 9.2. Tradução de valor

Explique o que aquilo muda na vida da pessoa.

> Na prática, isso significa que a data do fato precisa ser confirmada, porque o tempo decorrido pode alterar o que ainda é possível buscar.

---

# 10. OBJETIVO CONTROLA A ARQUITETURA

A skill deve adaptar perguntas, profundidade, explicação, objeções, CTA e próximo passo ao objetivo informado.

Exemplos:

- se o objetivo é agendar, não faça uma consulta completa antes do agendamento;
- se o objetivo é fechar, não pare numa qualificação superficial;
- se o objetivo é nutrir, não transforme cada mensagem em fechamento;
- se o objetivo é confirmar presença, não reabra toda a venda.

O objetivo controla o conteúdo e também o formato do produto.

---

# 11. PROFUNDIDADE SUBSTANTIVA E COMPLETUDE

Profundidade é uma propriedade do raciocínio e do conteúdo, não da encenação.

Em tarefas de consulta, explicação, diagnóstico, atendimento ou fechamento, não basta citar os tópicos que o profissional deverá abordar. A skill deve escrever conteúdo efetivamente utilizável.

Para cada assunto central, desenvolva, quando pertinente:

1. a consequência prática;
2. a lógica da regra;
3. a relação com os fatos que precisam ser investigados;
4. os elementos favoráveis;
5. as dúvidas ou limitações;
6. os fatos e documentos necessários para confirmação;
7. as alternativas disponíveis;
8. os riscos e expectativas;
9. os próximos passos;
10. o valor da atuação profissional.

Não substitua desenvolvimento por instruções vagas como:

- “explique o conceito”;
- “fale sobre os riscos”;
- “apresente os próximos passos”;
- “demonstre autoridade”;
- “trate a objeção”.

Escreva a explicação, a apresentação, a resposta e a condução.

## 11.1. Completude antes de concisão

Quando houver conflito entre uma resposta curta e uma resposta suficientemente desenvolvida, priorize a completude.

Depois organize o conteúdo para que permaneça:

- claro;
- utilizável;
- falável;
- sem repetição;
- sem prolixidade desnecessária.

Não use concisão como justificativa para omitir raciocínio, aplicação prática ou explicação relevante.

## 11.2. Profundidade proporcional ao objetivo

- Uma confirmação de presença deve ser breve.
- Uma triagem deve investigar apenas o necessário.
- Uma consulta deve explicar e contextualizar.
- Um fechamento deve reduzir incertezas suficientes para permitir uma decisão.
- Um parecer deve ter maior precisão técnica.
- Um roteiro de comunicação não precisa virar parecer, mas também não pode ser um resumo genérico.

---

# 12. QUALIFICAÇÃO E DESQUALIFICAÇÃO

Quando houver critérios no mapeamento ou nos dados do escritório, use-os.

Na ausência de critérios explícitos:

- faça uma leitura preliminar razoável;
- use linguagem aberta;
- não transforme dúvida em conclusão;
- prefira encaminhar para análise quando houver pertinência plausível;
- não invente um protocolo burocrático apenas para evitar decidir.

A frase “faz sentido aprofundar” não é promessa de direito.

---

# 13. GENERALIZAÇÕES

São permitidas para normalizar emoções e reduzir isolamento:

- “muita gente chega com essa dúvida”;
- “é comum pensar assim”;
- “muitas pessoas só descobrem isso depois”.

Não use generalizações para afirmar:

- frequência de êxito;
- taxa de reversão;
- aprovação;
- valor médio;
- facilidade do caso;
- superioridade do escritório.

---

# 14. PRESERVAÇÃO DO VALOR COMERCIAL

A cautela jurídica não pode apagar o benefício possível.

A saída deve explicar com clareza:

- o que pode ser buscado;
- por que isso importa;
- o que pode mudar;
- quais perdas podem ser evitadas;
- qual é o valor do trabalho profissional.

Sempre condicione quando necessário, mas não esconda a utilidade da solução.

---

# 15. PERGUNTAS AO USUÁRIO

Não faça uma bateria de perguntas antes de trabalhar.

Pergunte apenas quando a ausência impedir a escolha da arquitetura ou gerar resultados incompatíveis.

Dados operacionais não essenciais podem ser preenchidos por premissa adaptável.

---

# 16. REVISÃO INTERNA

Antes de entregar, verifique:

- o tipo de produto foi escolhido corretamente?
- a skill executou o trabalho ou devolveu um formulário?
- o mapeamento foi herdado?
- a persona orientou o material sem virar personagem?
- o resultado é reutilizável quando o pedido é genérico para um nicho?
- existe um tronco comum e bifurcações para as variações relevantes?
- o objetivo controlou a profundidade?
- os assuntos centrais foram realmente explicados?
- o profissional recebeu conteúdo pronto ou apenas temas para desenvolver?
- a saída ficou curta porque a tarefa era simples ou porque foi resumida demais?
- a aplicação prática, os documentos, os riscos e os próximos passos foram conectados?
- os ganhos foram claros e condicionados?
- as premissas adaptáveis foram úteis?
- placeholders ficaram restritos a dados exatos?
- existe promessa, estatística ou urgência inventada?
- o texto está específico para o nicho sem depender de uma história fictícia?
- objetivo, produto e canal foram definidos separadamente?
- a missão da skill específica foi respeitada?
- um roteiro falado fluido foi indevidamente transformado em manual?
- um fluxo de WhatsApp foi indevidamente transformado em ligação transcrita ou texto corrido?
- a arquitetura está adequada ao canal sem empobrecer o conteúdo?
- algum exemplo ou nicho anterior contaminou a saída atual?

Corrija silenciosamente.

---

# 17. TESTE DE REUTILIZAÇÃO

Este teste aplica-se a:

- playbooks;
- roteiros falados reutilizáveis;
- fluxos reutilizáveis de WhatsApp.

Antes de finalizar, pergunte:

- o material continua útil se o nome do cliente mudar?
- continua útil se mudarem datas, profissão, cidade e detalhes pessoais?
- preserva conteúdo específico para o nicho atual?
- as principais variações aparecem como bifurcações, sem criar uma biografia?
- outro profissional do mesmo nicho conseguiria utilizar o material?
- o formato continua sendo o produto solicitado?
- o roteiro falado permanece fluido?
- o WhatsApp permanece dividido em mensagens e momentos de resposta?
- algum elemento veio indevidamente de outro nicho?

Se a resposta for não, generalize os dados pessoais e preserve a especificidade jurídica do nicho.

---

# 18. CRITÉRIO DE CONCLUSÃO

A saída está pronta quando um profissional puder:

1. reconhecer seu nicho e o público atendido;
2. compreender o fluxo e as principais bifurcações;
3. utilizar a maior parte do conteúdo sem reescrevê-lo;
4. adaptar apenas particularidades do escritório e fatos do cliente real;
5. compreender quais premissas foram assumidas;
6. revisar tecnicamente os pontos jurídicos marcados;
7. reutilizar o material em atendimentos diferentes.

Não busque perfeição abstrata. Busque utilidade profissional, profundidade, replicabilidade e consistência.

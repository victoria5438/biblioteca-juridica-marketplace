---
name: playbook-atendimento-fechamento
description: Cria playbooks operacionais jurídicos reutilizáveis para consulta, atendimento e fechamento, partindo de lead já triado e qualificado. Use para padronizar a condução interna, treinar a equipe, documentar critérios, bifurcações, explicações, objeções, decisão e contratação.
argument-hint: [mapeamento de persona, recorte do serviço, informações herdadas da triagem e particularidades do escritório]
---

# Playbook de Atendimento e Fechamento Jurídico

## Objetivo

Produzir um playbook operacional interno, profundo e reutilizável para condução de consulta, atendimento e fechamento jurídico.

O material deve ensinar o profissional a operar cada etapa e, ao mesmo tempo, fornecer conteúdo suficientemente desenvolvido para uso real.

Não produza como saída principal:

- roteiro falado integral;
- fluxo de WhatsApp;
- conversa encenada;
- formulário;
- checklist superficial;
- lista de temas sem desenvolvimento;
- qualificação ou agendamento de consulta.

---

## Contexto obrigatório

Antes de produzir a saída:

1. leia `../../references/core-cognitivo.md`;
2. leia `../../references/core-escrita-oralidade.md`;
3. utilize o Mapeamento de Persona Jurídica fornecido pelo usuário ou disponível na conversa;
4. utilize as informações já existentes sobre o escritório, o serviço e a jornada;
5. priorize fatos confirmados e particularidades expressas sobre práticas genéricas.

Não execute novamente a skill de mapeamento de persona.

Não reproduza o mapeamento inteiro na saída.

Converta-o em decisões concretas de:

- recorte;
- prioridades;
- perguntas;
- profundidade;
- linguagem dos exemplos;
- bifurcações;
- objeções;
- fatores de decisão;
- explicação de valor;
- condução do fechamento.

---

## Natureza do produto

Esta skill produz um **playbook operacional reutilizável**.

O playbook é um ativo interno do escritório. Ele deve mostrar:

- o objetivo de cada etapa;
- o que o profissional recebe da etapa anterior;
- o que precisa confirmar ou compreender;
- por que determinada pergunta importa;
- o que observar nas respostas;
- como interpretar cenários diferentes;
- como explicar o assunto;
- quando aprofundar;
- quando mudar de ramo;
- como tratar objeções;
- como conduzir à decisão;
- como formalizar o próximo passo.

A saída pode conter:

- orientações;
- critérios;
- perguntas;
- motivos;
- explicações substantivas;
- exemplos de fala;
- bifurcações;
- erros a evitar;
- critérios de avanço;
- checklists internos.

Os exemplos de fala devem ser naturais e utilizáveis, mas não podem ocupar o lugar do manual operacional.

---

## Ponto de partida e limite

Esta skill parte da premissa de que o lead:

- já passou pela triagem;
- já foi classificado como qualificado para a consulta;
- possui contexto inicial suficiente para ser atendido;
- pode ter fatos, documentos ou requisitos que ainda precisam ser confirmados durante a consulta.

A consulta pode:

- aprofundar a linha do tempo;
- confirmar fatos;
- verificar documentos;
- identificar lacunas;
- validar a viabilidade jurídica;
- concluir que o caso pode ou não prosseguir;
- apresentar o serviço;
- conduzir à decisão de contratação.

Isso não constitui nova qualificação comercial.

Não utilize como etapas ou critérios:

- MQL;
- SQL;
- temperatura do lead;
- lead quente ou frio;
- intenção preliminar de contratar;
- caso de maior valor;
- lead que “vale seguir”;
- nova triagem disfarçada de consulta.

Quando o playbook for criado para uso genérico dentro de um nicho, indique quais informações mínimas devem chegar da triagem, sem reconstruir o processo de triagem.

A skill começa na preparação da consulta ou no recebimento do contexto qualificado.

A skill termina em uma destas situações:

- contratação e formalização imediata;
- hesitação com próximo passo concreto;
- recusa respeitosa;
- conclusão responsável de que não há elementos para apresentação da proposta;
- necessidade pontual de informação ou documento complementar.

Não inclui:

- captação;
- nutrição;
- triagem;
- qualificação comercial;
- convite para consulta;
- agendamento;
- confirmação de consulta;
- prevenção de ausência;
- recuperação de no-show;
- sequência prolongada de follow-up;
- acompanhamento jurídico depois do início da atuação;
- pós-venda.

---

## Informações de entrada

Utilize tudo o que já estiver disponível.

### Contexto estratégico

- nicho, serviço ou demanda jurídica;
- recorte de público;
- origem do lead, quando relevante;
- mapeamento de persona;
- nível de consciência;
- objeções;
- fatores de decisão;
- linguagem;
- subperfis e variações relevantes.

### Contexto da etapa

- informações que chegam da triagem;
- fatos já confirmados;
- documentos já recebidos ou analisados;
- pontos ainda pendentes;
- canal da consulta;
- quem conduzirá;
- objetivo final da conversa.

### Contexto do escritório

- posicionamento real;
- funcionamento do serviço;
- etapas reais da atuação;
- participação esperada do cliente;
- modelo de honorários;
- despesas e condições;
- fluxo de contratação;
- ferramentas;
- canais oficiais;
- política de comunicação;
- protocolo de segurança, quando houver;
- procedimento autorizado para quem quiser pensar.

Quando a saída for um playbook reutilizável e não houver um caso concreto, transforme os dados da triagem em uma **estrutura de passagem de contexto**, não em fatos inventados sobre um cliente.

Pergunte somente quando a ausência impedir a arquitetura ou exigir assumir uma condição comercial, financeira ou operacional que não pode ser presumida.

Não transforme a coleta de contexto em interrogatório.

---

## Hierarquia e não invenção

Respeite a hierarquia definida no Core Cognitivo.

Não invente:

- gratuidade de consulta ou análise;
- ausência de pagamento inicial;
- modelo por êxito;
- percentual;
- preço;
- parcelamento;
- ausência de custas ou despesas;
- prazo de retorno;
- canal de acompanhamento;
- disponibilidade do profissional;
- política de atendimento;
- protocolo de segurança;
- fluxo de assinatura;
- documento obrigatório;
- requisito jurídico;
- prazo legal;
- estatística;
- frequência de êxito;
- taxa de reversão;
- caso de sucesso;
- superioridade do escritório;
- promessa de resultado.

Use placeholders para dados exatos ausentes, como:

- `[ESCRITÓRIO]`;
- `[OAB]`;
- `[CANAL]`;
- `[HONORÁRIOS]`;
- `[PERCENTUAL]`;
- `[DESPESAS]`;
- `[FERRAMENTA]`;
- `[DOCUMENTO]`;
- `[DATA]`;
- `[HORÁRIO]`;
- `[LINK]`.

Escreva toda a orientação ao redor do placeholder.

Não use placeholders para substituir raciocínio, estratégia, explicação, perguntas ou condução.

---

## Recorte e especificidade

Antes de desenvolver o playbook, defina:

1. qual serviço ou demanda ele cobre;
2. para qual público;
3. de que ponto da jornada parte;
4. em qual decisão termina;
5. quais situações ficam fora do escopo;
6. quais subperfis exigem bifurcação própria.

Declare o recorte no início da saída.

Não diga que o playbook serve para todo o nicho quando ele tiver sido construído apenas para:

- determinados serviços;
- categorias específicas;
- fatos geradores delimitados;
- públicos específicos;
- determinada origem de lead;
- determinado canal;
- determinada etapa da jornada.

A arquitetura da skill é reutilizável entre nichos.

A saída deve ser profundamente específica para o nicho e o recorte atuais.

A personalização não está cumprida apenas porque a entrega menciona o nome do serviço.

O playbook deve refletir concretamente:

- situações vividas pelo público;
- dúvidas reais;
- linguagem;
- critérios relevantes;
- documentos;
- riscos;
- objeções;
- fatores de decisão;
- valor da consulta;
- valor do serviço;
- caminhos e limites próprios da demanda.

Aplique o teste:

> Este material poderia ser usado em outro nicho apenas trocando o nome do serviço e alguns termos?

Se a resposta for sim, aprofunde.

---

## Reutilização, tronco comum e bifurcações

O playbook deve funcionar com clientes diferentes dentro do recorte declarado.

Não escolha como fio condutor:

- nome;
- idade;
- profissão;
- cidade;
- composição familiar;
- estado emocional;
- rotina;
- dificuldade financeira;
- existência de cônjuge;
- documento;
- negativa;
- história individual.

Características predominantes da persona orientam a estratégia, mas não viram fatos do tronco comum.

Quando houver subperfis:

1. construa o tronco comum;
2. indique em qual ponto o cenário é identificado ou confirmado;
3. crie bifurcações apenas quando mudarem a investigação, a explicação, os documentos, o caminho, a objeção ou o próximo passo;
4. explique o critério para escolher cada ramo;
5. retorne ao fluxo comum quando possível.

Use referências específicas, como “gestante”, “segurada”, “empregado”, “aposentado”, “empresa” ou “familiar”, somente quando fizerem parte do recorte ou estiverem condicionadas.

---

## Profundidade obrigatória

O profissional não pode precisar inventar a parte principal do atendimento.

Não considere uma etapa concluída porque o texto apenas diz:

- “explique o direito”;
- “investigue os fatos”;
- “mostre o valor”;
- “trate a objeção”;
- “apresente os honorários”;
- “faça o fechamento”.

Desenvolva efetivamente:

- as perguntas;
- o motivo das perguntas;
- o que cada resposta pode alterar;
- os documentos e sua finalidade;
- a lógica jurídica em linguagem acessível;
- a relação entre fatos, regra e consequência;
- os cenários;
- os caminhos;
- os limites;
- o trabalho do escritório;
- a participação do cliente;
- as respostas às objeções;
- a condução até a decisão.

Não confunda profundidade com:

- repetição;
- excesso de títulos;
- história legislativa desnecessária;
- encenação de cliente;
- quantidade artificial de falas;
- linguagem de parecer;
- desenvolvimento de tópicos fora do recorte.

---

## Estrutura de cada etapa

Para cada etapa, inclua somente os componentes que agregarem valor.

### Objetivo

O que precisa ser alcançado naquele momento.

### Contexto recebido

Quais informações já chegaram da triagem ou da etapa anterior e não devem ser perguntadas novamente do zero.

### Orientação de condução

Como abordar o momento, qual postura adotar e como evitar ruptura de confiança.

### Perguntas sugeridas

Perguntas prontas, conectadas e adequadas ao nicho.

### Por que perguntar

A função jurídica, estratégica ou operacional da pergunta.

### O que observar

Sinais, lacunas, contradições, documentos, limites, objeções ou critérios.

### Explicação substantiva

O conteúdo que o profissional precisa dominar e pode utilizar para explicar o assunto.

### Exemplos de fala

Falas naturais, específicas para o nicho e adaptáveis a clientes diferentes.

### Bifurcações

O que muda conforme resposta, documento, cenário ou posição da pessoa.

### Erros a evitar

Condutas que geram confusão, repetição, promessa, pressão ou perda de confiança.

### Critério para avançar

O que precisa estar suficientemente esclarecido antes da próxima etapa.

Não repita mecanicamente todos os subtítulos em todas as etapas.

---

## Estrutura obrigatória do playbook

Adapte a profundidade e a ordem conforme o nicho, mas desenvolva os blocos pertinentes.

### 1. Preparação e passagem de contexto

- informações mínimas que devem chegar da triagem;
- fatos já confirmados;
- documentos disponíveis;
- pontos pendentes;
- riscos de fazer o cliente repetir tudo;
- preparação do profissional;
- campos que precisam ser adaptados pelo escritório.

A preparação não deve reconstruir a triagem.

### 2. Abertura e continuidade

- apresentação;
- reconhecimento do contato anterior;
- explicação breve de como a consulta funcionará;
- alinhamento do objetivo;
- segurança e permissão para avançar.

A abertura não deve prometer que haverá conclusão definitiva se ainda faltarem elementos.

Quando houver medo de fraude ou desconfiança no mapeamento, utilize apenas meios verificáveis realmente fornecidos, como:

- nome;
- OAB;
- canal oficial;
- site;
- perfil institucional;
- endereço;
- CNPJ;
- contrato.

Não apresente a própria ligação ou mensagem como prova suficiente de legitimidade.

### 3. Relato, confirmação e organização dos fatos

- retome o resumo já existente;
- permita correções;
- aprofunde somente o que falta;
- organize a linha do tempo;
- identifique fatos decisivos;
- diferencie fato confirmado de hipótese.

Não obrigue a pessoa a repetir integralmente o que já informou.

### 4. Validação da viabilidade jurídica e pontos pendentes

- indícios favoráveis;
- requisitos confirmados;
- requisitos pendentes;
- impedimentos aparentes;
- documentos necessários;
- contradições;
- necessidade de análise complementar;
- possibilidade de prosseguir ou não.

Este bloco não é qualificação comercial.

Não use linguagem de “lead aprovado”, “lead bom”, “caso de maior valor” ou equivalentes.

### 5. Síntese e prova de escuta

- devolva a situação organizada;
- confirme se a compreensão está correta;
- destaque o ponto central;
- separe relato, indício, confirmação e resultado.

### 6. Explicação jurídica acessível

Desenvolva:

1. consequência prática;
2. regra em linguagem simples;
3. fatores que alteram a análise;
4. relação com os fatos;
5. documentos;
6. caminhos;
7. limites;
8. próximo passo.

Não transforme a consulta em aula ou parecer.

### 7. Aplicação aos cenários do recorte

Para cada bifurcação relevante:

- diga o que muda;
- quais perguntas adicionais importam;
- quais documentos são relevantes;
- quais riscos aparecem;
- qual caminho pode ser considerado;
- quando retornar ao tronco comum.

### 8. Documentos e informações complementares

Ligue cada documento ao que ele precisa demonstrar.

Diferencie:

- documento disponível;
- documento ausente;
- documento útil;
- documento indispensável;
- documento complementar;
- documento cuja necessidade depende do cenário.

Não presuma lista universal.

### 9. Caminhos, limites e expectativas

Quando pertinente, desenvolva:

- alternativas administrativas, extrajudiciais ou judiciais;
- ordem possível das etapas;
- diferenças práticas;
- vantagens e limites;
- riscos;
- participação da autoridade responsável;
- incertezas que permanecem.

Não apresente medidas jurídicas como livre escolha do cliente quando a escolha depender de análise técnica.

### 10. Funcionamento e valor do serviço

Explique concretamente:

- o que o escritório fará;
- como organizará o caso;
- quais documentos analisará;
- quais etapas conduzirá;
- como reduzirá erros ou incertezas;
- como ocorrerá a comunicação;
- o que dependerá da pessoa;
- quais decisões ainda existirão;
- quais limites o serviço possui.

Demonstre valor pelo trabalho descrito.

Evite adjetivos vazios, como:

- excelente;
- completo;
- diferenciado;
- personalizado;
- especialista, quando não houver base ou posicionamento fornecido.

### 11. Participação real do cliente

Explique as ações que realmente podem depender da pessoa, como:

- documentos;
- informações;
- assinaturas;
- acessos;
- comparecimento;
- perícia;
- audiência;
- entrevista;
- resposta a exigência;
- atualização de dados.

Não prometa que “o cliente não precisará fazer nada” ou que “o escritório cuidará de tudo” se isso não for literalmente verdadeiro.

### 12. Honorários e condições

Apresente apenas o modelo informado.

Desenvolva, quando aplicável:

- forma de cobrança;
- valor ou percentual;
- base de cálculo;
- momento do pagamento;
- pagamento inicial;
- despesas separadas;
- parcelamento;
- efeito da ausência de resultado;
- registro no contrato.

Não derive gratuidade da cobrança por êxito.

Quando faltarem dados exatos, use placeholders e registre a pendência.

### 13. Dúvidas e objeções

Inclua apenas objeções pertinentes à consulta, ao serviço, aos honorários e à decisão.

Para cada objeção relevante, desenvolva:

1. como pode aparecer;
2. dúvida ou medo subjacente;
3. pergunta diagnóstica;
4. resposta substantiva;
5. exemplo de fala;
6. sinal de que foi esclarecida;
7. retomada do próximo passo.

Não trate como objeção:

- pergunta legítima ainda não respondida;
- dúvida decorrente de explicação superficial;
- solicitação de tempo que o procedimento do escritório permite;
- barreira criada por condição não informada.

Não invente vantagem sobre outro profissional nem prometa maior chance de resultado.

### 14. Proposta e decisão

Antes de pedir a decisão:

- sintetize;
- confirme que não há dúvida central pendente;
- apresente o serviço;
- alinhe limites;
- apresente honorários;
- explique o próximo passo.

Depois:

- faça uma pergunta clara;
- aguarde;
- não preencha o silêncio;
- não trate ausência de resposta como aceite.

### 15. Aceite, hesitação, recusa e ausência de proposta

#### Aceite

Conduza, conforme o fluxo real, para:

- dados;
- contrato;
- procuração;
- assinatura;
- pagamento, quando aplicável;
- documentos;
- confirmação do próximo passo.

Não elogie a decisão como vitória comercial.

Prefira confirmar e organizar a continuidade.

#### Hesitação

- identifique o motivo real;
- responda apenas ao ponto existente;
- utilize somente o passo autorizado pelo escritório;
- combine um próximo passo concreto quando isso fizer parte do procedimento.

Não crie sequência prolongada de follow-up.

#### Recusa

- confirme uma vez se existe dúvida não esclarecida;
- respeite a decisão;
- não use medo, culpa ou urgência;
- encerre com clareza.

#### Sem elementos para proposta responsável

- diga claramente o que ainda impede a conclusão;
- indique documento ou informação complementar, quando houver;
- ou conclua que o caso não deve prosseguir;
- não simule fechamento.

---

## Conclusão da análise e promessa de resultado

Quando os fatos e documentos permitirem conclusão profissional, o playbook pode orientar uma fala clara.

Exemplos de estrutura:

> Pelos documentos e pelas informações confirmadas, este requisito foi preenchido.

> A análise mostra que o caso se enquadra nessa regra e existe um caminho para seguir.

Depois, quando necessário, separe o limite:

> O resultado final depende da autoridade responsável e não pode ser garantido.

Não obrigue o profissional a falar de forma vaga quando a análise já estiver concluída.

Evite expressões artificiais de parecer, como:

- “juridicamente defensável”;
- “plausibilidade jurídica”;
- “tese sustentável”;
- “possibilidade abstrata de enquadramento”.

A conclusão da análise não autoriza prometer:

- deferimento;
- êxito;
- pagamento;
- valor;
- prazo;
- decisão favorável.

---

## Precisão jurídica proporcional

Esta skill produz um playbook de comunicação e operação, não um parecer.

- desenvolva conceitos consolidados relevantes;
- traduza a consequência prática;
- relacione regra, fatos e documentos;
- não invente tese, jurisprudência, prazo ou requisito;
- não use estatísticas ou frequência de êxito;
- não transforme ressalva em linguagem vazia;
- marque somente o ponto específico que exigir validação;
- use `[VALIDAR JURIDICAMENTE]` quando necessário;
- mantenha a dúvida técnica fora da fala categórica até que seja confirmada.

Não faça pesquisa extensa de legislação ou jurisprudência por padrão, salvo quando o usuário pedir ou quando a própria tarefa exigir validação atualizada.

---

## Formato da entrega

Entregue nesta ordem:

# 1. ESCOPO, PONTO DE PARTIDA E PREMISSAS

Bloco breve contendo:

- nicho;
- serviço;
- recorte;
- público;
- ponto de partida;
- ponto de encerramento;
- canal;
- condutor;
- informações herdadas da triagem;
- documentos já disponíveis, quando houver;
- honorários e condições informados;
- pendências que impedem uso imediato.

Não repita o Mapeamento de Persona.

# 2. VISÃO GERAL DA CONSULTA E DO FECHAMENTO

Mapa resumido das etapas, sem triagem ou agendamento.

# 3. PLAYBOOK OPERACIONAL PRINCIPAL

Desenvolva as etapas aplicáveis conforme a estrutura obrigatória.

Use os subtítulos internos apenas quando forem úteis.

# 4. BANCO DE OBJEÇÕES

Inclua somente as objeções relevantes para o recorte e a decisão de contratação.

# 5. FECHAMENTO E PRÓXIMOS PASSOS

Aceite, hesitação, recusa e ausência de proposta responsável.

# 6. PONTOS DE ADAPTAÇÃO

Lista curta com condições jurídicas, comerciais ou operacionais que precisam ser preenchidas ou confirmadas.

# 7. CHECKLIST INTERNO

Lista curta para consulta durante o atendimento.

---

## Critérios de aceite e revisão interna

Antes de finalizar, verifique silenciosamente:

### Produto e arquitetura

- a saída é um playbook operacional?
- o material ensina o profissional a conduzir?
- o conteúdo pronto está desenvolvido?
- a saída evitou virar roteiro falado integral?
- a saída evitou virar fluxo de WhatsApp?
- a skill partiu de lead já triado e qualificado?
- alguma etapa refez qualificação comercial?
- triagem ou agendamento entraram indevidamente?
- o playbook termina na decisão e formalização imediata?

### Recorte e reutilização

- o recorte foi declarado?
- o conteúdo cobre exatamente o recorte declarado?
- o material funciona com clientes diferentes dentro desse recorte?
- existe tronco comum?
- as bifurcações cobrem variações reais?
- alguma característica do subperfil dominante virou fato?
- algum exemplo de outro nicho contaminou a entrega?
- o material poderia ser usado em outro nicho apenas trocando nomes? Se sim, aprofunde.

### Profundidade e utilidade

- as explicações centrais estão efetivamente escritas?
- ficou claro por que as perguntas importam?
- as respostas possíveis foram ligadas a consequências?
- os documentos foram ligados ao que precisam demonstrar?
- os caminhos, riscos, limites e próximos passos foram desenvolvidos?
- o valor do serviço foi demonstrado concretamente?
- o profissional consegue utilizar o material sem improvisar a parte essencial?

### Segurança e não invenção

- foi presumida alguma gratuidade?
- foi inventada alguma condição comercial ou operacional?
- houve promessa de resultado?
- houve estatística, frequência de êxito ou superioridade não comprovada?
- foi criada urgência artificial?
- fatos, indícios, confirmações e resultado foram separados?
- a conclusão da análise está clara sem virar garantia?
- a cautela jurídica foi traduzida em linguagem natural?
- a participação do cliente foi descrita com realismo?
- o protocolo de segurança foi omitido quando não fornecido?

### Fechamento

- as objeções pertencem à decisão atual?
- a proposta aparece somente depois de compreensão suficiente?
- os honorários foram apresentados conforme dados reais?
- o aceite leva ao fluxo real de formalização?
- a hesitação utiliza somente o procedimento autorizado?
- a recusa é respeitada?
- a ausência de viabilidade não foi mascarada por fechamento artificial?

Corrija silenciosamente o que falhar.

---

## Critério de conclusão

O playbook está pronto quando um profissional consegue:

1. compreender o recorte e o ponto de partida;
2. receber o contexto da triagem sem refazê-la;
3. conduzir a consulta com profundidade;
4. validar a viabilidade jurídica sem linguagem de qualificação comercial;
5. explicar o Direito em linguagem acessível;
6. aplicar a explicação aos principais cenários;
7. apresentar concretamente o serviço;
8. tratar objeções pertinentes;
9. pedir uma decisão;
10. conduzir aceite, hesitação, recusa ou ausência de proposta;
11. reutilizar o material com clientes diferentes dentro do recorte;
12. adaptar apenas fatos do cliente e particularidades reais do escritório.

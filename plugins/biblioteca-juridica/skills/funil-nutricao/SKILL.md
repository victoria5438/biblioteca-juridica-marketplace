---
name: funil-nutricao
description: Cria funis jurídicos reutilizáveis de nutrição para leads frios ainda não qualificados, que não iniciaram o atendimento ou interromperam a interação antes da qualificação pelo SDR. Produz uma sequência progressiva de educação, identificação, confiança e ativação, encerrada assim que o lead responde e entra no processo de qualificação.
argument-hint: [mapeamento de persona, nicho ou direito, origem do lead, cenário de entrada, canal, cadência desejada, conteúdos e provas reais disponíveis e responsável pela qualificação]
---

# Funil de Nutrição Jurídica para Leads Frios

## Objetivo

Produzir um funil de nutrição jurídico reutilizável, específico para o nicho e destinado exclusivamente a **leads frios ainda não qualificados**.

O funil deve conduzir o lead de um estado como:

- não iniciou a conversa;
- abriu o canal, mas não respondeu;
- respondeu superficialmente e parou antes da qualificação;
- ainda não compreendeu por que o tema pode ser relevante;
- ainda não confia o suficiente para conversar com a equipe;

para uma ação observável:

- responder à mensagem;
- demonstrar interesse em entender;
- iniciar a conversa;
- retomar a interação interrompida;
- aceitar entrar na qualificação conduzida pelo SDR.

A função da sequência é:

- aumentar consciência;
- gerar identificação;
- explicar o tema em linguagem acessível;
- corrigir crenças iniciais;
- reduzir desconfiança;
- demonstrar relevância;
- facilitar a primeira resposta;
- reconduzir o lead ao SDR.

A função da sequência **não é qualificar o lead**.

Assim que o lead responder de forma que permita o início ou a retomada da conversa, a automação deve parar e o SDR deve assumir.

---

## Referências obrigatórias

Antes de produzir a saída:

1. leia `../../references/core-cognitivo.md`;
2. leia `../../references/core-escrita-oralidade.md`;
3. utilize o Mapeamento de Persona Jurídica fornecido pelo usuário ou disponível na conversa;
4. utilize o nicho, o direito ou o problema jurídico atual;
5. utilize a origem real do lead, quando informada;
6. identifique se o lead nunca interagiu ou se interrompeu antes da qualificação;
7. utilize somente conteúdos, provas e procedimentos efetivamente informados ou juridicamente sustentáveis.

Não execute novamente a skill de mapeamento de persona.

Não reproduza o mapeamento inteiro na saída.

Converta-o em decisões concretas de:

- ponto de entrada;
- estágio de consciência;
- arco da sequência;
- temas;
- ordem dos conteúdos;
- linguagem;
- ritmo;
- exemplos;
- mitos;
- objeções iniciais;
- formato;
- prova;
- CTAs;
- bifurcações;
- encerramento;
- passagem para o SDR.

---

## Natureza do produto

Esta skill produz um **funil de nutrição pré-qualificação**.

O produto principal é uma sequência planejada de contatos para leads frios, com mensagens prontas ou quase prontas para envio.

Pode conter:

- mensagens de WhatsApp;
- e-mails;
- textos de acompanhamento de conteúdo;
- áudios integralmente escritos, quando autorizados e úteis;
- roteiros curtos de vídeo;
- conteúdos educativos curtos;
- perguntas de ativação de baixa fricção;
- bifurcações mínimas;
- critérios de pausa;
- critérios de encerramento;
- handoff para o SDR.

Não produza como saída principal:

- campanha de anúncios;
- criativos de tráfego;
- calendário editorial;
- biblioteca de posts;
- formulário de triagem;
- questionário de qualificação;
- roteiro completo de SDR;
- classificação de lead;
- análise documental;
- consulta jurídica;
- parecer;
- agendamento;
- confirmação de consulta;
- recuperação de no-show;
- apresentação de proposta;
- fechamento;
- contratação;
- sequência pós-triagem;
- resgate de lead qualificado;
- follow-up de decisão;
- acompanhamento pós-contratação.

O funil aquece e ativa.

O SDR qualifica.

---

## Ponto de partida e limite

### A skill pode começar quando

O lead ainda não foi qualificado e:

- deixou seus dados após anúncio, formulário, landing page, conteúdo ou campanha;
- clicou para conversar, mas não enviou mensagem;
- recebeu uma primeira abordagem e não respondeu;
- iniciou uma conversa, mas parou antes de fornecer informações suficientes para a qualificação;
- respondeu apenas uma saudação ou manifestação genérica;
- demonstrou curiosidade, mas ainda não entrou na conversa com o SDR;
- integra uma base pré-qualificação cuja nutrição esteja autorizada pelo escritório.

### A skill termina quando

O lead:

- responde positivamente;
- faz uma pergunta;
- relata resumidamente sua situação;
- pede para entender melhor;
- aceita continuar;
- retoma a conversa;
- entra no atendimento ativo do SDR;
- pede para não receber novas mensagens;
- informa que o tema não se aplica;
- recusa continuar;
- permanece em silêncio até o encerramento previsto.

### A skill não se aplica quando

O lead:

- já concluiu a triagem;
- já foi qualificado;
- já foi desqualificado com fundamento suficiente;
- está aguardando agendamento;
- não avançou depois da qualificação;
- já possui consulta marcada;
- faltou à consulta;
- já recebeu devolutiva;
- está avaliando proposta;
- já contratou.

Esses cenários pertencem a outras skills.

Não amplie o escopo sob o argumento de “recuperação” ou “follow-up”.

Nesta skill, toda retomada ocorre **antes da qualificação**.

---

## Fronteira com a qualificação do SDR

A nutrição pode fazer perguntas simples destinadas a gerar resposta, como:

- “Esse tema tem relação com o que aconteceu com você?”
- “Você quer que a equipe explique quais informações precisam ser verificadas?”
- “Sua dúvida está mais ligada a [CENÁRIO A] ou [CENÁRIO B]?”
- “Quer continuar por aqui?”

Essas perguntas são **CTAs de ativação**, não uma triagem.

A nutrição não deve:

- coletar todos os requisitos;
- pedir uma sequência de datas;
- solicitar documentos;
- verificar elegibilidade;
- classificar o lead;
- concluir se o caso é qualificado;
- dizer que o lead tem ou não tem direito;
- conduzir a pessoa até o agendamento;
- substituir a conversa do SDR.

Quando o lead responder:

1. interrompa a sequência automática;
2. reconheça a resposta;
3. encaminhe o contexto ao SDR;
4. deixe a qualificação começar ou continuar no ponto adequado;
5. não envie os contatos seguintes como se nada tivesse acontecido.

---

## Entradas relevantes

Utilize tudo o que já estiver disponível.

### Contexto estratégico

- mapeamento de persona;
- nicho ou demanda jurídica;
- direito, proteção ou problema central;
- público e subperfis;
- estágio de consciência predominante;
- crença principal;
- mitos;
- dor consciente;
- impacto prático;
- desejo;
- objeções iniciais;
- linguagem;
- formalidade;
- formato preferencial;
- canais;
- conteúdos indispensáveis;
- arco emocional recomendado;
- urgência jurídica real;
- sinais de confiança relevantes.

### Contexto de aquisição

- origem do lead;
- campanha, anúncio, conteúdo ou formulário de entrada;
- promessa ou tema que motivou o clique;
- mensagem já recebida;
- informação que o lead já viu;
- canal autorizado;
- cenário de entrada;
- tempo de inatividade, quando relevante;
- cadência desejada, quando houver;
- limite de contatos;
- conteúdo existente que pode ser enviado.

### Cenário de entrada

Escolha um cenário principal:

#### Cenário A — nunca iniciou a conversa

O lead demonstrou interesse por clique, cadastro ou outra ação, mas ainda não conversou com o SDR.

#### Cenário B — recebeu abordagem e não respondeu

Existe contato autorizado, mas nenhuma resposta substantiva.

#### Cenário C — iniciou e parou antes da qualificação

O lead respondeu superficialmente, mas a qualificação ainda não começou ou não reuniu dados suficientes.

Não trate os três cenários como se fossem iguais.

### Contexto do escritório

- nome institucional;
- canal;
- responsável pela qualificação;
- forma real de passagem para o SDR;
- política de contatos;
- cadência;
- links;
- conteúdos existentes;
- provas reais autorizadas;
- identidade de comunicação;
- uso permitido de áudio ou vídeo.

Não solicite como entrada:

- honorários;
- condições comerciais;
- modelo de contratação;
- forma de pagamento;
- agenda;
- horários de consulta;
- contrato;
- documentos para contratação.

Essas informações não pertencem ao objetivo desta skill.

---

## Perguntas ao usuário

Não transforme a preparação em formulário.

Pergunte somente quando a ausência impedir:

- identificar o nicho;
- distinguir lead nunca ativado de lead que interrompeu antes da qualificação;
- reconhecer o canal;
- saber qual ação encerra o funil;
- saber quem assume depois da resposta;
- utilizar uma prova ou conteúdo que dependa de autorização.

Quando o mapeamento e o pedido já forem suficientes, execute diretamente.

A ausência de cadência não deve impedir o trabalho.

Nesse caso, use contatos numerados e placeholders de intervalo.

---

## Hierarquia e não invenção

Respeite a hierarquia do Core Cognitivo.

Não invente:

- depoimento;
- caso real;
- resultado;
- decisão judicial;
- tribunal;
- número de processo;
- estatística;
- quantidade de clientes;
- taxa de êxito;
- experiência específica do escritório;
- especialização;
- gratuidade;
- análise sem custo;
- honorários;
- pagamento por êxito;
- parcelamento;
- disponibilidade;
- agenda;
- prazo de atendimento;
- política de contato;
- encerramento automático;
- motivo do silêncio;
- documento já recebido;
- conclusão individual;
- autorização para contato;
- preferência por áudio;
- preferência por horário;
- compromisso de retorno;
- urgência comercial;
- prazo artificial.

Use placeholders somente para dados exatos, como:

- `[NOME]`;
- `[ESCRITÓRIO]`;
- `[SDR OU RESPONSÁVEL]`;
- `[CANAL]`;
- `[TEMA DE ENTRADA]`;
- `[LINK DO CONTEÚDO REAL]`;
- `[PROVA REAL AUTORIZADA]`;
- `[PRAZO JURÍDICO VALIDADO]`;
- `[INTERVALO DEFINIDO PELO ESCRITÓRIO]`;
- `[POLÍTICA DE ENCERRAMENTO]`.

Mesmo com placeholder, escreva a mensagem completa ao redor dele.

---

## Recorte e especificidade

Antes de escrever, identifique:

1. qual nicho está em foco;
2. qual problema ou direito motivou a aquisição;
3. qual público o funil cobre;
4. por qual canal o lead entrou;
5. o que ele já viu;
6. se nunca respondeu ou se interrompeu antes da qualificação;
7. qual estágio de consciência predomina;
8. qual crença impede a primeira conversa;
9. qual informação precisa ser compreendida;
10. qual ação simples levará ao SDR;
11. quais subperfis exigem bifurcação;
12. o que está expressamente fora da sequência.

A skill é reutilizável entre nichos.

A saída deve ser específica para:

- nicho;
- público;
- mecanismo jurídico;
- situação cotidiana;
- estágio;
- origem;
- cenário de entrada;
- canal;
- objetivo pré-qualificação.

Aplique o teste:

> Este funil poderia ser usado em outro nicho apenas trocando o nome do direito?

Se a resposta for sim, aprofunde:

- situação que desperta identificação;
- lógica jurídica;
- critério geral;
- consequência prática;
- mito;
- objeção;
- prova;
- vocabulário;
- CTA.

---

## Persona orienta; não vira lead individual

O mapeamento descreve padrões prováveis.

Ele pode orientar:

- linguagem;
- formalidade;
- tamanho;
- ritmo;
- escolha de temas;
- exemplos;
- objeções;
- CTAs;
- canal;
- formato;
- bifurcações.

Ele não autoriza afirmar que cada lead:

- tem determinada idade;
- mora em determinada cidade;
- possui cônjuge ou filhos;
- está sem renda;
- sente vergonha;
- prefere áudio;
- responde em determinado horário;
- tem dificuldade tecnológica;
- recebeu negativa;
- possui documentos;
- vive uma cena específica.

Use fatos individuais somente quando vierem:

1. da origem confirmada;
2. da interação real;
3. de dado fornecido;
4. de resposta da própria pessoa.

Padrões da persona devem aparecer como:

- generalizações responsáveis;
- hipóteses;
- perguntas;
- bifurcações.

Use `[NOME]`, nunca o nome fictício da persona.

### Exemplo adequado

> Muita gente pensa que parar de contribuir encerra toda proteção imediatamente. Nem sempre é assim, porque algumas datas ainda precisam ser verificadas.

### Exemplo inadequado

> Como você está desempregada e acabou de ter um bebê, provavelmente está preocupada com as contas.

---

## Estado inicial e estado final

### Estado inicial

Declare:

- origem;
- cenário de entrada;
- estágio de consciência;
- tema já visto;
- interação existente;
- principal barreira provável;
- ação ainda não realizada.

Não invente o motivo do silêncio.

Quando ele não for informado, registre:

> Motivo da ausência de resposta: não informado.

### Estado final

Defina uma ação observável e limitada à pré-qualificação, como:

- responder “quero entender”;
- iniciar a conversa;
- retomar a conversa;
- escolher um tema inicial;
- confirmar que deseja falar com a equipe;
- enviar uma primeira descrição curta;
- autorizar a continuidade pelo canal;
- entrar na qualificação com o SDR.

Não use como estado final:

- concluir triagem;
- ser qualificado;
- enviar todos os documentos;
- agendar;
- comparecer à consulta;
- receber proposta;
- contratar.

---

## Estágios de consciência aplicáveis

Use os estágios como ferramenta interna.

### Pouco consciente

A pessoa ainda não percebe que a situação pode ter dimensão jurídica.

Priorize:

- reconhecimento da situação;
- consequência prática;
- descoberta;
- linguagem cotidiana;
- pergunta simples.

### Consciente do problema

A pessoa sabe que algo está errado, mas não sabe que pode existir uma proteção ou caminho jurídico.

Priorize:

- explicação básica;
- diferença entre problema cotidiano e questão jurídica;
- critério geral;
- mito inicial;
- convite para entender.

### Consciente da solução

A pessoa sabe que pode existir uma saída jurídica, mas ainda não entende como verificar ou em quem confiar.

Priorize:

- método de análise;
- pontos que normalmente precisam ser verificados;
- limites;
- prova real ou informativa;
- papel da equipe;
- redução de desconfiança.

### Consideração inicial

A pessoa compara informações ou adia a primeira conversa, mas ainda não foi qualificada.

Priorize:

- objeção pré-qualificação;
- clareza sobre o que acontecerá ao responder;
- baixo esforço necessário;
- ausência de promessa;
- convite direto ao SDR.

Não apresente:

- proposta;
- honorários;
- contratação;
- agendamento;
- comparação comercial.

### Pronta para conversar

Pare de nutrir.

Faça o handoff imediato para o SDR.

---

## Tratamento dos cenários de entrada

### Cenário A — nunca iniciou a conversa

Não use:

- “vamos continuar”;
- “retomando nossa conversa”;
- “você parou de responder”;
- “vi que não concluiu”.

A abertura deve:

- conectar-se ao tema de entrada;
- explicar a relevância;
- oferecer uma primeira interação simples;
- permitir resposta sem exposição excessiva.

### Cenário B — recebeu abordagem e não respondeu

Não cobre retorno.

Não use:

- “viu minha mensagem?”;
- “aguardo sua resposta”;
- “ainda tem interesse?”;
- “por que não respondeu?”.

A nova mensagem deve acrescentar:

- informação;
- contexto;
- clareza;
- uma resposta mais fácil.

### Cenário C — iniciou e parou antes da qualificação

Retome somente o que estiver confirmado.

Não refaça a conversa inteira.

Não finja saber o motivo da interrupção.

Pode dizer:

> Você chegou a falar com a equipe sobre [TEMA CONFIRMADO], mas a conversa não avançou até a etapa em que conseguimos entender a situação.

Depois:

- entregue uma informação útil;
- simplifique a retomada;
- convide o lead a continuar;
- deixe a qualificação para o SDR.

Não retome uma pergunta técnica extensa dentro da nutrição.

---

## Arquitetura-base da sequência

Quando o usuário não definir quantidade, produza uma arquitetura-base de **7 contatos**.

Os sete contatos preservam o arco da referência original, mas não precisam ser enviados em sete dias consecutivos.

Use:

- `Contato 1` a `Contato 7`;
- `[INTERVALO DEFINIDO PELO ESCRITÓRIO]` quando a cadência não tiver sido informada.

Adapte ou reduza a quantidade somente quando:

- o usuário pedir;
- o canal exigir;
- o lead estiver mais consciente;
- já existir conteúdo recebido;
- uma sequência menor for claramente mais adequada.

Nunca prolongue a nutrição depois que o lead responder.

### Contato 1 — descoberta e relevância

Função:

- conectar o tema à situação cotidiana;
- mostrar que existe algo a compreender;
- gerar a primeira resposta.

### Contato 2 — identificação e impacto

Função:

- mostrar por que o tema importa;
- traduzir a dor ou consequência;
- reduzir sensação de isolamento;
- ampliar consciência.

### Contato 3 — conscientização e mecanismo

Função:

- explicar uma regra ou mecanismo central;
- corrigir interpretação simplista;
- mostrar o que precisa ser verificado;
- preservar o limite entre informação e análise individual.

### Contato 4 — confiança e prova

Função:

- demonstrar que o tema possui critérios verificáveis;
- usar prova real, institucional ou de método;
- reduzir medo de golpe, promessa ou improviso.

Se não houver case real autorizado, não crie narrativa de cliente.

### Contato 5 — quebra de objeção inicial

Função:

- trabalhar a principal barreira antes da conversa;
- explicar por que a objeção pode ser incompleta;
- convidar a pessoa a falar com o SDR.

### Contato 6 — reengajamento final

Função:

- sintetizar a utilidade;
- reduzir o esforço da resposta;
- oferecer uma escolha simples;
- avisar que a sequência está chegando ao fim, somente se isso corresponder à política real.

Não crie “última chance”, vaga, escassez ou prazo fictício.

### Contato 7 — encerramento respeitoso

Função:

- encerrar sem cobrança;
- permitir retorno futuro;
- respeitar silêncio;
- registrar o fim dos contatos conforme a política real.

Não use culpa, ameaça, perda inventada ou argumento comercial final.

---

## Arco cognitivo e emocional

Cada contato deve mudar alguma coisa.

### Arco cognitivo possível

1. “Esse tema existe.”
2. “Isso pode ter relação com situações como a minha.”
3. “Existe um critério que eu não conhecia.”
4. “Há uma forma séria de verificar.”
5. “Minha objeção inicial não encerra o assunto.”
6. “Responder é simples e não significa contratar.”
7. “Posso escolher conversar ou encerrar.”

### Arco emocional possível

1. distância;
2. identificação;
3. curiosidade;
4. segurança;
5. redução de resistência;
6. autonomia;
7. respeito.

Não repita o mesmo argumento com palavras diferentes.

Distribua funções distintas.

---

## Conteúdo de cada contato

Cada contato deve conter, quando pertinente:

1. ponte com a origem ou o contato anterior;
2. uma ideia principal;
3. desenvolvimento suficiente;
4. consequência prática;
5. CTA de ativação;
6. instrução interna de parada se houver resposta.

A mensagem pode ser curta.

Ela não pode ser vazia.

Evite:

- “você pode ter direito” sem explicar o motivo;
- “busque seus direitos”;
- “não deixe para depois”;
- “fale com especialista”;
- “estamos aqui para ajudar”;
- “seu caso parece bom”;
- frases de efeito sem conteúdo.

---

## CTAs de ativação

A CTA deve pedir apenas o necessário para iniciar ou retomar a conversa.

### Boas CTAs

- “Esse tema tem relação com o que aconteceu com você?”
- “Quer que a equipe explique o que precisa ser verificado?”
- “Você prefere entender primeiro [PONTO A] ou [PONTO B]?”
- “Se quiser continuar, responda ‘quero entender’.”
- “Quer retomar a conversa por aqui?”
- “Posso pedir para o SDR continuar com você?”

### CTAs inadequadas

- “Envie todos os seus documentos.”
- “Qual foi a data exata de cada contribuição?”
- “Escolha um horário.”
- “Confirme sua consulta.”
- “Você aceita a proposta?”
- “Posso enviar o contrato?”
- “Quanto pode investir?”
- “Quer contratar?”

Não use várias CTAs no mesmo contato.

Não use a mesma CTA em todos os contatos.

Toda resposta substantiva interrompe o funil e aciona o SDR.

---

## Conteúdo jurídico na nutrição

A sequência pode explicar:

- existência de uma proteção;
- requisito geral;
- mecanismo;
- diferença entre cenários;
- mito;
- prazo real;
- importância de uma data;
- motivo comum de dúvida;
- necessidade de verificar fatos;
- papel da qualificação inicial.

A sequência não deve:

- analisar o caso individual;
- concluir elegibilidade;
- prometer resultado;
- desqualificar;
- pedir prova documental completa;
- antecipar consulta;
- detalhar estratégia processual;
- conduzir o diagnóstico integral.

Use formulações como:

- “A lei prevê essa proteção quando...”
- “O ponto que costuma precisar de verificação é...”
- “Isso não depende apenas de [CRENÇA COMUM].”
- “Datas e documentos podem mudar o enquadramento.”
- “A equipe precisa entender alguns fatos antes de dizer se existe pertinência.”
- “Responder à mensagem inicia essa verificação; não significa que o direito já esteja confirmado.”

Evite cautela vazia.

Explique a regra sem transformar o conteúdo em parecer.

---

## Tradução jurídica e tradução de valor

Sempre realize duas traduções.

### Tradução jurídica

Explique o conceito em linguagem cotidiana.

> Período de graça é o tempo em que a pessoa pode continuar protegida pelo INSS mesmo depois de parar de contribuir.

### Tradução de valor

Explique o que isso pode mudar na situação prática.

> Na prática, isso pode fazer diferença para quem não estava trabalhando na data do nascimento, mas ainda permanecia protegida.

Não afirme que o cenário se aplica ao lead sem confirmação.

---

## Prova e confiança

### Case real autorizado

Use somente quando tiver sido fornecido e autorizado.

Apresente:

- contexto suficiente;
- obstáculo;
- ponto jurídico relevante;
- resultado factual;
- limite de comparação.

Não use a narrativa para prometer repetição do resultado.

### Prova institucional ou pública

Pode utilizar, quando tecnicamente validado:

- regra legal;
- decisão real;
- orientação pública;
- documento oficial;
- dado institucional;
- mudança normativa relevante.

Marque `[VALIDAR JURIDICAMENTE]` quando necessário.

### Prova de método

Quando não houver case real:

- mostre quais fatos costumam ser verificados;
- explique por que uma data importa;
- mostre como cenários diferentes recebem análises diferentes;
- explique que o SDR reúne informações antes da avaliação jurídica;
- demonstre seriedade pelo processo, não por autoelogio.

Não invente:

- cliente;
- história;
- tribunal;
- volume de casos;
- taxa de sucesso;
- especialização;
- resultado.

---

## Objeções iniciais

Trabalhe apenas objeções que impedem a primeira conversa.

Exemplos:

- “acho que isso não é para mim”;
- “já me disseram que não tenho direito”;
- “não quero cair em golpe”;
- “não entendo esse assunto”;
- “não tenho todos os documentos”;
- “não quero perder tempo”;
- “parece muito complicado”;
- “vou ver isso depois”.

Não trabalhe nesta skill:

- preço;
- honorários;
- percentual;
- parcelamento;
- contrato;
- comparação de proposta;
- decisão de contratação;
- objeções posteriores à consulta.

Se uma objeção comercial surgir durante a nutrição, interrompa a automação e encaminhe para atendimento humano, sem improvisar fechamento.

---

## Urgência e perda

Use urgência somente quando houver fundamento jurídico real.

Pode decorrer de:

- prescrição;
- decadência;
- prazo recursal;
- prazo administrativo;
- leilão;
- audiência;
- risco concreto de perda.

A mensagem deve explicar:

1. qual é o marco;
2. por que ele importa;
3. o que pode ser perdido;
4. o que ainda precisa ser validado;
5. por que vale iniciar a conversa.

Não use urgência em todos os contatos.

Não invente:

- prazo para responder à equipe;
- encerramento “amanhã”;
- disponibilidade limitada;
- última vaga;
- condição temporária;
- escassez.

Quando não houver urgência jurídica real, use:

- relevância;
- clareza;
- identificação;
- confiança;
- simplicidade da resposta.

---

## Formato por canal

### WhatsApp

Use:

- parágrafos curtos;
- uma ideia principal por bloco;
- leitura confortável em tela pequena;
- CTA simples;
- linguagem profissional;
- poucos emojis e apenas quando funcionais.

Não transforme cada contato em miniartigo.

Não fragmente artificialmente em muitas mensagens de uma linha.

### E-mail

Inclua:

- assunto;
- abertura;
- conteúdo;
- CTA;
- assinatura ou identificação.

Adapte o desenvolvimento.

Não copie mecanicamente a versão de WhatsApp.

### Áudio

Use somente quando:

- o canal permitir;
- houver ganho real;
- a política do escritório permitir;
- a pessoa tiver escolhido o formato ou houver autorização expressa.

Escreva o áudio integral.

Não escreva apenas “envie um áudio explicando”.

### Vídeo ou conteúdo externo

Quando recomendar conteúdo novo:

- escreva o roteiro completo ou briefing desenvolvido;
- indique a função dentro do arco;
- mantenha o limite pré-qualificação.

Quando utilizar conteúdo existente:

- use `[LINK DO CONTEÚDO REAL]`;
- escreva a mensagem de apresentação;
- explique por que vale acessar;
- inclua CTA posterior de ativação.

---

## Silêncio, resposta e interrupção

Silêncio não significa:

- consentimento;
- interesse;
- objeção;
- recusa;
- disponibilidade;
- preferência de canal;
- autorização para áudio;
- autorização para qualificação;
- autorização para agendamento.

A sequência pode continuar apenas de acordo com:

- canal autorizado;
- cadência real;
- política de contato;
- limite de contatos.

Quando o lead responder:

1. pare a automação;
2. reconheça a resposta;
3. não envie o contato seguinte;
4. passe o histórico ao SDR;
5. permita que o SDR faça a qualificação.

Quando o lead pedir para não receber mensagens:

- interrompa imediatamente;
- confirme o encerramento de forma breve;
- não envie último argumento;
- respeite a política aplicável.

---

## Bifurcações essenciais

Inclua somente ramos que mudem o comportamento da sequência.

### Se responder com interesse

> Entendi, [NOME]. Vou encaminhar sua resposta para [SDR OU RESPONSÁVEL], que vai continuar por aqui e entender os pontos necessários com você.

*Pare o funil e faça o handoff.*

### Se fizer pergunta geral

Responda de modo educativo e breve.

Depois:

> Para verificar como isso se relaciona à sua situação, [SDR OU RESPONSÁVEL] precisa entender alguns fatos com você. Vou pedir que continue por aqui.

*Pare o funil.*

### Se relatar a situação

Não faça análise dentro da automação.

> Obrigado por explicar. Esse contexto já ajuda a equipe a começar do ponto certo. Vou encaminhar sua mensagem para [SDR OU RESPONSÁVEL] continuar com você.

*Pare o funil.*

### Se disser “não sei”

Reduza a fricção.

> Tudo bem. Você não precisa saber enquadrar a situação agora. A equipe começa com algumas perguntas simples para entender se o tema tem relação com o que aconteceu. Quer continuar?

Se responder, pare e faça o handoff.

### Se disser que não tem documentos

Não encerre automaticamente.

> Não ter todos os documentos agora não significa, por si só, que não vale conversar. Primeiro a equipe entende o que aconteceu; depois explica o que realmente precisaria ser localizado.

> Quer iniciar essa conversa?

Se responder, pare e faça o handoff.

### Se disser que não se aplica

Agradeça e encerre.

Não tente converter por insistência.

### Se recusar ou pedir opt-out

Encerre imediatamente.

### Se fizer pergunta comercial

Não apresente condições.

> Essa parte depende das informações e do procedimento real do escritório. Vou encaminhar sua pergunta para a equipe responder corretamente.

*Pare o funil.*

### Se pedir agendamento

Não agende dentro da nutrição.

> Vou encaminhar sua mensagem para a equipe. Antes do agendamento, o SDR precisa entender os pontos iniciais e orientar a próxima etapa.

*Pare o funil.*

---

## Handoff para o SDR

O handoff deve ocorrer na primeira resposta que demonstre abertura para conversar.

Transmita ao SDR:

- nome ou identificador;
- origem do lead;
- campanha ou conteúdo de entrada;
- cenário de entrada;
- mensagens já recebidas;
- conteúdos enviados;
- resposta atual;
- dúvida apresentada;
- objeção mencionada;
- estágio de consciência aparente;
- consentimentos ou recusas expressos;
- ponto exato em que a automação parou.

Não transmita como fato:

- emoção presumida;
- renda presumida;
- composição familiar presumida;
- motivo presumido do silêncio;
- elegibilidade;
- conclusão jurídica;
- classificação inventada.

O SDR não deve repetir automaticamente:

- conteúdos que o lead já recebeu;
- perguntas já respondidas;
- explicações que motivaram a resposta.

---

## Formato da entrega

Entregue nesta ordem:

# 1. ESCOPO E PONTO DE PARTIDA

Bloco curto contendo:

- nicho;
- direito ou problema;
- público;
- canal;
- origem;
- cenário de entrada;
- estágio de consciência;
- estado inicial;
- barreira principal;
- estado final;
- responsável pelo handoff;
- quantidade de contatos;
- cadência informada ou placeholder;
- conteúdos e provas disponíveis;
- itens fora do escopo.

Não inclua condições comerciais.

# 2. MAPA ESTRATÉGICO

Apresente:

- crença principal;
- dúvida inicial;
- objeção pré-qualificação dominante;
- impacto prático;
- ganho informativo;
- urgência jurídica real, se houver;
- prova disponível;
- conteúdos indispensáveis;
- arco cognitivo;
- arco emocional;
- progressão das CTAs;
- critério de interrupção;
- critério de encerramento.

# 3. ARQUITETURA DA SEQUÊNCIA

Use tabela:

| Contato | Momento | Função | Mudança esperada | Conteúdo principal | CTA de ativação | Ação se responder |
|---|---|---|---|---|---|---|

Se houver datas ou intervalos fornecidos, inclua-os.

Se não houver, use `[INTERVALO DEFINIDO PELO ESCRITÓRIO]`.

# 4. MENSAGENS PRONTAS

Para cada contato:

## CONTATO [NÚMERO] — [FUNÇÃO INTERNA]

**Quando usar:** [condição interna curta]

**Mensagem pronta:**

> [mensagem]

*Se houver resposta, pare a sequência e faça o handoff para o SDR.*

Quando houver áudio, vídeo ou conteúdo, desenvolva integralmente o material necessário.

Não entregue duas versões de cada mensagem sem necessidade.

# 5. BIFURCAÇÕES DE RESPOSTA

Inclua somente:

- interesse;
- dúvida geral;
- relato inicial;
- “não sei”;
- falta de documentos;
- objeção inicial;
- pergunta comercial;
- pedido de agendamento;
- recusa;
- opt-out.

# 6. HANDOFF PARA O SDR

Explique:

- qual resposta encerra a nutrição;
- quem assume;
- quais informações acompanham;
- o que não deve ser repetido;
- o que não pode ser concluído antes da qualificação.

# 7. PONTOS DE ADAPTAÇÃO

Lista curta contendo apenas:

- nome institucional;
- responsável;
- canal;
- origem;
- link;
- conteúdo real;
- prova real;
- cadência;
- política de contato;
- prazo jurídico validado;
- validações técnicas específicas.

---

## Revisão interna obrigatória

Antes de entregar, verifique silenciosamente:

### Produto e jornada

- a saída é um funil para lead frio?
- o lead ainda não foi qualificado?
- a origem está clara?
- o cenário de entrada está claro?
- o objetivo é obter resposta e iniciar ou retomar a qualificação?
- a skill executou triagem?
- coletou requisitos em sequência?
- classificou o lead?
- pediu documentos?
- agendou?
- apresentou proposta?
- abordou honorários?
- tratou lead pós-triagem?
- tentou recuperar lead já qualificado?
- invadiu uma skill futura?

### Arco e progressão

- os contatos formam uma sequência?
- cada contato tem função diferente?
- o conteúdo avança?
- existe repetição?
- as CTAs evoluem?
- a arquitetura-base foi adaptada quando necessário?
- a sequência para na primeira resposta?
- o último contato encerra respeitosamente?

### Cenário de entrada

- a mensagem para quem nunca conversou finge continuidade?
- a mensagem para quem não respondeu cobra retorno?
- a mensagem para quem parou inventa o motivo?
- informações anteriores foram respeitadas?
- o lead é convidado a conversar sem exposição excessiva?

### Persona e factualidade

- a persona orientou sem virar lead individual?
- idade, família, renda, rotina, documento, negativa ou emoção foram presumidos?
- o motivo do silêncio foi inventado?
- o nome fictício da persona apareceu?
- o subperfil dominante contaminou todo o tronco?
- as bifurcações estão condicionadas?

### Conteúdo e especificidade

- o funil pertence ao nicho?
- poderia ser usado em outro nicho apenas trocando nomes?
- o mecanismo foi explicado?
- a consequência prática foi traduzida?
- o material contém mensagens prontas?
- os conteúdos recomendados foram escritos?
- o lead recebeu informação suficiente para entender por que vale responder?

### Segurança

- houve promessa?
- houve direito individual afirmado?
- houve desqualificação automática?
- houve case, estatística ou jurisprudência inventada?
- houve urgência artificial?
- houve prazo comercial inventado?
- houve condição comercial?
- houve procedimento institucional inventado?
- houve preferência de formato presumida?
- algum ponto controvertido exige `[VALIDAR JURIDICAMENTE]`?

### Canal e comportamento

- as mensagens são adequadas ao canal?
- o silêncio foi tratado como informação?
- a automação continuaria depois de resposta?
- a recusa foi respeitada?
- o opt-out encerra imediatamente?
- os intervalos seguem informação real ou placeholder?
- o último contato evita culpa, ameaça e pressão?
- o handoff oferece contexto suficiente ao SDR?

Corrija silenciosamente o que falhar.

---

## Critério de conclusão

O funil está pronto quando:

1. parte de lead frio ainda não qualificado;
2. distingue ausência de interação de interrupção pré-qualificação;
3. transforma o mapeamento em conteúdo específico;
4. constrói um arco progressivo;
5. educa sem executar triagem;
6. gera identificação sem transformar a persona em indivíduo;
7. explica Direito e consequência prática;
8. usa prova real, pública ou de método sem invenção;
9. trabalha apenas objeções anteriores à qualificação;
10. não aborda honorários ou condições comerciais;
11. usa CTAs de ativação proporcionais;
12. para na primeira resposta substantiva;
13. entrega o lead ao SDR com contexto;
14. respeita silêncio, recusa e opt-out;
15. permanece reutilizável dentro do recorte;
16. exige adaptação apenas de fatos, links, políticas e conteúdos reais.

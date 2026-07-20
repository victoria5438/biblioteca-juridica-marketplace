---
name: roteiro-whatsapp
description: Cria fluxos jurídicos assíncronos de consulta, devolutiva e fechamento pelo WhatsApp, partindo de lead já triado, qualificado e com análise documental inicial realizada. Use para apresentar a conclusão da análise, esclarecer pontos, explicar caminhos, apresentar o serviço e os honorários, tratar objeções, conduzir à decisão, formalizar a contratação e recuperar silêncios ocorridos nessa etapa.
argument-hint: [mapeamento de persona, recorte do serviço, resumo da triagem, documentos analisados, conclusão inicial e particularidades do escritório]
---

# Roteiro de Consulta e Fechamento pelo WhatsApp

## Objetivo

Produzir um fluxo conversacional jurídico assíncrono, profundo e reutilizável para consulta, devolutiva e fechamento pelo WhatsApp.

A maior parte da entrega deve ser composta por mensagens e áudios prontos ou quase prontos para envio.

O resultado deve acompanhar a progressão real da conversa:

- mensagem;
- espera;
- resposta;
- continuidade;
- bifurcação;
- explicação;
- chamada para ação;
- decisão;
- formalização;
- follow-up da própria consulta ou do fechamento.

Não produza como saída principal:

- playbook;
- manual operacional;
- apostila;
- checklist;
- transcrição de ligação;
- texto corrido para envio único;
- coleção de frases desconectadas;
- conversa fictícia completa;
- respostas inventadas do cliente;
- funil comercial completo;
- triagem;
- qualificação;
- agendamento.

---

## Contexto obrigatório

Antes de produzir a saída:

1. leia `../../references/core-cognitivo.md`;
2. leia `../../references/core-escrita-oralidade.md`;
3. utilize o Mapeamento de Persona Jurídica fornecido pelo usuário ou disponível na conversa;
4. utilize o resumo da triagem;
5. utilize os fatos confirmados;
6. utilize os documentos já analisados;
7. utilize a conclusão inicial do advogado;
8. utilize as particularidades reais do escritório;
9. priorize fatos confirmados e instruções expressas sobre padrões prováveis.

Não execute novamente a skill de mapeamento de persona.

Não reproduza o mapeamento na saída.

Converta-o em decisões concretas de:

- recorte;
- linguagem;
- tamanho das mensagens;
- ritmo;
- formalidade;
- escolha entre texto e áudio;
- ordem das explicações;
- bifurcações;
- objeções;
- fatores de decisão;
- tratamento do silêncio;
- chamadas para ação;
- fechamento.

---

## Ponto de partida e limite

Esta skill parte da premissa de que o lead:

- já passou pela triagem;
- já foi classificado como qualificado;
- já enviou os documentos iniciais;
- já teve esses documentos analisados;
- possui um resumo do caso disponível para o advogado;
- possui uma conclusão inicial que permite a devolutiva.

A skill começa:

- na passagem de contexto ao advogado; ou
- na primeira mensagem do advogado para iniciar a consulta assíncrona.

A skill termina em uma destas situações:

- contratação e formalização;
- hesitação com próximo passo concreto;
- recusa respeitosa;
- conclusão responsável de que o caso não deve prosseguir;
- necessidade pontual de documento ou informação complementar;
- encerramento da consulta sem contratação, quando esse for o objetivo definido.

Não inclui:

- captação;
- resposta a anúncio;
- acolhimento inicial de SDR;
- triagem;
- qualificação;
- desqualificação comercial;
- convite para consulta;
- agendamento;
- confirmação de consulta;
- prevenção de ausência;
- recuperação de no-show;
- reativação genérica;
- acompanhamento jurídico posterior ao início da atuação;
- pós-venda.

A skill não deve refazer a etapa anterior sob outro nome.

Não pergunte novamente:

- informações já confirmadas;
- documentos já analisados;
- critérios já verificados;
- interesse preliminar em resolver;
- “temperatura”;
- intenção de contratar antes da devolutiva.

---

## Natureza do produto

Esta skill produz uma **consulta e um fechamento assíncronos pelo WhatsApp**.

O fluxo deve indicar claramente:

- o que enviar;
- quando aguardar;
- como continuar;
- quando usar texto;
- quando usar áudio;
- como reagir;
- quando criar bifurcação;
- qual é o próximo passo;
- quando retomar;
- quando encerrar.

A maior parte da entrega deve ser formada por:

- mensagens prontas;
- áudios integralmente escritos;
- pausas;
- confirmações;
- perguntas complementares;
- continuidades;
- bifurcações;
- objeções;
- chamadas para ação;
- formalização.

Use notas internas somente quando forem indispensáveis, por exemplo:

- *Aguarde a resposta.*
- *Use este trecho somente se o fato estiver confirmado.*
- *Envie em áudio somente se o canal e a pessoa permitirem.*
- *Não avance sem esclarecer este ponto.*
- *Retome depois do prazo definido pelo escritório.*

Não exiba repetidamente:

- objetivo;
- por que perguntar;
- o que observar;
- erro a evitar;
- critério para avançar;
- estratégia comercial;
- comentário de bastidor.

Essas decisões devem orientar silenciosamente a escrita.

---

## Natureza assíncrona

O fluxo padrão ocorre de forma assíncrona.

Não presuma:

- horário reservado;
- presença simultânea;
- resposta imediata;
- consulta em tempo real;
- ligação;
- videochamada;
- disponibilidade contínua do advogado.

### Regra absoluta sobre silêncio

Silêncio não fornece informação.

A ausência de resposta nunca significa:

- autorização para continuar;
- preferência por áudio;
- preferência por texto;
- disponibilidade para ler;
- concordância;
- compreensão;
- aceite;
- recusa;
- autorização para enviar contrato;
- autorização para solicitar novos documentos.

Quando uma mensagem fizer uma pergunta ou oferecer escolha:

1. aguarde a resposta;
2. continue apenas com base no que a pessoa efetivamente disser;
3. ou use o follow-up correspondente depois do prazo definido pelo escritório.

Não escreva instruções como:

- “se não responder, envie o áudio”;
- “se ficar em silêncio, continue”;
- “a resposta curta confirma que está livre”;
- “na ausência de escolha, presuma o formato”.

Uma resposta como “pode” autoriza apenas a continuação geral. Ela não confirma disponibilidade imediata, preferência de formato ou concordância com etapas posteriores.

O texto pode ser usado como formato padrão apenas quando essa regra tiver sido expressamente definida pelo escritório.

Não envie áudio por falta de resposta.

Use mensagens que respeitem o canal, como:

> Quando puder, me confirme se recebeu.

> Pode ouvir com calma e me responder por aqui.

> Assim que você me responder esse ponto, eu continuo.

> Vou deixar a explicação organizada abaixo para você consultar com calma.

Não use frases que façam parecer que existe uma reunião marcada quando a conversa é assíncrona.

Só inclua ligação, videochamada ou conversa simultânea quando o usuário pedir expressamente essa bifurcação.

Nesse caso, trate-a como alternativa específica, sem transformar o fluxo principal em agendamento.

---

## Responsável pela conversa

A devolutiva, a explicação jurídica e a conclusão da análise devem ser conduzidas por advogado ou profissional juridicamente habilitado.

O advogado pode:

- retomar o contexto;
- apresentar a conclusão inicial;
- esclarecer fatos complementares;
- explicar conceitos;
- aplicar a regra aos elementos analisados;
- alinhar caminhos;
- expor limites;
- apresentar o serviço;
- explicar honorários;
- tratar objeções;
- conduzir à contratação.

Não pode:

- garantir resultado;
- inventar conclusão;
- ultrapassar os documentos e fatos;
- tratar possibilidade como decisão já obtida;
- atribuir ao órgão ou ao Judiciário um resultado futuro.

A equipe de atendimento pode participar somente de continuidades operacionais expressamente informadas, como:

- enviar link;
- confirmar recebimento;
- encaminhar contrato;
- solicitar assinatura;
- confirmar documento complementar;
- informar canal;
- registrar retorno combinado.

Não crie novamente uma fase de SDR dentro desta skill.

Não atribua conclusão jurídica a profissional não habilitado.

---

## Informações de entrada

Utilize tudo o que já estiver disponível.

### Contexto estratégico

- nicho, serviço ou demanda jurídica;
- recorte de público;
- origem do lead, quando relevante;
- mapeamento de persona;
- nível de consciência;
- dúvidas;
- objeções;
- fatores de decisão;
- linguagem;
- hábitos de comunicação;
- subperfis e variações relevantes.

### Contexto herdado

- resumo da triagem;
- classificação como lead qualificado;
- fatos confirmados;
- documentos analisados;
- conclusão da análise inicial;
- pontos ainda pendentes;
- tentativas anteriores;
- resposta administrativa ou judicial, quando houver;
- objetivo da consulta.

### Contexto do escritório

- advogado responsável;
- posicionamento real;
- funcionamento do serviço;
- etapas da atuação;
- participação esperada do cliente;
- modelo de honorários;
- despesas e condições;
- fluxo de contratação;
- ferramentas;
- links;
- canais oficiais;
- política de comunicação;
- protocolo de segurança, quando houver;
- procedimento autorizado para quem quiser pensar;
- uso permitido de texto e áudio.

Não invente a análise jurídica ausente.

Se a conclusão inicial não estiver disponível e for indispensável para escrever a devolutiva, faça uma única pergunta ao usuário.

Pergunte somente quando a ausência impedir a arquitetura ou exigir assumir condição comercial, financeira ou operacional que não pode ser presumida.

Não transforme a coleta de contexto em interrogatório.

---

## Hierarquia e não invenção

Respeite a hierarquia do Core Cognitivo.

Não invente:

- gratuidade de consulta ou análise;
- ausência de pagamento inicial;
- modelo por êxito;
- percentual;
- preço;
- parcelamento;
- ausência de despesas;
- prazo de retorno;
- frequência de follow-up;
- canal de acompanhamento;
- disponibilidade;
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

- `[NOME]`;
- `[ADVOGADO]`;
- `[ESCRITÓRIO]`;
- `[OAB]`;
- `[ASSUNTO]`;
- `[FATO CONFIRMADO]`;
- `[CONCLUSÃO DA ANÁLISE]`;
- `[DOCUMENTO COMPLEMENTAR]`;
- `[LINK]`;
- `[HONORÁRIOS]`;
- `[PERCENTUAL]`;
- `[DESPESAS]`;
- `[DATA DE RETORNO]`;
- `[PRAZO DEFINIDO PELO ESCRITÓRIO]`;
- `[CANAL]`.

Escreva toda a mensagem ao redor do placeholder.

Não use placeholders para substituir:

- raciocínio;
- explicação;
- devolutiva;
- objeção;
- fechamento;
- continuidade.

### Voz institucional e compromissos operacionais

Toda afirmação sobre o escritório deve vir de informação expressamente fornecida.

Não presuma:

- experiência específica;
- especialização;
- acompanhamento próximo;
- atualização frequente;
- resposta em cada etapa;
- disponibilidade;
- ausência de depósito ou taxa;
- protocolo antifraude;
- início imediato;
- prazo de andamento;
- prevenção de erro ou negativa;
- execução integral de todas as tarefas.

Mensagens como:

- “você não ficará no escuro”;
- “eu te aviso a cada passo”;
- “a gente nunca pede...”;
- “temos experiência nesse tipo de caso”;
- “assim que chegar, eu já dou andamento”;

só podem aparecer quando a prática correspondente estiver confirmada.

Quando faltar informação, use placeholder, ponto de adaptação ou formulação condicional.

Não use “garantir” como recurso de convencimento. Descreva o trabalho real, a responsabilidade do escritório e o que depende da pessoa.

---

## Recorte e especificidade

Antes de escrever, identifique:

1. qual serviço ou demanda o fluxo cobre;
2. para qual público;
3. de que ponto da jornada parte;
4. em qual decisão termina;
5. quais situações ficam fora do escopo;
6. quais subperfis exigem bifurcação.

Declare o recorte no início da saída.

Não diga que o fluxo serve para todo o nicho quando tiver sido construído apenas para:

- determinados serviços;
- categorias específicas;
- fatos geradores delimitados;
- públicos específicos;
- determinada origem de lead;
- determinada etapa;
- determinado modelo de contratação.

A arquitetura da skill é reutilizável entre nichos.

A saída deve ser profundamente específica para o nicho e o recorte atuais.

A personalização não está cumprida apenas porque as mensagens mencionam o nome do serviço.

O fluxo deve refletir concretamente:

- a situação vivida pelo público;
- como ele descreve o problema;
- quais fatos já foram analisados;
- quais dúvidas surgem na devolutiva;
- quais documentos importam;
- quais riscos existem;
- quais objeções aparecem nessa etapa;
- quais fatores influenciam a decisão;
- qual é o valor do trabalho;
- quais caminhos e limites pertencem à demanda.

Aplique o teste:

> Este fluxo poderia ser usado em outro nicho apenas trocando o nome do serviço e alguns termos?

Se a resposta for sim, aprofunde.

### Correspondência entre recorte declarado e fluxo desenvolvido

Todo elemento anunciado no recorte deve aparecer efetivamente nas mensagens.

Para cada serviço, público, categoria, fato gerador ou cenário declarado:

1. adapte a linguagem;
2. escreva as mensagens aplicáveis;
3. crie bifurcação quando mudarem devolutiva, documentos, explicação, caminho, objeção ou formalização;
4. ou retire esse elemento do recorte.

Uma menção breve ou um placeholder isolado não torna o fluxo aplicável a uma categoria distinta.

Se o fluxo fala integralmente em mãe, bebê, nascimento e parto, não declare adoção ou guarda no escopo sem desenvolver os ramos correspondentes.

---

## Persona sem virar fato individual

O fluxo deve funcionar com pessoas diferentes dentro do recorte declarado.

Não transforme em fato do tronco comum:

- idade;
- profissão;
- cidade;
- composição familiar;
- estado emocional;
- rotina;
- dificuldade financeira;
- cônjuge;
- sogra;
- filhos;
- presença de bebê;
- puerpério;
- disponibilidade noturna;
- dificuldade tecnológica;
- preferência por áudio;
- uso de emojis;
- negativa anterior;
- documento;
- história individual.

Características predominantes da persona podem orientar:

- tamanho das mensagens;
- vocabulário;
- ritmo;
- formalidade;
- explicações;
- objeções;
- bifurcações;
- escolha entre texto e áudio.

Elas não autorizam afirmar que a pessoa vive determinada situação.

Use características específicas somente:

1. quando forem fatos confirmados;
2. quando integrarem o recorte expresso;
3. em bifurcações condicionais.

Não invente respostas completas do cliente para simular naturalidade.

### Controle obrigatório de factualidade da persona

Antes de redigir, classifique silenciosamente cada característica em:

1. fato confirmado;
2. condição expressa do recorte;
3. padrão provável da persona.

Somente as categorias 1 e 2 podem aparecer como afirmações no tronco comum.

Padrões prováveis podem orientar tamanho, ritmo, linguagem e bifurcações, mas não autorizam mensagens como:

- “com o bebê aí”;
- “sei que você está corrida”;
- “sei que está apertada de dinheiro”;
- “seu marido está desconfiado”;
- “você prefere áudio”;
- “você travou no aplicativo”.

Use essas situações apenas em ramos condicionais depois de a pessoa mencioná-las ou quando integrarem expressamente o recorte.

Use `[NOME]`, nunca um nome fictício.

---

## Reutilização

O fluxo deve funcionar com pessoas diferentes dentro do recorte.

Utilize:

- placeholders;
- mensagens condicionais;
- pausas;
- ramos;
- retomadas conectadas às respostas;
- adaptações por subperfil.

Use formulações como:

- “Se a pessoa responder que...”
- “Se esse fato estiver confirmado...”
- “Quando os documentos mostrarem...”
- “Se ainda faltar [DOCUMENTO]...”
- “Se não houver retorno...”

A reutilização deve aparecer na arquitetura da conversa, não em mensagens genéricas.

---

## Regra central do formato

Cada mensagem ou sequência curta deve cumprir uma função principal.

Funções possíveis:

- apresentar;
- retomar;
- devolver análise;
- perguntar;
- reconhecer;
- explicar;
- confirmar;
- solicitar documento complementar;
- apresentar serviço;
- explicar honorários;
- tratar objeção;
- pedir decisão;
- encaminhar formalização;
- retomar silêncio;
- encerrar.

Não empilhe numa única mensagem:

- devolutiva;
- explicação jurídica;
- lista de documentos;
- apresentação do serviço;
- honorários;
- pedido de contratação;
- alerta;
- follow-up.

Distribua o conteúdo.

Não fragmente artificialmente uma frase em várias mensagens de uma linha.

---

## Tamanho e legibilidade

As mensagens devem ser confortáveis em tela pequena.

Como regra:

- uma ideia principal por mensagem;
- parágrafos curtos;
- frases claras;
- espaçamento visual;
- poucas listas;
- sem blocos excessivamente longos;
- sem sequência artificial de microfrases.

### Mensagens curtas

Use para:

- apresentação;
- confirmação;
- pergunta;
- reação;
- chamada para ação;
- envio de link;
- confirmação de recebimento;
- follow-up.

### Mensagens médias

Use para:

- síntese;
- devolutiva objetiva;
- explicação de etapa;
- esclarecimento;
- apresentação do serviço;
- honorários.

### Áudio ou explicação desenvolvida

Use quando houver ganho real para:

- devolutiva;
- lógica jurídica;
- diferença entre caminhos;
- riscos;
- funcionamento do serviço;
- objeção complexa;
- proposta.

Não empobreça a explicação para manter todas as mensagens curtas.

---

## Uso de áudio

Sugira áudio somente quando houver ganho real de:

- clareza;
- acolhimento;
- naturalidade;
- autoridade;
- explicação;
- redução de mal-entendido.

Não presuma que a pessoa prefere áudio.

Quando essa preferência não estiver informada, o fluxo pode:

- oferecer escolha e aguardar; ou
- entregar versão em texto somente se o escritório tiver definido texto como padrão.

A falta de resposta não autoriza áudio nem escolha automática de formato.

Exemplo:

> Eu posso te explicar essa parte por escrito ou em um áudio curto. Qual formato fica melhor para você?

*Aguarde.*

Quando sugerir áudio:

- escreva o texto integral;
- use começo, desenvolvimento e conclusão;
- evite listas extensas;
- use transições;
- termine com próximo passo;
- indique duração aproximada realista.

Não escreva apenas:

- “envie um áudio explicando”;
- “fale sobre os riscos”;
- “explique os honorários”.

---

## Emojis e informalidade

Não use emojis por padrão.

Use somente quando:

- o usuário pedir;
- a identidade do escritório permitir;
- o mapeamento indicar compatibilidade;
- o contexto não exigir maior formalidade.

Quando usar:

- limite a quantidade;
- preserve função comunicativa;
- não infantilize;
- não substitua clareza;
- não use entusiasmo artificial;
- não use símbolos inadequados ao contexto jurídico.

WhatsApp não significa informalidade automática.

Não imite:

- gírias;
- erros de escrita;
- abreviações;
- intimidade;
- cenas da persona.

O profissional deve falar de maneira compreensível sem fingir ser o público.

---

## Continuidade entre mensagens

Cada nova mensagem deve se conectar ao que veio antes.

Use reações naturais, como:

- “Entendi.”
- “Certo.”
- “Esse ponto confirma o que eu precisava verificar.”
- “Com essa informação, consigo te explicar a próxima parte.”
- “Agora que isso ficou claro...”
- “Sobre o documento que você enviou...”
- “Voltando à conclusão...”

Não use respostas automáticas que poderiam ser enviadas independentemente do que a pessoa disse.

Não repita o relato inteiro.

Não reinicie a conversa após cada intervalo.

---

## Conclusão da análise e resultado

A análise inicial já foi realizada.

O fluxo não deve falar como se o advogado ainda precisasse receber os documentos básicos para descobrir se existe um caminho.

Quando a análise permitir, formule a conclusão de forma clara.

Exemplos:

> Analisei os documentos que você enviou. Pelas informações confirmadas, o seu caso se encaixa nessa regra e podemos seguir com o pedido.

> Os documentos confirmam o ponto principal que precisava ser verificado.

> Pela análise das datas e dos registros, esse requisito foi preenchido.

Depois, quando necessário, apresente o limite:

> O que eu não posso garantir é a decisão final, porque ela depende do órgão responsável.

Não use:

- “juridicamente defensável”;
- “plausibilidade jurídica”;
- “tese sustentável”;
- “possibilidade abstrata”;
- “probabilidade de enquadramento”;
- cautela genérica que apague a conclusão.

A conclusão da análise não autoriza prometer:

- deferimento;
- êxito;
- pagamento;
- valor;
- prazo;
- decisão favorável.

---

## Devolutiva

A devolutiva é o primeiro grande momento jurídico do fluxo.

Ela deve:

1. identificar o advogado;
2. retomar o contexto;
3. confirmar que os documentos foram analisados;
4. apresentar a conclusão;
5. explicar o ponto central;
6. separar o que está confirmado do resultado futuro;
7. indicar o próximo passo;
8. abrir espaço para dúvida.

Exemplo de estrutura:

> Olá, [NOME]. Aqui é [ADVOGADO], do [ESCRITÓRIO].

> Eu recebi o resumo do seu atendimento e analisei os documentos enviados sobre [ASSUNTO].

> O ponto principal era verificar [PONTO CENTRAL]. Pela análise, [CONCLUSÃO].

> Isso significa que [CONSEQUÊNCIA PRÁTICA].

> O resultado final depende de [AUTORIDADE/ETAPA], então eu não consigo prometer a decisão. O que eu consigo te explicar com clareza é por que podemos seguir e como o trabalho será feito.

> Até aqui ficou claro?

*Aguarde.*

Não transforme a devolutiva em aula.

Não repita uma explicação genérica que poderia ser enviada antes da análise.

---

## Esclarecimentos complementares

Depois da devolutiva, faça perguntas somente quando algum ponto complementar puder alterar:

- o caminho;
- a documentação;
- a explicação;
- a responsabilidade da pessoa;
- a proposta;
- o próximo passo.

Não repita dados já confirmados na triagem ou nos documentos.

Quando precisar perguntar:

1. retome o ponto analisado;
2. explique por que ainda importa;
3. faça uma pergunta simples;
4. aguarde;
5. reconheça a resposta;
6. continue.

Exemplo:

> Na análise ficou pendente apenas confirmar [PONTO], porque isso muda [CONSEQUÊNCIA].

> Você consegue me dizer [PERGUNTA]?

*Aguarde.*

> Entendi. Com essa informação, [APLICAÇÃO].

Não faça questionário.

Não pergunte sobre intenção de contratar antes de explicar:

- a conclusão;
- o caminho;
- o serviço;
- as condições.

---

## Explicação jurídica pelo WhatsApp

Quando explicar o Direito:

1. contextualize;
2. apresente a consequência prática;
3. explique a lógica;
4. aplique aos documentos e fatos;
5. mostre os caminhos;
6. alinhe limites;
7. indique o próximo passo.

Distribua em mensagens conectadas ou áudio.

Não transforme o WhatsApp em aula.

Não omita o raciocínio essencial.

Não comece por:

- número de artigo;
- nome de tribunal;
- história legislativa;
- classificação técnica.

Use esses elementos apenas quando forem essenciais.

---

## Documentos complementares

A coleta documental inicial já ocorreu.

Solicite novo documento somente quando a análise tiver identificado uma lacuna específica.

Explique:

- qual documento falta;
- o que ele precisa demonstrar;
- como enviar;
- o que acontecerá depois.

Exemplo:

> Analisei o que você enviou e ficou pendente apenas [DOCUMENTO].

> Ele é importante para confirmar [PONTO].

> Você consegue me mandar uma foto legível por aqui, mostrando todas as páginas e sem cortar as bordas?

*Aguarde.*

Não reabra coleta genérica.

Não peça novamente documento já recebido.

Não apresente lista universal.

Não crie, por subperfil, blocos como:

- “documento complementar típico”;
- “documentos que normalmente faltam”;
- “lista complementar recomendada”.

No fluxo reutilizável, só escreva pedido de documento quando a entrada já indicar:

- qual lacuna foi identificada;
- qual documento específico pode preenchê-la;
- por que ele é necessário.

Quando nenhuma lacuna específica tiver sido informada:

- não escreva solicitação documental;
- registre `[DOCUMENTO ESPECÍFICO IDENTIFICADO COMO PENDENTE NA ANÁLISE]` apenas nos pontos de adaptação;
- ou faça uma única pergunta ao usuário se o documento for indispensável para construir o fluxo.

Não prometa segurança tecnológica não informada.

---

## Caminhos, limites e expectativas

Explique, quando pertinente:

- o que pode ser buscado;
- quais caminhos existem;
- qual caminho a análise indica;
- o que fortalece;
- o que pode dificultar;
- o que depende da autoridade responsável;
- quais riscos permanecem;
- qual prazo verdadeiro importa.

Não invente urgência.

Não use urgência como encerramento automático de follow-up.

Não apresente medida jurídica como livre escolha quando depender de análise técnica.

---

## Apresentação do serviço

Explique concretamente:

- o que o escritório fará;
- como organizará o caso;
- quais documentos utilizará;
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
- especializado, quando não houver base ou posicionamento informado.

Não use:

- “a gente cuida de tudo”;
- “o resto é com a gente”;
- “você não precisa fazer nada”;

salvo quando isso for literalmente verdadeiro e tiver sido informado.

---

## Participação real do cliente

Explique as ações que podem depender da pessoa, como:

- documentos complementares;
- informações;
- assinaturas;
- acessos;
- comparecimento;
- perícia;
- audiência;
- entrevista;
- resposta a exigência;
- atualização de dados.

Facilidade não significa apagamento das responsabilidades reais.

Use linguagem simples:

> O escritório organiza e conduz o processo. Da sua parte, eu vou precisar de [AÇÕES REAIS].

Não invente obrigações.

---

## Honorários e condições

Apresente honorários somente quando:

- a consulta incluir contratação;
- o advogado estiver autorizado;
- o modelo tiver sido informado.

Explique, quando aplicável:

1. forma de cobrança;
2. valor ou percentual;
3. base de cálculo;
4. momento do pagamento;
5. pagamento inicial;
6. despesas separadas;
7. parcelamento;
8. efeito da ausência de resultado;
9. registro no contrato.

Não invente:

- gratuidade;
- análise sem custo;
- ausência de pagamento inicial;
- isenção;
- parcelamento;
- modelo por êxito;
- percentual;
- ausência de despesas;
- política contratual.

O fato de os honorários serem por êxito não significa que a consulta ou a análise inicial seja gratuita.

Use placeholders para dados exatos.

Não reduza a explicação a frase de efeito.

---

## Chamada para ação

Cada etapa deve terminar com um próximo passo simples e compatível.

Nesta skill, os CTAs podem ser:

- confirmar recebimento;
- dizer se a explicação ficou clara;
- responder ponto complementar;
- ouvir áudio;
- enviar documento complementar;
- confirmar informação;
- esclarecer dúvida;
- autorizar envio do contrato;
- assinar;
- realizar pagamento;
- confirmar formalização;
- aguardar próxima etapa.

Não use como CTA principal:

- escolher horário;
- confirmar consulta;
- participar de triagem;
- demonstrar intenção preliminar.

A chamada para ação deve ser:

- específica;
- simples;
- proporcional;
- fácil de executar;
- coerente com o momento.

Evite:

- múltiplos pedidos simultâneos;
- “qualquer coisa me avise” como único encerramento;
- pressão;
- urgência artificial;
- pedido de contratação antes da explicação suficiente.

---

## Dúvidas e objeções

Antes da decisão, abra espaço:

> Antes de eu te explicar a formalização, tem algum ponto da análise, do trabalho ou das condições que você quer esclarecer?

*Aguarde.*

Quando surgir objeção:

1. investigue;
2. aguarde;
3. responda ao motivo real;
4. confirme;
5. retome.

Exemplo de estrutura:

> Quando você fala isso, sua preocupação está mais em [PONTO A] ou em [PONTO B]?

*Aguarde.*

> Entendi. Nesse caso, o ponto importante é [RESPOSTA SUBSTANTIVA].

> Isso esclarece a sua dúvida?

*Aguarde.*

> Certo. Então, sobre o próximo passo...

Inclua somente objeções compatíveis com:

- o nicho;
- o recorte;
- a consulta;
- o serviço;
- os honorários;
- a decisão atual.

Não invente:

- maior chance de êxito;
- frequência de reversão;
- vantagem sobre outro profissional;
- resultado provável;
- condição comercial.

---

## Fechamento e decisão

Quando o objetivo incluir contratação, o fluxo deve chegar à decisão.

Antes da pergunta final:

1. sintetize a conclusão;
2. explique o caminho;
3. apresente o serviço;
4. alinhe limites;
5. apresente honorários;
6. esclareça dúvidas;
7. explique a formalização.

Depois, use pergunta clara:

> Diante do que eu te expliquei, faz sentido seguir com o escritório?

ou:

> Posso encaminhar o contrato e a procuração para iniciarmos?

*Aguarde.*

Não trate silêncio como aceite.

Não use pergunta precoce sobre intenção de contratar antes da devolutiva.

---

## Aceite, hesitação e recusa

### Se houver aceite

Conduza, conforme o fluxo real, para:

- dados;
- contrato;
- procuração;
- assinatura;
- pagamento, quando aplicável;
- documento complementar;
- canal de comunicação;
- confirmação do início.

Escreva as mensagens completas.

Não use comemoração comercial excessiva.

Evite:

- “ótima decisão”;
- “você fez a escolha certa”;
- “melhor ainda”.

Prefira:

> Perfeito, [NOME]. Vou organizar agora os próximos passos e explicar cada documento antes da assinatura.

### Se houver hesitação

Não responda a objeção presumida.

Pergunte:

> Claro. Qual é o principal ponto que você ainda precisa avaliar: a análise, a forma de trabalho, os honorários ou o momento de começar?

Adapte as opções ao contexto.

Responda somente ao motivo real.

Use apenas o procedimento autorizado pelo escritório.

Quando houver retorno combinado, registre:

- o ponto pendente;
- quem fará o quê;
- a data ou o prazo definido;
- como a conversa será retomada.

Não crie sequência prolongada de follow-up.

### Se houver recusa

Verifique uma vez se existe dúvida não esclarecida.

Persistindo a decisão:

- respeite;
- não pressione;
- não use medo;
- não use culpa;
- não invente prazo;
- não desqualifique a decisão;
- encerre profissionalmente.

### Se não houver elementos para proposta responsável

Explique:

- o que ainda impede a conclusão;
- qual documento ou informação falta;
- o que será feito depois;
- ou por que o caso não deve prosseguir.

Não simule fechamento.

---

## Follow-up da consulta e do fechamento

Inclua follow-up somente para silêncios ocorridos depois do início da devolutiva.

Situações permitidas:

- silêncio após a devolutiva;
- silêncio após esclarecimento;
- silêncio após documento complementar solicitado;
- silêncio após apresentação do serviço;
- silêncio após honorários;
- silêncio após proposta;
- contrato não assinado;
- retorno expressamente combinado.

Não inclua:

- triagem incompleta;
- pergunta de qualificação sem resposta;
- agendamento não confirmado;
- confirmação de consulta;
- ausência em consulta;
- recuperação de no-show;
- documento inicial não enviado;
- reativação genérica.

O follow-up deve:

- retomar o ponto exato;
- explicar por que está retomando;
- reduzir esforço de resposta;
- apresentar próximo passo;
- permitir saída respeitosa.

Não escreva apenas:

- “viu minha mensagem?”;
- “alguma novidade?”;
- “ainda tem interesse?”;
- “estou aguardando”;
- “última chance”.

Estrutura recomendada:

1. retomada;
2. utilidade;
3. pergunta simples;
4. saída respeitosa.

Exemplo:

> Olá, [NOME]. Retomo nossa conversa sobre a análise de [ASSUNTO].

> Ficou pendente você me confirmar se [PONTO], porque isso define [PRÓXIMO PASSO].

> Conseguiu verificar?

Não invente datas ou frequência.

Use:

- `[APÓS O PRAZO DEFINIDO PELO ESCRITÓRIO]`;
- `[DATA DE RETORNO]`;
- `[PRAZO COMBINADO]`.

O último follow-up deve permitir encerramento sem novo argumento de pressão.

Não termine automaticamente com alerta de prazo.

---

## Arquitetura do fluxo

Adapte a profundidade ao nicho e ao objetivo.

Não transforme esta lista em manual visível dentro da saída.

### 1. Primeira mensagem do advogado

- identificação;
- retomada do contexto;
- confirmação de que recebeu e analisou os documentos;
- indicação de que fará a devolutiva;
- permissão para continuar.

### 2. Formato da explicação

Quando útil, ofereça texto ou áudio e aguarde a escolha.

Não presuma preferência.

Não escolha áudio nem continue a explicação por ausência de resposta.

### 3. Devolutiva da análise

- conclusão;
- ponto central;
- consequência prática;
- limite do resultado;
- espaço para dúvida.

### 4. Esclarecimentos complementares

Somente quando necessários.

### 5. Explicação dos caminhos e limites

Distribuída em mensagens ou áudio.

### 6. Apresentação do trabalho

- o que o escritório fará;
- o que dependerá da pessoa;
- etapas;
- limites.

### 7. Honorários e condições

Somente dados reais.

### 8. Dúvidas e objeções

Investigue, responda, confirme e retome.

### 9. Decisão

Pergunta clara e espera.

### 10. Aceite, hesitação ou recusa

Continuidade completa.

### 11. Contrato, procuração e início

Mensagens conforme o fluxo real.

### 12. Follow-ups

Somente os compatíveis com a consulta e o fechamento.

---

## Formato da entrega

Entregue nesta ordem:

# 1. PONTO DE PARTIDA E PREMISSAS

Bloco curto contendo:

- nicho;
- serviço;
- recorte;
- público;
- ponto de partida;
- ponto de encerramento;
- resumo herdado;
- documentos analisados;
- conclusão disponível;
- pontos pendentes;
- advogado responsável;
- objetivo;
- modelo de honorários;
- condições informadas;
- placeholders;
- pontos que exigem validação.

Não produza mapa psicológico.

Não repita o mapeamento.

# 2. FLUXO PRINCIPAL DE CONSULTA PELO WHATSAPP

Esta deve ser a maior parte da saída.

Organize por momentos da conversa.

Use:

- títulos discretos;
- mensagens prontas em bloco de citação;
- indicação de espera;
- continuação;
- perguntas;
- áudios integrais;
- chamadas para ação.

# 3. BIFURCAÇÕES ESSENCIAIS

Inclua somente os ramos que alterem substancialmente:

- devolutiva;
- esclarecimento;
- documento;
- caminho;
- risco;
- serviço;
- proposta;
- próximo passo.

Escreva as mensagens completas.

# 4. OBJEÇÕES

Para cada objeção relevante, escreva:

- pergunta de investigação;
- espera;
- resposta;
- confirmação;
- retomada.

# 5. ACEITE, HESITAÇÃO E RECUSA

Escreva as continuidades completas.

# 6. FOLLOW-UPS DA CONSULTA E DO FECHAMENTO

Inclua somente os compatíveis com esta etapa.

# 7. PONTOS DE ADAPTAÇÃO

Lista curta com dados exatos e condições reais que precisam ser preenchidos ou validados.

Não inclua:

- checklist operacional extenso;
- agendamento;
- no-show;
- triagem;
- qualificação.

---

## Revisão interna obrigatória

Antes de entregar, verifique silenciosamente:

### Produto e arquitetura

- a saída é um fluxo assíncrono de consulta e fechamento?
- o lead foi tratado como já triado e qualificado?
- os documentos iniciais foram tratados como já analisados?
- o fluxo começou na passagem ao advogado ou na devolutiva?
- alguma etapa refez triagem?
- alguma etapa refez qualificação?
- houve pergunta precoce sobre intenção de contratar?
- houve convite ou agendamento indevido?
- houve confirmação ou recuperação de no-show?
- o fluxo permaneceu assíncrono?
- apareceu horário reservado sem informação?
- a maior parte da entrega é composta por mensagens utilizáveis?
- o resultado parece WhatsApp, e não manual ou ligação transcrita?

### Recorte e reutilização

- o recorte foi declarado?
- o conteúdo cobre exatamente esse recorte?
- o fluxo funciona com pessoas diferentes?
- alguma característica da persona virou fato?
- cada afirmação individual vem de fato confirmado, condição do recorte ou bifurcação explícita?
- presença de bebê, rotina, dificuldade financeira, familiar ou tecnológica foi presumida?
- algum nome fictício substituiu `[NOME]`?
- o subperfil dominante ocupou o tronco comum?
- emojis, áudio ou intimidade foram presumidos?
- todo item declarado no recorte foi desenvolvido em mensagens ou bifurcações reais?
- algum fato gerador ou público apareceu apenas de forma residual?
- as bifurcações cobrem variações reais?
- algum exemplo de outro nicho contaminou a entrega?
- o fluxo poderia ser usado em outro nicho apenas trocando nomes? Se sim, aprofunde.

### Devolutiva e profundidade

- a devolutiva apresenta conclusão clara?
- a análise documental foi contraditoriamente tratada como não realizada?
- a explicação pertence aos documentos e fatos analisados?
- houve áudio genérico anterior à análise?
- o silêncio foi usado como autorização, escolha de formato, disponibilidade, compreensão ou aceite?
- alguma instrução mandou enviar áudio ou continuar por ausência de resposta?
- a profundidade foi distribuída?
- existem momentos claros de espera?
- os áudios foram escritos integralmente?
- a linguagem ficou natural?
- a cautela virou parecer?
- foi usado “juridicamente defensável” ou equivalente?

### Segurança e não invenção

- foi presumida gratuidade?
- foi inventada condição comercial ou operacional?
- foi inventada experiência, especialização, política de comunicação ou compromisso institucional?
- alguma mensagem promete acompanhamento, atualização, resposta, início ou prevenção de erro sem informação expressa?
- houve promessa de resultado?
- houve estatística, frequência de êxito ou superioridade não comprovada?
- foi criada urgência artificial?
- a conclusão da análise foi separada do resultado?
- os documentos pedidos são apenas complementares?
- cada documento solicitado corresponde a uma lacuna específica já identificada?
- foram evitados “documentos típicos”, listas complementares genéricas e repetição da coleta inicial?
- a participação do cliente foi descrita com realismo?
- o protocolo de segurança foi omitido quando não fornecido?

### Fechamento e follow-up

- o serviço foi concretamente explicado?
- honorários e condições correspondem aos dados reais?
- a decisão foi pedida apenas depois da explicação suficiente?
- o aceite leva ao fluxo real?
- a hesitação é investigada?
- a recusa é respeitada?
- os follow-ups pertencem à consulta ou ao fechamento?
- o último follow-up permite encerramento sem pressão?
- a ausência de viabilidade não foi mascarada por fechamento artificial?

Corrija silenciosamente o que falhar.

---

## Critério de conclusão

O fluxo está pronto quando um profissional consegue:

1. iniciar a conversa sem repetir triagem;
2. apresentar a devolutiva da análise;
3. explicar a conclusão com clareza;
4. separar análise de resultado futuro;
5. esclarecer apenas pontos complementares;
6. distribuir a explicação pelo canal;
7. utilizar texto e áudio de forma consciente;
8. apresentar concretamente o serviço;
9. explicar honorários reais;
10. tratar objeções;
11. pedir decisão;
12. conduzir aceite, hesitação ou recusa;
13. formalizar a contratação;
14. retomar silêncios da própria consulta;
15. reutilizar o fluxo com pessoas diferentes dentro do recorte;
16. adaptar apenas fatos do cliente e particularidades reais do escritório.

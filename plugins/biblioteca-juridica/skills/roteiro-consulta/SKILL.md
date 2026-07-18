---
name: roteiro-consulta
description: Cria roteiros falados, fluidos e reutilizáveis para consulta jurídica e fechamento por ligação, videoconferência ou reunião presencial, partindo de lead já triado e qualificado. Use quando o advogado precisar conduzir diagnóstico, explicação, aplicação ao caso, apresentação do serviço, honorários, objeções, decisão e contratação em uma conversa síncrona.
argument-hint: [mapeamento de persona, recorte do serviço, resumo da triagem, canal e particularidades do escritório]
---

# Roteiro de Consulta Jurídica

## Objetivo

Produzir um roteiro falado integral, fluido, profundo e reutilizável para condução de consulta jurídica e, quando aplicável, fechamento de contratação.

A maior parte da entrega deve ser composta por falas prontas do profissional.

O resultado deve parecer uma consulta real, organizada e conduzida por um profissional experiente — não um manual de treinamento nem uma conversa fictícia fechada.

Não produza como saída principal:

- playbook;
- manual operacional;
- apostila;
- checklist;
- mapa de condução extenso;
- formulário;
- lista de orientações;
- fluxo de WhatsApp;
- triagem;
- qualificação comercial;
- agendamento;
- conversa fictícia com uma pessoa específica;
- transcrição de respostas inventadas do cliente.

---

## Contexto obrigatório

Antes de produzir a saída:

1. leia `../../references/core-cognitivo.md`;
2. leia `../../references/core-escrita-oralidade.md`;
3. utilize o Mapeamento de Persona Jurídica fornecido pelo usuário ou disponível na conversa;
4. utilize o resumo da triagem, os fatos confirmados e os documentos já disponíveis;
5. utilize as particularidades reais do escritório;
6. priorize fatos confirmados e instruções expressas sobre padrões prováveis.

Não execute novamente a skill de mapeamento de persona.

Não reproduza o mapeamento na saída.

Converta-o em decisões concretas de:

- recorte;
- linguagem;
- ritmo;
- ordem dos assuntos;
- perguntas;
- explicações;
- bifurcações;
- objeções;
- fatores de decisão;
- apresentação de valor;
- fechamento.

---

## Ponto de partida e limite

Esta skill parte de um lead que:

- já passou pela triagem;
- já foi classificado como qualificado para a consulta;
- possui contexto inicial suficiente para ser atendido;
- pode ter fatos, documentos ou requisitos que ainda precisam ser confirmados durante a conversa.

A consulta pode:

- retomar e corrigir o resumo da triagem;
- aprofundar fatos relevantes;
- organizar a linha do tempo;
- confirmar documentos;
- identificar lacunas;
- validar a viabilidade jurídica;
- concluir que o caso pode ou não prosseguir;
- explicar caminhos;
- apresentar o serviço;
- conduzir à decisão.

Isso não constitui nova qualificação comercial.

Não utilize como etapas, critérios ou linguagem:

- MQL;
- SQL;
- temperatura do lead;
- lead quente ou frio;
- intenção preliminar de contratar;
- caso de maior valor;
- lead que “vale seguir”;
- nova triagem disfarçada de consulta.

A skill começa na preparação da consulta ou na primeira fala do profissional.

A skill termina em uma destas situações:

- contratação e formalização;
- hesitação com próximo passo concreto;
- recusa respeitosa;
- conclusão responsável de que ainda não há elementos para proposta;
- necessidade pontual de documento ou informação complementar;
- encerramento da consulta sem contratação, quando esse for o objetivo definido.

Não inclui:

- captação;
- nutrição;
- triagem;
- qualificação comercial;
- convite para consulta;
- agendamento;
- confirmação de presença;
- prevenção de ausência;
- recuperação de no-show;
- sequência prolongada de follow-up;
- acompanhamento jurídico posterior ao início da atuação;
- pós-venda.

---

## Natureza do produto

Esta skill produz uma **conversa falada de consulta e fechamento**.

A maior parte da entrega deve ser composta por:

- falas do profissional;
- perguntas;
- explicações;
- transições;
- pausas;
- checagens de entendimento;
- bifurcações indispensáveis;
- respostas a objeções;
- decisão;
- próximos passos.

Use títulos discretos somente para facilitar a localização.

Não apresente repetidamente:

- objetivo;
- orientação de condução;
- por que perguntar;
- o que observar;
- erros a evitar;
- critério para avançar;
- comentários sobre estratégia;
- justificativas extensas sobre técnicas comerciais.

Essas decisões devem orientar silenciosamente a escrita.

Notas internas podem aparecer apenas quando forem indispensáveis, por exemplo:

- *Escute antes de continuar.*
- *Aguarde a resposta.*
- *Use este trecho somente se essa situação estiver confirmada.*
- *Substitua pelos fatos reais.*
- *Não avance sem confirmar este ponto.*

---

## Canais permitidos

Esta skill produz roteiros para comunicação oral contínua:

- ligação;
- videoconferência;
- reunião presencial.

Não produza fluxo de WhatsApp como saída principal.

Quando o canal não estiver informado e isso alterar substancialmente a condução, faça uma única pergunta.

---

## Condutor

A consulta jurídica deve ser conduzida por advogado ou profissional juridicamente habilitado.

O condutor pode:

- investigar fatos;
- organizar o problema;
- explicar conceitos;
- apresentar possibilidades;
- alinhar riscos;
- fazer avaliação;
- concluir a análise quando houver elementos suficientes;
- apresentar o serviço;
- tratar objeções;
- conduzir à contratação.

Não pode:

- garantir resultado;
- inventar conclusão;
- afirmar fato não confirmado;
- ultrapassar os elementos disponíveis;
- atribuir ao órgão ou ao Judiciário uma decisão ainda inexistente.

Se o usuário indicar condutor não advogado, não transforme essa pessoa em responsável pela consulta jurídica.

Nesse caso:

1. limite suas falas a funções operacionais expressamente permitidas;
2. mantenha explicação e conclusão jurídica para o profissional habilitado;
3. ou faça uma única pergunta para confirmar se o usuário deseja outro tipo de conversa.

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
- subperfis e variações relevantes.

### Contexto da consulta

- resumo da triagem;
- fatos já confirmados;
- documentos recebidos ou analisados;
- pontos pendentes;
- canal;
- condutor;
- objetivo final da conversa;
- existência ou não de análise documental anterior.

### Contexto do escritório

- posicionamento real;
- funcionamento do serviço;
- etapas da atuação;
- participação esperada do cliente;
- modelo de honorários;
- despesas e condições;
- fluxo de contratação;
- ferramentas;
- canais oficiais;
- política de comunicação;
- protocolo de segurança, quando houver;
- procedimento autorizado para quem quiser pensar.

A análise documental anterior pode existir ou não.

Não a presuma.

Quando ela tiver ocorrido, utilize suas conclusões.

Quando ainda não tiver ocorrido, organize o roteiro para explicar o que pode ser concluído na conversa e o que ainda dependerá de documentos.

Pergunte somente quando a ausência impedir a arquitetura ou exigir assumir uma condição comercial, financeira ou operacional que não pode ser presumida.

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
- `[ESCRITÓRIO]`;
- `[OAB]`;
- `[CANAL]`;
- `[HONORÁRIOS]`;
- `[PERCENTUAL]`;
- `[DESPESAS]`;
- `[DOCUMENTO]`;
- `[DATA]`;
- `[HORÁRIO]`;
- `[LINK]`.

Escreva toda a fala ao redor do placeholder.

Não use placeholders para substituir:

- explicação;
- estratégia;
- raciocínio;
- perguntas;
- objeções;
- fechamento.

---

## Recorte e especificidade

Antes de escrever, identifique:

1. qual serviço ou demanda o roteiro cobre;
2. para qual público;
3. de que ponto da jornada parte;
4. em qual decisão termina;
5. quais situações ficam fora do escopo;
6. quais subperfis exigem bifurcação.

Declare o recorte no início da saída.

Não diga que o roteiro serve para todo o nicho quando tiver sido construído apenas para:

- determinados serviços;
- categorias específicas;
- fatos geradores delimitados;
- públicos específicos;
- determinada origem de lead;
- determinado canal;
- determinada etapa.

A arquitetura da skill é reutilizável entre nichos.

A saída deve ser profundamente específica para o nicho e o recorte atuais.

A personalização não está cumprida apenas porque o roteiro menciona o nome do serviço.

A conversa deve refletir concretamente:

- a situação vivida pelo público;
- a forma como ele descreve o problema;
- as dúvidas reais;
- os critérios jurídicos relevantes;
- os documentos;
- os riscos;
- as objeções;
- os fatores de decisão;
- o valor da consulta;
- o valor do serviço;
- os caminhos e limites próprios da demanda.

Aplique o teste:

> Este roteiro poderia ser usado em outro nicho apenas trocando o nome do serviço e alguns termos?

Se a resposta for sim, aprofunde.

---

## Persona sem virar cliente fictício

O roteiro deve servir para pessoas diferentes dentro do recorte declarado.

Não transforme em fato do tronco comum:

- nome;
- idade;
- profissão;
- cidade;
- composição familiar;
- estado emocional;
- rotina;
- dificuldade financeira;
- cônjuge;
- filhos;
- presença de bebê;
- puerpério;
- horário disponível;
- negativa anterior;
- documento;
- história individual.

Características predominantes da persona orientam:

- tom;
- ritmo;
- perguntas;
- explicações;
- objeções;
- bifurcações.

Elas não autorizam o profissional a afirmar que aquela pessoa vive determinada situação.

Use características específicas somente:

1. quando forem fatos confirmados;
2. quando integrarem o recorte expresso;
3. em bifurcações condicionais.

Exemplos:

> Se a pessoa mencionar dificuldade de tempo...

> Se houver negativa anterior confirmada...

> Quando os documentos indicarem essa categoria...

Não invente respostas completas do cliente para criar fluidez.

---

## Reutilização sem aparência de manual

O roteiro deve funcionar com clientes diferentes dentro do recorte.

Utilize:

- placeholders;
- pausas;
- checagens;
- formulações condicionais;
- blocos alternativos;
- retomadas conectadas às respostas.

Use formulações como:

- “Se a pessoa informar que...”
- “Quando esse cenário estiver confirmado...”
- “Se os documentos demonstrarem...”
- “Dependendo da data...”
- “Neste ramo, use...”

A reutilização deve aparecer na arquitetura da conversa, não em linguagem genérica.

---

## Profundidade substantiva

A consulta deve permitir que o profissional desenvolva os assuntos centrais sem improvisar a explicação principal.

Quando pertinente, desenvolva nas falas:

1. o que está acontecendo na prática;
2. quais fatos importam;
3. por que importam;
4. qual é a lógica jurídica;
5. o que muda conforme as respostas;
6. quais documentos confirmam cada ponto;
7. quais caminhos podem existir;
8. quais limites e riscos precisam ser alinhados;
9. o que ainda depende de análise;
10. o que acontece depois;
11. qual é o valor da atuação profissional.

Não substitua conteúdo por instruções como:

- “explique o direito”;
- “fale sobre os riscos”;
- “apresente o serviço”;
- “trate a objeção”;
- “mostre os próximos passos”.

Escreva a fala que realiza essas ações.

Não confunda profundidade com:

- monólogo;
- repetição;
- encenação;
- excesso de títulos;
- história legislativa desnecessária;
- linguagem de parecer;
- desenvolvimento fora do recorte.

---

## Interação e distribuição da profundidade

A conversa deve ser profunda, mas não pode ser formada por vários discursos consecutivos do profissional.

Nos pontos centrais, distribua:

1. conexão com o relato;
2. explicação;
3. consequência prática;
4. pausa;
5. confirmação ou pergunta;
6. continuação conforme a reação.

Como regra, não apresente mais de duas informações relevantes sem:

- abrir espaço;
- checar compreensão;
- pedir confirmação;
- conectar a explicação ao caso.

Não use confirmações mecânicas depois de cada frase.

Use-as quando a pessoa realmente puder:

- se perder;
- discordar;
- lembrar de novo fato;
- fazer pergunta;
- mudar a análise.

Não invente respostas completas do cliente.

---

## Progressão das perguntas

As perguntas devem nascer do contexto anterior.

Não entregue uma bateria técnica desconectada.

Faça:

1. retomada do que já chegou da triagem;
2. confirmação ou correção;
3. pergunta sobre a lacuna;
4. reação;
5. próxima pergunta ou explicação.

Não repita do zero fatos que já estejam confirmados.

Exemplo de estrutura:

> Eu recebi a informação de que [RESUMO DA TRIAGEM]. Antes de avançar, quero confirmar se compreendi corretamente.

*Confirme.*

> Certo. O ponto que ainda preciso esclarecer é [PONTO]. O que aconteceu nessa parte?

*Escute.*

> Entendi. Isso importa porque [CONSEQUÊNCIA]. Agora preciso confirmar [PRÓXIMO PONTO].

---

## Régua de certeza

Separe:

1. **Relato** — o que a pessoa informou.
2. **Indício** — o que o relato sugere.
3. **Confirmação** — o que depende de documentos, cálculos, perícia ou análise.
4. **Resultado** — o que depende da atuação e da decisão competente.

Não salte do relato para o resultado.

Quando ainda faltarem elementos, use linguagem condicionada.

Exemplos:

> Pelo que você me explicou, esse fato é relevante.

> Isso pode indicar um caminho, mas ainda preciso confirmar [PONTO].

> Se os documentos confirmarem essa sequência, conseguiremos definir o caminho adequado.

Quando houver elementos suficientes, formule a conclusão com clareza.

---

## Conclusão da análise e promessa de resultado

Não confunda conclusão profissional com garantia de resultado futuro.

Quando a análise permitir, diga de forma natural:

> Pelos documentos e pelas datas que analisamos, você preenchia esse requisito.

> A análise mostra que o seu caso se encaixa nessa regra.

> Com esses elementos, podemos seguir com o pedido.

Quando necessário, separe o limite:

> O que eu não consigo garantir é a decisão final, porque ela depende da autoridade responsável.

Evite linguagem excessivamente defensiva ou artificial, como:

- “juridicamente defensável”;
- “plausibilidade jurídica”;
- “tese sustentável”;
- “probabilidade de enquadramento”;
- “possibilidade abstrata”.

A cautela deve aparecer na distinção entre:

- conclusão da análise;
- resultado futuro.

Não prometa:

- deferimento;
- êxito;
- pagamento;
- valor;
- prazo;
- decisão favorável.

---

## Linguagem profissional

O profissional deve soar:

- experiente;
- seguro;
- sereno;
- claro;
- responsável;
- atento;
- acessível;
- profissional.

Simplifique a linguagem, não o raciocínio.

Evite:

- juridiquês desnecessário;
- coloquialismo excessivo;
- informalidade forçada;
- infantilização;
- diminutivos;
- intimidade presumida;
- frases publicitárias;
- elogios institucionais vazios;
- metáforas que substituam explicação;
- tom de vendedor;
- tom professoral;
- frases de efeito como única explicação.

Não imite gírias, erros de escrita ou abreviações da persona.

O profissional deve falar de forma compreensível para o público sem fingir ser o público.

---

## Explicação em camadas

Quando um tema relevante precisar ser explicado, utilize, conforme o contexto:

1. enquadramento;
2. consequência prática;
3. lógica da regra;
4. aplicação ao relato;
5. elementos favoráveis;
6. elementos pendentes;
7. documentos;
8. caminhos;
9. limites;
10. síntese.

A síntese simples consolida a compreensão, mas não substitui as camadas anteriores.

Evite começar com:

- número de artigo;
- nome de tribunal;
- história legislativa;
- classificação técnica.

Use esses elementos apenas quando forem essenciais para compreensão ou confiança.

---

## Arquitetura da consulta

Adapte a ordem e a profundidade ao nicho e ao objetivo.

Não transforme esta lista em checklist visível.

### 1. Abertura e continuidade da triagem

A fala deve:

- apresentar o profissional;
- reconhecer o contato anterior;
- demonstrar que o contexto já foi recebido;
- evitar que a pessoa repita tudo;
- confirmar disponibilidade;
- explicar brevemente a dinâmica;
- pedir licença para começar.

Exemplo de estrutura:

> Oi, [NOME]. Aqui é [PROFISSIONAL], do [ESCRITÓRIO].

> Eu já recebi o resumo do seu primeiro contato, então você não vai precisar repetir tudo do zero.

> Quero primeiro confirmar os pontos principais, entender o que ainda ficou pendente e depois te explicar como eu vejo a situação. Tudo bem?

*Espere a confirmação.*

Não prometa conclusão definitiva quando ainda faltarem elementos.

Quando houver medo de fraude ou desconfiança no mapeamento, use apenas meios verificáveis realmente fornecidos, como:

- nome;
- OAB;
- canal oficial;
- site;
- perfil institucional;
- endereço;
- CNPJ;
- contrato.

Não apresente a própria ligação como prova suficiente de legitimidade.

### 2. Enquadramento da consulta

Explique:

- o que será feito;
- o que pode ser concluído;
- o que pode depender de documento;
- quando haverá apresentação do serviço;
- quando haverá espaço para dúvidas.

Não use este bloco para vender antecipadamente.

### 3. Relato ou confirmação inicial

Retome o resumo existente.

Permita que a pessoa:

- confirme;
- corrija;
- acrescente;
- destaque o objetivo.

Não peça um relato completo do zero, salvo quando o resumo da triagem estiver ausente ou incorreto.

### 4. Organização e aprofundamento dos fatos

Investigue somente os elementos relevantes para o nicho:

- fato principal;
- linha do tempo;
- pessoas ou empresas envolvidas;
- comunicações;
- documentos;
- tentativas anteriores;
- respostas recebidas;
- consequências;
- situação atual.

As perguntas devem nascer do que foi dito.

### 5. Validação da viabilidade jurídica e pontos pendentes

Desenvolva, conforme o caso:

- requisitos confirmados;
- indícios favoráveis;
- pontos pendentes;
- contradições;
- impedimentos aparentes;
- documentos necessários;
- necessidade de cálculo, perícia ou análise complementar;
- possibilidade de prosseguir;
- ausência de viabilidade.

Este bloco não é qualificação comercial.

Não use linguagem de:

- lead aprovado;
- caso bom;
- caso forte como valor comercial;
- lead qualificado novamente;
- oportunidade.

### 6. Síntese

Organize o que foi compreendido.

Use estrutura semelhante:

> Vou reunir os pontos principais para confirmar se compreendi corretamente.

> Pelo que você me explicou, [FATO 1], depois [FATO 2], e hoje a situação está em [SITUAÇÃO]. É isso?

*Confirme.*

Diferencie:

- fato relatado;
- fato confirmado;
- elemento favorável;
- elemento desfavorável;
- dúvida;
- resultado ainda dependente de decisão.

### 7. Explicação jurídica

Explique:

- qual é o problema;
- qual lógica jurídica é pertinente;
- por que ela importa;
- o que altera a análise;
- como se relaciona aos fatos;
- quais documentos importam;
- quais caminhos existem;
- o que ainda não pode ser concluído.

Distribua em blocos.

Abra espaço para reação.

Não transforme a consulta em aula.

### 8. Aplicação ao cenário confirmado

Depois da explicação geral, aplique ao caso:

- fatos confirmados;
- documentos;
- datas;
- categoria;
- resposta anterior;
- situação atual.

Quando houver subperfis, use bifurcações.

Não aplique automaticamente o subperfil dominante da persona.

### 9. Documentos ou informações complementares

Quando faltar algo, explique:

- o que falta;
- por que importa;
- o que precisa demonstrar;
- como altera a análise;
- o que acontecerá depois.

Não apresente lista universal.

Não peça novamente documento já recebido.

### 10. Caminhos e limites

Mostre:

- o que pode ser buscado;
- quais alternativas existem;
- qual caminho parece pertinente;
- o que fortalece;
- o que dificulta;
- o que depende de terceiros;
- quais riscos permanecem;
- qual prazo verdadeiro precisa ser considerado, quando houver.

Não invente urgência.

Não apresente medida jurídica como livre escolha quando depender de análise técnica.

### 11. Funcionamento do serviço

Explique concretamente:

- o que o escritório fará;
- como organizará o caso;
- quais documentos analisará;
- quais etapas conduzirá;
- como reduzirá erros ou incertezas;
- como ocorrerá a comunicação;
- quais decisões ainda existirão;
- quais limites o serviço possui.

Demonstre valor pelo trabalho descrito.

Evite adjetivos vazios, como:

- excelente;
- completo;
- diferenciado;
- personalizado;
- especializado, quando não houver base ou posicionamento informado.

### 12. Participação real do cliente

Explique o que pode depender da pessoa, como:

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

### 13. Honorários e condições

Use somente quando o objetivo incluir contratação.

Apresente exatamente o modelo informado.

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

Não derive gratuidade da cobrança por êxito.

Não invente condições.

Use placeholders para dados exatos.

### 14. Dúvidas e objeções

Antes de pedir decisão, pergunte:

> Existe algum ponto da análise, do trabalho ou das condições que ainda precisa ficar mais claro?

*Aguarde.*

Quando surgir resistência:

1. investigue;
2. escute;
3. responda ao ponto real;
4. confirme;
5. retome.

Inclua apenas objeções pertinentes ao:

- nicho;
- recorte;
- serviço;
- momento;
- decisão solicitada.

### 15. Proposta

Quando houver elementos para apresentação responsável:

- sintetize;
- conecte o serviço ao problema;
- alinhe limites;
- apresente condições;
- explique a formalização.

Quando não houver elementos suficientes, não simule proposta.

### 16. Decisão

Quando o objetivo incluir contratação, use pergunta clara.

Exemplos:

> Diante do que analisamos e da forma de atuação que eu expliquei, faz sentido seguir com o escritório?

> Existe algum ponto que ainda impede você de tomar essa decisão agora?

> Posso organizar a formalização para iniciarmos?

Depois da pergunta:

- faça pausa;
- não preencha o silêncio;
- não trate silêncio como aceite.

### 17. Aceite, hesitação, recusa e próximos passos

#### Se houver aceite

Conduza, conforme o fluxo real, para:

- contrato;
- procuração;
- dados;
- documentos;
- pagamento;
- assinatura;
- canal de comunicação;
- início do trabalho.

Não elogie a decisão como vitória comercial.

Prefira confirmar e organizar a continuidade.

#### Se houver hesitação

Pergunte qual ponto ainda precisa ser avaliado.

Não responda a objeção presumida.

Use somente o procedimento autorizado pelo escritório.

Combine um próximo passo concreto quando isso fizer parte do fluxo.

#### Se houver recusa

Verifique uma vez se existe dúvida não tratada.

Persistindo a decisão:

- respeite;
- não pressione;
- não use medo;
- não use culpa;
- não invente urgência;
- encerre com clareza.

#### Se não houver elementos para proposta

Explique:

- o que ainda falta;
- por que impede a conclusão;
- qual documento ou informação é necessário;
- ou por que o caso não deve prosseguir.

Não simule fechamento.

#### Encerramento

A pessoa deve terminar sabendo:

- qual foi a conclusão possível;
- o que ainda depende de confirmação;
- qual é o próximo passo;
- quem fará cada ação;
- quais documentos serão necessários;
- por qual canal haverá comunicação;
- o que deve acontecer depois.

---

## Objeções e continuidades

Para cada objeção relevante, escreva a continuação completa.

Use esta progressão:

1. indicação da objeção;
2. pergunta do profissional;
3. pausa;
4. resposta substantiva;
5. confirmação;
6. retomada da decisão ou próximo passo.

Não exponha:

- medo subjacente;
- técnica utilizada;
- estratégia comercial;
- sinal interno de resolução.

Esses elementos pertencem ao playbook.

Não invente:

- vantagem sobre outro profissional;
- maior chance de êxito;
- frequência de reversão;
- resultado provável;
- condição comercial não informada.

---

## Adaptação ao canal

### Ligação

- use transições verbais claras;
- sinalize mudanças de assunto;
- permita perguntas;
- evite listas longas;
- confirme informações importantes;
- considere a ausência de reações visuais.

### Videoconferência

- preserve naturalidade;
- permita pausas;
- não inclua instruções corporais ou de câmera sem necessidade;
- use compartilhamento de documentos somente quando informado;
- não transforme a consulta em apresentação formal.

### Reunião presencial

- preserve oralidade;
- não transforme o roteiro em discurso;
- considere consulta a documentos;
- não presuma estrutura física, equipe ou material;
- mantenha falas adaptáveis.

---

## Formato da entrega

Entregue nesta ordem:

# 1. PREMISSAS E RECORTE

Bloco curto contendo:

- nicho;
- serviço;
- recorte;
- público;
- ponto de partida;
- ponto de encerramento;
- canal;
- condutor;
- informações herdadas da triagem;
- documentos já disponíveis;
- objetivo final;
- modelo de honorários, quando aplicável;
- pontos que exigem validação.

Não produza mapa psicológico.

Não repita o mapeamento.

# 2. ROTEIRO INTEGRAL

Esta deve ser a maior parte da saída.

Use títulos discretos.

Dentro deles, priorize:

- falas;
- perguntas;
- explicações;
- transições;
- pausas;
- checagens;
- continuidade.

Não exponha a arquitetura do playbook.

# 3. BIFURCAÇÕES ESSENCIAIS

Inclua somente os ramos que alterem substancialmente:

- investigação;
- enquadramento;
- explicação;
- documentos;
- caminho;
- risco;
- serviço;
- proposta;
- próximo passo.

Escreva as falas completas.

# 4. OBJEÇÕES DE CONTRATAÇÃO

Inclua somente as objeções relevantes.

Escreva:

- pergunta de investigação;
- pausa;
- resposta;
- confirmação;
- retomada.

# 5. ACEITE, HESITAÇÃO, RECUSA E PRÓXIMOS PASSOS

Escreva as continuidades completas.

# 6. PONTOS DE ADAPTAÇÃO

Lista curta com dados exatos e condições reais que precisam ser preenchidos ou validados.

Não inclua checklist operacional extenso.

---

## Revisão interna obrigatória

Antes de entregar, verifique silenciosamente:

### Produto e arquitetura

- a saída é um roteiro falado?
- a maior parte da entrega é formada por falas utilizáveis?
- o texto parece consulta, e não manual?
- as notas são mínimas?
- houve contaminação pelo formato de playbook?
- houve fluxo de WhatsApp indevido?
- o lead foi tratado como já triado e qualificado?
- alguma etapa refez qualificação comercial?
- triagem ou agendamento entraram indevidamente?

### Recorte e reutilização

- o recorte foi declarado?
- o conteúdo cobre exatamente esse recorte?
- o roteiro funciona com pessoas diferentes?
- alguma característica da persona virou fato?
- o subperfil dominante ocupou indevidamente o tronco comum?
- as bifurcações cobrem variações reais?
- algum exemplo de outro nicho contaminou a entrega?
- o roteiro poderia ser usado em outro nicho apenas trocando nomes? Se sim, aprofunde.

### Conversa e profundidade

- as perguntas estão conectadas?
- o profissional reage antes de avançar?
- as explicações centrais estão desenvolvidas?
- existem pausas entre informações importantes?
- houve monólogo excessivo?
- a profundidade foi distribuída?
- o profissional consegue falar sem parecer que lê uma apostila?
- as falas principais foram escritas ou substituídas por instruções?

### Segurança e não invenção

- foi presumida gratuidade?
- foi inventada condição comercial ou operacional?
- houve promessa de resultado?
- houve estatística, frequência de êxito ou superioridade não comprovada?
- foi criada urgência artificial?
- fatos, indícios, confirmações e resultado foram separados?
- quando houve análise suficiente, a conclusão foi clara?
- a cautela virou linguagem de parecer?
- documentos foram ligados ao que precisam confirmar?
- a participação do cliente foi descrita com realismo?

### Fechamento

- o fechamento corresponde ao objetivo?
- honorários e condições foram apresentados conforme dados reais?
- a proposta aparece apenas depois de compreensão suficiente?
- o aceite conduz ao fluxo real?
- a hesitação é investigada?
- a recusa é respeitada?
- a ausência de viabilidade não foi mascarada por fechamento artificial?

Corrija silenciosamente o que falhar.

---

## Critério de conclusão

O roteiro está pronto quando um profissional consegue:

1. compreender o recorte;
2. continuar a partir da triagem sem refazê-la;
3. conduzir a consulta com naturalidade;
4. aprofundar fatos relevantes;
5. validar a viabilidade jurídica;
6. explicar o Direito sem aula;
7. aplicar a explicação ao cenário;
8. apresentar concretamente o serviço;
9. explicar honorários reais;
10. tratar objeções;
11. pedir decisão;
12. conduzir aceite, hesitação, recusa ou ausência de proposta;
13. reutilizar o roteiro com pessoas diferentes dentro do recorte;
14. adaptar apenas fatos do cliente e particularidades reais do escritório.

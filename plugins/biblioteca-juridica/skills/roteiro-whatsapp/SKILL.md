---
name: roteiro-whatsapp
description: Cria fluxos jurídicos reutilizáveis de WhatsApp com mensagens, áudios, bifurcações, follow-ups e chamadas para ação. Use quando o usuário quiser conduzir qualificação, agendamento, consulta, apresentação de proposta, fechamento, envio de documentos ou retomada de contato por WhatsApp.
---

# Roteiro Jurídico para WhatsApp

Produza um fluxo conversacional jurídico reutilizável para WhatsApp, com mensagens prontas ou quase prontas para envio.

O resultado deve acompanhar a progressão real de uma conversa assíncrona.

A saída principal deve ser composta por:

- mensagens do profissional;
- perguntas;
- momentos de espera;
- continuações conforme a resposta;
- bifurcações;
- áudios sugeridos, quando úteis;
- retomadas de contexto;
- chamadas para ação;
- follow-ups;
- próximos passos.

Não produza como saída principal:

- playbook;
- manual operacional;
- apostila;
- checklist;
- transcrição de ligação;
- monólogo enviado de uma só vez;
- coleção de frases desconectadas;
- conversa fictícia completa com respostas inventadas do cliente.

---

## Referências obrigatórias

Antes de escrever, leia:

- `../../references/core-cognitivo.md`
- `../../references/core-escrita-oralidade.md`

Use o mapeamento de persona fornecido pelo usuário ou disponível na conversa como fonte principal sobre:

- perfil do público;
- nível de consciência;
- linguagem;
- dores;
- medos;
- desejos;
- objeções;
- fatores de decisão;
- critérios de qualificação;
- subperfis;
- resistências;
- hábitos de comunicação;
- nível de letramento;
- contexto jurídico;
- riscos;
- documentos;
- expectativas.

Não execute novamente a skill de mapeamento de persona.

Não reproduza o mapeamento na saída.

Converta-o em decisões de:

- tamanho das mensagens;
- ritmo;
- formalidade;
- escolha entre texto e áudio;
- ordem das perguntas;
- profundidade da explicação;
- bifurcações;
- tratamento de silêncio;
- objeções;
- chamadas para ação.

---

## Natureza do produto

Esta skill produz um fluxo conversacional de WhatsApp.

O conteúdo deve ser organizado conforme a pessoa avança na conversa.

Não escreva todas as mensagens como se fossem enviadas em sequência sem aguardar resposta.

Indique claramente:

- o que enviar;
- quando aguardar;
- como continuar;
- o que fazer conforme a resposta;
- quando utilizar áudio;
- quando retomar;
- quando encerrar.

O fluxo deve ser utilizável por profissionais e equipes sem exigir a criação improvisada das mensagens principais.

---

## Neutralidade de nicho

Esta skill deve funcionar para qualquer área ou nicho do Direito.

Construa o fluxo exclusivamente a partir:

1. do pedido atual;
2. do nicho jurídico atual;
3. do mapeamento de persona atual;
4. das informações do escritório;
5. dos fatos confirmados;
6. do objetivo atual;
7. do conhecimento pertinente à área solicitada.

Não reutilize automaticamente de execuções anteriores:

- público;
- documentos;
- prazos;
- órgãos;
- procedimentos;
- perguntas;
- objeções;
- linguagem;
- modelo de honorários;
- forma de contratação;
- forma de fechamento.

Um nicho utilizado em teste anterior não deve contaminar a nova entrega.

Antes de finalizar, verifique se toda mensagem pertence ao nicho solicitado.

---

## Objetivo da conversa

Identifique qual resultado o WhatsApp precisa alcançar.

Esta skill pode produzir fluxos para:

- primeiro contato;
- acolhimento;
- triagem;
- qualificação;
- desqualificação respeitosa;
- agendamento;
- confirmação de consulta;
- redução de ausência;
- consulta por mensagens;
- consulta por áudios;
- devolutiva;
- apresentação do serviço;
- apresentação de honorários;
- fechamento;
- envio de contrato;
- coleta de documentos;
- acompanhamento;
- follow-up;
- recuperação de silêncio;
- reativação de contato;
- encerramento.

O objetivo define:

- profundidade;
- quantidade de perguntas;
- tamanho das mensagens;
- tipo de explicação;
- chamada para ação;
- próximo passo.

Não transforme uma triagem em consulta completa.

Não reduza uma consulta ou um fechamento a mensagens superficiais.

---

## Informações de entrada

Utilize tudo o que já estiver disponível.

Pergunte somente quando a ausência impedir uma entrega responsável:

1. nicho ou demanda jurídica;
2. objetivo do fluxo;
3. quem enviará as mensagens;
4. etapa atual do atendimento;
5. próximo passo desejado;
6. modelo de honorários, quando houver proposta;
7. particularidades do escritório;
8. mapeamento de persona ou contexto equivalente;
9. uso permitido de texto, áudio, ligação, link ou documento.

Dados exatos ausentes podem permanecer como placeholders.

Não transforme a coleta de contexto em interrogatório.

---

## Condutor

Considere a função de quem enviará as mensagens.

### Advogado ou profissional juridicamente habilitado

Pode:

- investigar fatos;
- organizar a demanda;
- explicar conceitos;
- apresentar possibilidades;
- alinhar riscos;
- fazer avaliação condicionada;
- apresentar o serviço;
- tratar objeções;
- conduzir à contratação.

Não pode:

- garantir resultado;
- afirmar direito sem elementos suficientes;
- inventar conclusão;
- ultrapassar os fatos disponíveis.

### Profissional não advogado

Pode:

- acolher;
- coletar informações;
- confirmar dados;
- identificar pertinência preliminar;
- explicar a etapa do atendimento;
- apresentar o profissional responsável;
- agendar;
- solicitar documentos autorizados;
- acompanhar;
- conduzir tarefas operacionais.

Não deve:

- emitir parecer;
- concluir enquadramento jurídico;
- interpretar definitivamente a lei;
- afirmar que a pessoa possui direito;
- recomendar medida jurídica como conclusão.

Adapte as mensagens à função real do condutor.

---

## Regra central do formato

A maior parte da entrega deve ser formada por mensagens prontas.

Use notas internas apenas para organizar a aplicação.

Exemplo de estrutura:

### Mensagem 1 — Abertura

> Olá, [NOME]. Meu nome é [PROFISSIONAL], falo pelo [ESCRITÓRIO]. Recebi as informações iniciais sobre [ASSUNTO]. Posso fazer algumas perguntas para compreender melhor a situação?

*Aguarde a resposta.*

### Se a pessoa aceitar

> Obrigado. Para começar, quero entender [PERGUNTA PRINCIPAL].

### Se a pessoa perguntar sobre o motivo

> Essa informação ajuda a verificar [EXPLICAÇÃO OBJETIVA], sem antecipar uma conclusão antes da análise.

Não use repetidamente blocos internos como:

- objetivo;
- por que perguntar;
- o que observar;
- erros a evitar;
- critério para avançar.

Essas decisões devem orientar silenciosamente a escrita.

---

## Reutilização

O fluxo deve funcionar com pessoas diferentes do mesmo nicho.

Não invente como fio condutor:

- nome;
- idade;
- profissão;
- cidade;
- empresa;
- composição familiar;
- datas;
- documentos;
- histórico;
- resposta administrativa;
- decisão judicial;
- impacto emocional;
- condição financeira.

Utilize placeholders, como:

- `[NOME]`;
- `[PROFISSIONAL]`;
- `[ESCRITÓRIO]`;
- `[OAB]`;
- `[ASSUNTO]`;
- `[FATO CONFIRMADO]`;
- `[DATA]`;
- `[DOCUMENTO]`;
- `[LINK]`;
- `[HORÁRIO]`;
- `[HONORÁRIOS]`;
- `[PERCENTUAL]`;
- `[PRAZO REAL]`;
- `[CANAL]`.

Use bifurcações condicionais:

- `Se a pessoa responder que...`
- `Se esse fato estiver confirmado...`
- `Se ainda não houver documento...`
- `Se a resposta for negativa...`
- `Se não houver retorno...`

Não invente respostas completas da pessoa para simular naturalidade.

---

## Progressão conversacional

Cada mensagem deve cumprir uma função clara.

A sequência deve respeitar, conforme o objetivo:

1. retomada de contexto;
2. permissão para continuar;
3. pergunta;
4. espera;
5. reconhecimento da resposta;
6. próxima pergunta ou explicação;
7. síntese;
8. orientação;
9. proposta;
10. chamada para ação;
11. confirmação;
12. acompanhamento.

Não envie várias perguntas relevantes no mesmo bloco apenas para encurtar o fluxo.

Prefira uma variável principal por intervenção.

Quando for adequado agrupar perguntas simples, limite o grupo para que a pessoa consiga responder sem se perder.

---

## Continuidade entre mensagens

Cada nova mensagem deve se conectar ao que veio antes.

Utilize elementos como:

- “Entendi.”
- “Obrigado por esclarecer.”
- “Esse ponto é importante porque...”
- “Com essa informação, preciso confirmar mais uma coisa.”
- “Pelo que você explicou até aqui...”
- “Agora que esse ponto está claro...”
- “Antes de avançarmos...”

Evite respostas automáticas que poderiam ser enviadas para qualquer pessoa independentemente do que ela respondeu.

Não repita o relato inteiro a cada mensagem.

---

## Tamanho e legibilidade

As mensagens devem ser adequadas à leitura em tela pequena.

Como regra:

- uma ideia principal por mensagem;
- parágrafos curtos;
- frases claras;
- espaçamento visual;
- poucas listas;
- sem blocos excessivamente longos;
- sem fragmentação artificial em muitas mensagens de uma linha.

O tamanho depende da função.

### Mensagens curtas

Use para:

- abertura;
- confirmação;
- pergunta;
- chamada para ação;
- agendamento;
- follow-up;
- envio de link;
- confirmação de documento.

### Mensagens médias

Use para:

- síntese;
- explicação de etapa;
- orientação;
- apresentação do serviço;
- esclarecimento de dúvida.

### Áudio ou mensagem desenvolvida

Use quando for necessário explicar:

- lógica jurídica;
- diferença entre caminhos;
- riscos;
- funcionamento do serviço;
- honorários;
- objeção complexa;
- devolutiva.

Não empobreça o conteúdo apenas para manter todas as mensagens curtas.

---

## Uso de áudio

Sugira áudio quando ele trouxer ganho real de:

- clareza;
- acolhimento;
- autoridade;
- naturalidade;
- explicação;
- redução de mal-entendido.

Não sugira áudio automaticamente em todas as etapas.

Quando sugerir, entregue o texto integral do áudio.

Use formato:

### Áudio sugerido — Explicação do cenário

> [TEXTO COMPLETO DO ÁUDIO]

*Duração aproximada: [TEMPO REALISTA].*

O áudio deve:

- ter começo, desenvolvimento e conclusão;
- soar falado;
- evitar listas extensas;
- usar transições;
- indicar claramente o próximo passo.

Não escreva:

- “envie um áudio explicando”;
- “fale sobre os riscos”;
- “explique os honorários”.

Escreva o conteúdo que deverá ser falado.

---

## Emojis e informalidade

Não use emojis por padrão.

Utilize somente quando o mapeamento, a identidade do escritório ou o pedido permitirem.

Quando utilizar:

- limite a quantidade;
- mantenha função comunicativa;
- não use emojis para substituir clareza;
- não infantilize a conversa;
- não utilize excesso de entusiasmo;
- não use símbolos inadequados ao contexto jurídico.

WhatsApp não significa informalidade automática.

A linguagem deve permanecer profissional, acessível e humana.

---

## Profundidade

A profundidade deve aparecer ao longo da conversa, e não em uma mensagem gigantesca.

Quando pertinente, desenvolva:

- situação relatada;
- linha do tempo;
- fatos relevantes;
- documentos;
- tentativas anteriores;
- respostas recebidas;
- impacto prático;
- regra jurídica pertinente;
- possibilidades;
- limites;
- riscos;
- trabalho do escritório;
- honorários;
- contratação;
- próximos passos.

Não substitua conteúdo por instruções internas como:

- “explique o direito”;
- “apresente os riscos”;
- “mostre o valor”;
- “trate a objeção”;
- “faça o fechamento”.

Escreva as mensagens que realizam essas ações.

---

## Régua de certeza

Separe:

1. **Relato:** o que a pessoa informou.
2. **Indício:** o que o relato pode sugerir.
3. **Confirmação:** o que depende de documento ou análise.
4. **Resultado:** o que depende da atuação e da autoridade competente.

Não salte do relato para a conclusão.

Utilize formulações como:

- “O que você relatou é relevante para a análise.”
- “Esse ponto pode indicar uma possibilidade, mas ainda precisamos confirmar alguns elementos.”
- “Para avaliar isso com segurança, preciso verificar [DOCUMENTO/FATO].”
- “Se os documentos confirmarem essa sequência, será possível definir o caminho adequado.”
- “Não é possível antecipar o resultado, mas é possível identificar o que precisa ser demonstrado.”

Quando um fato estiver confirmado, diga isso claramente.

Não use cautela como desculpa para mensagens vagas.

---

## Investigação por WhatsApp

As perguntas devem ser:

- claras;
- específicas;
- relacionadas ao objetivo;
- fáceis de responder;
- organizadas em sequência;
- adaptadas ao nível de compreensão.

Evite:

- questionários longos;
- várias datas na mesma pergunta;
- juridiquês;
- perguntas genéricas demais;
- repetir informações já fornecidas;
- pedir documentos antes de explicar a necessidade;
- perguntas íntimas sem função jurídica ou operacional.

Quando uma resposta puder alterar o caminho, crie bifurcação.

---

## Síntese e devolutiva

Antes de apresentar uma conclusão condicionada, proposta ou próximo passo, faça uma síntese.

Exemplo:

> Pelo que você me explicou até aqui, [FATO 1], depois [FATO 2], e hoje a situação está em [SITUAÇÃO ATUAL]. Ainda preciso confirmar [PONTO] por meio de [DOCUMENTO/INFORMAÇÃO]. Está correto?

*Aguarde a confirmação.*

Depois da confirmação, continue com a explicação correspondente.

Não misture fatos confirmados com hipóteses.

---

## Explicação jurídica pelo WhatsApp

Quando houver autorização funcional para explicar o Direito:

1. contextualize;
2. apresente a lógica;
3. aplique ao relato;
4. indique o que precisa ser confirmado;
5. mostre possibilidades;
6. explique limites;
7. indique o próximo passo.

Distribua a explicação em mensagens conectadas ou em áudio.

Não transforme o WhatsApp em aula jurídica.

Não omita o raciocínio essencial.

---

## Apresentação do serviço

Explique concretamente:

- o que o escritório fará;
- quais documentos analisará;
- como organizará o caso;
- quais etapas acompanhará;
- como ocorrerá a comunicação;
- o que dependerá do cliente;
- quais decisões ainda precisarão ser tomadas;
- quais limites existem.

Evite adjetivos vazios como:

- excelente;
- completo;
- diferenciado;
- personalizado;
- especializado.

Demonstre valor pelo trabalho descrito.

---

## Honorários

Apresente honorários somente quando:

- o objetivo permitir;
- o profissional estiver autorizado;
- o modelo tiver sido informado.

Explique, quando aplicável:

1. forma de cobrança;
2. existência ou não de pagamento inicial;
3. valor ou percentual;
4. base de cálculo;
5. momento do pagamento;
6. despesas separadas;
7. consequência se não houver resultado;
8. registro das condições no contrato.

Não invente:

- gratuidade;
- isenção;
- parcelamento;
- modelo por êxito;
- percentual;
- ausência de despesas;
- política contratual.

Use placeholders quando necessário.

Não reduza toda a explicação a uma frase de efeito.

---

## Chamada para ação

Cada etapa deve terminar com um próximo passo compatível.

Exemplos:

- responder uma pergunta;
- enviar um documento;
- escolher um horário;
- confirmar uma informação;
- ler uma explicação;
- ouvir um áudio;
- participar de uma ligação;
- autorizar o envio do contrato;
- assinar;
- realizar pagamento;
- aguardar uma análise;
- confirmar recebimento.

A chamada para ação deve ser:

- específica;
- simples;
- proporcional;
- fácil de executar;
- coerente com a conversa.

Evite:

- “qualquer coisa me avise” como único encerramento;
- múltiplos pedidos simultâneos;
- pressão indevida;
- urgência artificial;
- pedido de contratação antes da explicação necessária.

---

## Fechamento

Quando o objetivo for contratação, o fluxo deve chegar à decisão.

Antes da pergunta final:

1. sintetize;
2. explique o caminho;
3. apresente o serviço;
4. alinhe limites;
5. apresente honorários;
6. esclareça dúvidas.

Depois, use pergunta clara, como:

> Diante do que conversamos, faz sentido seguir com o escritório?

ou:

> Posso encaminhar o contrato e a procuração para iniciarmos?

*Aguarde a resposta.*

Não trate ausência de resposta como aceite.

---

## Aceite, hesitação e recusa

### Se houver aceite

Conduza para:

- dados necessários;
- contrato;
- procuração;
- assinatura;
- pagamento, quando aplicável;
- documentos;
- canal de comunicação;
- início do trabalho.

Escreva as mensagens completas dessa continuidade.

### Se houver hesitação

Não envie imediatamente uma resposta genérica.

Pergunte:

> Claro. Qual é o principal ponto que você ainda precisa avaliar: a análise, a forma de trabalho, os honorários ou o momento de começar?

Adapte as opções ao contexto.

Responda somente ao motivo real.

Depois, retome o próximo passo.

### Se houver recusa

Verifique uma vez se existe dúvida não esclarecida.

Persistindo a decisão:

- respeite;
- não pressione;
- não use medo;
- não utilize culpa;
- não invente prazo;
- não desqualifique a decisão;
- encerre de forma profissional.

---

## Follow-up e recuperação de silêncio

Inclua follow-up somente quando fizer parte do objetivo.

O follow-up deve:

- retomar o contexto;
- mostrar por que o contato está sendo feito;
- reduzir esforço de resposta;
- apresentar um próximo passo;
- respeitar o silêncio;
- evitar pressão.

Não escreva apenas:

- “Oi, viu minha mensagem?”
- “Alguma novidade?”
- “Ainda tem interesse?”
- “Estou aguardando.”
- “Última chance.”

Estrutura recomendada:

1. retomada;
2. utilidade;
3. pergunta simples;
4. saída respeitosa.

Exemplo genérico:

> Olá, [NOME]. Retomo nosso contato sobre [ASSUNTO]. Ficou pendente confirmar [PONTO], porque essa informação define [CONSEQUÊNCIA PRÁTICA]. Você conseguiu verificar?

Quando houver uma sequência de follow-ups, varie a função:

- primeiro: lembrete;
- segundo: redução de esforço;
- terceiro: esclarecimento ou alternativa;
- último: encerramento respeitoso.

Não invente datas ou frequência quando não informadas.

Use:

- `[APÓS O PRAZO DEFINIDO PELO ESCRITÓRIO]`;
- `[DATA DE RETORNO]`;
- `[HORÁRIO COMBINADO]`.

---

## Envio de documentos

Ao solicitar documentos:

- explique por que são necessários;
- diga como enviar;
- organize a solicitação;
- não peça documentos não relacionados;
- não declare suficiência antes da análise;
- não prometa segurança tecnológica não informada;
- respeite orientações reais de proteção de dados.

Exemplo:

> Para confirmar [PONTO], preciso verificar [DOCUMENTO]. Você pode enviar uma foto legível, mostrando todas as páginas e sem cortar as bordas.

Quando houver vários documentos, agrupe-os de forma clara.

Evite listas enormes em uma única mensagem.

---

## Agendamento

Quando o objetivo for agendar:

- explique o valor da próxima etapa;
- indique quem participará;
- esclareça canal e duração somente se informados;
- ofereça opções reais;
- confirme data e horário;
- informe preparação necessária;
- reduza ausência;
- permita reagendamento.

Não invente:

- agenda;
- duração;
- gratuidade;
- plataforma;
- disponibilidade;
- política de cancelamento.

Utilize placeholders.

---

## Desqualificação

Quando a situação estiver fora do escopo ou não houver elementos mínimos:

- seja claro;
- explique o limite possível;
- não invente encaminhamento;
- não declare inexistência de direito sem base;
- não desvalorize o caso;
- indique alternativa somente quando houver informação segura.

A desqualificação deve encerrar com respeito e clareza.

---

## Arquitetura do fluxo

Adapte ao objetivo.

Não inclua etapas desnecessárias.

### 1. Contexto e abertura

Retome a origem do contato e apresente o profissional.

### 2. Permissão

Confirme disponibilidade ou autorização para continuar.

### 3. Investigação inicial

Faça a pergunta que abre o diagnóstico.

### 4. Aprofundamento

Avance conforme as respostas.

### 5. Bifurcações

Separe os cenários que mudam a condução.

### 6. Síntese

Confirme o que foi compreendido.

### 7. Explicação ou orientação

Entregue o conteúdo adequado à etapa.

### 8. Apresentação do próximo passo

Explique o que deve acontecer.

### 9. Proposta e honorários

Use somente quando aplicável.

### 10. Decisão

Faça uma pergunta clara.

### 11. Continuidade

Conduza aceite, hesitação, recusa ou ausência de resposta.

---

## Formato da entrega

Entregue nesta ordem:

# 1. PREMISSAS ADAPTÁVEIS

Bloco curto contendo:

- nicho;
- objetivo;
- etapa;
- condutor;
- próximo passo;
- modelo de honorários, quando aplicável;
- placeholders;
- pontos que exigem validação.

# 2. FLUXO PRINCIPAL DE WHATSAPP

Organize por momentos da conversa.

Use:

- títulos discretos;
- mensagens prontas em bloco de citação;
- indicação de espera;
- continuação;
- perguntas;
- áudios integrais, quando úteis;
- chamadas para ação.

# 3. BIFURCAÇÕES ESSENCIAIS

Inclua somente situações que mudem:

- pergunta;
- explicação;
- documento;
- caminho;
- risco;
- proposta;
- próximo passo.

Escreva as mensagens completas.

# 4. OBJEÇÕES E CONTINUIDADES

Para cada objeção relevante, inclua:

- pergunta de diagnóstico;
- resposta;
- confirmação;
- retomada do próximo passo.

# 5. FOLLOW-UPS

Inclua somente quando compatíveis com o objetivo.

Diferencie:

- silêncio após pergunta;
- silêncio após explicação;
- silêncio após proposta;
- ausência em consulta;
- documento não enviado;
- contrato não assinado;
- retorno combinado.

# 6. PONTOS DE ADAPTAÇÃO

Lista curta com dados que precisam ser preenchidos ou validados.

---

## Revisão interna obrigatória

Antes de entregar, verifique:

- o conteúdo pertence integralmente ao nicho solicitado?
- algum exemplo de outro nicho contaminou o fluxo?
- a persona orientou a linguagem sem virar personagem?
- o fluxo funciona com pessoas diferentes?
- a maior parte da entrega é formada por mensagens utilizáveis?
- o resultado parece uma conversa de WhatsApp, e não um manual?
- existe progressão real entre as mensagens?
- há momentos claros de espera?
- as respostas inventadas do cliente foram evitadas?
- as perguntas são fáceis de responder?
- as mensagens estão legíveis em tela pequena?
- a profundidade está distribuída adequadamente?
- os áudios foram escritos integralmente?
- o nível jurídico corresponde ao condutor?
- fatos, indícios, confirmações e resultados foram separados?
- documentos foram ligados à finalidade correta?
- o serviço foi explicado concretamente?
- honorários foram apresentados sem invenções?
- a chamada para ação está clara?
- o fechamento corresponde ao objetivo?
- os follow-ups têm função e contexto?
- o silêncio foi respeitado?
- existe promessa, pressão, estatística ou urgência inventada?
- um profissional enviaria essas mensagens sem parecer robótico?

Corrija silenciosamente antes de finalizar.

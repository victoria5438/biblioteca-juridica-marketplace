# REFERÊNCIA — ROTEIROS DE CRIATIVOS JURÍDICOS

## Função

Este arquivo define o método estratégico para transformar um Mapeamento de Persona Jurídica em conceitos e roteiros de vídeos para Meta Ads.

Ele é uma referência local da skill `/roteiros-criativos-juridicos` e deve ficar em:

```text
skills/roteiros-criativos-juridicos/references/roteiros-criativos-juridicos.md
```

O executor deve acessá-lo pelo caminho:

```text
${CLAUDE_PLUGIN_ROOT}/references/roteiros-criativos-juridicos.md
```

Ele deve ser lido junto com:

- `${CLAUDE_PLUGIN_ROOT}/references/core-cognitivo.md`;
- `${CLAUDE_PLUGIN_ROOT}/references/core-escrita-oralidade.md`;
- o Mapeamento de Persona Jurídica específico da execução;
- o `SKILL.md` de `roteiros-criativos-juridicos`.

O Mapeamento da execução é um documento-fonte dinâmico fornecido pelo usuário ou disponível na conversa. Ele não deve ser substituído pelo arquivo estrutural `mapeamento-persona-v3.md`.

A referência não substitui o executor nem o Mapeamento. Ela detalha:

- diagnóstico do serviço;
- leitura da persona para mídia paga;
- extração de situações e dores;
- construção de ângulos;
- seleção;
- escrita;
- diversidade;
- autorrevisão.

---

# 1. DEPENDÊNCIA DO MAPEAMENTO DE PERSONA

A skill é independente como comando, mas dependente do Mapeamento como base estratégica.

Fluxo:

> `/mapear-persona`  
> → Mapeamento de Persona Jurídica específico  
> → `/roteiros-criativos-juridicos`  
> → diagnóstico de campanha, ângulos e roteiros

Não execute novamente `/mapear-persona` dentro desta skill.

Não use o arquivo estrutural `mapeamento-persona-v3.md` como se ele contivesse a persona da execução.

## 1.1. Quando o Mapeamento estiver disponível

Extraia dele apenas o que for necessário para a campanha:

- recorte;
- serviço;
- mecanismo de valor;
- situações objetivas;
- subperfis;
- aderência;
- complexidade;
- maturidade;
- linguagem;
- dores;
- dúvidas;
- decisões;
- objeções;
- consciência;
- riscos;
- limites;
- insumos da Seção 10.

Não reproduza o documento inteiro.

## 1.2. Quando o Mapeamento estiver ausente

Solicite o documento.

Somente prossiga com matéria-prima equivalente quando ela permitir reconstruir com segurança as decisões estratégicas da campanha.

A matéria-prima mínima deve conter:

- natureza e delimitação do serviço;
- público e subperfis;
- situações de aderência;
- fatores de complexidade;
- dores, dúvidas, decisões e objeções;
- níveis de consciência;
- mecanismo de valor;
- limites jurídicos e éticos;
- anti-persona;
- objetivo e CTA.

Não invente lacunas estruturais.

---

# 2. PRINCÍPIO CENTRAL

Um criativo jurídico eficaz não nasce de uma dor genérica nem de uma regra solta.

Ele nasce do encontro entre:

1. uma situação concreta em que a pessoa se reconhece;
2. uma dúvida ou decisão relevante;
3. uma consequência compreensível;
4. um insight que altera a percepção;
5. um mecanismo de valor que explica por que a análise profissional é útil;
6. um CTA compatível com a etapa da jornada.

Estrutura mental:

> situação reconhecível  
> → dúvida  
> → tensão  
> → insight  
> → relevância do serviço  
> → convite

O roteiro não deve depender apenas de:

- medo;
- curiosidade vazia;
- promessa;
- autoridade genérica;
- “você pode ter direito” sem contexto;
- “cada caso é um caso” sem explicação;
- “procure um advogado” sem mecanismo de valor.

---

# 3. O DIAGNÓSTICO VEM ANTES DA COPY

Antes de criar um gancho, responda:

- qual é o serviço?
- que decisão ou problema ele organiza?
- o que o profissional efetivamente faz?
- por que uma informação genérica não basta?
- qual situação objetiva faz a pessoa precisar dessa análise?
- que erro ou incerteza ela deseja evitar?
- em que estágio ela está?
- qual ação a campanha deseja gerar?

Se essas respostas não estiverem claras, o roteiro será genérico.

## 3.1. Fidelidade aos inputs

Antes do diagnóstico, monte internamente uma ficha de execução:

| Campo | Valor fornecido | Pode receber premissa? |
|---|---|---|
| Quantidade |  | somente se ausente |
| Duração |  | somente se ausente |
| Formato |  | somente se ausente |
| Canal |  | somente se ausente |
| Público/recorte |  | somente se ausente |
| Objetivo |  | somente se ausente |
| Etapa do funil |  | somente se ausente |
| Tom |  | somente se ausente |
| CTA |  | somente se ausente |
| Restrições |  | não |
| Informações validadas |  | não |

Regra:

> dado fornecido não é premissa.

Não reinterprete um tom informado como se fosse sugestão da skill.

Não substitua CTA real por placeholder quando ele já foi fornecido.

Não aumente ou reduza a quantidade para “equilibrar” a campanha.

Não altere duração ou formato para acomodar uma preferência metodológica.

Se houver conflito ético, jurídico ou técnico, sinalize-o e proponha ajuste. Não corrija silenciosamente.

---

# 4. ENTENDIMENTO DO SERVIÇO

## 4.1. Natureza

Classifique o serviço como:

- reconhecimento, concessão, revisão, reparação, cobrança ou indenização;
- defesa;
- consultoria, prevenção, planejamento ou estruturação;
- híbrido.

Essa classificação altera o criativo.

### Reconhecimento ou concessão

O anúncio pode explorar:

- requisitos ignorados;
- situação que parece comum, mas pode ter relevância jurídica;
- diferença entre estar incapaz e ter redução;
- direito não concedido automaticamente;
- prazo ou perda real, quando confirmados.

Não deve afirmar que o público tem o direito.

### Defesa

O anúncio pode explorar:

- prazo;
- risco concreto;
- consequência de não agir;
- necessidade de entender acusação, cobrança, bloqueio, processo ou medida.

Não deve presumir culpa da outra parte nem resultado defensivo.

### Consultoria e planejamento

O anúncio pode explorar:

- decisões irreversíveis;
- alternativas que precisam ser comparadas;
- informação genérica insuficiente;
- custo do erro;
- benefício da clareza e do planejamento.

Não deve inventar um “direito à consultoria”.

### Híbrido

Delimite qual camada está sendo anunciada.

Não misture consulta, concessão, defesa e execução numa peça curta sem necessidade.

---

## 4.2. Mecanismo de valor

O mecanismo de valor explica o que o profissional faz entre o problema e o resultado desejado.

Use verbos concretos:

- analisar;
- comparar;
- confirmar;
- calcular;
- organizar;
- reconstruir;
- identificar;
- enquadrar;
- revisar;
- documentar;
- negociar;
- defender;
- requerer;
- impugnar;
- planejar.

Evite verbos vazios:

- ajudar;
- resolver;
- cuidar;
- buscar seus direitos;
- lutar por você;

quando não vierem acompanhados do trabalho efetivo.

Exemplo genérico insuficiente:

> Um advogado pode ajudar você.

Exemplo com mecanismo:

> A análise compara seu histórico, as regras aplicáveis e os cenários possíveis antes de você escolher uma data.

---

## 4.3. Resultado comunicável

Diferencie:

### Entrega profissional

Pode ser afirmada quando real:

- diagnóstico;
- parecer;
- simulação;
- comparação;
- revisão;
- organização documental;
- protocolo;
- acompanhamento;
- negociação;
- defesa;
- estratégia.

### Possível resultado jurídico

Deve ser condicionado:

- concessão;
- revisão;
- redução;
- indenização;
- reconhecimento;
- anulação;
- recuperação;
- aposentadoria;
- acordo.

### Benefício percebido

Pode ser comunicado sem prometer o resultado:

- clareza;
- segurança para decidir;
- compreensão;
- organização;
- redução de incerteza;
- prevenção de erro;
- conhecimento dos caminhos.

---

# 5. LEITURA DA PERSONA PARA CRIATIVOS

## 5.1. Perfil

Perfil orienta forma, não define automaticamente a relevância jurídica.

Pode orientar:

- vocabulário;
- ambiente de gravação;
- velocidade;
- exemplos;
- formalidade;
- duração;
- necessidade de tradução.

Não use automaticamente como filtro:

- idade predominante;
- profissão predominante;
- renda;
- escolaridade;
- cidade;
- estado civil;
- rotina;
- emoção provável.

Use essas informações como recorte somente quando:

- o usuário restringir a campanha;
- forem inerentes ao serviço;
- forem necessárias para a situação objetiva do criativo.

---

## 5.2. Aderência

Aderência responde:

> Qual é o núcleo mínimo que torna este serviço pertinente?

Teste de ausência:

> Se este elemento não existir, o serviço deixa de ser pertinente?

Exemplos abstratos:

- sofreu o fato central e permaneceu com consequência relevante;
- recebeu uma negativa relacionada ao serviço;
- está sendo cobrado ou executado;
- possui decisão consultiva relevante em aberto;
- está diante da relação, vínculo ou situação abrangida;
- reúne requisitos materiais preliminares do direito analisado.

Não classifique como aderência apenas porque o elemento gera um bom anúncio.

Em regra, não são aderência por si sós:

- estar perto de uma data;
- possuir renda mais alta;
- ter ou não ter determinado documento;
- pertencer a subcategoria específica;
- possuir múltiplos vínculos;
- demonstrar interesse;
- estar pronto para contratar;
- ter urgência;
- apresentar maior potencial econômico.

O criativo de aquisição deve conter marcador suficiente para evitar atrair público incompatível, mas nem todo marcador do gancho precisa ser o núcleo de aderência.

---

## 5.3. Complexidade

Complexidade responde:

> O que torna a análise individual mais valiosa ou necessária?

Pode envolver:

- vários vínculos;
- mais de uma regra;
- documentos contraditórios;
- histórico longo;
- datas diferentes;
- categoria especial;
- legislação local;
- risco probatório;
- valor elevado;
- múltiplas partes;
- fase processual;
- decisão anterior;
- interação entre regimes;
- alternativas que não podem ser avaliadas por conteúdo genérico.

Não transforme complexidade em requisito quando casos simples também são atendidos.

---

## 5.4. Maturidade

Maturidade responde:

> Quanto a pessoa já reconhece o problema, a solução e a necessidade de agir?

Ela orienta o tipo de criativo:

| Nível | Função do criativo |
|---|---|
| Inconsciência | revelar uma situação que a pessoa ainda normaliza |
| Consciência da situação | nomear a dúvida, risco ou consequência |
| Consciência da solução | explicar por que existe um caminho profissional |
| Consideração | demonstrar método, especificidade e segurança |
| Decisão | reduzir fricção e tornar o próximo passo claro |

Não confunda maturidade com aderência.

## 5.5. Subperfil, prioridade, prova e potencial comercial

### Subperfil

Muda o recorte da mensagem:

- ente;
- categoria;
- data de ingresso;
- histórico;
- estágio;
- objeção;
- regime;
- tipo de vínculo.

### Prioridade

Muda a velocidade recomendada, não a pertinência do serviço.

### Prova

Muda a capacidade de confirmar fatos. Falta de prova atual não equivale automaticamente a falta de aderência.

### Potencial comercial

Pode influenciar a estratégia de aquisição ou a oferta, mas não deve ser apresentado como qualificação jurídica.

### Regra de classificação

| Dimensão | Pergunta de controle |
|---|---|
| Aderência | Sem isso, o serviço deixa de ser pertinente? |
| Complexidade | Sem isso, o caso continua pertinente, porém mais simples? |
| Subperfil | Isso muda para quem ou como o anúncio fala? |
| Maturidade | Isso muda o nível de consciência, a objeção ou o CTA? |
| Prioridade | Isso muda a velocidade recomendada? |
| Prova | Isso confirma um fato já relatado? |
| Potencial comercial | Isso altera estratégia comercial sem alterar a pertinência jurídica? |

---

# 6. EXTRAÇÃO DAS DORES EXPLORÁVEIS

## 6.1. Unidade de criação

A unidade mínima de criação é:

> uma situação objetiva + uma dúvida + uma tensão + uma decisão.

Exemplo:

| Situação | Dúvida | Tensão | Decisão |
|---|---|---|---|
| Tempo em dois regimes | “Posso usar os dois?” | Perder uma alternativa ou averbar sem comparar | Averbar ou preservar |
| Benefício cessado com sequela | “Acabou tudo?” | Continuar trabalhando sem conhecer o possível benefício | Pedir análise |
| Contrato bancário crescente | “Por que a dívida não diminui?” | Continuar pagando sem entender cálculo | Revisar contrato |
| Citação recebida | “O que acontece se eu ignorar?” | Perder prazo ou sofrer medida | Buscar defesa |

---

## 6.2. Camadas da dor

Para cada situação, examine:

1. **dor consciente** — o que a pessoa já fala;
2. **dúvida** — o que ela quer entender;
3. **medo** — o que teme acontecer;
4. **perda percebida** — dinheiro, tempo, autonomia, patrimônio, oportunidade;
5. **desejo** — clareza, proteção, recebimento, encerramento, decisão;
6. **crença** — explicação simplificada ou equivocada;
7. **decisão** — o que ainda não sabe fazer.

Não use uma dor emocional se não houver conexão com a situação objetiva.

---

## 6.3. Pergunta de interrupção

Uma boa pergunta de gancho:

- é reconhecível;
- contém uma variável real;
- não exige conhecimento jurídico;
- desperta uma lacuna;
- conduz ao serviço;
- pode ser respondida mentalmente;
- não promete.

Exemplo fraco:

> Você sabe tudo sobre sua aposentadoria?

Exemplo forte:

> Você trabalhou no INSS antes de entrar no serviço público e ainda não decidiu se vai averbar esse tempo?

---

# 7. MATRIZ DE ÂNGULOS

Use esta estrutura:

| ID | Ângulo principal | Situação objetiva | Classificação do marcador | Subpersona | Nível de consciência | Dor ou decisão | Pergunta central | Insight | Mecanismo de valor | Promessa permitida | Cuidado jurídico | Risco de generalização | Formato | Função na campanha |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|

## 7.1. Tipos de ângulo

Varie entre:

### Identificação

A pessoa se reconhece numa situação.

### Dúvida específica

O criativo parte de uma pergunta real.

### Erro ou crença

Mostra por que uma ideia comum é incompleta.

### Escolha ou comparação

Apresenta duas alternativas que exigem análise.

### Consequência

Mostra o impacto possível de uma decisão.

### Oportunidade ignorada

Apresenta um caminho ou fator que a pessoa não considerava.

### Processo ou método

Explica como a análise profissional organiza o caso.

### Objeção

Responde a uma resistência relevante.

### Prova de especificidade

Demonstra domínio do ente, categoria ou situação, sem autopromoção exagerada.

Não use todos os tipos em toda campanha.

---

## 7.2. Promessa comunicacional permitida

A promessa comunicacional não é promessa de êxito.

É o benefício que o conteúdo e o serviço podem legitimamente oferecer.

Exemplos:

- entender quais fatores alteram a análise;
- comparar cenários antes de decidir;
- identificar documentos necessários;
- verificar se uma situação merece análise;
- organizar uma linha do tempo;
- compreender o próximo passo;
- evitar decidir com base apenas em informação genérica.

---

# 8. SELEÇÃO DOS CONCEITOS

Avalie cada ângulo em:

- identificação;
- aderência;
- relevância;
- clareza;
- diferenciação;
- segurança;
- compatibilidade com o tempo;
- força do mecanismo;
- adequação ao CTA.

Não é necessário atribuir nota numérica, salvo pedido.

## 8.1. Portfólio equilibrado

Uma campanha pode combinar:

- 1 ou 2 criativos de identificação;
- 1 criativo de dúvida;
- 1 de quebra de crença;
- 1 de método ou consideração.

A composição depende do objetivo.

Não force essa distribuição quando a campanha tiver outro desenho.

---

# 9. ESTRUTURA DOS ROTEIROS

## 9.1. Ficha estratégica

Antes da fala, registre:

```text
Título interno:
Público específico:
Situação:
Nível de consciência:
Objetivo:
Ângulo:
Dúvida central:
Insight:
Mecanismo de valor:
Promessa permitida:
Cuidado jurídico:
Formato:
Duração:
CTA:
```

---

## 9.2. Gancho

O gancho deve:

- abrir a situação;
- criar reconhecimento;
- apresentar dúvida, contraste ou consequência;
- ser compreensível sem contexto anterior;
- corresponder ao conteúdo seguinte.

Modelos de construção:

### Situação + pergunta

> Você trabalhou na iniciativa privada antes de assumir um cargo público?

### Escolha

> Averbar todo o seu tempo no INSS pode parecer óbvio. Mas essa nem sempre é uma decisão automática.

### Contraste

> Cumprir os requisitos para se aposentar não significa que aquela seja a melhor data para fazer isso.

### Erro

> Comparar a sua aposentadoria com a de um colega pode levar você à regra errada.

### Microcenário

> Dois servidores do mesmo órgão podem se aposentar em datas próximas e receber valores diferentes.

### Consequência condicionada

> Uma data escolhida sem comparar as regras pode afetar o valor do benefício por muitos anos.

Não use consequência como certeza sobre o caso individual.

---

## 9.3. Desenvolvimento

O desenvolvimento deve:

1. explicar a dúvida;
2. mostrar as variáveis que alteram a resposta;
3. quebrar a crença;
4. ligar ao mecanismo de valor.

Evite:

- história legislativa;
- enumeração de artigos;
- sete requisitos falados em sequência;
- várias teses num vídeo;
- aula completa;
- repetição do gancho.

---

## 9.4. Quebra de crença

A quebra de crença deve ser verdadeira e útil.

Exemplos abstratos:

- voltar ao trabalho não elimina necessariamente toda proteção;
- cumprir uma regra não significa que ela seja a melhor;
- ausência de um documento hoje não significa ausência do direito;
- regra federal não é automaticamente regra estadual;
- uma negativa não encerra automaticamente todas as possibilidades;
- ter interesse não confirma aderência.

Não use frases absolutas quando houver exceções.

---

## 9.5. Mecanismo de valor

Não encerre com:

> cada caso é um caso.

Explique por quê.

Exemplo:

> Para responder, é preciso comparar a data do fato, o tipo de vínculo, o histórico e os documentos que confirmam a sequela.

---

## 9.6. Delimitação jurídica do público

Antes do CTA, revise a premissa jurídica central.

Classifique-a como:

- universal;
- federal;
- estadual ou municipal de ente identificado;
- restrita a categoria;
- restrita a regime;
- dependente de data;
- dependente de opção;
- dependente de documento ou fato.

Se não for universal, a delimitação deve aparecer:

- na ficha estratégica;
- no gancho ou no início do desenvolvimento;
- na segmentação recomendada.

Não use “em alguns casos” no final como única correção para uma abertura ampla demais.

Não generalize:

- RPPS para qualquer pessoa chamada de servidor;
- regra federal para todos os entes;
- integralidade ou paridade para todo ingresso antigo;
- fundo específico para todo regime complementar;
- consequência jurídica sem as condições centrais.

Quando a ressalva necessária ocupar mais espaço que a ideia, restrinja o público ou escolha outro ângulo.

## 9.7. CTA

O CTA depende do estágio.

### Consciência da situação

> Converse com a equipe para entender quais informações precisam ser verificadas no seu caso.

### Consciência da solução

> Uma análise individual permite comparar os cenários antes da decisão.

### Consideração

> Fale com o escritório para conhecer como funciona o diagnóstico.

### Decisão

> Entre em contato para receber as orientações sobre a próxima etapa.

Use o CTA real do escritório quando fornecido.

Não presuma:

- consulta gratuita;
- avaliação sem custo;
- resposta imediata;
- vaga limitada;
- prazo;
- canal.

---

# 10. ORIENTAÇÃO VISUAL

A orientação visual deve reforçar a ideia, não apenas decorar.

Pode incluir:

- texto curto na tela;
- troca de enquadramento;
- documento genérico sem dados pessoais;
- linha do tempo;
- comparação visual;
- duas opções na tela;
- palavra-chave;
- print de sistema autorizado e anonimizado;
- B-roll relacionado;
- quadro ou papel;
- pausa e aproximação de câmera.

Não use:

- documento real com dados;
- resultado não autorizado;
- depoimento inventado;
- dinheiro como promessa;
- antes/depois enganoso;
- imagem sensacionalista;
- ambiente que contradiga a marca.

---

# 11. DURAÇÃO

A duração não é obtida apenas contando palavras.

Considere:

- velocidade natural;
- pausas;
- ênfase;
- texto na tela;
- mudança visual;
- complexidade do tema.

Faixas orientativas:

| Duração | Uso |
|---|---|
| 20–30 s | uma situação, um insight e CTA curto |
| 35–45 s | situação, explicação, quebra e mecanismo |
| 50–60 s | comparação ou explicação com mais variáveis |

Não comprima assunto complexo até perder sentido.

Não estenda uma ideia simples apenas para atingir tempo.

---

# 12. DIVERSIDADE ENTRE ROTEIROS

Verifique diversidade em:

- situação;
- subpersona;
- estágio;
- tipo de gancho;
- dor;
- crença;
- mecanismo;
- CTA;
- formato;
- ritmo.

## Sinais de repetição

- todos começam com “Você sabia?”;
- todos falam com a mesma subpersona;
- todos usam medo de perder dinheiro;
- todos explicam a mesma regra;
- todos terminam com “cada caso é um caso”;
- todos prometem análise sem mostrar o que será analisado;
- muda apenas o exemplo, mas o conceito é o mesmo.

---

# 13. AUTORREVISÃO DE FIDELIDADE

Antes da revisão jurídica, compare a saída com a ficha de execução.

Verifique:

- quantidade exata;
- duração solicitada;
- formato solicitado;
- canal correto;
- público e recorte;
- objetivo;
- etapa do funil;
- tom;
- CTA;
- restrições;
- condições comerciais;
- fatos fornecidos;
- premissas realmente necessárias.

Falhas típicas:

- entregar seis quando foram pedidos cinco, ou o inverso;
- transformar tom informado em premissa;
- substituir CTA fornecido por placeholder;
- ampliar o público;
- trocar a duração;
- criar prova ou condição não fornecida;
- ignorar restrição expressa.

Corrija antes de prosseguir.

# 14. AUTORREVISÃO JURÍDICA

Para cada roteiro, verifique:

- a categoria está corretamente delimitada?
- o público do gancho corresponde ao público para o qual a afirmação vale?
- a regra depende do ente, regime, categoria, data ou opção?
- a delimitação aparece cedo, e não apenas numa ressalva final?
- a data ou prazo está validado?
- a consequência é possível ou certa?
- a peça distingue requisito de prova?
- a falta de documento foi tratada como ausência do direito?
- o roteiro criou urgência não confirmada?
- o roteiro afirmou que a pessoa tem direito?
- o roteiro omitiu exceção capaz de tornar a mensagem enganosa?
- o CTA promete um resultado?
- o criativo atrai uma anti-persona por simplificação excessiva?
- algum fator de subperfil, complexidade, prioridade ou potencial comercial foi chamado de aderência?
- renda, documentação ou proximidade foram transformadas em qualificação sem base expressa?

Quando a afirmação puder ser corrigida com condição, condicione.

Quando a condição destruir a clareza ou exigir muitas ressalvas, escolha outro ângulo.

---

# 15. AUTORREVISÃO CRIATIVA

Verifique:

- o gancho para a atenção sem sensacionalismo?
- o público se reconhece?
- a fala tem uma pergunta ou tensão real?
- a peça mostra por que o serviço é necessário?
- existe uma única ideia principal?
- o roteiro cabe na duração?
- a linguagem é falável?
- o visual reforça a ideia?
- o CTA é consequência natural?
- o roteiro é diferente dos demais?
- a peça seria intercambiável com outro nicho?
- há alguma frase publicitária vazia?

---

# 16. QUADRO FINAL DE DIVERSIDADE

Use esta estrutura:

| Roteiro | Situação | Subpersona | Consciência | Tipo de gancho | Dor/decisão | Mecanismo de valor | CTA | Cuidado jurídico |
|---|---|---|---|---|---|---|---|---|

Ao final, informe:

- repetições corrigidas;
- lacunas intencionais;
- ângulos reservados para futura rodada;
- pontos que dependem de validação antes de veiculação.

---

# 17. TESTE ANTIGENERICIDADE

Pergunte:

> Este roteiro poderia ser usado em outro nicho apenas trocando o nome do serviço?

Se sim, reescreva.

O roteiro precisa conter:

- situação específica;
- dúvida específica;
- variável específica;
- mecanismo específico.

Não precisa conter artigo, número ou jargão para ser específico.

---

# 18. TESTE DE DESEJO PELO SERVIÇO

Pergunte:

> Depois de assistir, a pessoa apenas aprendeu uma regra ou compreendeu por que precisa de análise?

O criativo pode ensinar, mas deve também mostrar:

- o limite da informação genérica;
- as variáveis do caso;
- a decisão que precisa ser tomada;
- o que o trabalho profissional organiza.

Não esconda todo o conteúdo para “gerar curiosidade”.

Entregue um insight real e conecte-o ao mecanismo.

---

# 19. REVISÃO DE PUBLICIDADE JURÍDICA

A peça deve ser revisada conforme as normas éticas de publicidade aplicáveis à advocacia, especialmente o Estatuto da Advocacia, o Código de Ética e Disciplina e o Provimento CFOAB nº 205/2021, sem prejuízo de normas posteriores e orientações da Seccional competente.

## 19.1. Critério geral

O conteúdo deve ser:

- informativo;
- sóbrio;
- discreto;
- verdadeiro;
- verificável;
- não mercantilista.

## 19.2. Verificações obrigatórias

Pergunte:

- há indução direta à contratação?
- há estímulo ao litígio?
- a linguagem parece oferta varejista?
- o CTA converte informação em pressão comercial?
- há menção a preço, gratuidade, desconto ou pagamento como atrativo?
- há promessa de ganho, êxito, prazo ou economia?
- há resultado concreto, cliente, decisão ou caso patrocinado usado como oferta?
- há autoengrandecimento, comparação ou especialidade não comprovada?
- há medo ou vulnerabilidade explorados de forma abusiva?
- a autoridade mencionada é real e comprovável?
- a publicidade paga mantém caráter informativo?

Dados de contato e aplicativos de mensagem podem aparecer de modo informativo, com sobriedade e discrição.

A presença de WhatsApp não autoriza automaticamente uma chamada direta à contratação.

## 19.3. Campanhas pagas

Em anúncios pagos ou impulsionados:

- evite oferta direta de serviços;
- evite comando de compra ou contratação;
- mantenha o foco em conteúdo informativo e esclarecimento;
- sinalize a necessidade de validação pelo advogado responsável antes da veiculação.

A skill auxilia a revisão, mas não certifica conformidade ética definitiva.

# 20. CRITÉRIO DE CONCLUSÃO

O processo está completo quando:

- os inputs foram conferidos e preservados;
- nenhum dado fornecido foi tratado como premissa;
- o serviço foi compreendido;
- o público foi segmentado por situação;
- perfil, aderência, complexidade, subperfil, prioridade e maturidade foram separados;
- renda, documentos, proximidade e interesse comercial não foram tratados como aderência sem base expressa;
- as dores vieram de fatos concretos;
- a matriz de ângulos foi criada;
- os conceitos foram selecionados;
- cada roteiro possui ficha estratégica;
- os roteiros são faláveis;
- o visual foi orientado;
- o CTA é real;
- as afirmações jurídicas estão seguras, delimitadas cedo ou condicionadas;
- a peça passou pela revisão de publicidade jurídica;
- não há promessa;
- os conceitos são diversos;
- o quadro final permite enxergar a campanha como conjunto.



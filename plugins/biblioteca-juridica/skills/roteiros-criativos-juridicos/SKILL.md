---
name: roteiros-criativos-juridicos
description: Cria conceitos e roteiros estratégicos de vídeos para campanhas jurídicas de Meta Ads. Antes de escrever, diagnostica o serviço, segmenta situações objetivas da persona, extrai dores exploráveis, constrói ângulos distintos e revisa cada roteiro quanto a reconhecimento, relevância, precisão jurídica, ética e diversidade criativa.
argument-hint: Forneça o Mapeamento de Persona Jurídica, o serviço, o objetivo da campanha, a quantidade de roteiros, a duração, o formato de gravação, o tom e o CTA do escritório.
---

# Roteiros de Criativos Jurídicos

## Objetivo

Criar roteiros de vídeos para campanhas de Meta Ads direcionadas a serviços jurídicos.

A skill não deve partir diretamente para os roteiros.

Antes de escrever qualquer peça, deve:

1. compreender o serviço;
2. identificar as situações concretas que tornam a análise profissional relevante;
3. separar aderência, complexidade e maturidade comercial;
4. extrair dores e decisões exploráveis;
5. construir ângulos distintos;
6. selecionar os melhores conceitos para a campanha;
7. somente então produzir e revisar os roteiros.

Fluxo obrigatório:

> diagnóstico do serviço  
> → diagnóstico estratégico da persona  
> → situações e dores exploráveis  
> → matriz de ângulos  
> → seleção estratégica  
> → roteiros  
> → autorrevisão

---

# Referências e insumos obrigatórios

Antes de produzir a saída, leia integralmente:

1. `${CLAUDE_PLUGIN_ROOT}/references/core-cognitivo.md`
2. `${CLAUDE_PLUGIN_ROOT}/references/core-escrita-oralidade.md`
3. `${CLAUDE_PLUGIN_ROOT}/references/roteiros-criativos-juridicos.md`

Aplique cada referência nesta função:

- `core-cognitivo.md`: hierarquia das fontes, herança de contexto, limites de presunção, distinção entre persona e caso individual, régua de certeza e segurança da saída;
- `core-escrita-oralidade.md`: naturalidade, clareza, ritmo, autoridade profissional e adequação do roteiro à fala e ao formato;
- `roteiros-criativos-juridicos.md`: diagnóstico do serviço, leitura da persona para mídia paga, extração de situações e dores, matriz de ângulos, seleção, estrutura dos roteiros, diversidade e autorrevisão.

Utilize também o **Mapeamento de Persona Jurídica produzido para o serviço da execução**, fornecido pelo usuário ou disponível na conversa.

O Mapeamento é um insumo dinâmico da execução. Ele não é uma referência estrutural fixa da pasta da skill.

Não leia `mapeamento-persona-v3.md` para substituir o Mapeamento produzido. Esse arquivo orienta a criação do documento-fonte pela skill `/mapear-persona`; não contém os dados específicos do público e do serviço atual.

No Mapeamento fornecido, priorize:

- delimitação do recorte;
- natureza do serviço;
- situação jurídica ou prática central;
- mecanismo de valor;
- jornada e níveis de consciência;
- banco de linguagem;
- dores, riscos, desejos e transformação;
- objeções e barreiras;
- fatores de decisão, prova e fricção;
- aderência, complexidade, maturidade, anti-persona e roteamento;
- matriz da Seção 10 destinada a criativos.

Não execute novamente `/mapear-persona`.

Não reproduza o Mapeamento inteiro na saída.

## Quando uma referência não estiver acessível

Se algum dos três arquivos obrigatórios não estiver disponível:

1. informe qual arquivo não foi localizado;
2. não reconstrua silenciosamente seu conteúdo;
3. não produza a versão final dos roteiros sem a referência metodológica específica;
4. prossiga apenas se o usuário fornecer expressamente o conteúdo equivalente ou solicitar uma entrega provisória com a limitação registrada.

## Quando o Mapeamento não estiver disponível

Solicite o Mapeamento de Persona Jurídica.

Somente prossiga sem o documento quando o usuário fornecer matéria-prima equivalente suficiente para a execução, contendo, no mínimo:

- natureza e delimitação do serviço;
- público e subperfis relevantes;
- situações objetivas de aderência;
- fatores de complexidade;
- dores, dúvidas, decisões e objeções;
- níveis de consciência;
- mecanismo de valor do serviço;
- limites jurídicos e éticos;
- anti-persona ou critérios de exclusão relevantes;
- objetivo da campanha;
- CTA ou próxima etapa real.

Não invente esses elementos.

Uma descrição genérica do nicho, isoladamente, não substitui o Mapeamento.

# Hierarquia e segurança das informações

Use as fontes nesta ordem:

1. instrução expressa do usuário;
2. informações confirmadas do escritório e da campanha;
3. informações jurídicas validadas fornecidas pelo usuário;
4. Mapeamento de Persona;
5. fontes oficiais consultadas na execução, quando necessário;
6. referências gerais da Biblioteca;
7. premissas estratégicas sinalizadas.

## Regra de validação jurídica

A skill não deve refazer automaticamente toda a pesquisa jurídica já realizada no Mapeamento.

Use afirmações jurídicas nos roteiros somente quando:

- estiverem confirmadas no Mapeamento;
- tiverem sido fornecidas como validadas pelo usuário;
- ou forem verificadas em fonte oficial durante a execução.

Se uma afirmação relevante depender do ente, data, categoria, contrato, documento ou caso concreto:

- condicione a formulação;
- delimite o subperfil;
- ou marque o ponto internamente como `[VALIDAR JURIDICAMENTE]`.

Não leve a marcação para o roteiro final.

Quando a incerteza impedir uma fala segura, não use a afirmação na peça até que seja validada.

Concentre o maior rigor nos elementos que alteram:

- quem pode se reconhecer no anúncio;
- aderência ao serviço;
- categorias incluídas ou excluídas;
- prazo ou urgência;
- consequência jurídica;
- comparação de alternativas;
- expectativa criada pelo criativo.

---

# Inputs

Use, quando fornecidos:

- Mapeamento de Persona Jurídica;
- descrição do serviço;
- objetivo da campanha;
- quantidade de roteiros;
- duração desejada;
- formato de gravação;
- tom de comunicação;
- CTA utilizado pelo escritório;
- informações jurídicas já validadas;
- restrições da campanha;
- praça, ente, categoria ou subperfil;
- prova de autoridade real;
- oferta ou próxima etapa real.

## Fidelidade obrigatória aos inputs

Antes de iniciar o diagnóstico, consolide internamente os inputs expressos do usuário.

Respeite literalmente, quando fornecidos:

- quantidade de roteiros;
- duração ou faixa de duração;
- formato;
- canal;
- público ou recorte;
- objetivo da campanha;
- etapa do funil;
- tom;
- CTA;
- restrições;
- informações jurídicas validadas;
- condições operacionais reais.

Não transforme um dado fornecido em `[PREMISSA]`.

Não substitua silenciosamente:

- o tom informado por outro tom “recomendado”;
- o CTA fornecido por placeholder;
- a quantidade pedida por quantidade diferente;
- a duração solicitada por outra faixa;
- o formato escolhido por formato alternativo;
- o recorte definido por público mais amplo;
- a próxima etapa real por uma etapa presumida.

Use `[PREMISSA]` somente para dados ausentes.

Se um input expresso conflitar com:

- segurança jurídica;
- normas éticas da publicidade da advocacia;
- restrição técnica do formato;
- outro input mais específico e posterior;

não o altere silenciosamente. Registre o conflito, explique o ajuste necessário e apresente a alternativa segura.

Antes da entrega, faça uma conferência objetiva entre pedido e saída.

## Lacunas

Não faça uma bateria de perguntas.

Pergunte apenas quando a ausência impedir a criação de peças coerentes ou produzir alternativas incompatíveis.

O Mapeamento de Persona é a base estratégica preferencial e deve ser solicitado quando não estiver disponível.

São dados críticos:

- serviço;
- público ou recorte;
- objetivo da campanha;
- CTA ou próxima etapa;
- Mapeamento de Persona, ou a matéria-prima equivalente mínima definida na seção anterior.

Quantidade, duração, formato e tom podem ser preenchidos por premissas adaptáveis quando o usuário não informar.

Nesse caso, sinalize na leitura estratégica, por exemplo:

- `[PREMISSA DE CAMPANHA: 5 roteiros]`
- `[PREMISSA DE DURAÇÃO: 45 segundos]`
- `[PREMISSA DE FORMATO: vídeo falado para câmera]`

Não presuma:

- gratuidade;
- valor;
- parcelamento;
- prazo;
- atendimento nacional;
- resultado;
- consulta;
- análise sem custo;
- condição comercial.

---

# Escopo

A skill pode criar:

- diagnóstico estratégico do serviço;
- diagnóstico estratégico da persona para mídia paga;
- matriz de situações, dores e decisões;
- matriz de ângulos;
- priorização dos conceitos;
- roteiros de vídeos;
- ganchos;
- desenvolvimento;
- quebra de crença;
- CTA;
- orientação visual;
- duração estimada;
- notas de gravação;
- autorrevisão;
- quadro de diversidade da campanha.

A skill não deve:

- criar Mapeamento de Persona do zero;
- substituir pesquisa jurídica necessária;
- produzir segmentação técnica no Gerenciador de Anúncios;
- definir orçamento, lance ou configuração de campanha;
- prometer resultado jurídico;
- prometer desempenho publicitário;
- criar depoimento ou caso fictício como prova;
- inventar dados do escritório;
- usar medo ou urgência artificial;
- tratar renda, documentação ou proximidade temporal como requisitos jurídicos quando não forem;
- transformar todos os roteiros em explicações genéricas da mesma regra;
- escrever uma biografia fictícia da persona;
- adaptar o material para outro canal sem pedido.

---

# Execução obrigatória

## Etapa 1 — Entender o serviço

Identifique:

- serviço oferecido;
- problema ou decisão que ele organiza;
- natureza do serviço;
- o que o profissional efetivamente faz;
- entregável ou próxima etapa;
- mecanismo de valor;
- resultados que podem ser mencionados de forma condicionada;
- afirmações que dependem de validação;
- promessas, termos e simplificações que devem ser evitados.

Diferencie:

- resultado do trabalho profissional;
- possível resultado jurídico;
- benefício percebido;
- promessa proibida.

Exemplo de resultado profissional permitido:

> comparar cenários, organizar documentos, identificar alternativas e orientar a decisão.

Exemplo de promessa indevida:

> garantir a regra mais vantajosa ou assegurar determinado valor.

---

## Etapa 2 — Diagnosticar quem precisa do serviço

Separe quatro dimensões:

### A. Perfil da persona

Use apenas para calibrar:

- linguagem;
- ritmo;
- vocabulário;
- formato;
- nível de explicação;
- contexto de identificação.

Não transforme idade, profissão predominante, rotina ou renda em requisitos universais sem que o recorte determine isso.

### B. Aderência ao serviço

Aderência é o núcleo mínimo que torna o serviço pertinente.

Use o seguinte teste:

> Se este elemento estiver ausente, o serviço deixa de ser pertinente para aquela pessoa?

Se a resposta for “sim”, pode ser aderência.

Para serviços de reconhecimento de direito, use requisitos materiais preliminares.

Para serviços consultivos, use a situação ou decisão central que justifica a análise profissional.

Não classifique automaticamente como aderência:

- proximidade temporal;
- data de ingresso;
- existência de documentos;
- renda ou patrimônio;
- categoria especial;
- quantidade de vínculos;
- ente específico;
- objeção;
- urgência;
- interesse em contratar;
- disposição para falar com o escritório.

Esses elementos podem pertencer a subperfil, complexidade, prioridade, maturidade, prova ou viabilidade comercial.

### C. Complexidade e valor da análise

Identifique fatores que aumentam:

- número de cenários;
- necessidade de comparação;
- dificuldade probatória;
- risco de erro;
- dependência de documentos;
- impacto econômico ou estratégico.

Complexidade não substitui aderência.

### D. Maturidade comercial

Identifique:

- nível de consciência;
- proximidade da decisão;
- objeções;
- disposição para conversar;
- necessidade de educação prévia.

Maturidade não substitui aderência.

### E. Subperfis criativos

Subperfil criativo é um recorte de comunicação dentro do público aderente.

Pode ser formado por:

- ente;
- categoria;
- data de ingresso;
- histórico contributivo;
- tipo de contrato;
- estágio do problema;
- decisão em aberto;
- objeção;
- nível de consciência;
- fator de complexidade.

Um subperfil pode gerar um excelente ângulo sem constituir critério de aderência.

### Teste obrigatório de classificação

Para cada elemento relevante, classifique internamente:

- **aderência:** sem ele, o serviço deixa de ser pertinente;
- **complexidade:** sem ele, o serviço continua pertinente, mas a análise tende a ser mais simples;
- **subperfil:** muda para quem ou como o criativo fala;
- **maturidade:** muda o nível de explicação, a objeção ou o CTA;
- **prioridade/urgência:** muda a velocidade recomendada da ação;
- **prova:** ajuda a confirmar a situação;
- **potencial comercial:** influencia estratégia comercial, sem alterar a pertinência jurídica.

Não apresente renda, documentação, proximidade temporal ou interesse comercial como aderência, salvo quando o próprio serviço possuir um requisito objetivo dessa natureza confirmado no Mapeamento.

---

## Etapa 3 — Extrair dores exploráveis

Para cada situação objetiva relevante, identifique:

- dúvida consciente;
- medo ou tensão por trás da dúvida;
- possível prejuízo percebido;
- desejo;
- decisão que a pessoa não sabe tomar;
- crença que precisa ser quebrada;
- pergunta capaz de interromper a atenção;
- informação que faz o serviço parecer necessário;
- limite jurídico ou ético.

Não use dor vaga quando houver situação concreta.

Evite ângulos genéricos como:

- “você conhece seus direitos?”;
- “você sabe quando vai se aposentar?”;
- “não deixe dinheiro na mesa”;
- “procure um advogado”;

salvo quando forem desenvolvidos com um recorte específico que lhes dê sentido real.

---

## Etapa 4 — Criar a matriz de ângulos

Antes dos roteiros, produza uma matriz com:

- ângulo principal;
- situação objetiva;
- classificação do marcador central: aderência, complexidade, subperfil, maturidade, prioridade ou prova;
- subpersona;
- nível de consciência;
- dor ou decisão explorada;
- pergunta central;
- insight ou quebra de crença;
- mecanismo de valor do serviço;
- promessa comunicacional permitida;
- afirmação que exige cuidado;
- risco de generalização;
- formato recomendado;
- função do criativo na campanha.

### Regra de classificação do marcador

A coluna **“classificação do marcador central”** deve classificar o elemento descrito na coluna **“situação objetiva”** daquela mesma linha.

Não use essa coluna para repetir a aderência geral do público quando a situação objetiva descreve outro fenômeno.

Exemplos:

| Situação objetiva | Classificação adequada |
|---|---|
| ocupa cargo efetivo, está vinculado a RPPS e possui decisão previdenciária em aberto | aderência |
| pesquisa aposentadoria e aplica conteúdo de INSS ao próprio caso | maturidade ou subperfil comportamental |
| trabalhou na iniciativa privada antes do concurso | complexidade ou subperfil |
| está prestes a tomar uma decisão | prioridade |
| acredita que o RH já resolve toda a análise | maturidade |
| possui documento capaz de confirmar o período alegado | prova |

Faça o teste:

> Estou classificando exatamente o marcador descrito nesta linha ou apenas repetindo o perfil geral do público?

Quando mais de uma dimensão estiver presente, escolha a dimensão que exerce a função principal naquele ângulo e registre a secundária apenas quando ela também estiver descrita na própria situação objetiva.

Não importe para a classificação:

- a aderência geral do público;
- o perfil-base da campanha;
- uma condição presente apenas no Mapeamento;
- uma característica que não aparece naquela linha.

Exemplo obrigatório:

| Situação objetiva | Classificação correta | Classificação incorreta |
|---|---|---|
| está perto de se aposentar e acredita que basta completar o tempo | prioridade + maturidade | aderência + prioridade |
| aplica conteúdo do INSS ao próprio caso | maturidade ou subperfil comportamental | aderência |
| trabalhou no setor privado antes do cargo atual | complexidade ou subperfil | aderência + complexidade |

Aderência só pode aparecer como classificação daquela linha quando o próprio marcador descrito for o núcleo mínimo que torna o serviço pertinente.

Faça uma última pergunta:

> A palavra “aderência” descreve a situação desta linha ou apenas o fato de a campanha inteira já falar com público aderente?

Se apenas repetir o público geral, remova-a.

Crie mais ângulos do que o número final de roteiros quando isso ajudar a selecionar melhor.

Não escolha vários ângulos que apenas reformulem a mesma dúvida.

---

## Regra de delimitação por ente, categoria ou regime

Antes de selecionar um conceito, determine se a afirmação central é:

- universal para todo o recorte;
- aplicável apenas a determinado ente;
- aplicável apenas a determinada categoria;
- aplicável apenas a determinado regime;
- dependente de data, opção, documento ou condição específica.

Quando não for universal:

1. delimite o subperfil na ficha estratégica;
2. leve as condições materiais relevantes para a fala;
3. deixe a delimitação perceptível no gancho ou no início do desenvolvimento;
4. não use uma ressalva genérica no final para corrigir uma premissa ampla demais;
5. não apresente regra federal como regra geral de servidores estaduais ou municipais;
6. não apresente nome de fundo, regime ou programa específico para público que pode não estar abrangido.

A ficha estratégica não corrige sozinha uma fala ampla.

Se a ficha registra condições como data de ingresso, opção por regime complementar, exercício em determinada função, ente, categoria ou requisito adicional, a fala deve:

- mencionar as condições centrais de modo compreensível; ou
- abandonar a conclusão específica e reformular o ângulo para uma afirmação mais geral e segura.

Não substitua condições relevantes apenas por expressões vagas como:

- “depende de algumas condições”;
- “varia conforme o caso”;
- “entre outros pontos”;
- “cada caso é um caso”.

Se a delimitação tornar o roteiro confuso ou excessivamente carregado, descarte o ângulo, restrinja a campanha ou reformule a promessa comunicacional.

## Regra de precisão semântica e causal

A redação deve ser tão precisa quanto o recorte jurídico validado.

### Não deduza regime ou enquadramento a partir de rótulos amplos

Não trate como equivalentes, sem confirmação:

- concursado;
- servidor;
- servidor público;
- ocupante de cargo efetivo;
- vinculado a RPPS;
- segurado do RGPS;
- integrante de categoria especial.

Não use formulações como:

- “todo servidor concursado tem regime próprio”;
- “quem é efetivo está no RPPS”;
- “professor sempre tem regra reduzida”;
- “servidor se aposenta por regra diferente do INSS”;

quando o recorte necessário for mais específico.

Prefira reproduzir o escopo confirmado no Mapeamento, por exemplo:

> servidor titular de cargo efetivo vinculado a RPPS;

ou outra formulação tecnicamente adequada ao serviço analisado.

### Não aumente a intensidade da consequência

Evite expressões como:

- “muda bastante”;
- “trava um valor menor”;
- “vai receber menos pelo resto da vida”;
- “está trabalhando mais do que precisava”;
- “está deixando dinheiro na mesa”;
- “perdeu a melhor regra”;

quando a intensidade, o resultado ou a relação causal não tiverem sido validados.

Prefira:

- “pode alterar o cálculo”;
- “pode modificar o cenário aplicável”;
- “pode levar a uma decisão menos favorável”;
- “pode deixar parte do histórico fora da análise”;
- “merece comparação antes da decisão”.

A possibilidade comunicável deve continuar sendo apresentada como possibilidade.

### Diferencie funções sem atribuir falhas a terceiros

Ao mencionar RH, sindicato, contador, banco, médico, órgão público ou outro profissional:

- não presuma o que a instituição faz ou deixa de fazer em todos os casos;
- não atribua omissão, erro ou incapacidade sem base;
- não crie contraste depreciativo;
- diferencie funções e escopos de atuação.

Prefira:

> o papel do setor costuma estar concentrado no procedimento administrativo e na conferência funcional; a comparação estratégica entre regras, datas e valores é uma análise diferente.

Adapte a formulação ao contexto real, sem transformar o exemplo em afirmação universal.

### Preserve a precisão também no texto visual

Textos na tela, legendas e elementos gráficos não podem simplificar a regra além do que a fala permite.

Se a fala diz “tempo efetivamente exercido em funções de magistério”, não reduza para “tempo em sala” se isso alterar o alcance jurídico.

## Etapa 5 — Selecionar os conceitos

Escolha os ângulos mais fortes conforme:

- reconhecimento imediato;
- aderência ao serviço;
- relevância da dúvida;
- clareza do mecanismo de valor;
- possibilidade de explicação no tempo disponível;
- segurança jurídica;
- adequação ao nível de consciência;
- diversidade em relação aos demais;
- compatibilidade com o formato e CTA.

Explique brevemente por que cada conceito foi selecionado.

Quando um conceito for descartado por risco jurídico, genericidade ou repetição, registre isso de forma breve na análise interna.

---

## Etapa 6 — Gerar os roteiros

Para cada roteiro, entregue:

### Ficha estratégica

- título interno;
- público específico;
- situação objetiva;
- nível de consciência;
- objetivo;
- ângulo;
- dúvida central;
- promessa comunicacional permitida;
- afirmação jurídica sensível;
- formato;
- duração estimada.

### Roteiro

1. **Gancho inicial**
   - deve funcionar nos primeiros segundos;
   - deve partir de situação, pergunta, contraste, erro ou decisão concreta;
   - não deve depender de uma introdução longa.

2. **Desenvolvimento**
   - explique a situação em linguagem simples;
   - mostre por que a dúvida importa;
   - conecte a regra ou mecanismo à vida prática;
   - mantenha o foco em uma ideia principal.

3. **Quebra de crença ou insight**
   - apresente a informação que muda a forma de enxergar o problema;
   - não transforme a peça em aula;
   - não conclua o caso individual.

4. **Mecanismo de valor**
   - explique o que a análise profissional compara, confirma, organiza ou previne;
   - não use apenas “cada caso é um caso”.

5. **CTA**
   - convide para a próxima etapa real;
   - convide para análise, orientação, diagnóstico ou conversa;
   - não prometa resultado.

6. **Orientação visual**
   - indique o que gravar, mostrar, escrever na tela ou destacar;
   - mantenha compatibilidade com o formato informado;
   - não invente prova social.

7. **Notas de gravação**
   - ritmo;
   - pausas;
   - palavras de ênfase;
   - elementos visuais;
   - cuidados de oralidade.

---

## Etapa 7 — Autorrevisão

### Conferência dos inputs

Antes de revisar o conteúdo, confirme:

- a quantidade entregue é exatamente a solicitada?
- a duração corresponde ao pedido?
- o formato corresponde ao pedido?
- o tom fornecido foi preservado?
- o CTA fornecido foi utilizado, salvo conflito ético explicitado?
- o canal e a próxima etapa estão corretos?
- o público não foi ampliado ou reduzido silenciosamente?
- todas as restrições expressas foram respeitadas?
- algum dado fornecido foi marcado indevidamente como premissa?
- alguma premissa foi criada apesar de o dado já estar disponível?

Se houver divergência, corrija antes de continuar.

### Revisão estratégica, jurídica e criativa

Revise cada roteiro e responda internamente:

- fala com uma situação concreta?
- a pessoa consegue se reconhecer?
- desperta uma dúvida relevante?
- gera necessidade pelo serviço ou apenas explica uma regra?
- diferencia aderência, complexidade, subperfil, prioridade e maturidade?
- a classificação da matriz corresponde exatamente à situação objetiva daquela linha?
- a coluna de classificação apenas repetiu a aderência geral do público?
- algum subperfil ou fator de complexidade foi chamado de aderência?
- renda, documentação, proximidade ou interesse comercial foram usados como qualificação sem base expressa?
- deduz regime, enquadramento ou regra apenas a partir de rótulo como “concursado”, “servidor” ou “efetivo”?
- transforma característica provável em fato universal?
- a afirmação central é universal para o público realmente alcançado?
- quando depende de ente, categoria ou regime, isso aparece cedo e com clareza?
- contém promessa de resultado?
- contém urgência artificial?
- contém afirmação dependente do ente ou caso concreto?
- apresenta a condição necessária?
- usa intensidade, perda, ganho ou relação causal não confirmada?
- afirma que uma instituição ou profissional faz ou deixa de fazer algo sem base suficiente?
- diferencia funções sem desmerecer terceiros?
- o texto na tela preserva as mesmas condições e limites da fala?
- o CTA convida para análise em vez de prometer benefício?
- o gancho corresponde ao restante do roteiro?
- a fala soa natural em voz alta?
- cabe na duração?
- está suficientemente diferente dos demais?
- poderia ser usado em outro nicho apenas trocando termos?
- repete uma ideia já coberta por outro criativo?
- depende de prova, estatística ou autoridade inventada?

Corrija silenciosamente antes da entrega.

## Auditoria final baseada em evidências

Depois da autorrevisão, faça uma segunda passagem obrigatória sobre a versão integral dos roteiros.

Para cada roteiro, faça duas auditorias complementares.

### A. Auditoria de critérios

| Critério | Evidências completas | Status | Correção necessária |
|---|---|---|---|
| recorte jurídico preservado em todas as partes | todas as ocorrências que definem ou ampliam o público | aprovado/reprovado |  |
| condição jurídica material presente na fala | todos os trechos relacionados à conclusão sensível | aprovado/reprovado/não aplicável |  |
| intensidade sustentada | todas as expressões de intensidade encontradas | aprovado/reprovado |  |
| causalidade sustentada | todas as relações de causa e consequência encontradas | aprovado/reprovado |  |
| terceiros tratados por diferença de função | todas as menções ao terceiro | aprovado/reprovado/não aplicável |  |
| texto visual coerente com a fala | todos os textos visuais juridicamente relevantes | aprovado/reprovado |  |
| CTA compatível | todos os CTAs e chamadas auxiliares | aprovado/reprovado |  |

### B. Inventário exaustivo de ocorrências

| Nº | Componente | Trecho exato | Família de risco | Avaliação | Correção |
|---|---|---|---|---|---|
| 1 | gancho/desenvolvimento/ficha/tela/CTA/notas/quadro | citação literal | recorte/intensidade/causalidade/terceiros/promessa/outro | seguro/problemático | versão final corrigida |

O inventário deve conter **todas** as ocorrências localizadas, não apenas uma evidência representativa.

### Regra de prova

Não declare um critério como cumprido apenas por conclusão abstrata.

Toda aprovação deve estar sustentada por:

- lista completa de trechos relevantes;
- comparação literal entre todas as partes afetadas; e
- resultado de busca expressa por formulações de risco.

Uma evidência favorável não neutraliza uma ocorrência desfavorável.

É proibido escolher apenas o trecho que comprova a conclusão desejada e ignorar:

- o gancho;
- outra frase do desenvolvimento;
- o texto na tela;
- a nota de gravação;
- a ficha estratégica;
- o quadro final.

Se a busca localizar 4 ocorrências, as 4 devem ser analisadas.

O status só pode ser **Aprovado** quando:

- todas as ocorrências foram inventariadas;
- cada ocorrência recebeu avaliação;
- nenhuma ocorrência problemática permanece na versão final;
- o número de ocorrências analisadas coincide com o total localizado.

Se não houver evidência suficiente ou houver ocorrência não analisada, marque como reprovado.

### Busca obrigatória por formulações de risco

Procure no texto integral, inclusive em ficha, fala, CTA, orientação visual, notas e quadro final, termos ou construções equivalentes a:

- todo, sempre, nunca;
- concursado, servidor, efetivo, cargo efetivo;
- costuma estar, normalmente é, em geral tem;
- tempo parado, dinheiro parado, tempo que já é seu;
- receber menos, perder valor, travar valor;
- não dá para voltar atrás;
- decisão mais cara;
- resolver no chute, achismo;
- tarde demais, seria péssimo;
- trabalhando mais do que precisava;
- dinheiro na mesa;
- o RH não faz, o órgão não informa;
- melhor, mais vantajoso, ideal;
- resultado garantido, direito certo.

A presença do termo não reprova automaticamente. Ela obriga a verificar:

1. o recorte está explícito?
2. a intensidade foi validada?
3. a causalidade foi demonstrada?
4. a comparação está sustentada?
5. existe formulação mais precisa?

### Contagem obrigatória

Para cada família de risco, registre:

- total de ocorrências localizadas;
- total analisado;
- total corrigido;
- total remanescente.

Use o controle:

| Família | Localizadas | Analisadas | Corrigidas | Remanescentes |
|---|---:|---:|---:|---:|
| recorte e vínculo |  |  |  |  |
| intensidade |  |  |  |  |
| causalidade |  |  |  |  |
| terceiros |  |  |  |  |
| promessa/comercialidade |  |  |  |  |
| condições jurídicas |  |  |  |  |

Nenhuma família pode ser aprovada se:

- `Analisadas < Localizadas`; ou
- `Remanescentes > 0`.

### Varredura específica de recorte

Toda ocorrência de termos como:

- servidor;
- concursado;
- efetivo;
- cargo efetivo;
- RPPS;
- regime próprio;
- federal;
- estadual;
- municipal;
- professor;
- policial;
- categoria especial;

deve ser examinada no contexto.

O recorte não está preservado apenas porque uma frase posterior é precisa. Um gancho amplo continua sendo uma ocorrência problemática, mesmo que o desenvolvimento delimite corretamente depois.

### Ciclo obrigatório de correção

Quando qualquer linha estiver reprovada:

1. corrija o roteiro;
2. atualize ficha, fala, texto visual e quadro final;
3. repita a auditoria sobre a nova versão;
4. somente entregue quando não houver contradição entre roteiro e revisão final.

É proibido:

- manter frase problemática e declarar que ela foi removida;
- afirmar que o recorte foi preservado quando qualquer parte usa público mais amplo;
- usar uma frase precisa do desenvolvimento para ignorar um gancho impreciso;
- afirmar ausência de intensidade quando qualquer ocorrência emocional ou causal não validada permanece;
- analisar apenas uma das várias ocorrências da mesma família;
- registrar “Aprovado” quando a contagem de ocorrências estiver incompleta;
- usar a ficha estratégica para justificar condição que não aparece na fala;
- emitir conclusão de conformidade sem inventário completo e evidência textual.

---

# Estrutura da saída

Entregue nesta ordem:

## 1. Premissas e recorte da campanha

Síntese curta com:

- serviço;
- público;
- objetivo;
- etapa do funil;
- quantidade;
- duração;
- formato;
- tom;
- CTA;
- restrições;
- premissas adotadas;
- informações que ainda exigem validação.

## 2. Diagnóstico estratégico

Apresente:

- mecanismo de valor do serviço;
- situações de aderência;
- fatores de complexidade;
- níveis de maturidade;
- dores e decisões exploráveis;
- promessas permitidas;
- riscos de comunicação.

Não reproduza o Mapeamento.

## 3. Matriz de ângulos

Use a estrutura definida na referência.

## 4. Seleção recomendada

Indique os conceitos escolhidos e a função de cada um na campanha.

## 5. Roteiros completos

Entregue as fichas estratégicas e os roteiros.

## 6. Quadro de diversidade e revisão

Apresente uma síntese final demonstrando:

- subpersonas cobertas;
- situações cobertas;
- níveis de consciência cobertos;
- tipos de gancho;
- objetivos;
- repetições evitadas;
- pontos jurídicos condicionados;
- riscos corrigidos.

## 7. Quadro de conformidade por evidência

Apresente uma tabela final auditável:

| Roteiro | Família auditada | Ocorrências localizadas | Ocorrências analisadas | Trechos exatos e avaliação | Correções aplicadas | Remanescentes | Status |
|---|---|---:|---:|---|---|---:|---|

Regras:

- crie uma linha por roteiro e por família relevante;
- informe a quantidade total localizada e analisada;
- liste todos os trechos relevantes, não apenas um exemplo;
- identifique o componente de cada trecho: ficha, gancho, desenvolvimento, tela, CTA, notas ou quadro;
- não use descrições genéricas como “está condicionado”;
- quando não houver condição específica, registre “não aplicável”;
- quando uma formulação de risco tiver sido encontrada, mostre a versão corrigida;
- `Ocorrências analisadas` deve ser igual a `Ocorrências localizadas`;
- `Remanescentes` deve ser zero para receber “Aprovado”;
- o quadro deve refletir os roteiros efetivamente entregues.

Não exponha raciocínio privado ou cadeia de pensamento. Apresente apenas evidências textuais e conclusões úteis da revisão.

---

# Regras de escrita e oralidade

Os roteiros devem:

- soar naturais quando falados;
- usar frases curtas e compreensíveis;
- manter uma ideia principal por vídeo;
- começar pela consequência ou situação prática;
- traduzir termos técnicos;
- usar especificidade sem depender de personagem;
- evitar introduções institucionais longas;
- evitar listas extensas faladas;
- evitar juridiquês;
- evitar tom professoral;
- evitar frases publicitárias vazias;
- preservar autoridade natural;
- ter CTA coerente com o nível de consciência.

Use linguagem da persona para conexão, sem caricatura, erro forçado, gíria artificial ou intimidade excessiva.

Não comece todos os roteiros com:

- “Você sabia?”
- “Atenção, servidor!”
- “Se você...”
- “Muita gente não sabe...”

Varie os mecanismos de abertura:

- pergunta específica;
- contraste;
- erro comum;
- escolha;
- situação cotidiana;
- consequência;
- dúvida;
- afirmação contraintuitiva;
- microcenário;
- dado validado, quando houver.

---

# Revisão de publicidade jurídica

A saída deve passar por revisão específica de publicidade da advocacia.

Considere, no mínimo, o Estatuto da Advocacia, o Código de Ética e Disciplina, o Provimento CFOAB nº 205/2021 e normas posteriores aplicáveis.

O conteúdo deve permanecer:

- informativo;
- sóbrio;
- discreto;
- verdadeiro;
- verificável;
- compatível com a dignidade profissional.

Revise se o anúncio:

- induz diretamente à contratação;
- estimula litígio;
- mercantiliza o serviço;
- usa chamada típica de varejo;
- utiliza expressão persuasiva, autoengrandecimento ou comparação;
- menciona honorários, descontos, gratuidade ou forma de pagamento como atração;
- divulga resultado concreto, cliente, decisão ou caso patrocinado como oferta;
- explora medo, vulnerabilidade ou urgência sem base;
- apresenta especialidade ou autoridade não comprovada;
- usa CTA incompatível com o caráter informativo.

Dados de contato e aplicativos de mensagem podem ser indicados em caráter informativo, mas o CTA não deve converter o conteúdo em indução direta à contratação.

Quando a campanha for paga ou impulsionada, sinalize que a peça deve ser validada pelo advogado responsável à luz das regras éticas aplicáveis e das orientações da OAB competente.

A skill não certifica conformidade ética definitiva.

# Compliance e limites

Não use:

- garantia;
- promessa de êxito;
- promessa de valor;
- promessa de prazo;
- resultado certo;
- comparação com concorrentes;
- superioridade não comprovada;
- medo exagerado;
- urgência artificial;
- estatística não validada;
- prova social inventada;
- dramatização enganosa;
- frase que trate possibilidade como certeza;
- chamada que explore vulnerabilidade de forma abusiva;
- linguagem de mercantilização incompatível com a advocacia;
- indução direta à contratação;
- estímulo ao litígio;
- chamada varejista como “contrate agora”, “garanta sua vaga” ou equivalente;
- referência a honorários, gratuidade, desconto ou forma de pagamento como atrativo;
- resultado concreto ou caso patrocinado usado como oferta.

O criativo pode comunicar:

- relevância da análise;
- existência de alternativas;
- risco de decisão sem informação;
- necessidade de confirmação;
- organização de cenários;
- clareza;
- prevenção de erro;
- compreensão de direitos;
- orientação profissional;
- possibilidade condicionada.

---

# Critérios de conclusão

A saída está completa quando:

- utilizou o Mapeamento de Persona específico da execução, ou matéria-prima equivalente explicitamente suficiente;
- não confundiu o arquivo estrutural `mapeamento-persona-v3.md` com o documento-fonte produzido;
- não partiu diretamente para os roteiros;
- conferiu quantidade, duração, formato, tom, CTA, canal, público e restrições contra os inputs expressos;
- não marcou como premissa um dado já fornecido;
- compreendeu o serviço e seu mecanismo de valor;
- separou perfil, aderência, complexidade, subperfil, prioridade e maturidade;
- classificou o marcador específico de cada situação objetiva, sem apenas repetir a aderência geral do público;
- não tratou renda, documentos, proximidade temporal ou interesse comercial como aderência sem base expressa;
- não deduziu regime ou enquadramento jurídico apenas a partir de rótulos amplos;
- extraiu dores de situações objetivas;
- criou matriz de ângulos;
- selecionou conceitos distintos;
- escreveu os roteiros completos;
- conectou cada roteiro a uma subpersona e nível de consciência;
- apresentou CTA real e ético;
- delimitou cedo afirmações dependentes de ente, categoria, regime, data ou condição;
- condicionou afirmações dependentes do caso;
- evitou intensidade, causalidade e consequências não validadas;
- diferenciou funções de terceiros sem atribuir falha ou omissão universal;
- manteve texto visual, fala e ficha estratégica juridicamente coerentes;
- comprovou as conclusões da revisão com todas as ocorrências relevantes, e não com amostra conveniente;
- executou busca por formulações de risco em todos os componentes;
- contabilizou ocorrências localizadas, analisadas, corrigidas e remanescentes;
- não aprovou família com ocorrência não analisada ou remanescente;
- corrigiu contradições antes de produzir o quadro final;
- não usou a ficha estratégica para compensar condição ausente na fala;
- passou pela revisão específica de publicidade jurídica;
- evitou promessas;
- trouxe orientação visual;
- preservou oralidade;
- demonstrou diversidade;
- revisou juridicamente e criativamente as peças;
- entregou um processo de campanha, e não apenas textos isolados.


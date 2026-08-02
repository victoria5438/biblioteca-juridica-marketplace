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

Identifique as situações objetivas que tornam a análise pertinente.

Para serviços de reconhecimento de direito, use requisitos materiais preliminares.

Para serviços consultivos, use decisões, riscos, alternativas e variáveis que tornam a análise individual útil.

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

Crie mais ângulos do que o número final de roteiros quando isso ajudar a selecionar melhor.

Não escolha vários ângulos que apenas reformulem a mesma dúvida.

---

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

Revise cada roteiro e responda internamente:

- fala com uma situação concreta?
- a pessoa consegue se reconhecer?
- desperta uma dúvida relevante?
- gera necessidade pelo serviço ou apenas explica uma regra?
- diferencia aderência, complexidade e maturidade?
- transforma característica provável em fato universal?
- contém promessa de resultado?
- contém urgência artificial?
- contém afirmação dependente do ente ou caso concreto?
- apresenta a condição necessária?
- o CTA convida para análise em vez de prometer benefício?
- o gancho corresponde ao restante do roteiro?
- a fala soa natural em voz alta?
- cabe na duração?
- está suficientemente diferente dos demais?
- poderia ser usado em outro nicho apenas trocando termos?
- repete uma ideia já coberta por outro criativo?
- depende de prova, estatística ou autoridade inventada?

Corrija silenciosamente antes da entrega.

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

Não exponha raciocínio privado ou cadeia de pensamento. Apresente apenas conclusões úteis da revisão.

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
- linguagem de mercantilização incompatível com a advocacia.

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
- compreendeu o serviço e seu mecanismo de valor;
- separou perfil, aderência, complexidade e maturidade;
- extraiu dores de situações objetivas;
- criou matriz de ângulos;
- selecionou conceitos distintos;
- escreveu os roteiros completos;
- conectou cada roteiro a uma subpersona e nível de consciência;
- apresentou CTA real e ético;
- condicionou afirmações dependentes do caso;
- evitou promessas;
- trouxe orientação visual;
- preservou oralidade;
- demonstrou diversidade;
- revisou juridicamente e criativamente as peças;
- entregou um processo de campanha, e não apenas textos isolados.

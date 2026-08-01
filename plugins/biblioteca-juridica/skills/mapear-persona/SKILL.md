---
name: mapear-persona
description: Cria um Mapeamento de Persona Jurídica ultra-detalhado para alimentar as skills de marketing, qualificação, atendimento, vendas, nutrição e operação de escritórios de advocacia. Use quando o usuário pedir para mapear uma persona, público, serviço ou nicho jurídico.
argument-hint: [nicho jurídico e contexto opcional]
---

# Objetivo

Produzir o documento-fonte compartilhado de Mapeamento de Persona Jurídica da Biblioteca Jurídica.

O mapeamento deve organizar contexto jurídico-fático, linguagem, níveis de consciência, dores, objeções, fatores de decisão e critérios de qualificação de forma suficientemente específica para ser herdado pelas demais skills.

Esta skill produz matéria-prima estratégica. Não produz as peças finais derivadas.

# Referências obrigatórias

Antes de produzir a saída, leia integralmente:

1. `${CLAUDE_PLUGIN_ROOT}/references/core-cognitivo.md`
2. `${CLAUDE_PLUGIN_ROOT}/references/mapeamento-persona-v3.md`
3. `${CLAUDE_PLUGIN_ROOT}/references/core-escrita-oralidade.md`

Aplique as referências nesta função:

- `core-cognitivo.md`: raciocínio, hierarquia de fontes, limites de presunção, persona versus lead individual, régua de certeza e reutilização;
- `mapeamento-persona-v3.md`: estrutura obrigatória, profundidade, categorias e formato da entrega;
- `core-escrita-oralidade.md`: naturalidade da linguagem, uso não caricatural do banco de fala e adequação dos insumos de comunicação.

Esses arquivos integram o plugin e devem orientar toda a execução.

Caso algum arquivo obrigatório não esteja acessível:

1. informe claramente qual referência não foi localizada;
2. não reconstrua silenciosamente o conteúdo ausente;
3. não produza o mapeamento completo sem a referência estrutural `mapeamento-persona-v3.md`.

# Validação jurídica obrigatória

Antes de redigir informações jurídicas, faça verificação atualizada em fontes oficiais compatíveis com o nicho e a natureza do serviço.

## 1. Função da referência estrutural

Trate `mapeamento-persona-v3.md` como referência de estrutura, raciocínio e profundidade.

Não a trate como fonte jurídica definitiva.

## 2. Fontes prioritárias

Consulte prioritariamente:

- legislação no Portal Planalto;
- legislação e atos normativos de estados, municípios e entes competentes;
- páginas oficiais do INSS, gov.br e demais órgãos públicos relacionados;
- STF, STJ, TST, TSE, tribunais regionais ou tribunais locais quando jurisprudência e competência forem relevantes;
- agências reguladoras, conselhos, autarquias e sistemas oficiais aplicáveis;
- atos normativos, manuais e orientações oficiais vigentes.

Em caso de conflito, a fonte oficial atual prevalece sobre conhecimento prévio, exemplos, materiais antigos ou premissas.

## 3. Escopo mínimo da validação

Valide, conforme a natureza do serviço:

- público, categorias, vínculos ou situações abrangidas;
- requisitos materiais;
- fatos geradores;
- consequências exigidas;
- categorias incluídas e excluídas;
- incompatibilidades e impedimentos;
- marcos temporais;
- prescrição, decadência e prazos;
- documentos e meios de confirmação;
- vias administrativa, negocial, extrajudicial, consultiva e judicial;
- possibilidades de defesa ou atuação;
- variações por data, categoria, regime, contrato, ente ou local;
- pontos necessários para construir MQL e SQL jurídicos.

Não force categorias próprias de concessão de benefício quando o serviço for defensivo, consultivo, preventivo ou híbrido.

## 4. Qualificação juridicamente validada

A Seção 9 deve ser construída a partir de critérios juridicamente coerentes.

- Em serviços de reconhecimento, concessão, revisão, reparação, cobrança ou indenização, identifique os requisitos materiais que formam a pertinência preliminar do MQL.
- Em serviços de defesa, identifique a situação ou ameaça existente, o vínculo do lead, o estágio, o prazo e a possibilidade de atuação.
- Em serviços consultivos, preventivos, de planejamento ou estruturação, identifique as condições objetivas, decisões, riscos e alternativas que tornam a análise profissional relevante.
- Em serviços híbridos, apresente a qualificação em camadas.

Não confunda:

- requisito material;
- relato;
- indício;
- confirmação;
- documento;
- chance de êxito;
- urgência;
- complexidade;
- maturidade comercial;
- intenção de contratar.

## 5. Segurança jurídica

- Não crie subperfis juridicamente inelegíveis.
- Não transforme informação ausente em requisito não atendido.
- Não trate documento como requisito material quando ele for apenas meio de prova.
- Não conclua direito, viabilidade ou chance de êxito com base apenas em descrição genérica.
- Quando não houver confirmação suficiente ou existir controvérsia real, use `[VALIDAR JURIDICAMENTE]` apenas no ponto específico.
- Quando a informação depender de política do escritório, use `[VALIDAR COM O ESCRITÓRIO]`.
- Dentro da Seção 3, inclua o subtítulo **Fontes oficiais consultadas**, com as fontes utilizadas e a data da consulta.

# Execução

## 1. Entrada e delimitação

- Se o nicho jurídico não estiver informado, faça somente a pergunta inicial prevista na referência e ofereça o bloco opcional de contexto.
- Se o nicho estiver amplo demais, proponha de 2 a 3 sub-recortes e aguarde a escolha.
- Diferencie nicho, serviço, público, situação atendida e próxima etapa.
- Não trate uma área inteira como uma única persona quando existirem serviços materialmente diferentes.
- Se houver subperfis relevantes, produza um documento unificado com tronco comum e bifurcações inline.

## 2. Estrutura

- Desenvolva as 10 seções completas.
- Mantenha exatamente a numeração e os rótulos padronizados da v3.
- Não elimine categorias estruturais porque o nicho parece simples.
- Quando uma categoria não for aplicável, explique brevemente por que não se aplica, em vez de inventar conteúdo.
- Utilize tabelas quando elas facilitarem o consumo pelas skills posteriores.

## 3. Premissas e certeza

- Use premissas somente quando faltar contexto não crítico.
- Sinalize-as com as marcações previstas na referência.
- Não apresente premissa como estatística ou fato confirmado.
- Não presuma condições comerciais, gratuidade, parcelamento, prazo de retorno, atendimento irrestrito ou política de aceitação.
- Não transforme características predominantes da persona em fatos sobre leads individuais.

## 4. MQL e SQL

- Construa primeiro a situação qualificadora central.
- Defina MQL a partir da pertinência jurídica preliminar.
- Em serviços de reconhecimento de direito, use os requisitos materiais mínimos como núcleo do MQL.
- Defina SQL a partir da permanência da aderência, delimitação dos fatos, elementos de confirmação e contexto necessário para a próxima etapa real do escritório.
- Trate documentação como elemento de confirmação ou avanço quando aplicável, não como sinônimo automático de SQL.
- Separe aderência, complexidade, prioridade, urgência, maturidade, pendências e roteamento.
- Não utilize “lead quente” como sinônimo de lead qualificado.
- Não trate curiosidade, demora para responder ou resistência ao preço como desqualificação jurídica.

## 5. Linguagem e comunicação

- Registre linguagem literal suficiente para compreensão estratégica.
- Não caricature a persona.
- Não obrigue as skills posteriores a reproduzirem erros, gírias ou abreviações.
- Diferencie a fala da persona da voz profissional adequada para se comunicar com ela.

## 6. Limites da entrega

Não crie nesta skill:

- anúncios;
- roteiros de criativos;
- ganchos finais;
- CTAs;
- posts;
- mensagens de WhatsApp;
- sequências de nutrição;
- scripts de ligação;
- respostas a objeções prontas;
- playbooks finais;
- peças jurídicas.

Na Seção 10, forneça matrizes, critérios, tensões, dúvidas, riscos, mecanismos de valor e demais insumos estruturados para as skills derivadas.

# Critérios de aceite

A entrega somente está concluída quando:

- o nicho, o serviço e o recorte estão claramente delimitados;
- as 10 seções da v3 foram desenvolvidas;
- a persona está específica para o nicho e para o contexto brasileiro;
- a persona orienta sem virar personagem individual;
- o contexto jurídico-fático foi validado em fontes oficiais atuais;
- a natureza do serviço foi classificada corretamente;
- o mecanismo de valor do serviço está explícito;
- os requisitos materiais ou condições objetivas de aderência estão claros;
- o MQL representa pertinência jurídica preliminar;
- o SQL representa pertinência desenvolvida para a próxima etapa;
- documentos, urgência, complexidade, maturidade e operação estão separados;
- existem critérios de avanço, pendência, revisão, roteamento e não aderência;
- linguagem, jornada, dores, objeções, fatores de decisão e fricções estão conectados à situação concreta;
- a Seção 10 fornece matéria-prima para todas as skills derivadas sem criar as peças finais;
- premissas e pontos de validação estão sinalizados;
- o conteúdo respeita ética e comunicação jurídica;
- a entrega não é genérica;
- o mesmo documento não poderia ser reutilizado em outro nicho apenas trocando nomes;
- as skills posteriores conseguem utilizar a maior parte do conteúdo sem refazer a pesquisa estratégica básica.


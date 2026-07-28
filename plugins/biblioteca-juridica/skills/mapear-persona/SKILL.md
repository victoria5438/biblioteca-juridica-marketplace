---
name: mapear-persona
description: Cria um Mapeamento de Persona Jurídica ultra-detalhado para alimentar marketing, vendas, atendimento e nutrição de escritórios de advocacia. Use quando o usuário pedir para mapear uma persona, público ou nicho jurídico.
argument-hint: [nicho jurídico e contexto opcional]
---

# Objetivo

Produzir o documento-fonte de Mapeamento de Persona Jurídica da Biblioteca Jurídica.

## Referências obrigatórias

Antes de produzir a saída, leia integralmente:

1. `${CLAUDE_PLUGIN_ROOT}/references/core-cognitivo.md`
2. `${CLAUDE_PLUGIN_ROOT}/references/mapeamento-persona-v2.md`

Use também, quando aplicável:

3. `${CLAUDE_PLUGIN_ROOT}/references/core-escrita-oralidade.md`

Esses arquivos integram o plugin e devem orientar a execução desta skill.

Caso algum arquivo obrigatório não esteja acessível, informe claramente qual
referência não foi localizada. Não reconstrua silenciosamente o conteúdo ausente.

# Validação jurídica obrigatória

Antes de redigir qualquer informação jurídica, faça uma verificação atualizada em fontes oficiais.

1. Trate o arquivo `mapeamento-persona-v2.md` como referência de estrutura e profundidade, não como fonte jurídica definitiva.
2. Consulte prioritariamente:
   - legislação no Portal Planalto;
   - páginas oficiais do INSS e do gov.br;
   - STF, STJ, TST ou tribunais competentes quando a jurisprudência for relevante;
   - atos normativos oficiais aplicáveis.
3. Em caso de conflito, a fonte oficial atual prevalece sobre conhecimento prévio, exemplos ou premissas.
4. Valide, no mínimo:
   - quem pode receber o direito ou benefício;
   - categorias incluídas e excluídas;
   - requisitos;
   - incompatibilidades;
   - prazos;
   - documentos;
   - vias administrativa e judicial.
5. Não crie subperfis juridicamente inelegíveis.
6. Quando não encontrar confirmação suficiente ou houver controvérsia real, use `[VALIDAR JURIDICAMENTE]` apenas no ponto específico e evite afirmação categórica.
7. Dentro da Seção 3, inclua ao final o subtítulo **Fontes oficiais consultadas**, indicando brevemente as fontes utilizadas e a data da consulta.

# Execução

- Se o nicho jurídico não estiver informado, faça apenas a pergunta inicial prevista na referência e ofereça o bloco opcional de contexto.
- Se o nicho estiver amplo demais, proponha de 2 a 3 sub-recortes e aguarde a escolha.
- Se houver subperfis relevantes, produza um documento unificado com bifurcações inline.
- Desenvolva as 10 seções completas e mantenha os rótulos padronizados.
- Use premissas realistas quando faltar contexto não crítico e sinalize-as.
- Não crie anúncios, roteiros, posts ou mensagens de funil nesta skill.

# Critérios de aceite

- O documento contém matéria-prima suficiente para as demais skills.
- Há linguagem literal, contexto jurídico, jornada, dores, objeções, critérios e síntese acionável.
- A persona está específica para o nicho e o Brasil.
- O conteúdo respeita ética e comunicação jurídica.
- A entrega não é genérica nem depende de nova pesquisa para ser utilizada pelas próximas skills.

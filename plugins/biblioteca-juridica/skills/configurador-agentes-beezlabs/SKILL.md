---
name: configurador-agentes-beezlabs
description: Configura agentes jurídicos no modo básico do BeezLabs a partir de um Mapeamento de Persona Jurídica, com curadoria humana do plano de pré-qualificação, validação de consistência, geração de Regras, Etapas, FAQ, Base de Conhecimento sanitizada e JSON final importável. Use quando for criar, adaptar, revisar ou exportar um agente BeezLabs seguindo o Padrão Mestre.
---

# Configurador de Agentes BeezLabs — Modo Básico

## Objetivo

Transformar um **Mapeamento de Persona Jurídica** em uma configuração completa, controlada e replicável de agente no **modo básico do BeezLabs**, sem depender do Formulário Guiado nem do Gerador nativo do BeezLabs.

A Skill deve produzir, ao final:

1. **JSON final do agente**, pronto para importação quando todos os dados técnicos obrigatórios estiverem confirmados.
2. **Base de Conhecimento do Agente**, sanitizada e adequada para upload na aba Documentos.
3. **Relatório curto de configuração**, com resumo das decisões adotadas e eventuais pendências.

---

# 1. Fontes de entrada

A Skill trabalha com quatro fontes, em hierarquia:

1. **Decisões humanas aprovadas** — soberanas.
2. **Perfil Técnico do Agente** — IDs, workspace, responsáveis, políticas e ações autorizadas.
3. **Padrão Mestre de Configuração** — arquitetura universal.
4. **Mapeamento de Persona Jurídica** — inteligência do nicho.
5. **JSON-base** — molde técnico de serialização.

Nunca permita que uma fonte inferior sobrescreva uma superior.

Leia:
- `references/PADRAO_MESTRE_CONFIGURACAO_AGENTE_BASICO_BEEZLABS.md`
- `references/PERFIL_TECNICO_PADRAO_AGENTE_BEEZLABS.md`
- `templates/JSON_BASE_MESTRE_AGENTE_BASICO_BEEZLABS.json`
- `templates/TEMPLATE_PERFIL_TECNICO_AGENTE_BEEZLABS.json`

---

# Integração com a Biblioteca Jurídica

Esta Skill deve coexistir com as demais Skills da Biblioteca Jurídica sem sobrepor suas responsabilidades.

- `/mapear-persona` produz o Mapeamento de Persona Jurídica que pode servir como entrada desta Skill.
- `/pre-qualificacao` pode produzir um roteiro humano de pré-qualificação; quando esse roteiro vier aprovado pelo humano, trate-o como fonte soberana e siga para a Validação de Consistência.
- Esta Skill é responsável pela **configuração automatizada do agente BeezLabs**, incluindo Regras, Etapas, FAQ, Base de Conhecimento e JSON final.
- Não altere a responsabilidade das outras Skills nem transforme esta Skill em geradora genérica de materiais jurídicos.

---

# 2. Princípios inegociáveis

## 2.1. O agente realiza o processo de qualificação; não qualifica o lead

O agente coleta e organiza informações.

Não atribua, por iniciativa própria:
- qualificado;
- desqualificado;
- elegível;
- inelegível;
- aderente;
- não aderente;
- bom caso;
- potencial cliente;
- “tem direito”;
- “não tem direito”.

Critérios estratégicos de MQL, SQL, scoring ou aderência presentes no Mapeamento são inteligência para **desenho do fluxo e revisão humana**, não rótulos executáveis pelo agente.

## 2.2. A versão humana aprovada do fluxo é soberana

O Mapeamento de Persona é fonte de inteligência, não roteiro executável.

Depois que o humano aprovar as perguntas e objetivos de coleta:
- não reinsira perguntas removidas;
- não substitua perguntas por outras “melhores” sem alertar;
- não acrescente coleta apenas porque o Mapeamento contém mais dados;
- não transforme critérios estratégicos em perguntas extras.

A validação tem **poder de alerta, não de decisão**.

## 2.3. Documentos ampliam conhecimento; não autonomia

A Base de Conhecimento serve para:
- responder dúvidas;
- explicar conceitos;
- traduzir termos;
- contextualizar procedimentos.

Ela não pode:
- criar perguntas;
- criar etapas;
- criar critérios;
- gerar veredictos;
- executar ações técnicas.

## 2.4. Etapas representam objetivos e estados, não um questionário rígido

Antes de cada pergunta:
- consolidar todo o histórico;
- identificar o que já foi respondido;
- considerar informações espontâneas e antecipadas;
- perguntar somente o próximo dado realmente pendente e aplicável.

## 2.5. Não usar o Formulário Guiado nem o Gerador BeezLabs

Esta Skill substitui essa camada.

Não use nem gere o Formulário Guiado no fluxo principal, salvo se o usuário pedir explicitamente como saída adicional ou contingência.

---

# 3. Máquina de estados da Skill

A Skill deve trabalhar por fases e **não pular aprovações humanas**.

## FASE 1 — INGESTÃO E DIAGNÓSTICO

### Entradas mínimas
- Mapeamento de Persona Jurídica.

### Entradas opcionais
- Perfil Técnico já preenchido.
- Export JSON de um agente existente.
- Fluxo de pré-qualificação já definido pelo humano.
- Regras comerciais/institucionais confirmadas.
- Outros documentos relevantes do escritório.

### Se houver export JSON existente
Extraia automaticamente, quando presentes:
- nomes de etapas;
- IDs das etapas;
- ID do funil;
- usuário responsável;
- notificação;
- gatilhos;
- parâmetros;
- políticas técnicas inferíveis com segurança.

Não peça ao usuário dados que possam ser recuperados do arquivo fornecido.

Não presuma que IDs de outro workspace sejam reutilizáveis.

---

# 4. FASE 2 — PROPOSTA DO PLANO DE PRÉ-QUALIFICAÇÃO

Se o usuário ainda não forneceu um fluxo aprovado, gere uma proposta para curadoria.

## Estrutura obrigatória

### A. Pergunta de abertura do caso
- informação que pretende identificar;
- pergunta sugerida;
- por que ela é adequada para abertura.

### B. Objetivos principais de coleta
Para cada objetivo:
- **Informação a coletar**
- **Objetivo**
- **Relevância**
- **Pergunta sugerida**
- **Quando perguntar**
- **Quando não perguntar**
- **Tratamento especial**, se existir

### C. Objetivos condicionais
Mesma estrutura, deixando explícita a condição semântica que os torna aplicáveis.

### D. Gatilhos transversais
Exemplos:
- urgência;
- pedido de humano;
- pedido de áudio/ligação;
- situação fora do escopo;
- advogado já constituído;
- recusa explícita;
- outra interrupção real.

### E. Pontos que NÃO devem virar perguntas
Liste inteligência relevante do Mapeamento que deve ficar:
- com o humano;
- na FAQ;
- na Base de Conhecimento;
- como regra;
- ou fora do agente.

## Regra de parada

Após apresentar a proposta, **pare** e peça curadoria humana.

Não gere ainda o JSON final.

---

# 5. Quando o fluxo já vier definido pelo humano

Se o usuário fornecer uma pré-qualificação já definida:

1. Trate-a como versão soberana.
2. Não gere outra em paralelo.
3. Vá diretamente para a **Validação de Consistência**.
4. Só proponha alterações como alertas, nunca como substituição silenciosa.

---

# 6. FASE 3 — VALIDAÇÃO DE CONSISTÊNCIA

Compare a versão humana com o Mapeamento de Persona.

Apresente **somente alertas relevantes**.

Pode alertar sobre:
- lacuna material importante;
- pergunta redundante;
- pergunta que mistura dois objetivos;
- pergunta que mede algo diferente do pretendido;
- pergunta condicional tratada como geral;
- dependência indevida da pergunta anterior;
- risco de indução;
- risco de conclusão jurídica;
- risco de exclusão indevida;
- informação crítica de prazo/urgência sem tratamento;
- conflito entre política humana e conhecimento do Mapeamento;
- dado sensível solicitado sem necessidade aparente.

Não transforme a validação em revisão burocrática.

Se não houver alerta significativo, diga isso claramente e prossiga para confirmação.

## Regra de decisão

A Skill nunca decide pelo usuário.

Para cada alerta, informe:
- o que foi identificado;
- por que importa;
- alternativa possível, quando útil;
- decisão que precisa ser confirmada.

Após a validação, **pare novamente** e aguarde aprovação.

---

# 7. FASE 4 — CONSTRUÇÃO DA CONFIGURAÇÃO COMPLETA

Somente execute depois de aprovação humana clara do fluxo.

A partir daí, gere os componentes abaixo.

---

# 8. REGRAS

Use a arquitetura fixa do Padrão Mestre:

1. Identidade e função do agente
2. Personalidade, tom de voz e linguagem
3. Formato e naturalidade das respostas
4. Gestão de contexto, estado e antirrepetição
5. Condução do processo de qualificação
6. Escopo, confiabilidade e limites jurídicos
7. Proibições gerais de conduta
8. Privacidade e segurança
9. Escalonamento para atendimento humano
10. Regras técnicas e controle do CRM
11. Uso da Base de Conhecimento e Documentos

## Regras universais que devem permanecer

Inclua sempre:
- uma pergunta principal por mensagem;
- uso moderado do nome;
- não usar nome em mensagens consecutivas;
- empatia contextual, não automática;
- não reagir a toda resposta com “Entendi”, “Perfeito”, “Compreendo” etc.;
- consolidação do histórico;
- antirrepetição;
- respostas antecipadas contam como coletadas;
- resposta parcial gera somente pergunta de complemento;
- “não sei” é pendência, não exclusão;
- o agente realiza o processo de qualificação, mas não emite veredito;
- não inventar;
- não prometer resultado;
- limites de CRM;
- uso restrito de Documentos.

## Regras específicas do nicho

Inclua somente quando forem princípios **globais de comportamento**.

Não transforme em Regra:
- perguntas;
- critérios de resposta;
- documentos específicos;
- bifurcações;
- scripts;
- FAQ;
- critérios de MQL/SQL.

Esses elementos pertencem às Etapas, FAQ ou Base de Conhecimento.

---

# 9. ETAPAS — ARQUITETURA PADRÃO

No modo básico, gere um único editor semântico com:

1. **BOAS-VINDAS E IDENTIFICAÇÃO**
2. **ABERTURA DO CASO**
3. **QUALIFICAÇÃO**
4. **CONCLUSÃO DA TRIAGEM**
5. **EXCLUSÃO / ENCERRAMENTO**, quando aplicável
6. **ROTEAMENTO**, quando aplicável
7. **ESCALONAMENTO HUMANO**
8. **URGÊNCIAS E GATILHOS TRANSVERSAIS**, quando aplicável

---

# 10. BOAS-VINDAS E IDENTIFICAÇÃO

Padrão:

> Olá! Seja bem-vindo(a) ao [NOME DO ESCRITÓRIO].  
> Para iniciar seu atendimento, por favor, digite seu nome abaixo.

Depois:
- registrar o nome no campo padrão quando permitido;
- não pedir novamente;
- usar preferencialmente o primeiro nome;
- executar Smart Decision de entrada apenas se autorizada no Perfil Técnico.

---

# 11. ABERTURA DO CASO

Padrão:

> Prazer, [PRIMEIRO_NOME]! Antes de te direcionar para um dos nossos especialistas, posso te fazer algumas perguntas breves? É rápido e leva menos de cinco minutos.

Depois, inserir a pergunta de abertura aprovada para o nicho.

Se a informação já estiver no histórico:
- não repetir a pergunta;
- considerar o objetivo coletado;
- avançar.

---

# 12. QUALIFICAÇÃO

Comece sempre com a instrução-mãe do Padrão Mestre.

Para cada pergunta humana aprovada, transforme em bloco semântico:

## INFORMAÇÃO A COLETAR
**Objetivo:**  
**Relevância:**  
**Quando perguntar:**  
**Pergunta sugerida:**  
**Quando não perguntar:**  
**Tratamento especial:**  

Não é obrigatório exibir todos os campos se não agregarem valor.

## Tipos de condição permitidos

### Informação pendente
“Quando X ainda não tiver sido informado.”

### Contexto conhecido
“Quando já tiver sido identificado X, independentemente de quando essa informação surgiu.”

### Gatilho transversal
“Se surgir X em qualquer momento, interrompa a sequência normal e execute Y.”

Evite estruturar lógica como:
> “Se responder à pergunta anterior...”

Prefira estado semântico da conversa.

---

# 13. EXCLUSÃO, ROTEAMENTO E ESCALONAMENTO

## Exclusão
É saída operacional aprovada, não veredito jurídico.

## Roteamento
Demanda existe, mas pertence a outro serviço/fluxo.

Nunca dizer automaticamente:
- “você não tem direito”;
- “seu caso não serve”.

## Escalonamento
Usar nas hipóteses universais e específicas aprovadas.

Após transferência definitiva:
- não continuar a qualificação;
- executar apenas as Smart Decisions autorizadas.

---

# 14. FAQ

Gere FAQ a partir do Mapeamento e das políticas confirmadas.

A FAQ deve:
- responder dúvidas previsíveis;
- ser curta e segura;
- usar linguagem do lead;
- não prometer;
- não emitir conclusão individual;
- não duplicar perguntas de qualificação;
- não criar novo fluxo.

Priorize:
- conceitos;
- funcionamento do serviço;
- documentos;
- procedimentos;
- mitos;
- objeções informacionais;
- dúvidas de prazo/custo apenas quando confirmadas.

Se informação institucional/comercial estiver pendente:
- não invente;
- omita a resposta específica;
- ou mantenha item inativo somente se o formato final suportar isso sem placeholder.

---

# 15. BASE DE CONHECIMENTO DO AGENTE

Gere um documento sanitizado derivado do Mapeamento.

## Pode conter
- conceitos jurídicos gerais;
- definições;
- funcionamento;
- documentos e função;
- etapas do procedimento;
- diferenças conceituais;
- termos técnicos traduzidos;
- mitos;
- dúvidas recorrentes;
- informações institucionais confirmadas.

## Excluir
- MQL;
- SQL;
- scoring;
- lead quente/frio;
- critérios internos de aderência;
- perguntas de qualificação não aprovadas;
- estratégia de venda;
- jornada de consciência;
- estratégia de fechamento;
- gatilhos de marketing;
- notas internas;
- `[VALIDAR JURIDICAMENTE]` não resolvidos;
- `[VALIDAR COM O ESCRITÓRIO]` não resolvidos;
- classificações que possam induzir veredito.

## Estilo
O documento deve ser:
- declarativo;
- organizado por temas;
- conciso o suficiente para recuperação eficiente;
- profundo o suficiente para responder variações de dúvidas;
- sem instruções operacionais conflitantes com Regras e Etapas.

---

# 16. PERFIL TÉCNICO

Antes da exportação final, preencha ou extraia o Perfil Técnico.

Use `templates/TEMPLATE_PERFIL_TECNICO_AGENTE_BEEZLABS.json`.

## Não pedir antecipadamente o que não é necessário

A proposta e a validação do fluxo podem acontecer sem todos os IDs.

Os IDs são obrigatórios apenas quando forem necessários para produzir um **JSON pronto para importação**.

## Nunca inventar
- ID de etapa;
- ID de usuário;
- ID de notificação;
- ID de funil;
- política de horários;
- honorários;
- endereço;
- OAB;
- condições comerciais.

---

# 17. SMART DECISIONS

Use os modelos presentes no JSON-base.

Tipos:
- `transfer_stage`
- `transfer_user`
- `notify`
- `stop_agent`

## Regras

1. Só inserir uma ação se estiver autorizada no Perfil Técnico.
2. A existência do ID não autoriza seu uso automaticamente.
3. Usar o ID real correspondente.
4. Remover tokens de funções não utilizadas.
5. Nunca deixar `data-invalid="true"` em tokens que estão sendo montados como configuração final.
6. Não criar ID fictício para “fechar” o JSON.

---

# 18. GERAÇÃO DO JSON FINAL

Use `templates/JSON_BASE_MESTRE_AGENTE_BASICO_BEEZLABS.json` como estrutura.

## Processo

1. Copiar o JSON-base.
2. Aplicar identidade e escopo.
3. Inserir Regras completas.
4. Gerar Etapas em HTML dentro de `__BASIC_ETAPA__`.
5. Substituir o FAQ modelo pelas FAQs reais.
6. Aplicar gatilhos confirmados.
7. Aplicar notificações confirmadas.
8. Aplicar parâmetros padrão + sobrescritas.
9. Inserir somente Smart Decisions autorizadas.
10. Remover seções, tokens e objetos não aplicáveis.
11. Remover todos os placeholders.
12. Validar o JSON.

---

# 19. SHIPPING GATE DO JSON

O JSON só pode ser chamado de **“pronto para importação”** se passar por todos os testes:

## Estrutura
- JSON sintaticamente válido.
- `modo_config = "basico"`.
- exatamente um nó `ETAPA`.
- título do nó = `__BASIC_ETAPA__`.
- `conexoes = []`.
- existe REGRA `__BASIC_REGRAS__`.

## Placeholders
Pesquise por:
- `[[`
- `]]`

O resultado deve ser **zero** no arquivo final.

## IDs
Todos os IDs usados em:
- `transfer_stage`;
- `transfer_user`;
- `notify`;

devem existir no Perfil Técnico confirmado ou em export real fornecido pelo usuário.

## Comportamento
- Regras universais presentes.
- Qualificação não emite veredito.
- Documentos não ampliam autonomia.
- Uma pergunta principal por mensagem.
- Antirrepetição presente.
- Uso moderado do nome presente.
- Empatia contextual presente.

## Conteúdo
- nenhuma marcação `[VALIDAR ...]` ativa;
- nenhuma condição comercial inventada;
- nenhuma FAQ sem base;
- nenhuma pergunta não aprovada introduzida na qualificação.

## Resultado da validação

Se algum requisito falhar:
- não rotule como pronto para importação;
- liste a pendência;
- gere, no máximo, um rascunho.

---

# 20. RELATÓRIO DE CONFIGURAÇÃO

Entregue um resumo curto contendo:

- nome do agente;
- escritório;
- nicho;
- pergunta de abertura;
- objetivos de coleta aprovados;
- objetivos condicionais;
- exclusões;
- roteamentos;
- urgências;
- escalonamentos;
- quantidade de FAQs;
- Smart Decisions utilizadas;
- parâmetros que divergem do padrão;
- pendências restantes.

Não transformar o relatório em nova documentação extensa.

---

# 21. HOMOLOGAÇÃO

Depois da importação, recomendar teste dos seguintes cenários:

- identificação;
- uso do nome;
- excesso de empatia;
- resposta objetiva;
- informação antecipada;
- múltiplas respostas em uma mensagem;
- resposta parcial;
- “não sei”;
- retomada após silêncio;
- antirrepetição;
- objeção;
- FAQ;
- pergunta fora da FAQ com apoio dos Documentos;
- pedido de humano;
- áudio/ligação;
- urgência;
- roteamento;
- exclusão;
- movimentação de card;
- notificação;
- transferência de responsável;
- interrupção do agente.

Não considere homologação concluída apenas porque o JSON importou.

---

# 22. Modos de uso

## Modo normal
Mapeamento → proposta → curadoria → validação → aprovação → configuração completa.

## Fluxo já aprovado
Mapeamento + fluxo humano → validação → aprovação → configuração completa.

## Agente existente
Mapeamento + export atual → extrair Perfil Técnico e estrutura existente → validar fluxo humano → gerar nova versão.

## Apenas auditoria
Se o usuário pedir somente revisão de agente:
- não reprojete automaticamente;
- compare com o Padrão Mestre;
- classifique problemas por Regras, Etapas, FAQ, Documentos, Smart Decisions e parâmetros;
- recomende correções;
- só gere nova versão se solicitado.

---

# 23. Limite de escopo da versão atual

Esta versão da Skill é oficial para **modo básico do BeezLabs**.

Não reutilize automaticamente a arquitetura técnica para o modo avançado.

O Padrão Mestre comportamental pode ser aproveitado no modo avançado, mas estrutura de nós, conexões e transições deve possuir especificação própria antes de gerar JSON avançado.

---

# 24. Regra arquitetural final

Preserve sempre:

**REGRAS = como o agente se comporta**  
**ETAPAS = o que coleta, quando coleta e o que acontece**  
**FAQ = respostas controladas**  
**DOCUMENTOS = repertório complementar**  
**SMART DECISIONS = efeitos técnicos**  
**HUMANO = interpretação jurídica/comercial final**

Se uma instrução estiver na camada errada, corrija a arquitetura antes de exportar.

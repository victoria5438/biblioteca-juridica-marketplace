---
name: configurador-agentes-beezlabs
description: Configura agentes jurídicos no modo básico do BeezLabs a partir de um Mapeamento de Persona Jurídica, com curadoria humana do plano de pré-qualificação, validação de consistência, geração de Regras, Etapas, FAQ, Base de Conhecimento sanitizada, Perfil Técnico e JSON de produção ou homologação. Use quando for criar, adaptar, revisar, auditar ou exportar um agente BeezLabs seguindo o Padrão Mestre.
---

# Configurador de Agentes BeezLabs — Modo Básico

**Versão da Skill: 10.0.1**

## Objetivo

Transformar um **Mapeamento de Persona Jurídica** e decisões humanas aprovadas em uma configuração completa, controlada, auditável e replicável de agente no **modo básico do BeezLabs**, sem depender do Formulário Guiado nem do Gerador nativo do BeezLabs.

A Skill pode produzir três níveis de saída técnica:

1. **JSON de produção** — pronto para importação quando todos os dados técnicos necessários às ações que serão executadas estiverem confirmados.
2. **JSON de homologação** — importável para testes quando o usuário autorizar expressamente a omissão de ações técnicas que dependem de dados não confirmados. Deve ter zero placeholders e ser rotulado como não produtivo.
3. **Rascunho estrutural** — não importável/final, usado quando ainda há decisões essenciais de conteúdo ou estrutura em aberto.

Entregáveis finais, conforme o modo:
- JSON do agente;
- Base de Conhecimento sanitizada para a aba Documentos;
- relatório curto de configuração, pendências e impacto operacional;
- roteiro de homologação.

---

# 1. Fontes de entrada e hierarquia

A Skill trabalha com **cinco fontes**, em hierarquia:

1. **Decisões humanas aprovadas** — soberanas.
2. **Perfil Técnico do Agente** — fatos do workspace, IDs, responsáveis, políticas e ações autorizadas.
3. **Padrão Mestre de Configuração** — arquitetura universal.
4. **Mapeamento de Persona Jurídica** — inteligência do nicho.
5. **JSON-base** — molde técnico de serialização.

Nunca permita que uma fonte inferior sobrescreva uma superior.

Leia obrigatoriamente:
- `references/PADRAO_MESTRE_CONFIGURACAO_AGENTE_BASICO_BEEZLABS.md`
- `references/PERFIL_TECNICO_PADRAO_AGENTE_BEEZLABS.md`
- `templates/JSON_BASE_MESTRE_AGENTE_BASICO_BEEZLABS.json`
- `templates/TEMPLATE_PERFIL_TECNICO_AGENTE_BEEZLABS.json`

## 1.1. Registro interno de decisões aprovadas

Mantenha durante toda a execução um **registro interno de decisões humanas vigentes**. Ele deve incluir, quando aplicável:
- perguntas aprovadas e removidas;
- ordem preferencial aprovada;
- objetivos condicionais aprovados;
- gatilhos e seus tratamentos aprovados;
- documentos autorizados;
- políticas de escalonamento, roteamento e encerramento;
- redações expressamente aprovadas;
- exceções e compensações aprovadas, como informações obrigatórias de handoff;
- decisões técnicas posteriormente confirmadas.

Esse registro serve para **rastreabilidade entre fases**. Não precisa ser apresentado como burocracia ao usuário, mas nenhuma fase posterior pode perder, substituir ou contradizer silenciosamente uma decisão registrada.

---

# Integração com a Biblioteca Jurídica

Esta Skill deve coexistir com as demais Skills da Biblioteca Jurídica sem sobrepor responsabilidades.

- `/mapear-persona` produz o Mapeamento de Persona Jurídica que pode servir como entrada.
- `/pre-qualificacao` pode produzir um roteiro humano de pré-qualificação; quando vier aprovado, trate-o como fonte soberana e vá para a Validação de Consistência.
- Esta Skill é responsável pela **configuração automatizada do agente BeezLabs**, incluindo Regras, Etapas, FAQ, Base de Conhecimento, Perfil Técnico e JSON.
- Não altere a responsabilidade das outras Skills nem transforme esta Skill em geradora genérica de materiais jurídicos.

---

# 2. Princípios inegociáveis

## 2.1. O agente realiza o processo de qualificação; não qualifica o lead

O agente coleta, organiza e encaminha informações.

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

Critérios de MQL, SQL, scoring ou aderência presentes no Mapeamento são inteligência para desenho do fluxo e revisão humana, não rótulos executáveis pelo agente.

## 2.2. A versão humana aprovada do fluxo é soberana

O Mapeamento de Persona é fonte de inteligência, não roteiro executável.

Depois que o humano aprovar perguntas, objetivos, exceções ou redações:
- não reinsira perguntas removidas;
- não substitua perguntas por outras “melhores” sem alerta e nova decisão;
- não acrescente coleta apenas porque o Mapeamento contém mais dados;
- não transforme critérios estratégicos em perguntas extras;
- não elimine compensações aprovadas em fase anterior;
- não deixe uma instrução antiga sobreviver se ela contradizer decisão humana posterior.

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
- executar ações técnicas;
- autorizar comportamento não previsto nas Regras ou Etapas.

## 2.4. Etapas representam objetivos e estados, não questionário rígido

Antes de cada pergunta:
- consolidar todo o histórico;
- identificar o que já foi respondido;
- considerar informações espontâneas e antecipadas;
- identificar o próximo dado realmente pendente e aplicável;
- perguntar somente o necessário.

## 2.5. Uma mensagem coleta no máximo uma informação independente

O padrão não é apenas “uma pergunta principal”. É **um slot independente de informação por mensagem**.

Considere duas coletas independentes quando uma resposta puder existir sem a outra. Nesse caso:
- faça a primeira pergunta;
- aguarde a resposta;
- faça o complemento somente se ainda for aplicável.

Não avalie apenas quantidade de pontos de interrogação. Uma frase sem “?” também pode solicitar duas informações.

## 2.6. FAQ responde; Etapa coleta

A FAQ pode responder, explicar, esclarecer ou recusar uma conclusão indevida.

A FAQ **não pode**:
- pedir dado novo;
- solicitar confirmação;
- pedir documento;
- pedir que o lead informe prazo, valor, nome, data ou fato;
- criar complemento de qualificação;
- abrir um minifluxo paralelo.

Se a resposta depende de informação que deve ser coletada, responda a dúvida e deixe a coleta para a Etapa correspondente.

## 2.7. Princípios universais não podem ser estreitados silenciosamente pelo nicho

Uma regra específica não pode transformar princípio universal em regra posicional sem aprovação explícita.

Exemplo: se a empatia é contextual, uma instrução de nicho não pode restringi-la a “somente no relato do motivo”.

## 2.8. Ausência de configuração não prova política

Ao ler export, campos vazios, arrays vazios, `null` ou ausência de objeto significam, por padrão, **“não configurado/não demonstrado neste arquivo”**.

Nunca converta isso automaticamente em:
- “o escritório atende 24h”;
- “o recurso é proibido”;
- “o recurso é autorizado”;
- “não há custo”;
- “não agenda”;
- qualquer outra política institucional.

Política só é confirmada por dado explícito, decisão humana ou evidência técnica inequívoca.

## 2.9. Instrução comportamental não equivale a persistência técnica

“Registre”, “salve”, “faça um handoff”, “inclua no resumo” ou expressão semelhante não garante que o BeezLabs persista esse conteúdo.

Sempre diferencie:
- **comportamento desejado do agente**;
- **mecanismo técnico existente para persistir/transportar o resultado**.

Se o mecanismo não estiver confirmado, marque a persistência como requisito de homologação. Nunca prometa que `{{resumo}}`, campo, nota ou notificação obedecerá uma estrutura apenas porque a Etapa a descreve.

## 2.10. Não usar Formulário Guiado nem Gerador BeezLabs

Esta Skill substitui essa camada no fluxo principal, salvo se o usuário pedir explicitamente uma saída adicional ou contingência.

---

# 3. Máquina de estados da Skill

A Skill trabalha por fases e **não pula aprovações humanas de conteúdo**.

Sequência oficial:

**FASE 1 Ingestão → FASE 2 Proposta → Curadoria → FASE 3 Validação → Aprovação → FASE 4 Construção → FASE 5 Auditoria cruzada → Aprovação → FASE 6 Perfil Técnico/Serialização → JSON → Homologação.**

Quando já houver fluxo humano aprovado, FASE 2 pode ser pulada. Quando o usuário pedir explicitamente um JSON de homologação com dados técnicos faltantes, a FASE 6 pode operar em modo de homologação, sem inventar ou deixar placeholders.

---

# 4. FASE 1 — INGESTÃO E DIAGNÓSTICO

## Entradas mínimas
- Mapeamento de Persona Jurídica.

## Entradas opcionais
- Perfil Técnico já preenchido;
- export JSON de agente existente;
- fluxo de pré-qualificação já definido pelo humano;
- regras comerciais/institucionais confirmadas;
- outros documentos relevantes do escritório.

## 4.1. Se houver export JSON existente

Extraia automaticamente, quando presentes e rastreáveis:
- nomes e IDs de etapas;
- ID/nome de funil;
- usuário responsável;
- notificações e destinatários;
- gatilhos;
- parâmetros;
- políticas **explicitamente declaradas**;
- recursos tecnicamente configurados.

Para cada dado extraído, preserve internamente a **proveniência**: export/arquivo, campo e, quando útil, modo do agente de origem.

Não peça ao usuário o que puder ser recuperado com segurança do arquivo.

### Regras para export de outro modo de configuração

Se o export for `avancado` e o novo agente `basico`, ou vice-versa:
- IDs e fatos do mesmo workspace podem ser reutilizados quando sua identidade técnica estiver clara;
- parâmetros podem ser reaproveitados quando compatíveis;
- políticas explícitas podem ser aproveitadas como evidência;
- **arquitetura de nós, conexões e transições não é reutilizável automaticamente**;
- nunca converta um fluxo avançado em básico copiando sua topologia.

Nunca presuma que IDs de outro workspace sejam reutilizáveis.

### Regra de ausência

Campo vazio não é política. Array vazio não é política. Ausência de configuração não confirma “sim” nem “não”.

---

# 5. FASE 2 — PROPOSTA DO PLANO DE PRÉ-QUALIFICAÇÃO

Se o usuário ainda não forneceu fluxo aprovado, gere uma proposta para curadoria.

## Estrutura obrigatória

### A. Pergunta de abertura do caso
- informação que pretende identificar;
- pergunta sugerida;
- por que é adequada para abertura.

### B. Objetivos principais de coleta
Para cada objetivo:
- **Informação a coletar**;
- **Objetivo**;
- **Relevância**;
- **Pergunta sugerida**;
- **Quando perguntar**;
- **Quando não perguntar**;
- **Tratamento especial**, se existir.

### C. Objetivos condicionais
Mesma estrutura, com condição semântica explícita.

### D. Gatilhos transversais
Exemplos:
- urgência;
- pedido de humano;
- pedido de áudio/ligação;
- situação fora do escopo;
- advogado já constituído;
- recusa explícita;
- outra interrupção real.

Para qualquer gatilho que possa gerar ação técnica, já indique conceitualmente:
- condição observável;
- efeito pretendido;
- momento do efeito;
- como tratar ambiguidade.

Não invente IDs nesta fase.

### E. Pontos que NÃO devem virar perguntas
Liste inteligência relevante do Mapeamento que deve ficar:
- com o humano;
- na FAQ;
- na Base de Conhecimento;
- como regra;
- ou fora do agente.

## 5.1. Pré-auditoria silenciosa da proposta

Antes de apresentar a FASE 2:
- verifique se cada mensagem coleta no máximo um slot independente;
- verifique se não há gatilho subjetivo com efeito técnico;
- verifique se perguntas condicionais não foram tratadas como gerais;
- verifique se não há conflito interno entre autorização de documentos, escalonamento, exclusão ou sequência;
- verifique se nenhum princípio universal foi restringido sem necessidade.

Corrija silenciosamente problemas de construção antes de mostrar a proposta.

## Regra de parada

Depois de apresentar a proposta, **pare** e peça curadoria humana. Não gere Regras completas nem JSON.

---

# 6. Quando o fluxo já vier definido pelo humano

Se o usuário fornecer pré-qualificação já definida:
1. trate-a como soberana;
2. não gere outra em paralelo;
3. registre as decisões explícitas;
4. vá diretamente para a FASE 3;
5. proponha alterações somente como alertas.

---

# 7. FASE 3 — VALIDAÇÃO DE CONSISTÊNCIA

Faça duas validações, nesta ordem.

## 7.1. Frente A — fluxo humano × Mapeamento

Compare a versão humana com o Mapeamento e alerte somente sobre questões materiais, como:
- lacuna importante;
- redundância;
- pergunta que mistura dois slots independentes;
- pergunta que mede algo diferente do objetivo;
- condicional tratada como geral;
- dependência indevida da pergunta anterior;
- risco de indução;
- risco de conclusão jurídica;
- risco de exclusão indevida;
- prazo/urgência sem tratamento;
- dado sensível desnecessário;
- conflito entre política aprovada e inteligência do Mapeamento.

## 7.2. Frente B — consistência interna pós-curadoria

Depois de incorporar decisões humanas, revise **a versão aprovada contra ela mesma** e contra decisões anteriores.

Procure especialmente:
- Regra que proíbe algo autorizado em Etapa;
- Etapa que coleta algo removido pela curadoria;
- FAQ que volta a coletar uma informação;
- Base que cria critério, pergunta ou ação;
- exceção aprovada que contradiz instrução global anterior;
- compensação aprovada que desapareceu;
- princípio universal indevidamente restringido por regra específica;
- duas instruções diferentes para o mesmo gatilho;
- saída que exige mecanismo técnico ainda inexistente, sem sinalização.

## 7.3. Regra de decisão

A Skill nunca decide pelo usuário.

Para cada alerta relevante, informe:
- o que foi identificado;
- por que importa;
- alternativa possível, quando útil;
- decisão que precisa ser confirmada.

Não transforme a validação em revisão burocrática. Se nada material existir, diga isso claramente.

Após a validação, **pare** e aguarde aprovação.

---

# 8. FASE 4 — CONSTRUÇÃO DA CONFIGURAÇÃO DE CONTEÚDO

Somente execute depois de aprovação humana clara do fluxo.

Nesta fase gere:
1. Regras;
2. Etapas;
3. FAQ;
4. Base de Conhecimento sanitizada.

**Não instancie ainda o JSON final. Não permita que a necessidade de IDs técnicos reabra ou interrompa a construção de conteúdo.**

---

# 9. REGRAS

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
- uma informação independente por mensagem;
- uso moderado do nome;
- não usar nome em mensagens consecutivas;
- empatia contextual, não automática, em qualquer etapa em que houver contexto real;
- não reagir a toda resposta com “Entendi”, “Perfeito”, “Compreendo” etc.;
- consolidação do histórico;
- antirrepetição;
- respostas antecipadas contam como coletadas;
- resposta parcial gera somente complemento;
- “não sei” é pendência, não exclusão;
- o agente realiza o processo de qualificação, mas não emite veredito;
- não inventar;
- não prometer resultado;
- limites de CRM;
- uso restrito de Documentos;
- FAQ não é camada de coleta.

## Regras específicas do nicho

Inclua somente quando forem princípios globais de comportamento.

Não transforme em Regra:
- perguntas;
- condições pontuais;
- bifurcações;
- scripts de resposta;
- itens de FAQ;
- critérios de MQL/SQL.

Documentos específicos só entram em Regra quando o objetivo for delimitar autorização global de coleta; o pedido concreto continua na Etapa.

---

# 10. ETAPAS — ARQUITETURA PADRÃO

No modo básico, gere um único editor semântico com, quando aplicável:
1. abertura/identificação;
2. abertura do caso;
3. qualificação;
4. conclusão da triagem;
5. exclusão/encerramento;
6. roteamento;
7. escalonamento humano;
8. urgências e gatilhos transversais;
9. handoff/repasse interno, quando aprovado e necessário.

## 10.1. Identificação depende da origem do contato

Não presuma que o lead precisa informar o nome.

Antes de escrever a abertura, determine:
- o agente inicia ou responde o contato?
- o nome já vem confiavelmente do CRM/formulário?
- o nome precisa ser coletado?

Se o nome já existe, não peça novamente. Se não existir e a coleta for necessária/autorizada, solicite uma vez. Não prometa registro em campo se o mecanismo técnico não estiver confirmado.

## 10.2. Abertura do caso

A pergunta “posso fazer algumas perguntas?” pode ser cortesia, quando aprovada; não transforme automaticamente em condição de avanço.

Não pré-classifique produto, caso ou natureza jurídica antes da coleta correspondente.

---

# 11. QUALIFICAÇÃO

Comece com a instrução-mãe do Padrão Mestre.

Para cada pergunta humana aprovada, transforme em bloco semântico:

## INFORMAÇÃO A COLETAR
**Objetivo:**  
**Relevância:**  
**Quando perguntar:**  
**Pergunta sugerida:**  
**Quando não perguntar:**  
**Tratamento especial:**

Não é obrigatório exibir todos os campos se não agregarem valor.

## Regra de slot independente

Se uma redação pedir duas informações que podem ser respondidas separadamente, divida em:
- pergunta inicial;
- complemento condicional, em outra mensagem.

## Tipos de condição permitidos

### Informação pendente
“Quando X ainda não tiver sido informado.”

### Contexto conhecido
“Quando já tiver sido identificado X, independentemente de quando surgiu.”

### Gatilho transversal
“Se surgir X em qualquer momento, execute Y.”

Evite “se responder à pergunta anterior...”. Prefira estado semântico.

---

# 12. EXCLUSÃO, ROTEAMENTO E ESCALONAMENTO

## Exclusão
É saída operacional aprovada, não veredito jurídico.

## Roteamento
Demanda existe, mas pertence a outro serviço/fluxo. Nunca dizer automaticamente “você não tem direito” ou “seu caso não serve”.

## Escalonamento
Usar nas hipóteses universais e específicas aprovadas.

Após transferência definitiva:
- não continuar qualificação;
- executar apenas Smart Decisions autorizadas.

Se houver instrução de handoff, não presuma que a transferência ou notificação transportará o conteúdo sem mecanismo técnico confirmado.

---

# 13. GATILHOS TRANSVERSAIS DETERMINÍSTICOS

Todo gatilho que muda estado, prioridade ou executa Smart Decision deve declarar quatro elementos:

1. **Condição observável** — fato detectável na conversa.
2. **Efeito** — continuar, interromper, escalonar, rotear, notificar etc.
3. **Momento** — imediatamente, após complemento, após conclusão, ou outro momento definido.
4. **Ambiguidade** — o que fazer quando a condição não puder ser confirmada com segurança.

Evite termos como:
- “muito recente”;
- “muito antigo”;
- “urgência real”;
- “se houver espaço na conversa”;
- “quando parecer grave”.

Se o conceito jurídico não puder ser transformado em critério objetivo aprovado, use uma bifurcação de **incerteza → revisão humana**, em vez de inventar limiar.

---

# 14. FAQ

Gere FAQ a partir do Mapeamento, das decisões aprovadas e das políticas confirmadas.

A FAQ deve:
- responder dúvidas previsíveis;
- ser curta e segura;
- usar linguagem do lead;
- não prometer;
- não emitir conclusão individual;
- não duplicar perguntas de qualificação;
- não criar fluxo;
- **não coletar informação**.

Antes de aceitar cada item, aplique este teste:

1. A resposta termina pedindo ao lead que informe algo novo?
2. A resposta solicita documento, confirmação, data, valor, prazo, nome ou fato?
3. A resposta cria uma próxima pergunta que pertence às Etapas?

Se qualquer resposta for “sim”, remova a coleta da FAQ e deixe-a na Etapa correspondente.

Se informação institucional/comercial estiver pendente:
- não invente;
- use resposta genérica segura somente se ela estiver autorizada;
- ou omita o item específico.

---

# 15. BASE DE CONHECIMENTO DO AGENTE

Gere documento sanitizado derivado do Mapeamento.

## Pode conter
- conceitos jurídicos gerais;
- definições;
- funcionamento;
- documentos e função;
- etapas de procedimento;
- diferenças conceituais;
- termos técnicos traduzidos;
- mitos;
- dúvidas recorrentes;
- informações institucionais confirmadas.

## Excluir
- MQL/SQL/scoring;
- lead quente/frio;
- critérios internos de aderência;
- perguntas não aprovadas;
- estratégia de venda/fechamento;
- jornada de consciência;
- gatilhos de marketing;
- notas internas;
- validações pendentes;
- classificações que induzam veredito;
- informações institucionais não confirmadas;
- instruções de ação técnica.

## Teste obrigatório de sanitização por bloco

Para cada bloco, responda:
1. **Isso é conhecimento declarativo?** Se não, provavelmente está na camada errada.
2. **Isso pode induzir nova pergunta, decisão, veredito ou ação?** Se sim, reescreva ou exclua.
3. **Isso contém algo que o agente não está autorizado a comunicar?** Se sim, exclua ou transforme em limite interno fora do Documento.

O documento deve ser declarativo, organizado, recuperável e sem instruções operacionais conflitantes.

---

# 16. FASE 5 — AUDITORIA CRUZADA PÓS-CONSTRUÇÃO

Antes de solicitar/aplicar o Perfil Técnico final, faça uma auditoria de **continuidade e fronteiras** entre:
- registro de decisões humanas;
- Regras;
- Etapas;
- FAQ;
- Base de Conhecimento.

Verifique obrigatoriamente:
- cada decisão humana vigente foi materializada;
- nenhuma pergunta removida reapareceu;
- nenhuma compensação/handoff aprovado desapareceu;
- nenhuma Regra contradiz uma Etapa;
- FAQ responde e não coleta;
- Documento conhece e não decide;
- toda mensagem de coleta respeita um slot independente;
- gatilhos com efeitos técnicos são determinísticos;
- princípios universais não foram estreitados sem aprovação;
- nenhum comportamento descrito como persistente depende de mecanismo técnico ainda não demonstrado.

## Regra de parada da FASE 5

Se houver conflito material, apresente-o e aguarde decisão humana.

Se não houver, apresente uma síntese curta e peça **aprovação da configuração de conteúdo** antes de serializar o JSON.

---

# 17. FASE 6 — PERFIL TÉCNICO

Somente depois da FASE 5 aprovada, consolide/extrate o Perfil Técnico final.

Use `templates/TEMPLATE_PERFIL_TECNICO_AGENTE_BEEZLABS.json`.

## 17.1. Estados dos dados técnicos

Trate cada informação como:
- **confirmada** — informada pelo humano ou explicitamente demonstrada;
- **extraída** — obtida de export real, com proveniência;
- **padrão técnico** — valor seguro definido no JSON-base para parâmetro, não política;
- **não confirmada** — `null`/ausente;
- **não aplicável** — somente quando isso tiver sido definido de forma explícita.

Não transforme `null` em `false` nem campo vazio em política.

## 17.2. Nunca inventar
- ID de etapa;
- ID de usuário;
- ID de notificação;
- ID de funil;
- política de horários;
- honorários;
- endereço;
- OAB;
- condições comerciais;
- autorização de ação técnica.

## 17.3. Proveniência em export

Quando extrair informação de agente existente, registre internamente:
- arquivo/export de origem;
- modo do agente de origem;
- campo que sustenta a informação;
- eventual conflito encontrado.

Export é evidência técnica; não é soberano sobre decisão humana aprovada.

---

# 18. SMART DECISIONS

Use os modelos presentes no JSON-base.

Tipos:
- `transfer_stage`
- `transfer_user`
- `notify`
- `stop_agent`

## Regras
1. Só inserir ação autorizada.
2. A existência do ID não autoriza seu uso.
3. Usar ID real rastreável.
4. Remover tokens de funções não utilizadas.
5. Nunca deixar `data-invalid="true"` na configuração entregue como importável.
6. Não criar ID fictício.
7. Cada token deve corresponder a gatilho/estado com condição, efeito e momento definidos.
8. Se uma ação depende de ID ausente, isso não autoriza substituir por outra etapa “parecida”.

## Persistência e notificações

Antes de afirmar que um handoff estruturado será salvo/enviado:
- identifique qual mecanismo técnico transporta o conteúdo;
- diferencie `{{resumo}}` automático de um resumo estrutural exigido pela Etapa;
- se não houver garantia, registre teste obrigatório de homologação.

---

# 19. GERAÇÃO TÉCNICA DO JSON

Use `templates/JSON_BASE_MESTRE_AGENTE_BASICO_BEEZLABS.json` como molde.

## 19.1. JSON de produção

Use quando todos os dados necessários às ações que permanecerão no arquivo estiverem confirmados.

Processo:
1. copiar o JSON-base;
2. aplicar identidade e escopo;
3. inserir Regras aprovadas;
4. gerar Etapas em HTML dentro de `__BASIC_ETAPA__`;
5. substituir FAQ modelo pelas FAQs reais;
6. aplicar gatilhos confirmados;
7. aplicar notificações confirmadas;
8. aplicar parâmetros padrão + sobrescritas confirmadas;
9. inserir somente Smart Decisions autorizadas;
10. remover objetos/tokens não aplicáveis;
11. remover todos os placeholders;
12. validar JSON;
13. executar shipping gate.

## 19.2. JSON de homologação

Só use quando o usuário **autorizar expressamente** seguir sem dados técnicos necessários a algumas ações.

Regras:
- nunca inventar ID;
- nunca deixar placeholder;
- remover **somente a ação técnica dependente do dado ausente**, preservando comportamento e outras ações independentes quando autorizadas;
- não substituir silenciosamente a etapa ausente por outra;
- listar cada ação omitida, motivo e impacto;
- rotular claramente como **JSON DE HOMOLOGAÇÃO — NÃO PRODUÇÃO**;
- indicar quais cenários técnicos não poderão ser validados;
- passar pelo shipping gate adaptado.

Exemplo: se `transfer_stage` não puder ser montado por falta de ID, mas `transfer_user`, `notify` e `stop_agent` estiverem confirmados e autorizados, os três podem permanecer no ponto correto.

## 19.3. Rascunho estrutural

Use quando ainda houver decisão essencial de conteúdo, gatilho ou arquitetura em aberto. Pode conter marcações internas para revisão, mas **não deve ser apresentado como importável**.

---

# 20. SHIPPING GATE DO JSON

O JSON só pode ser rotulado conforme o modo se passar pelos testes correspondentes.

## Estrutura
- JSON sintaticamente válido;
- `modo_config = "basico"`;
- exatamente um nó `ETAPA`;
- título `__BASIC_ETAPA__`;
- `conexoes = []`;
- REGRA `__BASIC_REGRAS__` presente.

## Placeholders e resíduos
Pesquisar:
- `[[`
- `]]`
- `[VALIDAR`
- `data-invalid="true"`
- marcadores de trabalho temporários.

Produção e homologação importável exigem resultado zero.

## IDs e proveniência
Todos os IDs de `transfer_stage`, `transfer_user` e `notify` devem existir no Perfil confirmado ou em export real compatível do mesmo workspace.

Nenhum ID pode ser inferido por semelhança de nome.

## Rastreabilidade das decisões
- todas as decisões humanas vigentes aparecem onde deveriam;
- nenhuma decisão aprovada foi perdida entre fases;
- nenhuma pergunta removida reapareceu;
- nenhuma redação expressamente fixada foi alterada sem nova decisão.

## Fronteiras de camada
- Regras = comportamento global;
- Etapas = coleta/estado/processo;
- FAQ = resposta, sem coleta;
- Documentos = conhecimento, sem autorização;
- Smart Decisions = efeitos técnicos;
- persistência = somente quando houver mecanismo técnico.

## Consistência cruzada
- nenhuma Regra contradiz Etapa;
- nenhuma FAQ cria objetivo de coleta;
- nenhum Documento cria pergunta, critério, veredito ou ação;
- nenhuma regra específica restringe princípio universal sem aprovação;
- autorização de documento está consistente em todas as camadas.

## Conversação
- uma informação independente por mensagem;
- antirrepetição;
- uso moderado do nome;
- empatia contextual;
- respostas antecipadas e parciais tratadas corretamente.

## Gatilhos
Para cada gatilho que executa ação:
- condição observável;
- efeito definido;
- momento definido;
- tratamento de ambiguidade definido quando necessário.

## Políticas
- nenhuma política institucional derivada apenas de campo vazio/array vazio;
- nenhum honorário, SLA, horário, abrangência ou condição comercial inventado.

## Persistência
Se houver requisito de handoff, nota, resumo ou campo:
- mecanismo técnico confirmado; **ou**
- requisito explícito de homologação registrado.

## Relatório
- contagens de FAQs, gatilhos, tokens e ações devem ser **derivadas do artefato final**, não digitadas por estimativa;
- relatório deve diferenciar presente, omitido, pendente e não aplicável.

## Resultado

### Produção
Se requisito obrigatório de produção falhar, não rotule como pronto para produção.

### Homologação
Pode ser aprovado para homologação se:
- omissões técnicas forem deliberadas/autorizadas;
- nenhuma ação dependente estiver montada com dado fictício;
- impacto estiver documentado;
- zero placeholders permanecerem.

---

# 21. RELATÓRIO DE CONFIGURAÇÃO

Entregue resumo curto contendo:
- nome do agente;
- escritório;
- nicho;
- modo técnico: produção / homologação / rascunho;
- pergunta de abertura;
- objetivos principais e condicionais;
- exclusões, roteamentos, urgências e escalonamentos;
- quantidade de FAQs **calculada do artefato**;
- Smart Decisions presentes por tipo e ID;
- ações deliberadamente omitidas e impacto;
- parâmetros que divergem do padrão;
- pendências de produção;
- requisitos obrigatórios de homologação.

Não transforme o relatório em nova documentação extensa.

---

# 22. HOMOLOGAÇÃO

Importar não é homologar.

Depois da importação, testar no mínimo:
- identidade e origem do contato;
- disponibilidade/ausência de nome no CRM;
- uso moderado do nome;
- uma informação independente por mensagem;
- resposta objetiva sem “Entendi/Perfeito” automático;
- empatia com e sem contexto emocional;
- informação antecipada;
- múltiplas respostas numa mensagem;
- resposta parcial;
- “não sei”;
- retomada após silêncio;
- FAQ;
- pergunta fora da FAQ com apoio de Documentos;
- FAQ que poderia tentar coletar informação;
- pedido de humano;
- áudio/ligação;
- gatilho claramente positivo, claramente negativo e ambíguo quando houver limiar;
- urgência;
- roteamento;
- exclusão;
- movimentação de card disponível no modo testado;
- notificação;
- transferência de responsável;
- interrupção do agente;
- documentos autorizados e vedados;
- **persistência do handoff/resumo**.

## 22.1. Teste de persistência

Se a configuração depender de `{{resumo}}`, nota, campo ou mensagem interna:
- compare o conteúdo realmente persistido/enviado com a estrutura exigida;
- verifique se informações críticas e advertências não foram descartadas;
- se o mecanismo não reproduzir o necessário, a produção fica bloqueada até solução técnica ou revisão da exigência.

---

# 23. Modos de uso

## Modo normal
Mapeamento → proposta → curadoria → validação → construção → auditoria cruzada → aprovação → Perfil Técnico → JSON.

## Fluxo já aprovado
Mapeamento + fluxo humano → validação → construção → auditoria cruzada → aprovação → Perfil Técnico → JSON.

## Agente existente
Mapeamento + export atual → extrair fatos técnicos com proveniência → não copiar arquitetura incompatível entre modos → validar fluxo humano → construir nova versão.

## JSON de homologação com dados técnicos faltantes
Depois da configuração de conteúdo aprovada, se o usuário decidir testar sem determinados IDs: omitir apenas as ações dependentes, preservar ações independentes, zero placeholders, relatório de impacto e rótulo explícito de homologação.

## Apenas auditoria
Se o usuário pedir somente revisão:
- não reprojete automaticamente;
- compare com o Padrão Mestre;
- classifique problemas por Regras, Etapas, FAQ, Documentos, Smart Decisions, parâmetros e persistência;
- recomende correções;
- só gere nova versão se solicitado.

---

# 24. Limite de escopo da versão atual

Esta versão é oficial para **modo básico do BeezLabs**.

Não reutilize automaticamente arquitetura técnica para modo avançado.

O Padrão Mestre comportamental pode ser aproveitado, mas nós, conexões e transições do modo avançado exigem especificação própria antes de gerar JSON avançado.

---

# 25. Regra arquitetural final

Preserve sempre:

**REGRAS = como o agente se comporta**  
**ETAPAS = o que coleta, quando coleta e o que acontece**  
**FAQ = respostas controladas, sem coleta**  
**DOCUMENTOS = repertório complementar, sem autorização nova**  
**SMART DECISIONS = efeitos técnicos**  
**PERFIL TÉCNICO = fatos, IDs, políticas confirmadas e autorizações**  
**PERSISTÊNCIA = mecanismo técnico comprovado ou requisito de homologação**  
**HUMANO = interpretação jurídica/comercial final**

Se uma instrução estiver na camada errada, corrija a arquitetura **antes** da serialização.

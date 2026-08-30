# PERFIL TÉCNICO DO AGENTE — PADRÃO BEEZLABS

**Versão do perfil: 10.0.1**

## 1. Finalidade

O Perfil Técnico reúne as informações que **não devem ser inferidas do Mapeamento de Persona** e que são necessárias para transformar o JSON-base mestre em um agente realmente importável no BeezLabs.

Ele não substitui o Mapeamento de Persona e não contém a estratégia de qualificação.

Sua função é fornecer à Skill:

- identidade operacional do agente;
- estrutura do workspace;
- IDs reais;
- responsáveis e notificações;
- políticas operacionais do escritório;
- configurações técnicas que diferem do padrão;
- informações institucionais confirmadas que podem aparecer no atendimento.

---

# 2. Princípio de preenchimento

O Perfil Técnico deve ser o mais curto possível e conter apenas fatos operacionais/sistêmicos necessários.

A Skill trabalha com cinco estados de informação:

## CONFIRMADO
Informado ou aprovado expressamente pelo humano.

## EXTRAÍDO
Obtido de export real, com proveniência rastreável.

## PADRÃO TÉCNICO
Valor seguro do JSON-base aplicável a parâmetro técnico. Não é política institucional.

## NÃO CONFIRMADO
Representado por `null`, string vazia ou ausência controlada. **Nunca converter automaticamente em `false`.**

## NÃO APLICÁVEL
Usar somente quando a não aplicação tiver sido expressamente confirmada ou decorrer de decisão técnica aprovada.

A Skill nunca deve inventar IDs, usuários, etapas, notificações, horários, honorários, autorizações ou políticas internas.

### Regra crítica para booleanos

- `true` = confirmado/autorizado.
- `false` = confirmado como não autorizado/não aplicável.
- `null` = desconhecido/não confirmado.

**`false` não é valor padrão para desconhecido.**

### Proveniência

Sempre que um dado vier de export, manter internamente:
- arquivo/export de origem;
- modo de configuração do agente de origem;
- campo ou objeto que sustenta o dado;
- observação de conflito, quando houver.

---

# 3. BLOCO A — IDENTIFICAÇÃO DO AGENTE

### Obrigatórios

**Nome do escritório**  
Ex.: Silva & Souza Advocacia

**Nome público do agente**  
Nome utilizado na conversa com o lead.  
Ex.: Clara

**Nome técnico do agente no BeezLabs**  
Ex.: AGENTE PRINCIPAL - REVISIONAL

**Serviço / nicho atendido**  
Ex.: Revisional de juros bancários

**Escopo resumido do agente**  
Uma frase delimitando exatamente o que esse agente atende.  
Ex.: Primeiro atendimento de consumidores com contratos bancários para análise revisional de juros e encargos.

### Opcionais

**Descrição técnica do agente**  
Se não informada, a Skill cria uma descrição curta a partir do nicho e do objetivo.

**Cuidados de linguagem específicos do público**  
Ex.: evitar infantilização; falar diretamente com cuidador; evitar termos técnicos sem tradução.

---

# 4. BLOCO B — ESTRUTURA DO FUNIL / CRM

Este bloco informa à Skill quais Smart Decisions devem ser inseridas no JSON.

## Obrigatórios quando houver movimentação automática

Para cada etapa utilizada, informar:

- nome da etapa;
- ID real da etapa;
- finalidade da etapa.

Estrutura mínima recomendada:

### Etapa inicial
**Nome:**  
**ID:**  

Usada após identificação/entrada do lead.

### Etapa de qualificação
**Nome:**  
**ID:**  

Usada quando o atendimento entra efetivamente em triagem.

### Etapa de conclusão
**Nome:**  
**ID:**  

Usada quando a coleta termina e o atendimento segue para análise humana.

### Etapa de encerramento/perdido
**Nome:**  
**ID:**  

Usada somente quando houver hipóteses operacionais aprovadas de encerramento.

## Condicionais

### Etapa de roteamento
Preencher se demandas fora do escopo forem movidas para uma etapa específica.

**Nome:**  
**ID:**  

### Etapa de urgência
Preencher apenas se urgências possuírem etapa específica.

**Nome:**  
**ID:**  

### Etapa de escalonamento
Preencher apenas se o escalonamento humano utilizar uma etapa diferente da conclusão ou roteamento.

**Nome:**  
**ID:**  

### ID do funil
Informar quando necessário para conferência, documentação ou futuras ações técnicas.

**Nome do funil:**  
**ID do funil:**  

---

## 4.1. Regra de extração por export

Quando houver export de agente existente:

- reutilize IDs somente quando o export for do mesmo workspace ou isso estiver confirmado;
- valores explícitos podem ser classificados como EXTRAÍDOS;
- campos vazios, arrays vazios e objetos ausentes não confirmam política;
- um export em modo avançado pode fornecer fatos do workspace para um agente básico, mas **não autoriza copiar arquitetura de nós/conexões**;
- conflito entre nome do funil, ID ou outra referência deve permanecer pendente até confirmação;
- export é evidência técnica, não substitui decisão humana aprovada.

---

# 5. BLOCO C — ESCALONAMENTO HUMANO

## Obrigatório quando houver transferência automática

**Nome do responsável ou equipe:**  
**ID do usuário no BeezLabs:**  

A Skill deve usar esse usuário apenas nas hipóteses de escalonamento definidas nas Etapas.

## Condicional — Notificação

Se o escalonamento exigir notificação:

**Nome da notificação:**  
**ID da notificação:**  

**Template da notificação:**  
Se não informado e o workspace aceitar o padrão, usar:

Lead {{nome}} {{telefone}} transferido para atendimento humano.

{{resumo}}

## Política de escalonamento

Informar somente particularidades que não façam parte do padrão universal.

Exemplos:
- todo pedido de áudio transfere;
- atendimento de reclamação vai para determinada pessoa;
- determinado serviço fora do escopo vai para outro setor.

---

## Persistência do repasse / resumo

Se notificações, transferências ou conclusão dependerem de handoff estruturado, registrar separadamente:
- mecanismo esperado (`{{resumo}}`, nota interna, campo, mensagem interna etc.);
- se a persistência já foi tecnicamente confirmada;
- quais elementos do handoff são críticos;
- requisito de homologação quando ainda não houver garantia.

Não presumir que `{{resumo}}` automático obedecerá à estrutura sem teste.

---

# 6. BLOCO D — POLÍTICAS OPERACIONAIS DO ESCRITÓRIO

Essas informações não devem ser inventadas pela Skill.

Preencher somente o que estiver confirmado. Campo vazio/array vazio em export **não** responde sim/não. Se a política não estiver demonstrada, mantenha `null`/pendente.

## Atendimento humano
**Atendimento humano disponível?** sim / não  
**Horário, se houver:**  

## Áudio
**O agente pode receber áudio?** sim / não  
**O agente pode responder em áudio?** sim / não  
**Pedido de resposta em áudio gera escalonamento?** sim / não  

## Ligação
**Pedido de ligação gera escalonamento?** sim / não  

## Agendamento
**Agendamento habilitado?** sim / não  
Se sim:
- tipo de agenda;
- responsável;
- regras;
- duração;
- antecedência;
- restrições.

## Horários do agente
**Agente atende 24h?** sim / não  
Se não:
- dias;
- horário;
- comportamento fora do horário.

## Pós-intervenção humana
**O agente deve permanecer pausado após intervenção humana?** sim / não  
**Tempo de intervenção, se aplicável:**  

---

# 7. BLOCO E — INFORMAÇÕES INSTITUCIONAIS CONFIRMADAS

Este bloco serve para alimentar FAQ e Base de Conhecimento quando o Mapeamento de Persona indicar pontos dependentes do escritório.

Preencher somente informações que o agente esteja autorizado a informar.

## Escritório
**Cidade/UF:**  
**Endereço:**  
**Atendimento presencial:** sim / não  
**Atendimento online:** sim / não  
**Abrangência territorial:**  

## Canais
**Telefone:**  
**WhatsApp:**  
**E-mail:**  
**Site:**  
**Instagram:**  

## Identificação profissional
**Nome do advogado responsável:**  
**OAB:**  

## Comercial
**Pode informar honorários no primeiro atendimento?** sim / não  

Se sim:
- modelo de cobrança;
- valor;
- parcelamento;
- consulta;
- êxito;
- custas/despesas.

Se não:
- usar resposta genérica de encaminhamento para equipe responsável.

## Outras políticas
Exemplos:
- política de consulta;
- remarcação;
- documentação;
- assinatura;
- atendimento nacional;
- serviços não atendidos.

---

# 8. BLOCO F — GATILHOS DE ENTRADA

Condicional.

Preencher quando o agente for ativado por frases específicas de campanha ou integração.

Para cada gatilho:

**Texto:**  
**Tipo:** CONTEM / EXATO / COMECA_COM  
**Ativo:** sim / não  

A Skill não deve inventar frases de gatilho técnico apenas porque existem anúncios ou campanhas no Mapeamento de Persona.

---

# 9. BLOCO G — PARÂMETROS TÉCNICOS

Se nenhum valor for informado, a Skill deve usar o padrão do JSON-base mestre.

## Padrões atuais

**Modo:** básico  
**Temperatura:** 0.5  
**Max tokens:** 4096  
**Resumo automático:** ativo  
**Detecção de sentimento:** ativa  
**Debounce:** 45000 ms  
**Delay mínimo:** 1000 ms  
**Delay máximo:** 3000 ms  
**Máximo de mensagens sem resposta:** 5  
**Histórico de mensagens:** 10  
**Nível máximo de risco:** 0.8  
**Tempo de intervenção:** 1440 min  
**Geração de imagem:** desabilitada  

## Sobrescritas

Preencher somente quando algum agente precisar divergir do padrão:

**Temperatura:**  
**Max tokens:**  
**Debounce:**  
**Delay mínimo:**  
**Delay máximo:**  
**Histórico:**  
**Mensagens sem resposta:**  
**Nível de risco:**  
**Tempo de intervenção:**  
**Outros:**  

---

# 10. BLOCO H — AÇÕES TÉCNICAS AUTORIZADAS

A Skill deve saber não apenas quais IDs existem, mas **quais ações estão autorizadas**.

Cada ação deve ter um estado explícito:
- `true` = autorizada;
- `false` = explicitamente não autorizada/não aplicável;
- `null` = ainda não decidida.

A existência de um ID **não autoriza automaticamente seu uso**.

Mapear, quando aplicável:
- mover para etapa inicial;
- mover para qualificação;
- mover para conclusão;
- mover para encerramento;
- mover para roteamento;
- mover para urgência/escalonamento;
- atribuir usuário por tipo de saída;
- notificar por tipo de saída;
- interromper após conclusão;
- interromper após exclusão;
- interromper após escalonamento/roteamento;
- outras ações específicas.

Quando uma mesma ação variar por gatilho, registrar a autorização no nível necessário para não generalizar indevidamente.

---

# 11. CAMPOS MÍNIMOS PARA SAÍDA TÉCNICA

## 11.1. JSON de produção

Para um agente com movimentação e escalonamento, confirmar todos os dados necessários **às ações que permanecerão no arquivo**, incluindo:
- identidade do agente/escritório;
- serviço e escopo;
- IDs/nome das etapas efetivamente utilizadas;
- funil quando necessário para conferência/ação;
- usuário responsável quando houver transferência;
- notificação quando houver `notify`;
- autorização de cada ação;
- gatilho de entrada quando exigido;
- políticas que apareçam na conversa.

Não é necessário exigir ID de função que foi expressamente definida como não aplicável.

## 11.2. JSON de homologação

Pode ser gerado com dado técnico faltante **somente por decisão expressa do usuário**. Nesse caso:
- remover a ação dependente do dado ausente;
- preservar ações independentes confirmadas;
- não usar placeholder;
- não substituir por ID/etapa semelhante;
- registrar ação omitida, motivo, impacto e cenário que não poderá ser homologado;
- rotular como homologação, não produção.

---

# 12. COMPORTAMENTO DA SKILL DIANTE DE INFORMAÇÕES AUSENTES

## Se faltar informação estratégica
Use o Mapeamento ou apresente alerta de consistência.

## Se faltar decisão de pré-qualificação
Proponha e aguarde curadoria humana.

## Se faltar informação institucional
Não invente. Remova informação específica da FAQ/Base ou mantenha a política como `null`/pendente. Não transforme ausência em “não”.

## Se faltar ID técnico necessário
Há três caminhos:

1. **Produção** — aguardar confirmação e somente depois gerar JSON de produção.
2. **Homologação autorizada** — omitir apenas a ação dependente, zero placeholders, documentar impacto e rotular como homologação.
3. **Rascunho** — quando a estrutura/conteúdo ainda não estiver fechada.

## Se uma função não for usada
Remover token, bloco ou objeto correspondente. Não deixar placeholder técnico.

## Se houver requisito de persistência não confirmado
Não declarar que o dado será salvo/enviado. Registrar item de homologação e indicar o mecanismo que precisa ser verificado.

---

# 13. HIERARQUIA DAS FONTES

Ao gerar o agente, a Skill deve obedecer à seguinte hierarquia:

### 1. Decisões humanas aprovadas
Fluxo, perguntas, políticas e exceções confirmadas.

### 2. Perfil Técnico
IDs, workspace, responsáveis, ações e políticas operacionais.

### 3. Padrão Mestre de Configuração
Arquitetura e regras universais.

### 4. Mapeamento de Persona
Fonte de inteligência e conhecimento do nicho.

### 5. JSON-base
Molde técnico de serialização/importação.

O Mapeamento de Persona não pode sobrescrever decisão humana aprovada nem dado técnico do Perfil.

---

# 14. SAÍDAS ESPERADAS DA SKILL

Depois de aprovado o conteúdo e consolidado o Perfil Técnico, a Skill pode entregar:

### 1. JSON de produção
- zero placeholders;
- IDs reais e rastreáveis;
- modo básico;
- ações autorizadas;
- validado pelo shipping gate completo.

### 2. JSON de homologação
- zero placeholders;
- somente IDs confirmados;
- ações dependentes de dados ausentes removidas;
- relatório explícito de omissões e impacto;
- rótulo “não produção”.

### 3. Base de Conhecimento
Documento sanitizado derivado do Mapeamento.

### 4. Relatório curto
Resumo de configuração, proveniência técnica relevante, ações presentes/omitidas, pendências e requisitos de homologação. Contagens devem ser derivadas do artefato final.

---

# 15. REGRA FINAL DO PERFIL TÉCNICO

O Perfil Técnico contém apenas o que é **factual, operacional ou sistêmico**. Ele não vira novo briefing estratégico.

A estratégia vem do Mapeamento e da curadoria humana.

O Perfil responde:

**“Em qual workspace este agente vai operar, quais dados estão realmente confirmados, quais ações estão autorizadas e quais requisitos técnicos ainda precisam ser homologados?”**

Princípio final: **desconhecido é `null`; `false` é decisão negativa explícita; ausência de configuração não é política.**


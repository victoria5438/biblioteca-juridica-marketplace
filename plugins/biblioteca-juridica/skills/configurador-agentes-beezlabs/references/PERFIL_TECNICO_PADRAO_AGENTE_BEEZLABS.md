# PERFIL TÉCNICO DO AGENTE — PADRÃO BEEZLABS

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

O Perfil Técnico deve ser o mais curto possível.

A Skill deve trabalhar com três categorias de campo:

## OBRIGATÓRIO
Sem essa informação, o JSON final não pode ser considerado pronto para importação.

## CONDICIONAL
Só é necessário quando determinada função for usada.

## OPCIONAL / PADRÃO
Se não for informado, a Skill utiliza o valor definido no JSON-base mestre.

A Skill **nunca deve inventar IDs, usuários, etapas, notificações, horários, honorários ou políticas internas**.

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

# 6. BLOCO D — POLÍTICAS OPERACIONAIS DO ESCRITÓRIO

Essas informações não devem ser inventadas pela Skill.

Preencher somente o que estiver confirmado.

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

Marcar:

- [ ] mover para etapa inicial após identificação
- [ ] mover para etapa de qualificação
- [ ] mover para etapa de conclusão
- [ ] mover para perdido/encerramento
- [ ] mover para etapa de roteamento
- [ ] mover para etapa de urgência
- [ ] atribuir usuário no escalonamento
- [ ] notificar no escalonamento
- [ ] interromper agente após conclusão
- [ ] interromper agente após exclusão
- [ ] interromper agente após escalonamento
- [ ] outra ação: __________________

A existência de um ID no Perfil Técnico **não autoriza automaticamente seu uso**.

---

# 11. CAMPOS MÍNIMOS PARA GERAR O JSON FINAL

Para um agente básico típico com movimentação de CRM e escalonamento humano, o conjunto mínimo é:

1. Nome do escritório
2. Nome público do agente
3. Nome técnico do agente
4. Serviço/nicho
5. Escopo resumido
6. ID + nome da etapa inicial
7. ID + nome da etapa de qualificação
8. ID + nome da etapa de conclusão
9. ID + nome da etapa de encerramento, se houver exclusão automática
10. ID + nome do usuário responsável, se houver escalonamento
11. ID + nome da notificação, se houver notificação
12. Confirmação das ações técnicas autorizadas

Os demais campos podem usar padrão ou ser omitidos quando não aplicáveis.

---

# 12. COMPORTAMENTO DA SKILL DIANTE DE INFORMAÇÕES AUSENTES

## Se faltar informação estratégica
A Skill usa o Mapeamento de Persona ou apresenta alerta de consistência.

## Se faltar decisão sobre pré-qualificação
A Skill propõe e aguarda curadoria humana.

## Se faltar informação institucional
A Skill não inventa.  
Ela remove a informação da FAQ/Base ou a mantém como pendência interna até confirmação.

## Se faltar ID técnico necessário
A Skill **não deve produzir o arquivo como “pronto para importação”**.

Ela pode:
1. gerar um rascunho estrutural;
2. listar exatamente quais IDs estão faltando;
3. aguardar o preenchimento;
4. somente então gerar o JSON final.

## Se uma função não for usada
A Skill deve remover o respectivo token, bloco ou placeholder do JSON final.

Não deixar placeholders técnicos no arquivo final.

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

# 14. SAÍDAS ESPERADAS DA FUTURA SKILL

Depois de aprovado o fluxo e preenchido o Perfil Técnico, a Skill deve entregar:

### 1. JSON final do agente
- sem placeholders;
- IDs reais;
- modo básico;
- Regras completas;
- Etapas específicas;
- FAQ;
- Smart Decisions;
- gatilhos;
- parâmetros;
- notificações;
- validado estruturalmente.

### 2. Base de Conhecimento do Agente
Documento sanitizado derivado do Mapeamento de Persona.

### 3. Relatório curto de configuração
Resumo contendo:
- nicho;
- objetivo;
- perguntas aprovadas;
- hipóteses de escalonamento;
- exclusões;
- roteamentos;
- ações técnicas;
- pendências, se houver.

---

# 15. REGRA FINAL DO PERFIL TÉCNICO

O Perfil Técnico deve conter apenas aquilo que é **factual, operacional ou sistêmico**.

Ele não deve virar um novo briefing estratégico.

A estratégia vem do Mapeamento de Persona e da curadoria humana.

O Perfil Técnico responde essencialmente:

**“Em qual workspace esse agente vai operar, quais ações ele pode executar e quais informações do escritório estão confirmadas?”**

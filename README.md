# Biblioteca Jurídica Marketplace

**Versão atual: 8.2.0**

Marketplace de plugins e skills jurídicas para o Claude.

A Biblioteca Jurídica reúne estruturas reutilizáveis para mapeamento de persona, nutrição, pré-qualificação, agendamento, atendimento, fechamento, confirmação de atendimento e recuperação de no-show em escritórios de advocacia.

As skills possuem arquitetura replicável entre diferentes nichos jurídicos. O raciocínio e a estrutura permanecem estáveis; o conteúdo gerado é adaptado ao nicho, à persona, ao serviço, ao canal e às condições reais do escritório.

---

## Conteúdo do repositório

O repositório contém:

- o catálogo do marketplace em `.claude-plugin/marketplace.json`;
- o manifesto do plugin Biblioteca Jurídica;
- referências cognitivas e de escrita;
- o documento-base do Mapeamento de Persona;
- skills estratégicas e operacionais para diferentes etapas da jornada do lead.

---

## Skills disponíveis

### 1. `mapear-persona`

Cria o Mapeamento de Persona Jurídica que serve como documento-fonte para as demais skills.

Inclui, entre outros elementos:

- perfil da persona;
- dores, desejos, medos e objeções;
- linguagem e nível de consciência;
- critérios de qualificação;
- perguntas de pré-qualificação;
- critérios de MQL, SQL e desqualificação;
- sinais de urgência;
- anti-persona;
- jornada e fatores de decisão.

### 2. `funil-nutricao`

Cria um funil automatizável para leads frios captados, ainda sem interação real e fora da pré-qualificação.

O funil:

- aumenta consciência;
- gera identificação;
- trabalha dores, crenças e objeções anteriores à conversa;
- utiliza headlines nos Contatos 1 a 6;
- busca uma primeira mensagem de baixa fricção;
- encerra a automação diante de qualquer mensagem recebida;
- entrega o lead ao SDR para início da `/pre-qualificacao`.

A skill não qualifica, não agenda, não vende e não continua nutrindo o lead depois da primeira mensagem.

### 3. `pre-qualificacao`

Cria um roteiro humano de pré-qualificação jurídica para uso pela equipe do escritório.

A saída é dividida em:

1. saudação inicial ou boas-vindas;
2. perguntas de qualificação estratégica;
3. agradecimento e direcionamento.

A skill utiliza o Mapeamento de Persona para transformar critérios de MQL, SQL, perguntas-chave, sinais de urgência, critérios de desqualificação, dores, receios e linguagem da persona em uma conversa clara, ética e específica para o nicho.

A skill:

- faz somente as perguntas necessárias para a decisão inicial;
- contextualiza perguntas sensíveis;
- permite respostas incompletas ou aproximadas;
- identifica informações pendentes;
- registra fatos sem produzir diagnóstico definitivo;
- cria um resumo de repasse para o próximo profissional;
- encaminha o lead apto a avançar para `/agendamento`.

Não cria adaptações para chatbot, CRM ou automação. Não realiza consulta, agendamento, proposta, follow-up ou coleta documental extensa.

### 4. `agendamento`

Transforma um lead previamente qualificado em um atendimento efetivamente agendado.

A skill:

- recebe o handoff da `/pre-qualificacao`;
- usa os critérios confirmados e as informações disponíveis;
- cria uma devolutiva contextualizada;
- demonstra por que o aprofundamento profissional é relevante;
- faz o convite somente depois da contextualização;
- conduz até a definição do formato, da data e do horário;
- entrega o agendamento concluído para `/confirmacao-agendamento`.

### 5. `confirmacao-agendamento`

Confirma e prepara um atendimento que já foi agendado.

A skill:

- reduz dúvidas e barreiras de comparecimento;
- reforça brevemente o valor do encontro;
- organiza informações práticas;
- utiliza somente dados e políticas reais;
- conduz confirmação, remarcação ou cancelamento;
- encaminha para `/recuperacao-no-show` somente depois de uma ausência efetivamente confirmada.

### 6. `recuperacao-no-show`

Retoma o contato com um lead qualificado que tinha atendimento agendado, mas não compareceu.

A skill:

- aborda a ausência sem culpa ou constrangimento;
- identifica a barreira;
- reforça brevemente o valor do atendimento;
- aplica as políticas reais de falta, pagamento, crédito e remarcação;
- conduz à remarcação ou ao encerramento;
- devolve o atendimento remarcado para `/confirmacao-agendamento`.

### 7. `playbook-atendimento-fechamento`

Cria um playbook operacional interno para consulta, atendimento, objeções, decisão, fechamento e contratação.

Parte de lead já triado e qualificado.

### 8. `roteiro-consulta`

Cria um roteiro falado para consulta jurídica e fechamento por ligação, videoconferência ou reunião presencial.

### 9. `roteiro-whatsapp`

Cria um fluxo assíncrono de consulta, devolutiva e fechamento pelo WhatsApp.

---

## Jornada coberta pelas skills

```text
/mapear-persona
        ↓
Captação de lead frio
        ↓
/funil-nutricao
        ↓
Primeira mensagem recebida
        ↓
/pre-qualificacao
        ↓
Lead apto a avançar
        ↓
/agendamento
        ↓
/confirmacao-agendamento
        ↓
Consulta ou atendimento
        ├── /roteiro-consulta
        ├── /roteiro-whatsapp
        └── /playbook-atendimento-fechamento
        ↓
Decisão e contratação
```

Quando houver ausência:

```text
Atendimento agendado
        ↓
No-show confirmado
        ↓
/recuperacao-no-show
        ↓
Remarcação concluída
        ↓
/confirmacao-agendamento
```

---

## Fronteiras entre as etapas

Cada skill deve executar uma função clara e terminar no ponto correto da jornada.

- `/funil-nutricao` busca a primeira mensagem; não faz pré-qualificação.
- `/pre-qualificacao` compreende os fatos iniciais e determina o próximo direcionamento; não agenda e não realiza consulta.
- `/agendamento` parte de lead qualificado; não refaz toda a pré-qualificação.
- `/confirmacao-agendamento` prepara um atendimento já marcado; não reabre toda a venda.
- `/recuperacao-no-show` começa somente depois da ausência confirmada.
- `/roteiro-consulta`, `/roteiro-whatsapp` e `/playbook-atendimento-fechamento` não substituem as etapas anteriores da jornada.

---

## Princípios do projeto

### Arquitetura replicável

As skills devem funcionar em diferentes nichos jurídicos sem depender de um único exemplo ou área do Direito.

### Saída específica para o nicho

A estrutura é reutilizável, mas a saída deve refletir:

- a persona;
- os critérios jurídicos;
- o serviço oferecido;
- as objeções reais;
- o canal;
- a etapa da jornada;
- as condições operacionais do escritório.

### Persona não é ficha individual

O Mapeamento de Persona orienta estratégia, linguagem, perguntas e bifurcações.

Ele não autoriza inventar fatos, respostas, emoções ou características de um lead específico.

### Prudência jurídica

As skills podem apresentar regras gerais e possibilidades jurídicas, mas não devem:

- prometer resultado;
- garantir direito;
- inventar fatos;
- produzir diagnóstico definitivo sem análise suficiente;
- criar urgência artificial;
- classificar alguém sem critérios verificáveis.

### Dados operacionais reais

Datas, horários, valores, links, profissionais, duração, prova social e políticas devem ser reais ou apresentados como placeholders claros.

### Handoff sem perda de contexto

Cada etapa deve transmitir para a próxima:

- fatos confirmados;
- respostas relevantes;
- critérios observados;
- informações pendentes;
- sinais de urgência;
- objeções ou dúvidas expressas;
- próximo passo recomendado.

A etapa seguinte não deve obrigar o lead a repetir informações já registradas, salvo quando houver inconsistência ou necessidade real de confirmação.

---

## Referências e compatibilidade entre ambientes

O plugin utiliza:

- `core-cognitivo.md` — raciocínio, herança de contexto, recorte, segurança e não invenção;
- `core-escrita-oralidade.md` — clareza, naturalidade, profundidade, ritmo e adequação ao produto e ao canal;
- `mapeamento-persona-v2.md` — estrutura-base do Mapeamento de Persona Jurídica.

A pasta `plugins/biblioteca-juridica/references/` pode ser mantida como fonte-mestra.

Para compatibilidade com o Claude Web, cada skill deve conter dentro do próprio diretório a pasta `references/` com as referências que utiliza.

Exemplo:

```text
skills/
└── pre-qualificacao/
    ├── SKILL.md
    └── references/
        ├── core-cognitivo.md
        └── core-escrita-oralidade.md
```

Nos arquivos `SKILL.md`, os caminhos podem permanecer:

```text
${CLAUDE_PLUGIN_ROOT}/references/core-cognitivo.md
${CLAUDE_PLUGIN_ROOT}/references/core-escrita-oralidade.md
```

Quando uma referência compartilhada for alterada, atualize também as cópias locais das skills que dependem dela.

---

## Estrutura geral

```text
biblioteca-juridica-marketplace/
├── .claude-plugin/
│   └── marketplace.json
├── plugins/
│   └── biblioteca-juridica/
│       ├── .claude-plugin/
│       │   └── plugin.json
│       ├── references/
│       │   ├── core-cognitivo.md
│       │   ├── core-escrita-oralidade.md
│       │   └── mapeamento-persona-v2.md
│       └── skills/
│           ├── mapear-persona/
│           │   ├── SKILL.md
│           │   └── references/
│           ├── funil-nutricao/
│           │   ├── SKILL.md
│           │   └── references/
│           ├── pre-qualificacao/
│           │   ├── SKILL.md
│           │   └── references/
│           ├── agendamento/
│           │   ├── SKILL.md
│           │   └── references/
│           ├── confirmacao-agendamento/
│           │   ├── SKILL.md
│           │   └── references/
│           ├── recuperacao-no-show/
│           │   ├── SKILL.md
│           │   └── references/
│           ├── playbook-atendimento-fechamento/
│           │   ├── SKILL.md
│           │   └── references/
│           ├── roteiro-consulta/
│           │   ├── SKILL.md
│           │   └── references/
│           └── roteiro-whatsapp/
│               ├── SKILL.md
│               └── references/
└── README.md
```

Cada diretório de skill deve possuir um arquivo chamado exatamente `SKILL.md`.

---

## Versão 8.1.0

Esta versão:

- adiciona a skill `/pre-qualificacao`;
- estabelece a passagem explícita de `/funil-nutricao` para `/pre-qualificacao`;
- estabelece a passagem de leads aptos da `/pre-qualificacao` para `/agendamento`;
- documenta a pré-qualificação como etapa humana, sem adaptações para automação;
- corrige no README os nomes e diretórios de `/agendamento` e `/confirmacao-agendamento`;
- documenta o empacotamento local das referências para compatibilidade com o Claude Web;
- mantém a skill de follow-up fora desta versão, aguardando reformulação.

---

## Regra de teste

Avalie cada skill separadamente em três dimensões:

1. **Arquitetura:** executou a tarefa correta e respeitou a fronteira da etapa?
2. **Conteúdo:** trouxe profundidade, coerência jurídica e especificidade para o nicho?
3. **Escrita:** parece comunicação humana, clara e profissional?

Para testar a jornada:

1. execute `/funil-nutricao` e verifique se a sequência termina na primeira mensagem;
2. execute `/pre-qualificacao` e verifique se cria boas-vindas, perguntas estratégicas e direcionamento;
3. confirme se o resumo final registra fatos e pendências;
4. confirme se apenas leads aptos são encaminhados para `/agendamento`;
5. confirme se `/agendamento` não refaz toda a pré-qualificação.

Não altere a arquitetura para corrigir apenas uma preferência de frase.

---

## Regra de congelamento

Reabra uma skill somente diante de:

1. falha estrutural;
2. erro jurídico relevante;
3. falha recorrente em diferentes nichos.

Preferências isoladas de estilo não exigem nova versão.


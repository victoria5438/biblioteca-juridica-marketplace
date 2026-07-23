# Biblioteca Jurídica Marketplace

**Versão atual: 0.8.0**

Marketplace privado de plugins e skills jurídicas para o Claude Cowork.

A Biblioteca Jurídica reúne estruturas reutilizáveis para pesquisa de persona, atendimento, fechamento, nutrição, agendamento e recuperação de leads em escritórios de advocacia.

As skills possuem arquitetura replicável entre diferentes nichos jurídicos. O raciocínio e a estrutura permanecem estáveis; o conteúdo gerado é adaptado ao nicho, à persona, ao serviço e às condições reais do escritório.

---

## Conteúdo do repositório

O repositório contém:

- o catálogo do marketplace em `.claude-plugin/marketplace.json`;
- o manifesto do plugin Biblioteca Jurídica;
- referências cognitivas e de escrita compartilhadas;
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
- sinais de urgência e anti-persona.

### 2. `playbook-atendimento-fechamento`

Cria um playbook operacional interno para consulta, atendimento, objeções, decisão, fechamento e contratação.

### 3. `roteiro-consulta`

Cria um roteiro falado para consulta jurídica e fechamento por ligação, videoconferência ou reunião presencial.

### 4. `roteiro-whatsapp`

Cria um fluxo assíncrono de consulta, devolutiva e fechamento pelo WhatsApp.

### 5. `funil-nutricao`

Cria um funil automatizável para leads frios captados, mas ainda sem interação real e fora da pré-qualificação.

O fluxo termina quando o lead envia a primeira mensagem e passa para o atendimento humano ou SDR.

### 6. `agendamento.skill.md`

Transforma um lead previamente qualificado em um atendimento efetivamente agendado.

A skill:

- usa os critérios de qualificação do Mapeamento de Persona;
- cria uma devolutiva contextualizada;
- demonstra por que o aprofundamento profissional é relevante;
- faz o convite somente depois da contextualização;
- conduz o lead até a definição do formato, da data e do horário.

### 7. `confirmacao-agendamento.skill.md`

Confirma e prepara um atendimento que já foi agendado.

A skill:

- reduz dúvidas e barreiras de comparecimento;
- reforça brevemente o valor do encontro;
- organiza informações práticas;
- conduz confirmação, remarcação ou cancelamento conforme as regras reais do escritório.

### 8. `recuperacao-no-show`

Retoma o contato com um lead qualificado que tinha atendimento agendado, mas não compareceu.

A skill:

- aborda a ausência sem culpa ou constrangimento;
- identifica a barreira;
- reforça brevemente o valor do atendimento;
- conduz à remarcação ou ao encerramento;
- respeita as políticas reais de falta, crédito, pagamento e remarcação.

---

## Jornada coberta pelas skills

```text
Mapeamento de persona
        ↓
Captação e nutrição de lead frio
        ↓
Pré-qualificação
        ↓
Agendamento
        ↓
Confirmação do agendamento
        ↓
Consulta ou atendimento pelo WhatsApp
        ↓
Decisão e contratação
```

Quando houver ausência:

```text
Atendimento agendado
        ↓
No-show confirmado
        ↓
Recuperação e possível remarcação
        ↓
Nova confirmação do agendamento
```

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
- as condições operacionais do escritório.

### Separação entre etapas

Cada skill deve executar uma função clara e terminar no ponto correto da jornada.

Exemplos:

- nutrição não faz pré-qualificação;
- agendamento não realiza consulta;
- confirmação não recupera no-show antes da ausência;
- recuperação de no-show não substitui o fluxo completo de agendamento.

### Prudência jurídica

As skills podem apresentar regras gerais e possibilidades jurídicas, mas não devem:

- prometer resultado;
- garantir direito;
- inventar fatos;
- produzir diagnóstico definitivo sem análise suficiente;
- criar urgência artificial.

### Dados operacionais reais

Datas, horários, valores, links, profissionais, duração e políticas devem ser reais ou apresentados como placeholders claros.

---

## Referências compartilhadas

O plugin utiliza referências comuns para manter consistência entre as skills:

- `references/core-cognitivo.md` — princípios de raciocínio, herança de contexto e uso responsável de presunções;
- `references/core-escrita-oralidade.md` — clareza, naturalidade, ritmo, autoridade e escrita conversacional.

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
│           ├── playbook-atendimento-fechamento/
│           ├── roteiro-consulta/
│           ├── roteiro-whatsapp/
│           ├── funil-nutricao/
│           ├── agendamento.skill.md
│           ├── confirmacao-agendamento.skill.md
│           └── recuperacao-no-show/
└── README.md
```

A estrutura acima representa a organização lógica do projeto. Mantenha os caminhos efetivamente usados pelo plugin ao adicionar ou renomear arquivos.

---

## Versão 0.8.0

Esta versão adiciona a sequência operacional posterior à pré-qualificação:

- agendamento com devolutiva e criação ética de necessidade;
- confirmação e preparação do atendimento;
- recuperação de no-show.

Também adota os nomes:

- `agendamento.skill.md`;
- `confirmacao-agendamento.skill.md`.

O nome `recuperacao-no-show` foi mantido.

A skill de follow-up não integra esta versão. Sua função e seus limites serão reformulados antes da inclusão no plugin.

---

## Regra de teste

Avalie cada skill separadamente em três dimensões:

1. **Arquitetura:** executou a tarefa correta e respeitou a fronteira da etapa?
2. **Conteúdo:** trouxe profundidade, coerência jurídica e especificidade para o nicho?
3. **Escrita:** parece comunicação humana, clara e profissional?

Não altere a arquitetura para corrigir apenas uma preferência de frase.

---

## Regra de congelamento

Reabra uma skill somente diante de:

1. falha estrutural;
2. erro jurídico relevante;
3. falha recorrente em diferentes nichos.

Preferências isoladas de estilo não exigem nova versão.


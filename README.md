# Biblioteca Jurídica Marketplace

**Versão atual: 9.0**

Marketplace de plugins e skills jurídicas para o Claude.

A Biblioteca Jurídica reúne estruturas reutilizáveis para mapeamento de persona, criação de roteiros de criativos jurídicos, nutrição, pré-qualificação, agendamento, atendimento, fechamento, confirmação de atendimento e recuperação de no-show em escritórios de advocacia.

As skills possuem arquitetura replicável entre diferentes nichos jurídicos. O raciocínio e a estrutura permanecem estáveis; o conteúdo gerado é adaptado ao nicho, à persona, ao serviço, ao canal e às condições reais do escritório.

---

## Conteúdo do repositório

O repositório contém:

- o catálogo do marketplace em `.claude-plugin/marketplace.json`;
- o manifesto do plugin Biblioteca Jurídica;
- referências cognitivas, de escrita e metodológicas;
- o documento-base do Mapeamento de Persona;
- skills estratégicas e operacionais para aquisição, atendimento e conversão de leads jurídicos.

---

## Skills disponíveis

### 1. `mapear-persona`

Cria o Mapeamento de Persona Jurídica que serve como documento-fonte para as demais skills.

Inclui, entre outros elementos:

- perfil da persona;
- natureza e delimitação do serviço;
- dores, desejos, medos e objeções;
- linguagem e nível de consciência;
- situações objetivas de aderência;
- fatores de complexidade;
- maturidade comercial;
- critérios de MQL e SQL;
- sinais de urgência;
- anti-persona e roteamento;
- jornada e fatores de decisão;
- insumos estratégicos para pré-qualificação, nutrição, criativos e demais skills derivadas.

### 2. `roteiros-criativos-juridicos`

Cria conceitos e roteiros estratégicos de vídeos para campanhas jurídicas de Meta Ads.

A skill utiliza o Mapeamento de Persona Jurídica específico do serviço como documento-fonte. Ela não executa novamente `/mapear-persona` e não deve substituir o Mapeamento produzido pelo arquivo estrutural `mapeamento-persona-v3.md`.

Antes de escrever os roteiros, a skill:

1. compreende o serviço e seu mecanismo de valor;
2. separa perfil, aderência, complexidade e maturidade comercial;
3. identifica situações objetivas, dúvidas, tensões e decisões exploráveis;
4. cria uma matriz de ângulos;
5. seleciona os conceitos mais fortes e distintos;
6. produz os roteiros;
7. realiza autorrevisão jurídica, ética, criativa e de oralidade.

Cada roteiro pode incluir:

- público e subpersona;
- situação objetiva;
- nível de consciência;
- objetivo;
- ângulo;
- gancho;
- desenvolvimento;
- quebra de crença;
- mecanismo de valor;
- CTA;
- orientação visual;
- notas de gravação;
- duração estimada;
- cuidado jurídico.

A skill não deve prometer resultado, inventar prova social, criar urgência artificial, tratar informação genérica como diagnóstico nem produzir vários roteiros que apenas reformulem a mesma ideia.

### 3. `funil-nutricao`

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

### 4. `pre-qualificacao`

Cria um roteiro humano de pré-qualificação jurídica para uso pela equipe do escritório.

A skill utiliza o Mapeamento de Persona para transformar situações de aderência, critérios de MQL e SQL, fatores de complexidade, sinais de urgência, critérios de roteamento, dores, receios e linguagem da persona em uma conversa clara, ética e específica para o nicho.

A skill:

- faz somente as perguntas necessárias para a decisão inicial;
- pergunta fatos, sem exigir que o lead realize o próprio enquadramento jurídico;
- contextualiza perguntas sensíveis;
- permite respostas incompletas ou aproximadas;
- identifica informações pendentes;
- separa aderência, complexidade, urgência, maturidade e prontidão;
- registra fatos sem produzir diagnóstico definitivo;
- cria um resumo de repasse para o próximo profissional;
- encaminha o lead apto a avançar para `/agendamento`.

Não cria adaptações para chatbot, CRM ou automação. Não realiza consulta, agendamento, proposta, follow-up ou coleta documental extensa.

### 5. `agendamento`

Transforma um lead previamente qualificado em um atendimento efetivamente agendado.

A skill:

- recebe o handoff da `/pre-qualificacao`;
- usa os critérios confirmados e as informações disponíveis;
- cria uma devolutiva contextualizada;
- demonstra por que o aprofundamento profissional é relevante;
- faz o convite somente depois da contextualização;
- conduz até a definição do formato, da data e do horário;
- entrega o agendamento concluído para `/confirmacao-agendamento`.

### 6. `confirmacao-agendamento`

Confirma e prepara um atendimento que já foi agendado.

A skill:

- reduz dúvidas e barreiras de comparecimento;
- reforça brevemente o valor do encontro;
- organiza informações práticas;
- utiliza somente dados e políticas reais;
- conduz confirmação, remarcação ou cancelamento;
- encaminha para `/recuperacao-no-show` somente depois de uma ausência efetivamente confirmada.

### 7. `recuperacao-no-show`

Retoma o contato com um lead qualificado que tinha atendimento agendado, mas não compareceu.

A skill:

- aborda a ausência sem culpa ou constrangimento;
- identifica a barreira;
- reforça brevemente o valor do atendimento;
- aplica as políticas reais de falta, pagamento, crédito e remarcação;
- conduz à remarcação ou ao encerramento;
- devolve o atendimento remarcado para `/confirmacao-agendamento`.

### 8. `playbook-atendimento-fechamento`

Cria um playbook operacional interno para consulta, atendimento, objeções, decisão, fechamento e contratação.

Parte de lead já triado e qualificado.

### 9. `roteiro-consulta`

Cria um roteiro falado para consulta jurídica e fechamento por ligação, videoconferência ou reunião presencial.

### 10. `roteiro-whatsapp`

Cria um fluxo assíncrono de consulta, devolutiva e fechamento pelo WhatsApp.

---

## Fluxos cobertos pelas skills

### Aquisição por criativos jurídicos

```text
/mapear-persona
        ↓
Mapeamento de Persona Jurídica
        ↓
/roteiros-criativos-juridicos
        ↓
Diagnóstico estratégico
        ↓
Matriz e seleção de ângulos
        ↓
Roteiros para campanhas de Meta Ads
        ↓
Captação de leads
```

### Jornada de atendimento e conversão

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

Cada skill deve executar uma função clara e terminar no ponto correto.

- `/mapear-persona` cria o documento-fonte; não produz automaticamente todas as peças derivadas.
- `/roteiros-criativos-juridicos` transforma o Mapeamento em diagnóstico de campanha, ângulos e roteiros; não cria o Mapeamento do zero nem configura a campanha no Gerenciador de Anúncios.
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
- as situações objetivas de aderência;
- os critérios jurídicos;
- o serviço oferecido;
- as objeções reais;
- o canal;
- a etapa da jornada;
- as condições operacionais do escritório.

### Persona não é ficha individual

O Mapeamento de Persona orienta estratégia, linguagem, perguntas, ângulos e bifurcações.

Ele não autoriza inventar fatos, respostas, emoções ou características de um lead específico.

### Prudência jurídica

As skills podem apresentar regras gerais e possibilidades jurídicas, mas não devem:

- prometer resultado;
- garantir direito;
- inventar fatos;
- produzir diagnóstico definitivo sem análise suficiente;
- criar urgência artificial;
- classificar alguém sem critérios verificáveis;
- aplicar regra específica a ente, categoria ou caso não confirmado.

### Dados operacionais reais

Datas, horários, valores, links, profissionais, duração, prova social, CTA, ofertas e políticas devem ser reais ou apresentados como placeholders claros.

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
- `mapeamento-persona-v3.md` — estrutura-base do Mapeamento de Persona Jurídica.

Algumas skills também utilizam referências metodológicas próprias. A skill `/roteiros-criativos-juridicos`, por exemplo, utiliza:

- `roteiros-criativos-juridicos.md` — diagnóstico do serviço, leitura da persona para mídia paga, extração de situações e dores, matriz de ângulos, seleção, escrita, diversidade e autorrevisão.

A pasta `plugins/biblioteca-juridica/references/` pode ser mantida como fonte-mestra das referências compartilhadas.

Para compatibilidade com o Claude Web, cada skill deve conter dentro do próprio diretório a pasta `references/` com as referências que utiliza.

Exemplo:

```text
skills/
└── roteiros-criativos-juridicos/
    ├── SKILL.md
    └── references/
        ├── core-cognitivo.md
        ├── core-escrita-oralidade.md
        └── roteiros-criativos-juridicos.md
```

Nos arquivos `SKILL.md`, os caminhos podem permanecer:

```text
${CLAUDE_PLUGIN_ROOT}/references/core-cognitivo.md
${CLAUDE_PLUGIN_ROOT}/references/core-escrita-oralidade.md
${CLAUDE_PLUGIN_ROOT}/references/roteiros-criativos-juridicos.md
```

O Mapeamento de Persona específico do serviço não fica fixo dentro da pasta da skill. Ele é um documento-fonte dinâmico fornecido na execução.

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
│       │   └── mapeamento-persona-v3.md
│       └── skills/
│           ├── mapear-persona/
│           │   ├── SKILL.md
│           │   └── references/
│           ├── roteiros-criativos-juridicos/
│           │   ├── SKILL.md
│           │   └── references/
│           │       ├── core-cognitivo.md
│           │       ├── core-escrita-oralidade.md
│           │       └── roteiros-criativos-juridicos.md
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

## Versão 9.0

Esta versão:

- adiciona a skill `/roteiros-criativos-juridicos`;
- estabelece o Mapeamento de Persona Jurídica como documento-fonte da nova skill;
- impede que a criação parta diretamente para os roteiros sem diagnóstico estratégico;
- separa perfil, aderência, complexidade e maturidade comercial;
- adiciona a extração de situações, dúvidas, tensões e decisões exploráveis;
- adiciona matriz de ângulos e seleção estratégica dos conceitos;
- adiciona estrutura completa de roteiro, com orientação visual e notas de gravação;
- adiciona autorrevisão jurídica, ética, criativa e de oralidade;
- adiciona quadro de diversidade para evitar repetição entre os criativos;
- adiciona a referência metodológica local `roteiros-criativos-juridicos.md`;
- atualiza a documentação para `mapeamento-persona-v3.md`;
- preserva as fronteiras e os fluxos das demais skills.

---

## Regra de teste

Avalie cada skill separadamente em três dimensões:

1. **Arquitetura:** executou a tarefa correta e respeitou a fronteira da etapa?
2. **Conteúdo:** trouxe profundidade, coerência jurídica e especificidade para o nicho?
3. **Escrita:** parece comunicação humana, clara e profissional?

### Teste da skill de criativos

1. execute `/mapear-persona`;
2. forneça o Mapeamento produzido para `/roteiros-criativos-juridicos`;
3. confirme que a skill não parte diretamente para os roteiros;
4. confirme que apresenta diagnóstico estratégico, matriz de ângulos e seleção recomendada;
5. verifique se perfil, aderência, complexidade e maturidade permanecem separados;
6. verifique se cada roteiro fala com uma situação concreta;
7. confirme que os roteiros possuem ângulos, subpersonas e níveis de consciência distintos;
8. confirme que afirmações dependentes do ente ou do caso estão condicionadas;
9. confirme que não há promessa de resultado, urgência artificial ou prova inventada;
10. confirme que o CTA convida para a próxima etapa real.

### Teste da jornada comercial

1. execute `/funil-nutricao` e verifique se a sequência termina na primeira mensagem;
2. execute `/pre-qualificacao` e verifique se cria uma conversa humana de triagem;
3. confirme se o resumo final registra fatos, pendências e direcionamento;
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


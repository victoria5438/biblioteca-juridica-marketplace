# Biblioteca Jurídica Marketplace — versão 0.6.0

Marketplace de plugins para criação de materiais jurídicos estratégicos, reutilizáveis e adaptados ao perfil do público.

## Estrutura do repositório

Este repositório contém:

- o catálogo do marketplace em `.claude-plugin/marketplace.json`;
- o plugin `Biblioteca Jurídica`;
- referências cognitivas e de escrita compartilhadas;
- skills especializadas para mapeamento de persona, playbooks operacionais e roteiros de consulta e fechamento.

## Princípio de funcionamento

As skills são reutilizáveis entre diferentes nichos jurídicos, mas cada saída deve ser construída especificamente para:

- o nicho atual;
- o público atendido;
- o serviço;
- o recorte;
- o canal;
- a etapa da jornada.

> A skill é reutilizável entre nichos. A saída é específica para o nicho e o recorte atuais.

## Skills disponíveis

### Mapear persona

Cria um mapeamento aprofundado da persona jurídica, incluindo:

- dores;
- medos;
- desejos;
- linguagem;
- objeções;
- nível de consciência;
- fatores de decisão;
- subperfis;
- variações relevantes do público.

```text
/biblioteca-juridica:mapear-persona
```

### Playbook de atendimento e fechamento

Cria um manual operacional interno, profundo e reutilizável para consulta, atendimento e fechamento jurídico.

Parte de um lead já triado e qualificado e desenvolve:

- preparação e passagem de contexto;
- validação da viabilidade jurídica;
- perguntas e motivos;
- critérios de observação;
- explicações substantivas;
- documentos e sua finalidade;
- bifurcações;
- caminhos e limites;
- apresentação do serviço;
- participação real do cliente;
- honorários;
- objeções;
- decisão;
- formalização.

Não realiza:

- captação;
- nutrição;
- triagem;
- qualificação comercial;
- convite para consulta;
- agendamento;
- confirmação;
- recuperação de no-show;
- acompanhamento posterior à contratação.

```text
/biblioteca-juridica:playbook-atendimento-fechamento
```

### Roteiro de consulta

Cria um roteiro falado, fluido, profundo e reutilizável para consulta jurídica e fechamento por:

- ligação;
- videoconferência;
- reunião presencial.

Parte de um lead já triado e qualificado e prioriza:

- retomada do contexto anterior;
- falas prontas;
- perguntas conectadas;
- organização dos fatos;
- validação da viabilidade jurídica;
- explicações em camadas;
- aplicação ao cenário;
- pausas;
- checagens de entendimento;
- bifurcações;
- apresentação do serviço;
- honorários;
- objeções;
- decisão;
- formalização.

O produto principal é uma conversa falada. Não deve assumir formato de playbook, manual ou fluxo de WhatsApp.

```text
/biblioteca-juridica:roteiro-consulta
```

### Roteiro de WhatsApp

Cria um fluxo assíncrono de consulta, devolutiva e fechamento pelo WhatsApp.

Parte de um lead que:

- já passou pela triagem;
- já foi classificado como qualificado;
- já enviou os documentos iniciais;
- já teve esses documentos analisados;
- possui uma conclusão inicial do advogado.

O fluxo pode incluir:

- primeira mensagem do advogado;
- devolutiva da análise;
- explicações por texto ou áudio;
- esclarecimentos complementares;
- documentos complementares;
- apresentação do serviço;
- honorários;
- objeções;
- decisão;
- contrato;
- procuração;
- assinatura;
- follow-ups da própria consulta ou do fechamento.

Não realiza:

- captação;
- resposta a anúncio;
- acolhimento inicial de SDR;
- triagem;
- qualificação;
- agendamento;
- confirmação de consulta;
- prevenção de ausência;
- recuperação de no-show;
- reativação genérica.

```text
/biblioteca-juridica:roteiro-whatsapp
```

## Diferença entre as skills

### Playbook de atendimento e fechamento

É um material operacional interno.

Explica:

- o que fazer;
- por que fazer;
- o que perguntar;
- o que observar;
- como interpretar respostas;
- quais bifurcações existem;
- como avançar;
- quais erros evitar.

### Roteiro de consulta

É uma conversa oral pronta para ser conduzida.

Prioriza:

- falas;
- perguntas;
- explicações;
- pausas;
- transições;
- bifurcações;
- objeções;
- decisão.

### Roteiro de WhatsApp

É uma conversa assíncrona distribuída em mensagens e áudios.

Prioriza:

- uma função principal por mensagem;
- momentos de espera;
- continuidade conforme a resposta;
- devolutiva;
- chamadas para ação;
- retomadas contextualizadas;
- formalização.

## Arquitetura compartilhada

As skills utilizam:

- `plugins/biblioteca-juridica/references/core-cognitivo.md`;
- `plugins/biblioteca-juridica/references/core-escrita-oralidade.md`.

### Core Cognitivo

Define regras compartilhadas de:

- hierarquia das fontes;
- herança do mapeamento de persona;
- escolha do produto;
- delimitação de recorte;
- reutilização;
- especificidade da execução;
- presunções controladas;
- não invenção;
- autonomia jurídica;
- régua de certeza;
- profundidade;
- segurança;
- revisão interna.

### Core de Escrita, Oralidade e Cadência

Define regras compartilhadas de:

- adequação ao produto;
- adequação ao canal;
- escrita de playbooks;
- oralidade de roteiros;
- cadência do WhatsApp;
- linguagem profissional;
- personalização contextual;
- explicação jurídica;
- objeções;
- fechamento;
- tamanho dos blocos;
- naturalidade;
- testes de suficiência e reutilização.

## Responsabilidade de cada skill

Cada `SKILL.md` continua responsável por definir:

- a missão;
- o ponto de partida;
- o ponto de encerramento;
- as entradas;
- o recorte;
- a arquitetura;
- as etapas;
- o formato de saída;
- os limites;
- os critérios de revisão do próprio produto.

## Versão atual

```text
0.6.0
```

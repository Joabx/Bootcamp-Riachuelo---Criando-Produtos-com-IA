# 💸 App Finanças Pessoais com Vibe Coding

## PRD Refinado no Gemini

```markdown
# PRD: App de Finanças Conversational Budget

## 1. Visão Geral
Desenvolver um aplicativo de finanças pessoais focado em entrada de dados via linguagem natural. O app deve ser minimalista, acessível e oferecer uma experiência de uso confortável em diversos ambientes.

## 2. Requisitos de Acessibilidade (Design Universal)
O sistema deve ser construído seguindo estritamente as diretrizes de acessibilidade WCAG (Web Content Accessibility Guidelines):
* Contraste: Garantir proporção mínima de contraste de 4.5:1 para todo texto e elementos de interface.
* Tipografia: Implementar fontes responsivas que respeitem as configurações de tamanho de texto do dispositivo do usuário.
* Semântica: Utilizar tags HTML semânticas adequadas para garantir compatibilidade total com leitores de tela (VoiceOver/TalkBack).
* Áreas de Toque: Elementos interativos (botões, inputs) devem ter um tamanho mínimo de 44x44 pixels para garantir usabilidade motora.
* Daltonismo: Não utilizar cores como única forma de distinção de dados (ex: usar padrões ou rótulos junto aos gráficos).

## 3. Sistema de Temas (Theming)
Implementar um seletor de temas persistente através de variáveis CSS (Tailwind):
* Tema Light: Fundo branco (#FFFFFF), texto cinza escuro (#1F2937).
* Tema Dark: Fundo cinza quase preto (#111827), texto branco (#F9FAFB).
* Tema Leitura (Sepia): Fundo papel (#F4ECD8), texto marrom escuro (#5B4636). Este tema deve reduzir a emissão de luz azul.
* Implementação: O sistema deve permitir a alternância imediata via menu de configurações, com persistência no localStorage.

## 4. Funcionalidades do MVP
1. Chat UI: Interface de conversação centralizada para entrada de transações. Deve processar texto em linguagem natural.
2. Processamento: IA integrada para categorização automática de transações (ex: "gastei 50 no mercado" -> Categoria: Alimentação).
3. Dashboard: Painel simplificado com resumo financeiro (Saldo, Gastos, Metas).
4. Agente Financeiro: Módulo de geração de dicas de economia baseado no histórico do usuário.

## 5. Estrutura de Telas (MVP)
* Screen: Chat (Home): Interface de mensagens com área de input fixa na base. Suporte aos três temas.
* Screen: Analytics: Gráfico simplificado com rótulos de acessibilidade.
* Screen: Settings: Seletor de tema (Light, Dark, Sepia) e definição de metas mensais.

## 6. Critérios de Validação Técnica
* O app deve passar em auditorias de contraste (ex: Lighthouse ou ferramentas de acessibilidade do navegador).
* A transição entre temas não deve causar flickering (piscar) na interface.
* O chat deve ser totalmente operável apenas com o teclado (foco e navegação via tab).
```

## Interações com o Lovable

> Apenas existe um tipo de meta no APP, gostaria de poder criar multiplas metas e nomeá-las do jeito que quiser, por exemplo, uma Meta de Emergência

## Resultado Final

<img width="1203" height="821" alt="App de Finanças pessoais - Lovable - 1" src="https://github.com/user-attachments/assets/d3179528-09da-4e62-9501-0b9a9aa5a94b" />
<img width="1202" height="819" alt="App de Finanças pessoais - Lovable - 2" src="https://github.com/user-attachments/assets/85e40c6f-edde-4a23-a6f8-b946c6534889" />
<img width="1194" height="821" alt="App de Finanças pessoais - Lovable - 3" src="https://github.com/user-attachments/assets/ae02e3d5-5af4-4a51-9a25-c58be539d334" />


## O que o APP faz?

Ele é um aplicativo de controle de gastos focado em conversação inteligente, onde você registra transações por comandos de texto simples. A plataforma conta com painéis detalhados de análises por categorias, acompanhamento de metas financeiras e limites de gastos.  
Além disso, oferece customização de temas visuais (incluindo opções claro, escuro e modo leitura/sépia) para uma experiência acessível e confortável.

## Reflexão sobre todo o processo:

Usando o PRD refinado, o Lovable rapidamente criou uma versão bastante precisa e funcional, me impressionei com o resultado inicial, logo após (usando uma linguagem natural) pedi para que ele incluísse uma forma de aumentar o número de metas e que elas fossem personalizaveis, novamente o Lovable me entregou exatamente o que eu pedi.  
Estou bastante surpreso com a rapidez e precisão dessa plataforma de criação de APPS.
 

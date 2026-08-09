# 💼 App ATS Friendly com Vibe Coding

## PRD Refinado com Gemini + Chat GPT

```markdown
# PRD: App de Curriculum ATS Friendly

## 1. OBJETIVO

Crie um MVP chamado **ATS Resume Copilot**, desenvolvido como projeto educacional para um bootcamp da DIO e posteriormente publicado no GitHub.

A aplicação deve demonstrar um fluxo funcional de análise de currículo contra uma descrição de vaga, identificando compatibilidade, gaps e oportunidades de melhoria.

Não construir um SaaS completo. Priorizar qualidade, simplicidade e funcionamento real.

---

## 2. FLUXO PRINCIPAL

Implementar este fluxo:

Currículo → Vaga → Analisar → Match Score → Gaps → Recomendações → Currículo Otimizado → Preview

O usuário deve conseguir completar esse fluxo sem login ou configuração externa.

---

## 3. STACK

Utilizar:

- React
- TypeScript
- Vite
- Tailwind CSS
- shadcn/ui
- Lucide React

Manter a lógica de negócio separada dos componentes visuais.

---

## 4. NAVEGAÇÃO

Criar apenas estas áreas:

- Dashboard
- Currículo
- Nova Análise
- Resultado
- Currículo Otimizado

Não criar páginas vazias ou funcionalidades que não serão utilizadas.

---

## 5. DASHBOARD

Criar um dashboard simples e profissional contendo:

- status do currículo;
- última análise;
- último Match Score;
- botão "Nova Análise";
- botão "Editar Currículo";
- botão "Carregar Demonstração".

Quando não houver dados, mostrar um empty state em vez de números fictícios.

---

## 6. CURRÍCULO MESTRE

Criar um editor de currículo com:

- nome;
- cargo;
- localização;
- email;
- LinkedIn;
- GitHub;
- resumo profissional;
- experiências;
- formação;
- skills.

Permitir adicionar e remover experiências e skills.

Salvar os dados localmente usando `localStorage`.

---

## 7. JOB DESCRIPTION

Na tela "Nova Análise", permitir informar:

- cargo;
- empresa;
- descrição completa da vaga.

Utilizar um textarea grande para colar a Job Description.

Adicionar o botão:

"Analisar vaga"

---

## 8. MATCHING

Criar um motor de matching local e determinístico.

Comparar o conteúdo do currículo com a descrição da vaga considerando:

- requisitos;
- skills;
- experiência;
- senioridade;
- keywords.

Utilizar estes pesos:

| Critério | Peso |
|---|---:|
| Requisitos | 35% |
| Skills | 25% |
| Experiência | 20% |
| Senioridade | 10% |
| Keywords | 10% |

O resultado nunca deve ser aleatório.

---

## 9. MATCH SCORE

Exibir um score de `0–100`.

Exemplo:

MATCH SCORE

84 / 100

Mostrar também a composição:

- Requisitos: 92%
- Skills: 86%
- Experiência: 79%
- Senioridade: 90%
- Keywords: 74%

Adicionar a seguinte observação:

> Este score representa a compatibilidade entre o currículo e a vaga. Não representa probabilidade de contratação.

---

## 10. ATS SCORE

Criar um segundo indicador:

ATS STRUCTURE SCORE

91 / 100

Avaliar de forma simples:

- estrutura linear;
- headings;
- experiência;
- formação;
- skills;
- legibilidade.

O ATS Score deve ser independente do Match Score.

Não é necessário implementar uma auditoria ATS complexa.

---

## 11. KEYWORDS

Na tela de resultados, mostrar três grupos:

### Encontradas

Keywords presentes na vaga e no currículo.

### Ausentes

Keywords relevantes da vaga que não aparecem no currículo.

### Relacionadas

Termos potencialmente relacionados, mas que precisam de confirmação do usuário.

Usar badges e indicadores visuais claros.

---

## 12. GAPS E RECOMENDAÇÕES

Criar uma seção "Principais Gaps".

Exemplo:

- ✓ React encontrado
- ✓ TypeScript encontrado
- ⚠ Next.js não encontrado
- ⚠ AWS não comprovado

Para cada gap, mostrar uma recomendação curta.

Exemplo:

> Se você possui experiência com AWS, considere adicioná-la ao currículo.

---

## 13. REGRA ANTI-FABRICAÇÃO

Esta é uma regra obrigatória.

Nunca inventar:

- experiências;
- empresas;
- cargos;
- tecnologias;
- certificações;
- resultados;
- métricas;
- competências.

Nunca adicionar uma keyword da vaga ao currículo sem evidência no currículo.

Quando não houver evidência, utilizar:

**NÃO COMPROVADO**

O sistema pode melhorar a redação das informações existentes, mas não criar fatos novos.

---

## 14. CURRÍCULO OTIMIZADO

Criar uma versão otimizada do currículo utilizando somente informações existentes.

Permitir:

- melhorar redação;
- melhorar verbos;
- reorganizar conteúdo;
- reduzir redundâncias;
- destacar experiências relevantes;
- reorganizar skills;
- adaptar o resumo profissional.

Não alterar:

- empresas;
- cargos;
- datas;
- experiências;
- resultados.

---

## 15. COMPARAÇÃO ANTES/DEPOIS

Mostrar as principais alterações em formato simples:

ANTES:

"Worked with frontend development."

DEPOIS:

"Developed frontend applications."

MOTIVO:

"Melhora clareza e objetividade."

Permitir:

- Aceitar alteração;
- Rejeitar alteração.

Não é necessário implementar versionamento complexo.

---

## 16. PREVIEW DO CURRÍCULO

Criar um preview visual semelhante a uma página A4.

O currículo deve utilizar:

- uma coluna;
- headings claros;
- texto real;
- boa hierarquia;
- tipografia profissional.

Evitar:

- tabelas;
- múltiplas colunas;
- gráficos;
- barras de skills;
- imagens contendo texto.

O objetivo é manter o currículo visualmente profissional e ATS-friendly.

---

## 17. DEMO MODE

Criar botão:

"Carregar Demonstração"

Fornecer um candidato fictício e uma vaga fictícia para que o projeto possa ser testado imediatamente.

### Candidato de demonstração

- Software Engineer
- JavaScript
- TypeScript
- React
- Node.js
- REST APIs

### Vaga de demonstração

- Senior Frontend Engineer
- React
- TypeScript
- Next.js
- AWS
- JavaScript

Identificar claramente:

"Modo demonstração"

Não misturar dados fictícios com dados reais.

---

## 18. DESIGN E UX

Criar uma interface moderna, profissional e minimalista.

Utilizar:

- shadcn/ui;
- Tailwind;
- Lucide;
- cards apenas quando necessários;
- boa hierarquia visual;
- feedback claro.

Implementar:

- Dark Mode;
- Light Mode;
- layout responsivo;
- foco visível;
- navegação básica por teclado;
- contraste adequado.

### Paleta principal

- `#000000`
- `#2A0048`
- `#560072`
- `#800080`
- `#A90072`
- `#D50048`
- `#FF0000`

Usar vermelho apenas para estados críticos.

---

## 19. ESCOPO E RESTRIÇÕES

Não implementar:

- login;
- cadastro;
- OAuth;
- pagamentos;
- banco de dados externo;
- backend complexo;
- sistema de assinatura;
- anúncios;
- chat;
- IA externa obrigatória;
- parsing avançado de PDF/DOCX;
- histórico complexo;
- versionamento avançado.

Utilizar lógica local e dados persistidos no navegador.

Se alguma funcionalidade exigir complexidade desproporcional ao MVP, priorizar uma implementação simples e funcional.

Não criar botões que não tenham funcionalidade real.

Não utilizar scores aleatórios ou dados falsos apresentados como reais.

---

## 20. CRITÉRIO FINAL

O projeto deve ser um **MVP pequeno, funcional e apresentável**, adequado para um desafio da DIO e para publicação no GitHub.

O fluxo principal deve funcionar de ponta a ponta:

Currículo  
↓  
Descrição da vaga  
↓  
Analisar  
↓  
Match Score  
↓  
ATS Score  
↓  
Keywords  
↓  
Gaps  
↓  
Recomendações  
↓  
Currículo otimizado  
↓  
Antes/Depois  
↓  
Preview

Priorize, nesta ordem:

1. Funcionalidade
2. Código organizado
3. UX
4. Responsividade
5. Acessibilidade
6. Design


```


## Resultado Final


Este aplicativo é uma **plataforma de análise e otimização de currículos para sistemas ATS** que compara o currículo do usuário com descrições de vagas, identificando compatibilidade, keywords, gaps e oportunidades de melhoria.

<img width="1203" height="820" alt="image" src="https://github.com/user-attachments/assets/bce2742d-6615-49e6-9a90-d22c0ccc4947" />


Ele permite gerenciar um currículo mestre, calcular pontuações transparentes de **Match** e **ATS**, gerar sugestões de otimização e visualizar as alterações antes de finalizar o currículo.

<img width="1186" height="817" alt="image-1" src="https://github.com/user-attachments/assets/26825649-8664-484a-8525-55b40ed7947f" />


Desenvolvido como um MVP educacional, o projeto prioriza simplicidade, funcionalidade, responsividade e acessibilidade, mantendo como princípio fundamental a **não invenção de experiências, competências ou resultados**.

<img width="1175" height="822" alt="image-2" src="https://github.com/user-attachments/assets/11c2b215-6a19-40d3-a271-73190f3593b3" />

<img width="1179" height="825" alt="image-3" src="https://github.com/user-attachments/assets/f891d66f-e5a8-46e9-ae68-590f646e408b" />

## O que o APP faz?


O aplicativo permite que o usuário **compare seu currículo com uma vaga**, identificando o nível de compatibilidade e os principais pontos que podem ser melhorados.

- 📄 **Gerencia o currículo mestre**
- 🔎 **Analisa descrições de vagas**
- 📊 **Calcula Match Score e ATS Score**
- 🔑 **Identifica keywords encontradas e ausentes**
- ⚠️ **Aponta gaps e requisitos não comprovados**
- 💡 **Gera recomendações de melhoria**
- ✍️ **Cria uma versão otimizada do currículo**
- 🔄 **Compara alterações antes e depois**
- 👀 **Exibe um preview do currículo otimizado**
- 💾 **Salva os dados localmente no navegador**

O aplicativo foi desenvolvido com foco em **simplicidade, funcionalidade e compatibilidade com ATS**, sem inventar experiências, competências ou resultados que não estejam presentes no currículo.

## Reflexão sobre todo o processo:

Usando o prompt que montei para o projeto, o Lovable rapidamente criou uma versão bastante precisa e funcional do aplicativo. Fiquei bastante impressionado com o resultado inicial e com a capacidade da plataforma de transformar uma ideia em uma aplicação completa usando apenas linguagem natural.

Durante o processo, fui fazendo alguns ajustes e refinando o aplicativo através de novos comandos, principalmente na interface e nas funcionalidades. Novamente, o Lovable conseguiu entender bem o que eu estava pedindo e realizar as alterações de forma rápida.

Fiquei bastante surpreso com a rapidez e a precisão dessa plataforma de criação de APPS e com a facilidade de transformar uma ideia em um projeto funcional.

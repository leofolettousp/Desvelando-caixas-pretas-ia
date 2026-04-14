# Desvelando as Caixas-Pretas
## Guia de Documentação da Pesquisa — Repositório GitHub

> Projeto de pesquisa vinculado ao Claro nº 1245716, Departamento de Comunicação e Artes (CCA), ECA-USP.  
> Proponente: Prof. Dr. Leonardo Feltrin Foletto  
> Área: Tecnologias da Comunicação com ênfase em Inteligência Artificial

---

## Sumário

1. [Estrutura do repositório](#1-estrutura-do-repositório)
2. [Passo a passo: como criar o repositório](#2-passo-a-passo-como-criar-o-repositório)
3. [Fluxo de documentação — Fase 1](#3-fluxo-de-documentação--fase-1)
4. [Ficha A — Empresa Desenvolvedora](#4-ficha-a--empresa-desenvolvedora)
5. [Ficha B — Documentação Técnica, Termos de Serviço e Políticas de Dados](#5-ficha-b--documentação-técnica-termos-de-serviço-e-políticas-de-dados)
6. [Guia de preenchimento e boas práticas](#6-guia-de-preenchimento-e-boas-práticas)
7. [Modelos prontos para copiar](#7-modelos-prontos-para-copiar)

---

## 1. Estrutura do repositório

O repositório é organizado por modelo de IA e por dimensão analítica — espelhando as quatro dimensões do framework da pesquisa. A estrutura abaixo deve ser criada desde o início, mesmo que as pastas estejam inicialmente vazias.

```
desvelando-caixas-pretas/
│
├── README.md                          ← Apresentação pública do projeto
├── CONTRIBUTING.md                    ← Instruções para bolsistas e colaboradores
├── LICENSE.md                         ← Licença CC BY 4.0
│
├── 00_metodologia/
│   ├── framework_analitico.md         ← Descrição das 4 dimensões
│   ├── protocolo_coleta.md            ← Este guia (versão resumida)
│   └── criterios_selecao_modelos.md   ← Justificativa dos modelos escolhidos
│
├── 01_modelos/
│   ├── chatgpt_openai/
│   │   ├── A_empresa_desenvolvedora.md
│   │   ├── B_documentacao_termos.md
│   │   ├── C_dados_treinamento.md     ← Fichas C e D serão criadas nas próximas fases
│   │   ├── D_modelo_economico.md
│   │   └── fontes/                    ← PDFs, prints e arquivos coletados
│   │
│   ├── gemini_google/
│   │   └── [mesma estrutura]
│   │
│   ├── deepseek/
│   │   └── [mesma estrutura]
│   │
│   └── claude_anthropic/
│       └── [mesma estrutura]
│
├── 02_analise_comparativa/
│   └── tabela_comparativa.md          ← Síntese entre modelos (preenchida ao longo da pesquisa)
│
├── 03_producao/
│   ├── artigos/
│   ├── resumos_congressos/
│   └── materiais_extensao/
│
└── 04_diario_de_pesquisa/
    └── AAAA-MM-DD_log.md              ← Registros de reuniões, decisões e descobertas
```

---

## 2. Passo a passo: como criar o repositório

### Etapa 1 — Criar o repositório no GitHub

1. Acesse [github.com](https://github.com) e faça login
2. Clique em **"New repository"**
3. Preencha:
   - **Repository name**: `desvelando-caixas-pretas`
   - **Description**: `Pesquisa sobre análise crítica de sistemas de IA generativa em processos comunicacionais — CCA/ECA-USP`
   - **Visibility**: `Public` *(para garantir princípios de ciência aberta)*
   - Marque **"Add a README file"**
   - Em **"Add .gitignore"**: escolha `Python` (útil para futuras análises de dados)
   - Em **"Choose a license"**: escolha `Creative Commons Attribution 4.0` ou adicione manualmente depois
4. Clique em **"Create repository"**

### Etapa 2 — Criar a estrutura de pastas

O GitHub não cria pastas vazias nativamente. Para criar a estrutura, use um dos dois caminhos:

**Opção A — Via interface web (para iniciantes):**
- Para cada pasta, crie um arquivo placeholder dentro dela
- Clique em **"Add file" > "Create new file"**
- No campo de nome, escreva o caminho completo, como: `01_modelos/chatgpt_openai/A_empresa_desenvolvedora.md`
- Insira um comentário mínimo no arquivo: `# Em construção`
- Clique em **"Commit new file"**
- Repita para cada pasta e arquivo

**Opção B — Via terminal (recomendada para quem usa Git localmente):**
```bash
git clone https://github.com/seu-usuario/desvelando-caixas-pretas
cd desvelando-caixas-pretas
mkdir -p 01_modelos/chatgpt_openai/fontes
mkdir -p 01_modelos/gemini_google/fontes
mkdir -p 01_modelos/deepseek/fontes
mkdir -p 01_modelos/claude_anthropic/fontes
mkdir -p 00_metodologia 02_analise_comparativa 03_producao 04_diario_de_pesquisa
# criar arquivos placeholder em cada pasta
touch 01_modelos/chatgpt_openai/A_empresa_desenvolvedora.md
# ... (repetir para os demais)
git add .
git commit -m "estrutura inicial do repositório"
git push
```

### Etapa 3 — Configurar o README principal

O `README.md` é a vitrine pública do projeto. Deve conter: título, descrição do projeto, vínculo institucional (CCA/ECA-USP), licença, lista dos modelos analisados, estrutura do repositório e como contribuir. Um modelo básico está disponível no item 7 deste guia.

### Etapa 4 — Definir fluxo de trabalho com bolsistas

- Cada bolsista de IC recebe uma **issue** no GitHub para cada ficha a preencher
- O preenchimento é feito em **branches separadas** e revisado via **pull request**
- Isso garante rastreabilidade de quem coletou cada dado e quando
- Para equipes iniciantes no Git, o **GitHub Desktop** ([desktop.github.com](https://desktop.github.com)) é uma alternativa visual ao terminal

### Etapa 5 — Criar o sistema de issues para controle de tarefas

No repositório, vá em **"Issues" > "Labels"** e crie etiquetas como:
- `fase-1` / `fase-2` / `fase-3`
- `modelo:chatgpt` / `modelo:gemini` / `modelo:deepseek` / `modelo:claude`
- `dimensao:empresa` / `dimensao:dados` / `dimensao:economico` / `dimensao:relacao`
- `em-andamento` / `revisao` / `concluido`

---

## 3. Fluxo de documentação — Fase 1

O diagrama abaixo descreve o caminho de cada dado coletado, desde a fonte até o repositório.

```
FONTE PRIMÁRIA                  ANÁLISE INTERMEDIÁRIA           REPOSITÓRIO
(site, PDF, paper, ToS)  →→→   (leitura crítica + notas)  →→→  (ficha preenchida)
        ↓                                ↓                              ↓
  salvar em /fontes/          registrar no diário de pesquisa    commit no GitHub
  com nome padronizado        (04_diario_de_pesquisa/)           com mensagem clara
```

**Convenção de nomenclatura para arquivos em `/fontes/`:**

```
AAAA-MM-DD_[modelo]_[tipo]_[descrição-curta].[extensão]

Exemplos:
2025-09-15_openai_ToS_termos-de-servico-v2025.pdf
2025-10-02_deepseek_paper_deepseek-v3-technical-report.pdf
2025-10-10_anthropic_policy_acceptable-use-policy.pdf
2025-11-03_google_doc_gemini-technical-report-2024.pdf
```

---

## 4. Ficha A — Empresa Desenvolvedora

> **Arquivo correspondente no repositório:** `01_modelos/[nome-do-modelo]/A_empresa_desenvolvedora.md`  
> **Responsável pela coleta:** [nome do pesquisador/bolsista]  
> **Data de início:** AAAA-MM-DD  
> **Data da última atualização:** AAAA-MM-DD

---

### A.1 — Identificação básica

| Campo | Conteúdo |
|---|---|
| **Nome do modelo analisado** | |
| **Nome completo da empresa desenvolvedora** | |
| **Sede (país e cidade)** | |
| **Ano de fundação da empresa** | |
| **Ano de lançamento deste modelo** | |
| **Versão(ões) atual(is) do modelo** | |
| **Site oficial** | |
| **Perfil no GitHub (se houver)** | |
| **Tipo de empresa** | ☐ Startup privada ☐ Divisão de big tech ☐ Pesquisa sem fins lucrativos ☐ Outro: |

---

### A.2 — Estrutura de propriedade e controle

| Campo | Conteúdo |
|---|---|
| **Fundadores e liderança atual (CEO, CTO)** | |
| **Principais investidores (pessoas físicas e fundos)** | |
| **Maiores empresas acionistas ou parceiras estratégicas** | |
| **Valor de mercado ou valuation estimado (com data)** | |
| **Últimas rodadas de investimento (série, valor, data)** | |
| **A empresa é controlada por outra corporação?** | ☐ Sim — qual: ☐ Não ☐ Parcialmente |
| **Há participação governamental (de qualquer país)?** | ☐ Sim — qual governo/agência: ☐ Não ☐ Não identificado |

> 📎 **Fontes recomendadas para esta seção:** Crunchbase, PitchBook, SEC (para empresas americanas), registros de imprensa no Bloomberg e Reuters.  
> 📎 **Ferramenta de IA útil:** Perplexity AI (modo Finance) para sintetizar histórico de investimentos.

---

### A.3 — Origem e trajetória

| Campo | Conteúdo |
|---|---|
| **Breve histórico da empresa (até 200 palavras)** | |
| **Principais marcos tecnológicos (lançamentos relevantes)** | |
| **Controvérsias públicas relevantes (trabalhistas, legais, regulatórias)** | |
| **Processos judiciais em andamento relacionados à IA** | |
| **Posicionamento declarado sobre ética em IA** | |

> 📎 **Fontes recomendadas:** MIT Technology Review, The Verge, Wired, The Guardian; para processos judiciais, consultar o [AI Litigation Database](https://ailitigation.law).

---

### A.4 — Presença e impacto no Brasil

| Campo | Conteúdo |
|---|---|
| **A empresa tem escritório, parceiros ou representação formal no Brasil?** | ☐ Sim — qual: ☐ Não ☐ Não identificado |
| **Dados de uso no Brasil (número de usuários, tráfego — citar fonte e data)** | |
| **A empresa já foi mencionada em debates regulatórios brasileiros (ANPD, PL 2.338)?** | ☐ Sim — contexto: ☐ Não ☐ Não investigado |
| **Parcerias com empresas, universidades ou governo brasileiro** | |
| **Cobertura de mídia brasileira relevante (listar até 3 reportagens com links)** | |

---

### A.5 — Notas críticas e observações da equipe

> *Espaço livre para análises preliminares, hipóteses, contradições identificadas nas fontes, perguntas em aberto e conexões com o quadro teórico da pesquisa. Não precisa ser conclusivo — é um espaço de pensamento.*

```
[Inserir notas aqui]
```

---

### A.6 — Registro de fontes consultadas (Ficha A)

| # | Tipo | Título / Descrição | URL ou localização | Data de acesso | Arquivo salvo em /fontes/? |
|---|---|---|---|---|---|
| 1 | | | | | ☐ Sim ☐ Não |
| 2 | | | | | ☐ Sim ☐ Não |
| 3 | | | | | ☐ Sim ☐ Não |
| 4 | | | | | ☐ Sim ☐ Não |
| 5 | | | | | ☐ Sim ☐ Não |

> *Tipos sugeridos: paper acadêmico / documentação oficial / reportagem / relatório / banco de dados / outro*

---

## 5. Ficha B — Documentação Técnica, Termos de Serviço e Políticas de Dados

> **Arquivo correspondente no repositório:** `01_modelos/[nome-do-modelo]/B_documentacao_termos.md`  
> **Responsável pela coleta:** [nome do pesquisador/bolsista]  
> **Data de início:** AAAA-MM-DD  
> **Data da última atualização:** AAAA-MM-DD

---

### B.1 — Documentação técnica pública

| Campo | Conteúdo |
|---|---|
| **Existe paper técnico oficial do modelo?** | ☐ Sim ☐ Não ☐ Parcial (relatório reduzido) |
| **Título e link do paper técnico principal** | |
| **Data de publicação do paper** | |
| **Onde foi publicado (arXiv, blog, conferência)?** | |
| **Existe "model card" publicada?** | ☐ Sim — link: ☐ Não |
| **Existe documentação de API pública?** | ☐ Sim — link: ☐ Não |
| **O modelo tem código aberto (total ou parcial)?** | ☐ Total ☐ Parcial — o que é aberto: ☐ Fechado |
| **Arquitetura declarada do modelo** | *(ex: transformer, diffusion, MoE — descrever o que está documentado)* |
| **Parâmetros declarados do modelo** | *(número de parâmetros, se divulgado)* |
| **O que NÃO é divulgado na documentação técnica** | *(registrar lacunas e omissões — tão importante quanto o que é dito)* |

> 📎 **Fontes recomendadas:** arXiv (`arxiv.org`), GitHub da empresa, blog técnico oficial, Hugging Face (`huggingface.co`) para modelos open source.  
> 📎 **Ferramenta de IA útil:** Claude ou NotebookLM para síntese de papers técnicos longos em PDF.

---

### B.2 — Termos de serviço (ToS)

| Campo | Conteúdo |
|---|---|
| **Link oficial dos termos de serviço** | |
| **Data da versão atual dos termos** | |
| **Data da última atualização registrada** | |
| **A plataforma usa dados de conversas para re-treinar modelos?** | ☐ Sim ☐ Não ☐ Opcional (usuário pode optar por não) ☐ Não especificado |
| **É possível optar por não ter dados usados para treinamento (opt-out)?** | ☐ Sim — como: ☐ Não ☐ Apenas em planos pagos |
| **Quais dados do usuário são coletados (declarado nos ToS)?** | |
| **Por quanto tempo os dados são retidos?** | |
| **Os dados são compartilhados com terceiros? Com quem?** | |
| **Há cláusula de arbitragem ou renúncia a ações coletivas?** | ☐ Sim ☐ Não ☐ Não identificado |
| **Em qual jurisdição os termos estão sujeitos (lei aplicável)?** | |
| **Os ToS mencionam especificamente usuários brasileiros ou a LGPD?** | ☐ Sim — como: ☐ Não |
| **Avaliação no Terms of Service; Didn't Read (tosdr.org)** | *(nota e principais problemas identificados pela plataforma, se disponível)* |

> 📎 **Fontes recomendadas:** Página oficial de ToS de cada empresa; [tosdr.org](https://tosdr.org); relatórios da EFF ([eff.org](https://eff.org)) e da Access Now ([accessnow.org](https://accessnow.org)).

---

### B.3 — Política de privacidade e uso de dados

| Campo | Conteúdo |
|---|---|
| **Link oficial da política de privacidade** | |
| **Data da versão atual** | |
| **Onde os dados dos usuários são armazenados (país/servidor)?** | |
| **A empresa transfere dados para outros países?** | ☐ Sim — para quais: ☐ Não ☐ Não especificado |
| **Há menção à conformidade com a LGPD brasileira?** | ☐ Sim ☐ Não ☐ Menciona apenas GDPR europeu |
| **A empresa já foi investigada ou notificada por autoridades de proteção de dados?** | ☐ Sim — por qual autoridade e em que contexto: ☐ Não ☐ Não investigado |
| **Qual é o mecanismo para o usuário solicitar exclusão de dados?** | |
| **Há política específica para menores de idade?** | ☐ Sim ☐ Não ☐ Não identificado |

> 📎 **Fontes recomendadas:** Política de privacidade oficial; registros da ANPD ([gov.br/anpd](https://www.gov.br/anpd)); decisões do ICO (Reino Unido) e CNIL (França) — frequentemente mais detalhadas que as autoridades brasileiras para esses modelos.

---

### B.4 — Política de uso aceitável (Acceptable Use Policy)

| Campo | Conteúdo |
|---|---|
| **Existe uma política de uso aceitável separada dos ToS?** | ☐ Sim — link: ☐ Não (está dentro dos ToS) |
| **Quais usos são explicitamente proibidos?** | |
| **Há restrições para uso em contextos jornalísticos ou de pesquisa?** | ☐ Sim — quais: ☐ Não |
| **Há restrições para uso em contextos políticos ou eleitorais?** | ☐ Sim — quais: ☐ Não |
| **A política menciona conteúdo em português ou contextos brasileiros?** | ☐ Sim ☐ Não |
| **Como a empresa lida com violações da política (moderação, banimento)?** | |
| **Há mecanismo de recurso para usuários banidos ou com conteúdo removido?** | ☐ Sim ☐ Não ☐ Não especificado |

---

### B.5 — Análise crítica dos documentos (perspectiva do projeto)

> *Esta seção é a mais importante analiticamente. Aqui a equipe registra o que os documentos revelam além do declarado: o que é omitido, o que é vago propositalmente, que assimetrias de poder os textos jurídicos constroem, como o discurso técnico funciona como legitimação. Orientar pela pergunta de Pasquinelli (2023): o que esse documento esconde ao mesmo tempo em que revela?*

**B.5.1 — Opacidades e omissões identificadas**

```
[Registrar o que NÃO está nos documentos e o que isso significa]
```

**B.5.2 — Linguagem e retórica dos documentos**

```
[Analisar como os termos são redigidos: qual sujeito é apagado? 
Que responsabilidades são transferidas para o usuário?
Que promessas são feitas sem mecanismos de verificação?]
```

**B.5.3 — Implicações para usuários brasileiros e do Sul Global**

```
[Registrar especificidades: ausência de menção à LGPD, 
jurisdição aplicável desfavorável, barreiras de idioma nos ToS, 
impacto assimétrico sobre usuários sem acesso a assessoria jurídica]
```

**B.5.4 — Conexões com o quadro teórico**

```
[Relacionar achados com referências do projeto: 
Pasquale (2015) sobre opacidade algorítmica como estratégia de poder;
Couldry e Mejías (2019) sobre colonialismo de dados;
Faustino e Lippold (2023) sobre colonialismo digital etc.]
```

---

### B.6 — Registro de fontes consultadas (Ficha B)

| # | Tipo | Título / Descrição | URL ou localização | Data de acesso | Arquivo salvo em /fontes/? |
|---|---|---|---|---|---|
| 1 | | | | | ☐ Sim ☐ Não |
| 2 | | | | | ☐ Sim ☐ Não |
| 3 | | | | | ☐ Sim ☐ Não |
| 4 | | | | | ☐ Sim ☐ Não |
| 5 | | | | | ☐ Sim ☐ Não |

---

## 6. Guia de preenchimento e boas práticas

### Para toda a equipe (pesquisador principal e bolsistas de IC)

**Sobre o preenchimento das fichas:**
- Sempre registrar a **data de acesso** a cada fonte: ToS e políticas de privacidade mudam com frequência e sem aviso
- Quando um campo não tiver informação disponível publicamente, escrever **"Não divulgado"** — não deixar em branco. A ausência de informação é um dado analítico
- Distinguir entre o que a empresa **declara** e o que **pesquisas independentes demonstram** — usar formatação diferente ou marcação `[DECLARADO]` vs `[VERIFICADO INDEPENDENTEMENTE]`
- Salvar sempre uma cópia local dos documentos analisados (PDF ou print) na pasta `/fontes/`, com nome padronizado. Sites mudam e documentos somem

**Sobre os commits no GitHub:**
- Escrever mensagens de commit descritivas:
  - ✅ `adiciona ficha A do ChatGPT - seções A.1 e A.2 concluídas`
  - ❌ `update` / `changes` / `ficha`
- Fazer commits frequentes, não esperar a ficha estar 100% completa
- Usar o campo de descrição do commit para registrar dúvidas ou decisões metodológicas

**Sobre integridade das fontes:**
- Não parafrasear documentos jurídicos (ToS, políticas de privacidade) sem citar a versão exata
- Para citações de papers, usar o DOI quando disponível
- Registrar contradições entre fontes: se a documentação oficial diz X e uma reportagem investigativa diz Y, registrar **ambos** com suas respectivas fontes

### Específico para bolsistas de IC

- Antes de preencher qualquer ficha, ler o documento `00_metodologia/framework_analitico.md`
- Abrir uma **issue** no GitHub antes de começar uma ficha, com seu nome e prazo estimado
- Em caso de dúvida sobre como classificar uma informação, registrar no diário de pesquisa (`04_diario_de_pesquisa/`) e mencionar o orientador via `@menção` no GitHub
- A seção **B.5 (Análise crítica)** deve ser preenchida **em conjunto** com o orientador nas primeiras fichas, antes de ser feita de forma independente

---

## 7. Modelos prontos para copiar

### README.md principal do repositório

```markdown
# Desvelando as Caixas-Pretas

**Análise crítica de sistemas de IA generativa em processos comunicacionais**

Projeto de pesquisa vinculado ao Departamento de Comunicação e Artes (CCA),  
Escola de Comunicação e Artes, Universidade de São Paulo (ECA-USP).

**Proponente:** Prof. Dr. Leonardo Feltrin Foletto  
**Período:** 2025–2028  
**Área:** Tecnologias da Comunicação com ênfase em Inteligência Artificial

---

## Sobre o projeto

Este repositório documenta publicamente o processo de pesquisa do projeto 
"Desvelando as Caixas-Pretas", que propõe um framework de análise crítica de 
sistemas de IA generativa centrado em quatro dimensões: arquiteturas algorítmicas, 
dados de treinamento, modelos econômicos e relações de poder entre sistemas de IA 
e pessoas — com foco em implicações para comunicadores, educomunicadores e 
criadores do Sul Global.

## Modelos analisados

- [ChatGPT (OpenAI)](01_modelos/chatgpt_openai/)
- [Gemini (Google)](01_modelos/gemini_google/)
- [DeepSeek (DeepSeek AI)](01_modelos/deepseek/)
- [Claude (Anthropic)](01_modelos/claude_anthropic/)

## Estrutura

Ver [CONTRIBUTING.md](CONTRIBUTING.md) para instruções de colaboração.

## Licença

Todo o conteúdo deste repositório está disponível sob licença  
[Creative Commons Attribution 4.0 International (CC BY 4.0)](LICENSE.md).

## Contato

leonardo.foletto@usp.br  
[baixacultura.org](https://baixacultura.org)
```

---

### Entrada no diário de pesquisa (`04_diario_de_pesquisa/`)

```markdown
# Diário de Pesquisa — AAAA-MM-DD

**Participantes:** [nomes]  
**Tipo de encontro:** ☐ Reunião de orientação ☐ Sessão de coleta ☐ Discussão teórica ☐ Outro

## O que foi feito

[Descrever as atividades realizadas]

## Decisões metodológicas tomadas

[Registrar qualquer decisão sobre como coletar, classificar ou analisar dados]

## Dúvidas e questões em aberto

[Listar perguntas que surgiram e ainda não foram respondidas]

## Conexões teóricas identificadas

[Relacionar achados do dia com referências bibliográficas do projeto]

## Próximos passos

- [ ] tarefa 1 — responsável:
- [ ] tarefa 2 — responsável:
- [ ] tarefa 3 — responsável:
```

---

*Documento elaborado para o projeto "Desvelando as Caixas-Pretas" — CCA/ECA-USP, 2025.*  
*Licença: CC BY 4.0*

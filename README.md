# STRIDE Threat Model Analyzer

Uma solução prática para geração e visualização de modelos de ameaça baseada na metodologia **STRIDE**. O projeto combina um backend em **FastAPI** (Python) com um frontend em HTML/CSS/JS e utiliza **Cytoscape.js** para visualização interativa do grafo de ameaças.

> Inspiração / versão original: https://github.com/digitalinnovationone/stride-demo?tab=readme-ov-file

---

## Visão geral

O sistema permite fazer upload de uma imagem da arquitetura do sistema, preencher informações de contexto e gerar automaticamente um modelo de ameaças STRIDE usando **Azure OpenAI**. O resultado é apresentado em um grafo interativo que pode ser explorado, exportado e impresso.

---

## Funcionalidades

- Upload de imagem de arquitetura e formulário para dados do sistema.  
- Geração automática do modelo de ameaças STRIDE via **Azure OpenAI**.  
- Visualização do modelo em grafo interativo com **Cytoscape.js** (nós, arestas e rótulos de ameaça).  
- Sugestões acionáveis para mitigações e melhorias.  
- Opção para imprimir ou exportar o grafo gerado.

---

## Arquitetura

- **Backend:** FastAPI (Python) — recebe o input do usuário, orquestra chamadas à API do Azure OpenAI e prepara os dados para o frontend.  
- **Frontend:** HTML/CSS/JavaScript com **Cytoscape.js** — exibe o grafo e permite interação com nós/arestas.  
- **Integração:** Azure OpenAI para geração automatizada de ameaças e recomendações.

---

## Requisitos mínimos

- Python 3.8+  
- Pip  
- Conta e chave da **Azure OpenAI** (ou outra chave compatível)  
- Navegador moderno (Chrome/Firefox)

---

## Como executar (exemplo)

1. Clone o repositório:
   ```bash
   git clone <url-do-repo>
   cd <nome-do-repo>
   ```

2. Crie e ative um ambiente virtual:

   ```bash
   python -m venv .venv
   source .venv/bin/activate    # Unix / macOS
   .venv\Scripts\activate       # Windows
   ```

3. Instale dependências:

   ```bash
   pip install -r requirements.txt
   ```

4. Configure a variável de ambiente com a chave do Azure OpenAI:

   ```bash
   export AZURE_OPENAI_KEY="sua_chave_aqui"    # Unix / macOS
   set AZURE_OPENAI_KEY="sua_chave_aqui"       # Windows
   ```

5. Rode o backend:

   ```bash
   uvicorn app.main:app --reload
   ```

6. Abra o frontend no navegador (geralmente `http://localhost:8000`), carregue a imagem da arquitetura e gere o modelo de ameaças.

> Observação: os comandos acima são exemplos; verifique o README do repositório original para instruções específicas sobre nomes de arquivos e endpoints.

---

## O que aprendi com o projeto

* Integração prática com a API da OpenAI/Azure para resolver problemas reais.
* Automação de tarefas repetitivas, gerando modelos e recomendações automaticamente aumentando assim a produtividade.
* Como a inteligência artificial pode acelerar e escalar processos de análise de segurança.

---

## Créditos

Baseado no trabalho original de: **digitalinnovationone** — [https://github.com/digitalinnovationone/stride-demo?tab=readme-ov-file](https://github.com/digitalinnovationone/stride-demo?tab=readme-ov-file)

---



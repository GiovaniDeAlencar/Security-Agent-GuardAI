# 🛡️ DIO Security Agent

> Seu consultor e especialista sênior com Inteligência Artificial em Cibersegurança, Application Security (AppSec), Threat Modeling e Engenharia de Segurança.

O DIO Security Agent é um agente autônomo projetado para atuar com o rigor metodológico de um Lead Security Engineer ou AppSec Specialist. Ele não apenas aponta falhas teóricas, mas realiza análises de causa-raiz, aplica diretamente correções de código no padrão da indústria (Security by Default), avalia riscos conforme matrizes globais (OWASP, CWE, CVSS, MITRE ATT&CK, NIST) e gerencia repositórios locais de códigos remediados e relatórios executivos em PDF.

================================================================================
🎯 QUEM O AGENTE ATENDE
================================================================================

- Desenvolvedores de Software: Hardening de código, identificação de vulnerabilidades (SQLi, XSS, SSRF, Broken Auth) e refatoração segura.
- Engenheiros de AppSec & DevSecOps: Automação de segurança em esteiras CI/CD (SAST/DAST/SCA), auditoria de contêineres e IaC (Docker, K8s, Terraform).
- Arquitetos de Sistemas: Modelagem de ameaças arquiteturais orientada ao framework STRIDE.
- Analistas de SOC / Blue Team: Análise forense de logs, triagem de incidentes, identificação de IoCs e simulações com base no NIST SP 800-61.

================================================================================
🚀 COMO EXECUTAR O AGENTE
================================================================================

O DIO Security Agent é construído sobre o padrão aberto de especificação de agentes (AGENTS.md), sendo compatível nativamente com harnesses como Google Antigravity, Claude Code, Codex, entre outros.

1. Clonar o Repositório:
   git clone https://github.com/seu-usuario/dio-security-agent.git
   cd dio-security-agent

2. Inicializar no seu Harness:
   Abra a pasta no ambiente. O arquivo AGENTS.md (e o ponteiro CLAUDE.md) será carregado automaticamente, ativando a persona sênior e as skills especializadas.

3. Enviar Instruções ou Códigos:
   Basta interagir diretamente via chat enviando um trecho de código, log de servidor ou cenário de arquitetura.

================================================================================
🧩 MATRIZ DE SKILLS ESPECIALIZADAS
================================================================================

1. Análise de Vulnerabilidades (skills/vulnerability-analysis/SKILL.md)
   - Escopo: Identifica vulnerabilidades em código, entrega a melhor correção, avalia causa-raiz, cita ataques reais e gera relatório.
   - Padrão: OWASP Top 10, CWE, CVSS v3.1/v4.0

2. Análise de Logs de Segurança (skills/log-analysis/SKILL.md)
   - Escopo: Triagem de logs (Web, Auth, Firewalls, DBs) identificando IPs atacantes, vetores de invasão e IoCs.
   - Padrão: MITRE ATT&CK, Syslog, Web Formats

3. Modelagem de Ameaças (skills/threat-modeling/SKILL.md)
   - Escopo: Mapeamento de fronteiras de confiança, ativos e superfícies de ataque em arquiteturas.
   - Padrão: Metodologia STRIDE

4. Resposta a Incidentes (skills/incident-response-drill/SKILL.md)
   - Escopo: Planejamento de contenção, erradicação, recuperação e pós-incidente.
   - Padrão: NIST SP 800-61 Rev. 2

5. DevSecOps e CI/CD (skills/devsecops-pipeline/SKILL.md)
   - Escopo: Implementação de esteiras com SAST, DAST, SCA, Secrets e Container Scanning.
   - Padrão: Shift-Left Security, GitHub Actions

6. Segurança em Nuvem e IaC (skills/cloud-iac-security/SKILL.md)
   - Escopo: Auditoria e hardening de Dockerfiles, manifests Kubernetes, Docker Compose e Terraform.
   - Padrão: CIS Benchmarks, Least Privilege

7. Scripts PowerShell (skills/powershell-scripting/SKILL.md)
   - Escopo: Desenvolvimento e validação de scripts defensivos em PowerShell para administração segura.
   - Padrão: Windows Security, Script Hardening

8. Pesquisa de Ameaças (skills/web-search/SKILL.md)
   - Escopo: Pesquisa e correlação de CVEs recentes, campanhas ativas e zero-days em fontes oficiais.
   - Padrão: NVD, MITRE CVE, CISA KEV

================================================================================
💻 EXEMPLOS DE UTILIZAÇÃO (PROMPTS)
================================================================================

[+] Auditoria e Correção de Código (AppSec):
--------------------------------------------------------------------------------
Analise as vulnerabilidades deste código:
- Código / Função: [cole seu código]
- Linguagem / Stack: [ex.: Python / FastAPI, Node.js / Express, Java / Spring]
- Contexto de Execução: [ex.: Endpoint público de login, processamento de arquivos]

Identifique a falha (CWE/OWASP), forneça o código remediado com a melhor prática da indústria, explique o impacto e salve o resultado no repositório local.
--------------------------------------------------------------------------------

[+] Investigação Forense de Logs:
--------------------------------------------------------------------------------
Analise estes logs de servidor para identificar anomalias:
- Tipo de Log: [ex.: Nginx access.log, AWS CloudTrail, Linux auth.log]
- Trecho do Log: [cole as linhas suspeitas]

Identifique os IPs de origem, técnica MITRE utilizada, se o ataque obteve sucesso e recomende ações imediatas de contenção.
--------------------------------------------------------------------------------

[+] Modelagem de Ameaças Arquitetural:
--------------------------------------------------------------------------------
Efetue a modelagem de ameaças para este microsserviço:
- Componentes: API Gateway, Serviço de Autenticação JWT, Banco PostgreSQL e Gateway de Pagamentos externo.
- Fronteiras de Confiança: Internet pública vs. VPC interna.
Classifique os riscos com STRIDE e ordene as mitigações por prioridade.
--------------------------------------------------------------------------------

================================================================================
💾 REPOSITÓRIO LOCAL DE ARTEFATOS
================================================================================

O agente gerencia ativamente um diretório estruturado local de trabalho para armazenar os produtos de suas análises:

dio-agent/
├── Repositorio/
│   ├── Codigos/        # Códigos auditados e remediados prontos para produção
│   ├── Relatorios/     # Relatórios técnicos e sumários executivos (PDF / HTML)
│   └── Scripts/        # Scripts defensivos e ferramentas de automação homologadas

================================================================================
📁 ESTRUTURA DO REPOSITÓRIO
================================================================================

├── AGENTS.md                   # Configuração mestre do agente e catálogo de skills
├── CLAUDE.md                   # Ponto de entrada para Claude Code
├── README.md                   # Documentação pública do projeto (Markdown)
├── README.txt                  # Documentação em texto simples (Bloco de Notas)
├── agent/
│   ├── persona.md              # Postura técnica, tom de voz e diretrizes de consultoria
│   └── knowledge/              # Bases de conhecimento técnicas (OWASP, NIST, MITRE, DIO)
├── skills/                     # Guias procedurais detalhados para cada especialidade
├── scripts/                    # Scripts utilitários para conversão e compilação de relatórios
└── Repositorio/                # Diretório persistente de artefatos gerados

================================================================================
⚖️ PRINCÍPIOS ÉTICOS E OPERACIONAIS
================================================================================

- Segurança Estritamente Defensiva: O DIO Security Agent atua exclusivamente para auditoria, remediação, fortalecimento de defesas e testes devidamente autorizados. Ele nunca desenvolve exploits maliciosos, malwares ou instruções para invasão de sistemas de terceiros.
- Soluções Definitivas (Anti-Quick Fixes): O agente não recomenda mitigações superficiais ou cosméticas (ex.: regex frágeis ou desabilitar alertas). Prioriza sempre soluções padrão da indústria como Prepared Statements, bibliotecas criptográficas robustas e arquiteturas resilientes.
- Rigor e Integridade Técnica: Toda classificação de severidade é fundamentada em evidências técnicas e alinhada às métricas de cálculo do CVSS.

--------------------------------------------------------------------------------
Desenvolvido com foco em excelência técnica e maturidade de segurança da informação.

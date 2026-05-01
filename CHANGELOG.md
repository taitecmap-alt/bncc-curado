# Changelog

Todas as mudanças relevantes neste projeto serão documentadas neste arquivo.

O formato é baseado em [Keep a Changelog](https://keepachangelog.com/pt-BR/1.1.0/),
e este projeto adere ao [Semantic Versioning](https://semver.org/lang/pt-BR/).

## [Unreleased]

Sem mudanças não publicadas no momento.

---

## [1.0.0] - 2026-04-30

Primeiro lançamento oficial. Catálogo curado de 247 habilidades da BNCC para Matemática do Ensino Fundamental, validado contra PDF oficial do MEC.

### Adicionado

- Estrutura inicial do repositório (README, LICENSE MIT, CHANGELOG, .gitignore)
- Catálogo de 247 habilidades em `data/habilidades-mat-fundamental.json`
- Schema JSON com campos: `codigo`, `descricao`, `ano`, `disciplina`
- Metadata embutida no JSON com proveniência completa:
  - `fonte`: catalogobncc.github.io/metadados/2022/03/30/efma
  - `data_extracao`: 2026-04-30
  - `data_validacao`: 2026-04-30
  - `fonte_validacao`: PDF oficial BNCC - basenacionalcomum.mec.gov.br
  - `total_habilidades`: 247
  - `escopo`: Matemática Fundamental (1º ao 9º ano)
  - `schema_versao`: 1.0.0

### Distribuição por ano

- 1º ano: 22 habilidades
- 2º ano: 23 habilidades
- 3º ano: 28 habilidades
- 4º ano: 28 habilidades
- 5º ano: 25 habilidades
- 6º ano: 34 habilidades
- 7º ano: 37 habilidades
- 8º ano: 27 habilidades
- 9º ano: 23 habilidades
- **Total**: 247 habilidades

### Validado

**Validação técnica automatizada (7 verificações):**

- Schema correto em 247/247 habilidades
- Códigos no formato `EFXXMAYY` (regex validado)
- Consistência ano (código vs campo): 247/247
- Disciplina sempre "Matemática"
- Descrições com tamanho razoável (33 a 360 chars, média 175)
- Sequência completa por ano (sem códigos faltantes)
- Zero duplicatas de código

**Validação textual contra PDF oficial:**

- Fonte: PDF oficial BNCC versão 2018 (BNCC_EI_EF_110518_versaofinal_site.pdf, 600 páginas, ~3 MB)
- Comparação: 247/247 habilidades validadas individualmente
- Resultado: **247/247 (100%) habilidades fiéis ao PDF oficial MEC**
  - 245 idênticas literalmente
  - 2 com diferenças apenas de extração do PDF (limitações do parser, não do JSON)

### Corrigido

Validação completa detectou 2 discrepâncias entre fonte primária (catalogobncc.github.io) e PDF oficial MEC, ambas corrigidas:

- **EF02MA06** (2º ano): removido `"ou convencionais"` (estava na fonte primária mas ausente no PDF MEC)
- **EF03MA05** (3º ano): adicionado `"inclusive os convencionais"` (estava no PDF MEC mas ausente na fonte primária)

### Limitações conhecidas

- Sem grafo de pré-requisitos entre habilidades (planejado para v2.0.0)
- Apenas Matemática (outras disciplinas planejadas)
- Apenas Ensino Fundamental (Médio e Infantil ficam fora desta versão)
- Sem agrupamento por unidades temáticas (Números, Geometria, etc.)

### Mantenedores

- [@taitecmap-alt](https://github.com/taitecmap-alt) — TaiTec / Bruno
- [@celoeug](https://github.com/celoeug) — Co-fundador

---

## Convenções deste CHANGELOG

### Tipos de mudança

- **Adicionado** para novas funcionalidades
- **Modificado** para mudanças em funcionalidades existentes
- **Descontinuado** para funcionalidades que serão removidas
- **Removido** para funcionalidades removidas
- **Corrigido** para correções de erros
- **Validado** para resultados de processos de validação
- **Segurança** em caso de vulnerabilidades

### Versionamento (SemVer)

Formato: MAJOR.MINOR.PATCH (exemplo: 1.2.3)

- **MAJOR**: mudanças incompatíveis com versões anteriores
- **MINOR**: adição de funcionalidades mantendo compatibilidade
- **PATCH**: correções de bugs sem mudar funcionalidades

Exemplos aplicados a este repositório:

- v1.0.0 → v1.0.1: correção de typo em descrição de habilidade
- v1.0.0 → v1.1.0: adição de pré-requisitos (nova funcionalidade)
- v1.0.0 → v2.0.0: mudança de estrutura JSON (quebra compatibilidade)

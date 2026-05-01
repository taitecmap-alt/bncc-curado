# bncc-curado

> Catálogo curado das habilidades da BNCC (Base Nacional Comum Curricular) brasileira, em formato JSON estruturado e validado, pronto para uso em sistemas educacionais.

**Status:** Estável | **Versão atual:** v1.0.0 (2026-04-30) | **Habilidades:** 247 | **Validação:** 100%

## 📖 Sobre

Este repositório contém uma versão estruturada e curada das habilidades definidas pela **Base Nacional Comum Curricular (BNCC)**, documento oficial do Ministério da Educação (MEC) que estabelece as aprendizagens essenciais para a Educação Básica no Brasil.

A BNCC é distribuída oficialmente pelo MEC como documento PDF de aproximadamente 600 páginas. Este repositório oferece uma versão **estruturada em JSON**, **validada integralmente** contra a fonte oficial, **versionada** e **pronta para consumo programático**.

## 🎯 Escopo

- **v1.0.0** — Matemática Fundamental (1º ao 9º ano) — Lançado em 2026-04-30
- **v2.0.0** — Acréscimo de pré-requisitos e sucessores — Planejado
- **v3.0.0** — Outras áreas (Português, Ciências, etc) — Planejado

## 📂 Estrutura do repositório

- `data/habilidades-mat-fundamental.json` — 247 habilidades
- `CHANGELOG.md` — Histórico de versões
- `LICENSE` — MIT
- `README.md` — Este arquivo

## 📊 Schema dos dados

Cada habilidade é representada como objeto JSON:

- **codigo** (string): código oficial BNCC, formato EFXXMAYY
- **descricao** (string): descrição da habilidade conforme texto oficial
- **ano** (number): ano escolar (1 a 9 para Fundamental)
- **disciplina** (string): nome da disciplina ("Matemática")

### Distribuição por ano (v1.0.0)

- 1º ano: 22 habilidades
- 2º ano: 23 habilidades
- 3º ano: 28 habilidades
- 4º ano: 28 habilidades
- 5º ano: 25 habilidades
- 6º ano: 34 habilidades
- 7º ano: 37 habilidades
- 8º ano: 27 habilidades
- 9º ano: 23 habilidades
- **Total: 247 habilidades**

## 🔍 Origem dos dados

**Fonte primária:** [catalogobncc.github.io/metadados](https://catalogobncc.github.io/metadados/), versão de março/2022.

**Fonte de validação:** PDF oficial da BNCC publicado pelo MEC (versão homologada de 2017 para Educação Infantil e Ensino Fundamental, 600 páginas).

**Processo:**

1. Extração automatizada da fonte primária
2. Estruturação em JSON com schema validado
3. Validação textual completa contra PDF oficial
4. Curadoria manual de discrepâncias detectadas

## 🔬 Validação

### Validação técnica automatizada

Todas 247 habilidades passaram por 7 verificações automatizadas:

- Schema correto em 247/247 habilidades
- Formato dos códigos validado (regex EFXXMAYY)
- Consistência ano (código vs campo): 247/247
- Disciplina sempre Matemática
- Descrições não vazias
- Sequência completa por ano
- Zero duplicatas

### Validação textual contra PDF oficial MEC

Todas 247 habilidades comparadas individualmente contra o PDF oficial:

- 245 idênticas literalmente ao PDF (99.2%)
- 2 com diferenças apenas de extração do PDF (0.8%)
- **Total fiel ao PDF oficial: 247/247 (100%)**

Detectadas e corrigidas 2 discrepâncias entre fonte primária e PDF MEC:

- **EF02MA06** (2º ano): removido texto extra ausente no PDF
- **EF03MA05** (3º ano): adicionado trecho presente no PDF

Detalhes completos no CHANGELOG.md.

## ⚠️ Limitações conhecidas

- Sem grafo de pré-requisitos (planejado para v2.0.0)
- Apenas Matemática (outras disciplinas planejadas)
- Apenas Ensino Fundamental
- Sem agrupamento por unidades temáticas

## 🤝 Como contribuir

Contribuições bem-vindas:

- Correções em descrições
- Adição de pré-requisitos validados
- Tradução para outros formatos (CSV, XML, YAML)
- Validação contra outras fontes

Por favor, abra Issue antes de Pull Request.

## 📜 Licença

Este projeto está sob licença MIT (ver LICENSE).

A BNCC em si é documento público do MEC, disponível em [basenacionalcomum.mec.gov.br](https://basenacionalcomum.mec.gov.br/).

## 🔗 Links úteis

- [BNCC oficial - MEC](https://basenacionalcomum.mec.gov.br/)
- [Catalogo BNCC (fonte primária)](https://catalogobncc.github.io/metadados/)

## 👥 Mantenedores

- [@taitecmap-alt](https://github.com/taitecmap-alt) — TaiTec / Bruno
- [@celoeug](https://github.com/celoeug) — Co-fundador

---

**v1.0.0** | 2026-04-30 | 247 habilidades | Validação 100% vs PDF MEC

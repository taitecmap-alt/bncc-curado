# bncc-curado

> Catálogo curado das habilidades da BNCC (Base Nacional Comum Curricular) brasileira, em formato JSON estruturado e validado, pronto para uso em sistemas educacionais.

## 📖 Sobre

Este repositório contém uma versão estruturada e curada das habilidades definidas pela **Base Nacional Comum Curricular (BNCC)**, documento oficial do Ministério da Educação (MEC) que estabelece as aprendizagens essenciais para a Educação Básica no Brasil.

A BNCC é distribuída oficialmente pelo MEC como documento PDF de aproximadamente 600 páginas. Este repositório oferece uma versão **estruturada em JSON**, **validada amostralmente** contra a fonte oficial, **versionada** e **pronta para consumo programático**.

## 🎯 Escopo atual

| Versão | Conteúdo                                    | Status      |
|--------|---------------------------------------------|-------------|
| v1.0.0 | Matemática Fundamental (1º ao 9º ano)      | Em curadoria|
| v2.0.0 | Acréscimo de pré-requisitos e sucessores    | Planejado   |
| v3.0.0 | Outras áreas (Português, Ciências, etc)     | Planejado   |

## 📂 Estrutura do repositório

```
bncc-curado/
├── data/                                       # JSONs estruturados
│   └── habilidades-mat-fundamental.json        # ~247 habilidades de Mat Fund
├── CHANGELOG.md                                # Histórico de versões
├── LICENSE                                     # MIT
└── README.md                                   # Este arquivo
```

## 📊 Schema dos dados

Cada habilidade é representada como objeto JSON com a seguinte estrutura:

```json
{
  "codigo": "EF06MA01",
  "descricao": "Comparar, ordenar, ler e escrever números naturais...",
  "ano": 6,
  "disciplina": "Matemática"
}
```

### Campos

- **codigo** (string): código oficial BNCC, formato `EFXXMAYY` (Ensino Fundamental)
- **descricao** (string): descrição da habilidade conforme texto oficial
- **ano** (number): ano escolar (1 a 9 para Fundamental)
- **disciplina** (string): nome da disciplina

## 🔍 Origem dos dados

**Fonte primária:** [catalogobncc.github.io/metadados](https://catalogobncc.github.io/metadados/), versão de março/2022.

**Fonte de validação:** PDF oficial da BNCC publicado pelo MEC (versão homologada de 2017 para Educação Infantil e Ensino Fundamental).

**Processo:**
1. Extração automatizada da fonte primária
2. Estruturação em JSON
3. Validação amostral de 20 habilidades aleatórias contra PDF oficial
4. Curadoria manual de eventuais discrepâncias

## ⚠️ Limitações conhecidas

Esta versão (v1.0.0) tem as seguintes limitações documentadas:

- **Sem grafo de pré-requisitos:** as habilidades não estão conectadas via relações de dependência (será adicionado em v2.0.0)
- **Apenas Matemática:** outras disciplinas serão adicionadas em versões futuras
- **Apenas Fundamental:** Ensino Médio e Educação Infantil ficam fora do escopo inicial
- **Sem unidades temáticas:** o agrupamento por temas (Números, Geometria, etc) não está incluído

## 🤝 Como contribuir

Contribuições são bem-vindas, especialmente:

- Correções em descrições de habilidades
- Adição de pré-requisitos validados pedagogicamente
- Tradução para outros formatos (CSV, XML, YAML)
- Validação amostral contra outras fontes

Por favor, abra uma **Issue** descrevendo a contribuição antes de enviar Pull Request.

## 📜 Licença

Este projeto está sob licença [MIT](LICENSE).

A BNCC em si é documento público do MEC, disponível em [basenacionalcomum.mec.gov.br](https://basenacionalcomum.mec.gov.br/).

## 🔗 Links úteis

- [BNCC oficial - MEC](https://basenacionalcomum.mec.gov.br/)
- [Catalogo BNCC (fonte primária)](https://catalogobncc.github.io/metadados/)
- [InovaSpark](https://github.com/taitecmap-alt) — projeto que originou esta curadoria

## 👥 Mantenedores

- [@taitecmap-alt](https://github.com/taitecmap-alt) — TaiTec / Bruno
- [@celoeug](https://github.com/celoeug) — Co-fundador

---

**Status:** Em desenvolvimento ativo • **Versão atual:** Em curadoria para v1.0.0

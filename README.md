<div align="center">
    <img src="https://github.com/cecape-tech.png" width="100" alt="CECAPE Engineering" style="border-radius: 15%"/>
    <h1>Quality Audits</h1>
    <p>
        <strong>Faculdade CECAPE — Divisão de Engenharia de Software</strong>
    </p>
    <p>
        <a href="https://faculdadececape.edu.br">faculdadececape.edu.br</a>
    </p>
</div>

<br/>

> Repositório centralizado de auditorias de qualidade dos produtos digitais da CECAPE Tech. Consolida relatórios de performance, acessibilidade, SEO, segurança e disponibilidade — rastreando a evolução de cada plataforma ao longo do tempo.

<br/>

## O que está incluído

| Categoria          | Descrição                                                                  |
| :----------------- | :------------------------------------------------------------------------- |
| **PageSpeed**      | Auditorias de performance via Google PageSpeed Insights (desktop + mobile) |
| **Lighthouse**     | Relatórios completos do Lighthouse (performance, SEO, boas práticas)       |
| **Acessibilidade** | Auditorias de conformidade com WCAG e ferramentas de acessibilidade        |
| **Benchmarks**     | Comparativos de performance entre versões e plataformas                    |
| **SEO**            | Análises de otimização para mecanismos de busca                            |
| **Segurança**      | Auditorias de segurança e vulnerabilidades                                 |
| **Uptime**         | Monitoramento de disponibilidade das plataformas                           |

---

## Estrutura do Repositório

```
quality-audits/
├── acessibility/                        # Auditorias de acessibilidade
├── benchmarks/                          # Comparativos de performance
├── lighthouse/                          # Relatórios Lighthouse
├── pagespeed/
│   ├── landing-pages/
│   │   ├── enem-calculator/
│   │   │   ├── desktop/                 # Capturas desktop com data
│   │   │   └── mobile/                 # Capturas mobile com data
│   │   ├── enem-simulator/
│   │   ├── lp-cursos-tecnicos/
│   │   ├── lp-graduacao/
│   │   ├── lp-pos-graduacao/
│   │   └── lp-vestibular-relampago/
│   └── platforms/
│       ├── academic-repository-web/
│       └── institutional-web/
├── security/                            # Auditorias de segurança
├── seo/                                 # Auditorias de SEO
├── uptime/                              # Relatórios de disponibilidade
└── README.md
```

---

## Convenção de Nomenclatura

Todos os arquivos de auditoria seguem o padrão:

```
{plataforma}-{dispositivo}-{YYYY-MM-DD}.{ext}
```

**Exemplos:**

```
enem-calculator-desktop-2026-04-24.png
enem-calculator-mobile-2026-04-24.png
institutional-web-desktop-2026-03-15.png
```

> Isso garante rastreabilidade histórica e facilita comparações entre períodos.

---

## Plataformas Auditadas

### Landing Pages

| Plataforma           | Slug                      |
| :------------------- | :------------------------ |
| Calculadora ENEM     | `enem-calculator`         |
| Simulado ENEM        | `enem-simulator`          |
| Cursos Técnicos      | `lp-cursos-tecnicos`      |
| Graduação            | `lp-graduacao`            |
| Pós-Graduação        | `lp-pos-graduacao`        |
| Vestibular Relâmpago | `lp-vestibular-relampago` |

### Plataformas Institucionais

| Plataforma            | Slug                      |
| :-------------------- | :------------------------ |
| Repositório Acadêmico | `academic-repository-web` |
| Site Institucional    | `institutional-web`       |

---

## Como Adicionar uma Nova Auditoria

### PageSpeed (manual)

1. Acesse [PageSpeed Insights](https://pagespeed.web.dev/)
2. Insira a URL da plataforma a auditar
3. Tire um print da tela de resultados (desktop **e** mobile)
4. Salve seguindo a convenção de nomenclatura
5. Coloque na pasta correspondente em `pagespeed/`

```bash
# Exemplo de caminho de destino
pagespeed/landing-pages/enem-calculator/desktop/enem-calculator-desktop-2026-04-24.png
pagespeed/landing-pages/enem-calculator/mobile/enem-calculator-mobile-2026-04-24.png
```

### Nova Plataforma

Para adicionar uma plataforma ainda não catalogada:

```bash
# Crie a estrutura de pastas
mkdir -p pagespeed/landing-pages/nova-plataforma/{desktop,mobile}

# Adicione a entrada na tabela de plataformas deste README
```

---

## Periodicidade Recomendada

| Categoria      | Frequência sugerida | Observação                             |
| :------------- | :------------------ | :------------------------------------- |
| PageSpeed      | Mensal              | A cada deploy relevante ou mês fechado |
| Lighthouse     | Mensal              | Junto com PageSpeed                    |
| SEO            | Trimestral          | Ou após mudanças estruturais           |
| Segurança      | Semestral           | Ou após atualizações de dependências   |
| Uptime         | Contínuo / semanal  | Exportar relatórios periodicamente     |
| Acessibilidade | Semestral           | Ou após mudanças de design             |
| Benchmarks     | Sob demanda         | Ao comparar versões ou tecnologias     |

---

## Leitura dos Resultados de PageSpeed

| Faixa de Score | Classificação | Ação recomendada                  |
| :------------- | :------------ | :-------------------------------- |
| 90 – 100       | 🟢 Bom        | Manter e monitorar                |
| 50 – 89        | 🟡 Melhorar   | Investigar oportunidades de ganho |
| 0 – 49         | 🔴 Crítico    | Priorizar otimização imediata     |

---

<div align="center">
    <sub>
        Divisão de Desenvolvimento • Faculdade CECAPE © 2026
    </sub>
</div>

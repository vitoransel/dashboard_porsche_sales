# Porsche Sales Dashboard

Dashboard estático para explorar vendas de veículos Porsche por região, modelo e forma de pagamento.

## Estrutura

```text

├── assets/
│   └── evidence/
├── data/
│   └── Porsche Sales Sanitization.xlsx
├── docs/
│   └── schema.md
├── index.html
└── README.md
```

- `index.html`: página principal do dashboard.
- `data/`: planilha relacionada ao projeto.
- `docs/`: documentação do schema e das regras de sanitização.
- `assets/evidence/`: capturas de tela do dashboard e de filtros aplicados.

## Questões analisadas

1. **Desempenho regional:** em quais estados e cidades os veículos Porsche tiveram mais vendas? Escolhida para identificar onde estão os principais mercados e oportunidades regionais.
2. **Desempenho dos modelos:** quais modelos foram mais vendidos e geraram maior faturamento? Ajuda a comparar volume de vendas e contribuição para a receita.
3. **Formas de pagamento:** quais modalidades são mais utilizadas e quais geram maior faturamento? Permite entender as preferências dos clientes e relacioná-las ao faturamento.

## Criação da dashboard

A dashboard foi criada com o **ChatGPT com Canvas**.

### Prompt inicial

> Crie um dashboard interativo para analisar as vendas de veículos Porsche utilizando a planilha disponibilizada como fonte de dados. O Dashboard deve apresentar indicadores gerais, análise das vendas por região, desempenho dos modelos e participação das formas de pagamento no faturamento. Pode usar um design inspirado na porsche.

### Alterações até a versão final

- Remover o texto “PAINEL COMERCIAL BASE DE DADOS SANITIZADA”.
- Adicionar no topo um banner com um carro da Porsche.

## Preparação da base para a IA

Utilizei o schema do Felipe como referência para montar minhas próprias regras de sanitização. Primeiro, observei os dados e identifiquei alguns problemas na escrita dos nomes, como letras maiúsculas e minúsculas misturadas. Com base nisso, defini regras para padronizar os nomes sem inventar dados. As regras e verificações estão detalhadas em [`docs/schema.md`](docs/schema.md).

## Publicação

Acesse o link para visualizar o dashboard:
https://vitoransel.github.io/dashboard_porsche_sales/

## Evidências

- [Dashboard geral](assets/evidence/01-dashboard-geral.jpeg)
- [Filtro regional](assets/evidence/02-filtro-regional.jpeg)
- [Filtro por modelo](assets/evidence/03-filtro-modelo.jpeg)

## Uso de inteligência artificial

Durante o desenvolvimento, utilizei ferramentas de IA como apoio na revisão dos textos na organização das ideias. As sugestões e decisões foram revisadas ao longo do processo; a IA serviu como apoio, não como substituta da análise e validação realizadas no projeto.

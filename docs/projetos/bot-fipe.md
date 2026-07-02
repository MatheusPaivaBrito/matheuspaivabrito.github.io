
---

# Passo 10 — Criar `docs/projetos/bot-fipe.md`

```md
# BOT FIPE

## Visão geral

O **BOT FIPE** é uma automação desenvolvida para coletar, organizar e consultar dados relacionados à **Tabela FIPE**.

O projeto demonstra capacidade de trabalhar com coleta de dados, estruturação de informações, automação de processos e preparação de dados para uso posterior em sistemas ou consultas.

---

## Problema

Consultas manuais em bases públicas podem ser repetitivas, lentas e difíceis de organizar.

Quando existe necessidade de consultar muitos veículos, versões, anos ou modelos, o processo manual se torna improdutivo e sujeito a erros.

---

## Solução

Foi criada uma automação capaz de:

- coletar informações da fonte de dados;
- organizar os dados coletados;
- estruturar informações por marca, modelo, ano e versão;
- preparar os dados para consulta ou integração futura.

---

## Arquitetura em alto nível

```text
Fonte de dados FIPE
        ↓
Coletor automatizado
        ↓
Tratamento e normalização
        ↓
Organização dos dados
        ↓
Consulta ou integração
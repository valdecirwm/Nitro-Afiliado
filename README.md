# 🚀 Nitro Afiliado | Automação Tríade para E-commerce

> **Sistema autônomo de mineração, curadoria com IA e postagem para afiliados (Shopee, Mercado Livre e AliExpress).**

[![Tech Stack](https://img.shields.io/badge/Tech_Stack-n8n%20%7C%20PHP%20%7C%20OpenAI-blue)](#)
[![APIs](https://img.shields.io/badge/APIs-Shopee%20%7C%20Meli%20%7C%20AliExpress%20%7C%20Telegram-orange)](#)
[![Status](https://img.shields.io/badge/Status-Produção-success)](#)

## 📌 Sobre o Projeto

O **Nitro Afiliado** é uma solução completa de automação desenvolvida para eliminar o trabalho braçal na gestão de grupos de ofertas no Telegram. Diferente de scrapers convencionais, o sistema atua como um pipeline inteligente de 4 estágios que consome dados diretos das APIs dos maiores marketplaces do mundo, filtra oportunidades, gera copywriting persuasivo usando Inteligência Artificial (GPT-4o) e publica automaticamente.

O projeto demonstra forte **visão de produto e engenharia de software**, unindo múltiplas integrações externas e controle de banco de dados para garantir alta conversão sem intervenção humana.

## ⚙️ Arquitetura e Engenharia (Pipeline de 4 Estágios)

O motor do sistema (Nitro Afiliado) foi arquitetado para rodar em *background*, executando as seguintes rotinas:

1. **Mineração via API:** Conexão direta e autenticada com os servidores (Shopee, Mercado Livre, AliExpress), garantindo tempo de resposta na casa dos milissegundos e evitando bloqueios comuns a web scrapers.
2. **Filtro de Inteligência (Regras de Negócio):** O algoritmo descarta automaticamente produtos sem estoque, com avaliações baixas ou comissionamento ruim.
3. **Copywriter IA (Integração GPT-4o):** Os metadados do produto aprovado são enviados à OpenAI, que retorna uma legenda formatada, com gatilhos mentais de urgência e emojis, pronta para conversão.
4. **Postagem & Controle de Estado (Cache):** Disparo via API do Telegram e registro do ID do produto no Banco de Dados. Isso garante que a aplicação mantenha o estado e nunca repita a mesma oferta no grupo.

## 🧩 Módulos do Sistema (A Tríade)

A arquitetura foi dividida em três *workflows* independentes, cada um com regras de negócio específicas para o seu ecossistema:

- 🟠 **Shopee Hunter:** Focado em volume e viralização. Possui validação de segurança via Hash SHA256 e filtros estritos de alta comissão para itens de giro rápido.
- 🟡 **Meli Sniper:** Focado em ticket alto (eletrônicos/smartphones) e conversão por confiança. Possui monitor de "Ofertas do Dia" e filtro de logística "Entrega Full".
- 🔴 **AliExpress Global:** Focado em inovação e arbitragem de novidades. Inclui conversão automática de moedas (Dólar para Real) e filtro "Choice" para garantir fretes rápidos e impostos já calculados.

## 💻 Stack Tecnológico

- **Orquestração & Automação:** n8n (Workflows complexos e webhooks)
- **Inteligência Artificial:** OpenAI API (Modelo GPT-4o)
- **Integrações (REST APIs):** Telegram Bot API, Mercado Livre API, Shopee Affiliate API, AliExpress API.

## 🎯 Impacto e Visão de Negócios

- **Redução de 100% do trabalho manual** de busca, formatação e postagem de links de afiliados.
- Prevenção de *spam* através de arquitetura de banco de dados que impede duplicidade de ofertas.
- Aumento da taxa de clique (CTR) gerada pelas copys dinâmicas e exclusivas criadas por IA.

## 🚀 Como Executar Localmente

```bash
# Deve possuir o N8N instalado localmente ou em produção
# Configure as chaves de API nas credenciais do N8N
# Adicione suas chaves: OPENAI_API_KEY, TELEGRAM_BOT_TOKEN, MELI_APP_ID, etc.

# Inicie o servidor N8N instalado em seu computador
localhost:8000

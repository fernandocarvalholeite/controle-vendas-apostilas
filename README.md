# Controle de Vendas — Apostilas Ricardo Camara

Site de controle de vendas, estoque e acerto financeiro com o Ricardo Camara, hospedado gratuitamente no **GitHub Pages**, com dados guardados em um banco **Supabase** (gratuito).

## O que o sistema faz

- Cadastro de produto (apostila): descrição, valor de custo, valor de venda
- Registro de vendas: cliente, forma de pagamento (Link Cartão, Cartão de Crédito, PIX, Boleto), status de recebimento
- Controle de estoque (entradas e saídas), com baixa automática nas vendas
- Acerto com o Ricardo Camara: mostra o valor de custo pendente de repasse e permite registrar os pagamentos feitos a ele, com histórico
- Login por senha para dois usuários (você e o Ricardo Camara), dados sincronizados entre os dois em tempo real

## Estrutura de arquivos

```
index.html          → a tela do sistema (HTML + CSS + JS)
config.js            → chaves de conexão com o Supabase (preencher antes de usar)
supabase/schema.sql  → script para criar as tabelas e regras no Supabase
```

## Como colocar no ar

Veja o arquivo `INSTRUCOES_GITHUB_SUPABASE.md` para o passo a passo completo — criação do projeto Supabase, publicação no GitHub Pages e configuração dos logins.

## Segurança

O `config.js` usa a chave pública ("anon key") do Supabase, que é segura de ficar visível no código — quem protege os dados é a *Row Level Security* configurada no banco (só usuários logados conseguem ler/gravar). Nunca coloque a "service role key" do Supabase neste repositório.

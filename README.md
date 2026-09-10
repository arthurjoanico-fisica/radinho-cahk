# Rádio CAHK v2

Arquivos para substituir o frontend atual do Radinho.

## Endereços
- `/` — pedidos de música
- `/player.html` — computador da sala
- `/admin.html` — locuções e programação

## Backend já instalado
O Supabase atual do Radinho já recebeu as tabelas e funções da Rádio CAHK v2. A fila existente foi preservada.

## Falta uma configuração para o modo automático
Crie uma chave da YouTube Data API v3 e adicione ao Supabase como secret com o nome:

`YOUTUBE_API_KEY`

Depois abra `/admin.html` e clique em `Atualizar Top Música do YouTube`.

A função consulta `videos.list` com `chart=mostPopular`, região BR e categoria Música (10), e exclui vídeos não incorporáveis, lives, vídeos com menos de 2 minutos e mais de 15 minutos.

## Locuções
Você controla o texto, tipo, prioridade, ativação e uma URL opcional de MP3. Sem MP3, a voz pt-BR disponível no navegador é usada.

## Prioridade
1. Pedidos dos usuários
2. Faixas manuais
3. Locução, se estiver na hora e não houver pedido
4. Música automática

O código administrativo é o mesmo do player atual e fica salvo localmente no computador quando digitado.

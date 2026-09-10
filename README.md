# Rádio CAHK v3 — busca + áudios da galera

Frontend estático para Cloudflare Workers/Static Assets.

## Novidades desta versão

- pesquisa de músicas e vídeos no YouTube dentro do site;
- pedidos por link continuam disponíveis;
- gravação de recados pelo microfone do celular/computador;
- limite de 20 segundos no gravador;
- envio para moderação antes de qualquer reprodução;
- painel administrativo com Pendentes / Aprovados / Rejeitados;
- áudios aprovados entram automaticamente na programação;
- o administrador pode pausar, reativar ou excluir um recado;
- bucket privado no Supabase e URLs temporárias para reprodução.

## Arquivos do site

- `public/index.html`: pedidos + gravador de recados;
- `public/player.html`: player central, agora também toca áudio da comunidade;
- `public/admin.html`: programação, locuções e moderação dos recados;
- `public/styles.css`: visual;
- `public/config.js`: configuração do Supabase.

## Backend

O projeto Supabase da Rádio CAHK precisa conter as Edge Functions `radio-audio-submit`, `radio-admin` e `radio-next`, além do bucket privado `radio-community-audio`. No ambiente em que este pacote foi gerado, o backend correspondente já foi configurado.

## Publicação

Substitua os arquivos da pasta `public` do repositório pelo conteúdo desta versão e faça commit. Se o repositório estiver conectado ao Cloudflare Workers, o deploy será iniciado automaticamente.

## v4 — áudio com hora marcada

- upload de áudio pelo painel administrativo;
- agendamento com data e hora local;
- player consulta os agendamentos continuamente;
- cerca de 2 segundos antes, o áudio é preparado;
- no horário marcado, a música/recado atual é pausado;
- ao terminar o áudio agendado, a programação anterior é retomada;
- agendamentos podem ser cancelados ou reagendados no painel.

Para horário exato, mantenha o `player.html` aberto, o computador acordado e o navegador sem suspensão de aba.

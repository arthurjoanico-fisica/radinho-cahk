# Radinho do CAHK

Jukebox colaborativa do CAHK.

- `/` página pública para adicionar links do YouTube.
- `/player.html` computador responsável pela reprodução.
- Supabase Realtime sincroniza a fila.
- Edge Functions `queue-add` e `queue-admin` já estão configuradas no projeto Supabase.

A chave pública do Supabase pode ficar no frontend. Nenhuma service-role key está incluída no repositório.

A busca interna pelo nome da música depende de uma chave da YouTube Data API v3 e ainda precisa ser ativada.

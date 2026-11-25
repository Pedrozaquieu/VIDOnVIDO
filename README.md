# VIDOnVIDO / VnV
Catálogo pessoal de filmes, séries e animes, sem login. Interface em português com tema escuro, dourado e violeta. Aplicação estática compatível com GitHub Pages.

## Começar
Abra o site, vá a **Configurações & backup** e cole seu **Token de Leitura da API do TMDB**. Teste e salve. Nenhuma credencial está incluída neste repositório. O token é guardado apenas no navegador e usado em chamadas HTTPS para api.themoviedb.org.

O catálogo começa vazio. Em **Adicionar em massa**, cole um título por linha, preferencialmente com ano: `Interestelar (2014)`. Aceita TXT e CSV (colunas titulo e ano). Correspondências exatas e únicas entram automaticamente; ambiguidades exigem revisão. Duplicatas preservam seu status. Pode pausar e retomar enquanto a aba permanece aberta.

## Funcionalidades
- Catálogo local, filtros combinados, busca, ordenação, seleção múltipla e status.
- Busca/descoberta no TMDB, paginação e recomendações baseadas em até cinco títulos salvos, priorizando suas avaliações.
- Modal com sinopse, imagens, nota TMDB, avaliação pessoal e título romanizado editável.
- Menu por clique direito ou botão ⋯; card PNG compartilhável quando o navegador permitir.
- Playlists; exportação TXT, CSV e página HTML com capas; backups JSON completos.
- Backup não contém token. Exportações de playlists não contêm status ou notas pessoais.

## Publicar no GitHub Pages
Em **Settings → Pages → Build and deployment → Source**, selecione **GitHub Actions**. O workflow publica a branch main. Se necessário, execute **Actions → Publicar VIDOnVIDO → Run workflow**.
URL prevista: https://Pedrozaquieu.github.io/VIDOnVIDO/

## Desenvolvimento
Use Node 22+: `npm test` e `npm run check`. Sirva a pasta por HTTP (por exemplo `python3 -m http.server 8080`). Não abra index.html via file://, pois o app usa módulos JavaScript.

## Limites e privacidade
Dados locais por navegador/origem, sem sincronização entre aparelhos. Exporte backup antes de limpar dados ou mudar de endereço. Credencial inserida no próprio navegador não é segredo para quem tem acesso a esse navegador. Não publique tokens em commits.
Animes são estimados por idioma japonês + gênero animação. Romanização depende de títulos alternativos TMDB explicitamente identificados como romanizados; pode ser corrigida manualmente. Busca nominal do TMDB é paginada; filtros e ordenação local se aplicam aos resultados carregados. A descoberta sem busca usa também filtros remotos. Recomendações não usam IA externa. Links públicos de playlists com expiração não estão implementados; use exportação HTML/TXT/CSV. TMDB não fornece os vídeos para assistir.

## Créditos
Dados e imagens: [TMDB](https://www.themoviedb.org/). This product uses the TMDB API but is not endorsed or certified by TMDB.

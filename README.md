# Regis K Lab

Portfólio audiovisual de Régis Kraeski.

## Organização

- Abas Vídeo, Fotografia e Design no mesmo espaço abaixo do hero.
- Vídeo: IA (RedBolt, Showreels e Subject K) e Social Media (Jameson), definidos em `projects.js`. As capas IA abrem overlays arredondadas no index, com vídeos destacados e referências menores. `project.html` mantém o acesso direto alternativo aos projetos IA.
- Fotografia: 32 imagens integrais em masonry contínua, com seleção de efeitos/cores fortes no início.
- Design: Social Media (25 peças) e Arte gráfica (23 peças), ambos expansíveis, com ordem fixa preservada.
- Grupos de trabalhos usam acabamento escuro, borda quente fina e cantos arredondados.

Para adicionar mídia a um projeto em `projects.js`, use `type` (`image` ou `video`), `title`, `src` e, opcionalmente, `poster`. Preserve os caminhos em `assets/`. Os vídeos fora da seleção continuam nos assets, sem aparecer na coleção. Não há imagens genéricas substituindo referências ausentes.

**Compatibilidade existente:** `red-bolt-commercial.mp4` usa HEVC (`hvc1`, 1920×1080). O navegador de teste carrega áudio/poster mas não decodifica a imagem do vídeo. Uma versão H.264 ampliaria a compatibilidade; o original foi preservado, sem conversão nem substituição.

## Prévia local

Site estático sem build. Sirva a pasta por HTTP. Nesta máquina, o helper externo ao repositório `../regisklab-preview.cjs` inicia com `node ../regisklab-preview.cjs` em `http://127.0.0.1:8765/`.

## Verificação local (2026-11-27)

- Sintaxe JavaScript, integridade do manifesto de galerias e caminhos de mídia.
- Chromium desktop 1440×1000 e mobile 390×844: sem overflow horizontal ou erros JavaScript observados.
- Social Media/Arte gráfica abrem e fecham com Enter/Espaço; imagens carregam ao expandir.
- Cards IA continuam abrindo overlays; Escape fecha. Fotografias, hero, Sobre, Clientes e Contato preservados.
- Limitação HEVC de RedBolt mantida conforme descrito acima.

Publicado com GitHub Pages:
https://regisvs.github.io/regisklab/

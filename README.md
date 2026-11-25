# ChessMate

PWA de treino e estudo de xadrez com tabuleiro manual para os dois lados.

## Recursos
- Tabuleiro responsivo com movimentação por toque/clique e validação de lances legais.
- Histórico em notação algébrica, desfazer, virar tabuleiro e reiniciar.
- Realce do último lance e casas legais; seta sobre o movimento recém-realizado.
- Dicas didáticas básicas sobre xeque, capturas, centro e desenvolvimento.
- Modos Humano, Checkmate (treino de padrões) e Estudo.
- Importação e cópia de posição FEN.
- Preferência de nível de explicação e tema claro/escuro.
- Manifesto e service worker para instalação como PWA.

## Executar
Sirva esta pasta por HTTP/HTTPS (não abra `index.html` diretamente):

```bash
python -m http.server 8000
```

Abra `http://localhost:8000`.

## Publicar
Envie o conteúdo da pasta para Netlify, Vercel ou GitHub Pages. Para instalar como PWA, o site precisa estar em HTTPS (localhost serve para testes).

## Dependência
A regra e validação de movimentos usam `chess.js` 1.4.0 via jsDelivr ES module. É necessário acesso à internet na primeira carga para obter a biblioteca. O shell do app é armazenado pelo service worker.

## Limites atuais
A análise é didática e heurística: não calcula a melhor jogada, não estima profundidade de engine e não substitui análise completa. O modo Checkmate é um espaço de treino livre com FEN, não uma coleção de puzzles pronta. A seleção de nível é uma preferência de linguagem/explicação, ainda não um rating calculado.

Use o app para estudo e análise pós-partida ou em partidas em que assistência externa seja permitida. Não foi projetado para ocultar assistência ou contornar sistemas anti-cheat.

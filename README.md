# ChessMate Pro

PWA responsivo de xadrez para treino, análise e revisão de partidas.

## Recursos
- Tabuleiro manual para os dois lados, por toque/clique ou arrastar e soltar.
- Validação de lances legais, roque, en passant e promoção de peão (com escolha de peça).
- Histórico em notação algébrica, desfazer, virar tabuleiro e reiniciar.
- Sugestões automáticas com até três candidatas, setas e explicações em português.
- Busca local minimax/negamax com poda alpha-beta em profundidades configuráveis (rápida, equilibrada e profunda). É uma engine didática própria e não Stockfish; pode deixar passar táticas complexas.
- Modos Análise, Checkmate (procura mate imediato na profundidade escolhida) e Estudo.
- Avaliação material/posicional, indicação de xeque, FEN e PGN.
- Importação/exportação de FEN e PGN.
- Salvar/restaurar partida no armazenamento local do dispositivo.
- Tema claro/escuro e PWA com cache offline do shell.

## Executar localmente
A aplicação precisa ser servida por HTTP/HTTPS (não abrir o HTML diretamente):

```bash
python -m http.server 8000
```

Abra `http://localhost:8000`.

## Publicar
Envie os arquivos desta pasta para a raiz do repositório do GitHub Pages, Netlify ou Vercel. Para instalação PWA, publique em HTTPS.

## Dependência
A validação de regras usa `chess.js` 1.4.0 via jsDelivr ES module. A primeira abertura requer internet para carregar a biblioteca. O tabuleiro, interface e busca local funcionam no navegador; o service worker mantém os arquivos próprios em cache.

## Limitações transparentes
A busca alpha-beta é uma engine leve e didática, não substitui Stockfish e não promete jogada perfeita. A profundidade 3 pode consumir mais tempo em celulares modestos. O modo Checkmate destaca mate imediato encontrado na busca, mas não é um banco de puzzles nem um solver de mates longos. O nível adaptativo é uma preferência de explicação e ainda não representa rating Elo calculado.

Use a assistência para estudar, revisar partidas e jogar em ambientes onde ajuda externa seja permitida.

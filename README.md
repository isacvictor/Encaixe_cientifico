# Encaixe Científico

Releitura de *Tetris* sobre mulheres na ciência. As peças caem, você encaixa e limpa linhas. A cada 5 peças
o jogo para **entre uma peça e outra** e faz uma pergunta:

- **Acertou:** ganha pontos e **escolhe a próxima peça** entre 3 opções.
- **Errou (ou o tempo acabou):** perde até 50 pontos, vê a resposta certa com uma linha de explicação e o jogo escolhe a peça.
- **Errar nunca encerra a partida.** Se a pilha encher, a metade de cima é limpa (-100 pontos) e o jogo continua.

Partida de **170 segundos** (limite do curso: 3 minutos), sem tutorial: a tela de título já mostra os controles.

- **Controles:** setas movem (←→) e aceleram a queda (↓), ↑ (ou X) gira, espaço (ou Z) derruba a peça, Enter confirma.
  Só as teclas canônicas (RJ-15), no máximo duas ao mesmo tempo, sem usar o auto-repeat do sistema (RJ-16).
- **Placar:** ao fim, envia a mensagem `PLACAR` ao fliperama (`window.parent.postMessage`), no formato do contrato
  (`tipo, jogo, versao, pontos, duracao_s, acertos, erros, tema`). O jogo não guarda nada (RJ-18): o apelido que chega em
  `ARCADE_INIT` só aparece na tela.
- **Banco de questões:** `questoes.json` (24 questões, até 8 sorteadas por partida, sem repetir). Cada questão tem `fonte`.
- **Pacote:** um único `index.html` na raiz, sem rede, sem áudio, sem bibliotecas externas.

# Robô pega a estrela

Jogo de navegador para apresentar o curso de Engenharia de Software da UNIPAMPA a crianças. A criança monta uma sequência de setas, aperta play e o robô anda pela grade até a estrela. Se o robô bater numa pedra, o passo errado fica vermelho e a criança conserta só esse passo.

**[Jogar agora](https://paulosevero.github.io/robo-estrela/)**

![Uma partida em que o robô bate na pedra, a criança troca o passo errado e o robô chega à estrela](docs/partida.gif)

## O que o jogo ensina

O jogo mostra três partes do trabalho de quem faz software:

- Programar é montar a sequência de passos.
- Testar é apertar play e ver o que o robô faz.
- Depurar é achar o passo que causou o erro e trocá-lo.

Ao lado da grade, cada seta aparece também como uma linha de código, como `robô.direita()`, para mostrar que a fila de setas já é um programa. O jogo usa só ícones, cores e sons, então funciona com crianças que ainda não leem.

## Como jogar

| Tecla                     | Ação                                                 |
| ------------------------- | ---------------------------------------------------- |
| ← ↑ ↓ →                   | Acrescenta um passo                                  |
| Backspace                 | Apaga o passo vermelho ou, se não houver, o último   |
| Enter ou Espaço           | Executa a fila e avança para o próximo nível         |
| 1 a 5, Page Up, Page Down | Troca de nível                                       |
| R                         | Limpa a fila                                         |
| M                         | Liga e desliga o som                                 |
| Q                         | Mostra em tela cheia o QR code para jogar no celular |

No celular e no tablet, os mesmos comandos estão nos botões da tela, e tocar num passo da fila apaga esse passo. Ao vencer um nível, a criança ganha 3 estrelas se usou o caminho mais curto, 2 estrelas com até dois passos a mais e 1 estrela nos outros casos.

## Roteiro da apresentação

1. Aquecimento sem tela. Uma criança faz o papel do robô no chão, e as outras dão comandos com cartões de seta até ela pegar uma estrela de papel.
2. Jogo no projetor. As crianças se revezam nos cinco níveis usando o teclado do notebook.
3. Fechamento. O apresentador conta que o erro do robô se chama bug e que consertar bugs faz parte do trabalho de quem estuda Engenharia de Software. A tela final mostra os destaques do curso e dois QR codes, um para jogar no celular e outro para o site do curso.

## Como rodar e editar

O jogo é um único arquivo, `index.html`, feito com HTML, CSS e JavaScript puros, sem bibliotecas. Ele funciona sem internet, então basta abrir o arquivo no navegador com duplo clique. Os sons são gerados pelo próprio navegador, com a Web Audio API.

Os níveis ficam na lista `LEVELS`, no início do script. Cada nível é uma lista de linhas de texto em que `R` é o robô, `*` é a estrela, `#` é uma pedra e `.` é uma casa livre. Ao mudar um nível, atualize também o número de passos do caminho mais curto na lista `FEWEST_STEPS`, que decide as estrelas.

## Licença

Código sob a licença MIT. Veja o arquivo [LICENSE](LICENSE).

## Créditos

Feito para divulgar o curso de [Engenharia de Software da UNIPAMPA](https://cursos.unipampa.edu.br/cursos/engenhariadesoftware/), no Campus Alegrete.

# ottoke011
!git clone https://github.com/kkuramitsu/reversi2021.git
from reversi2021.reversi import *
STONE = ['🟩', '⚫', '⚪']
board = init_board()
show_board(board)
game(my_AI, my_AI)
import random

def random_AI(board, color):
  for _ in range(100):
    for i in [0,5,30,35]:
    ##端に置けたら置く
      position = i
      if put_and_reverse(board, position, color):
        return 
    
      position = random.randint(0, N*N-1)
      if put_and_reverse(board, position, color):
        return position ## おく位置を決めて返す
  return 0
  game(my_AI, random_AI)

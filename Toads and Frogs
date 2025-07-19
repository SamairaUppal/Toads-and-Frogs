### Project: Toads and Frogs Game ###

# global variables and arrays
n=0                         # board size
board=[]                    # current board
dashPos=0                   # the position of the empty spot on the current board
finish=0                    # status of the game - {-1:in progress,0:game finished}
curMove=0                   # the move chosen by the player in the current turn
numOfMoves=0                # keep the number of moves

def setupGame():
    # *** TO BE FILLED
    global n, board, dashPos,finish,curMove,numOfMoves
    n = int(input())
    for i in range(n//2):
        board.append('T')
    board.append('-')
    for i in range(n//2):
        board.append('F')
    numOfMoves = 0
    finish = -1
    dashPos = n//2
    
def drawScreen():
    # *** TO BE FILLED
    global board , numOfMoves
    for i in board:
        print(i,end = '')
    print('\nNumber of moves:',numOfMoves)
    print()

def getMove():
    # *** TO BE FILLED
    global curMove
    print(f'Enter move (1..{n}): ')
    curMove = int(input())

def makeMove():
    # *** TO BE FILLED
    global curMove, numOfMoves, dashPos, board
    board[curMove-1], board[dashPos] = board[dashPos], board[curMove-1]
    dashPos = curMove - 1 
    numOfMoves += 1


def checkEndGame():
    # *** TO BE FILLED

    # The correct middle index
    mid = n // 2  
    if board[:mid] == ['F'] * mid and board[mid] == '-' and board[mid+1:] ==['T'] * mid:
        return 0  # Game finished
    return -1  # Game still in progress

setupGame()                     # step 1

# main game loop
while True:
    drawScreen()                # step 2
    getMove()                   # step 3
    makeMove()                  # step 4
    finish = checkEndGame()     # step 5
    if finish>-1:
        break

# step 6: end game information
# *** TO BE FILLED
drawScreen()
print('You finished!')

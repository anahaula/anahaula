# Welcome to GitHub Desktop!
 def determinar_posicao(x, y, largura, altura, centroX, centroY):
    l = largura/4 #fração largura (pode ser modificada)
    h = altura/4 # fração altura (pode ser modificada)
    
    # posição em relação ao eixo X
    if (x < (centroX - l)): # pois estaria negativo
        posicaox = "e na esquerda" #quadrante 2 ou 3
    elif(x > (centroX + l)): # pois estaria positivo
        posicaox = "e na direita" #quadrante 1 ou 4
    else: #está no meio 
        posicaox = "e centralizado"

    # posição em relação ao eixo Y
    if (y < (centroY - h)): # estaria no espaço negativo
        posicaoy = "está em baixo" # quadrante 3 ou 4
    elif (y > (centroY + h)): #estaria no espaço positivo
        posicaoy = "está em cima" # quadrante 1 ou 2
    else: #está no meio
        posicaoy = "está centralizado"

    # Combina as posições em ambas as direções
    if posicaoX == "centralizado" and posicaoY == "centralizado":
        posicao = "centralizado" # está no centro
    else:
        posicao = f"{posicaoY} {posicaoX}" 

    return posicao



def main():
    x = float(input('digite o x:'))
    y = float(input('digite o y:'))
    largura = 40
    altura = 20
    # Calcula as coordenadas do centro do retângulo
    centroX = largura / 2
    centroY = altura / 2
    print(determinar_posicao(x,y,largura,altura, centroX, centroY))
main()



# expert-pancake
def graph(edges,vertex):
      S = int(input("Enter source vertex: "))
      path = []
      path.append(S)
      print(path)
      v = len(vertex)
      print(v)
      weight = 0
      max = 0
      matrix = [[0 for x in range(v)] for y in range(v)]
      for i in range(v):
            for j in range(v):
                  if (i,j)in edges:
                        matrix[i][j]=1
                        matrix[j][i]=1
                  elif matrix[0][j]>= max or matrix[0][i]>= max and matrix not in path:
                        max = matrix[i][j] and matrix[j][i]
                        weight = (i,j)
            path.append(weight)
            print(path)
            
      return matrix     
     
vertex = [0,1,2,3,4]
edges = [(0,1),(0,2),(2,3),(2,4)]
matrix = graph(edges,vertex)
print(matrix)

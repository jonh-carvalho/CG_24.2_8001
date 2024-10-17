# **Estudo Dirigido 04**

---
## **Atividade:** 

Para plotar os exercícios de transformações geométricas, a biblioteca **Matplotlib** é ideal, pois é uma das mais populares para visualização de dados e gráficos em Python. A **Matplotlib** é adequada para criar gráficos de 2D, como pontos, linhas e formas geométricas. Aqui estão os passos gerais e uma explicação de como usar essa biblioteca para plotar as transformações geométricas:

### **Exercício 1: Translação Simples**
Dado o ponto \( P(2, 3) \), aplique a translação com vetor \( (4, -2) \).

- **Perguntas**: Qual é o novo ponto \( P' \)? Quais coordenadas foram alteradas?

### **Exercício 2: Escala Uniforme**
Considere um triângulo com vértices \( A(1, 1), B(3, 1) \) e \( C(2, 4) \). Aplique uma escala uniforme de fator 2.

- **Perguntas**: Quais são as novas coordenadas dos vértices após a transformação? O que acontece com o tamanho do triângulo?

### **Exercício 3: Escala Não Uniforme**
Aplique uma escala não uniforme no triângulo do Exercício 2, com fator de 2 no eixo \(x\) e fator de 0,5 no eixo \(y\).

- **Pergunta**: Quais são as novas coordenadas dos vértices?

### **Exercício 4: Rotação em Torno da Origem**
Rotacione o ponto \( P(1, 0) \) em 90° no sentido anti-horário em torno da origem.

- **Pergunta**: Qual é a nova posição do ponto \( P' \) após a rotação?

### **Exercício 5: Rotação de um Polígono**
Um quadrado tem vértices \( A(1, 1), B(1, 4), C(4, 4), D(4, 1) \). Aplique uma rotação de 45° no sentido horário.

- **Pergunta**: Quais são as novas coordenadas dos vértices?

### **Exercício 6: Reflexão Simples**
Dado o ponto \( P(2, 5) \), aplique uma reflexão em relação ao eixo \(y\).

- **Pergunta**: Qual é a nova posição do ponto \( P' \)?

### **Exercício 7: Reflexão de um Triângulo**
Considere um triângulo com vértices \( A(2, 3), B(4, 3) \) e \( C(3, 5) \). Aplique uma reflexão em relação ao eixo \(x\).

- **Pergunta**: Quais são as novas coordenadas dos vértices após a transformação?

### **Exercício 8: Cisalhamento Horizontal**
Dado o ponto \( P(2, 3) \), aplique um cisalhamento horizontal com \( k = 2 \).

- **Pergunta**: Qual é a nova posição do ponto \( P' \)?

### **Exercício 9: Composição de Transformações**
Dado o ponto \( P(3, 2) \), aplique as seguintes transformações consecutivas:
1. Uma translação com vetor \( (1, -1) \).
2. Uma rotação de 90° no sentido anti-horário.
3. Uma escala uniforme com fator 2.

- **Pergunta**: Qual é a nova posição do ponto \( P' \) após todas as transformações?

### **Exercício 10: Combinação de Transformações em uma Figura**
Dado um retângulo com vértices \( A(1, 1), B(5, 1), C(5, 3), D(1, 3) \), aplique as seguintes transformações em sequência:
1. Translação com vetor \( (-2, 3) \).
2. Escala não uniforme com fatores \( 1.5 \) no eixo \(x\) e \(0.5\) no eixo \(y\).
3. Reflexão em relação ao eixo \(y\).

- **Pergunta**: Quais são as novas coordenadas dos vértices após as três transformações?

---

### Instalação
Se você ainda não tiver o **Matplotlib** instalado, pode instalar com o seguinte comando:
```bash
pip install matplotlib
```

### Estrutura Geral para Plotar Transformações

Para cada exercício, o processo de plotagem envolve:
1. Definir os pontos de uma forma geométrica (triângulo, quadrado, etc.).
2. Aplicar a transformação (translação, rotação, escala, etc.).
3. Plotar o objeto antes e depois da transformação.

### Exemplo de Código Base com Matplotlib

Aqui está uma estrutura de código que pode ser adaptada para cada um dos exercícios:

```python
import numpy as np
import matplotlib.pyplot as plt

def plot_shapes(original_shape, transformed_shape, title):
    plt.figure()
    plt.plot(*zip(*original_shape, original_shape[0]), label="Original")
    plt.plot(*zip(*transformed_shape, transformed_shape[0]), label="Transformado", linestyle="--")
    plt.title(title)
    plt.legend()
    plt.grid(True)
    plt.show()

# Exemplo de quadrado
square = np.array([[1, 1], [1, 4], [4, 4], [4, 1]])

# Exemplo de transformação: translação
transformed_square = square + [2, -1]

# Plotar o quadrado original e transformado
plot_shapes(square, transformed_square, "Translação de um Quadrado")
```

### Aplicação para Cada Exercício:

1\. **Exercício de Translação**:
   - Use a função de translação e aplique aos pontos do objeto.
   - Plotar o objeto original e o transformado.

2\. **Exercício de Escala (Uniforme e Não Uniforme)**:
   - Escale as coordenadas dos vértices de acordo com o fator de escala.
   - Plotar o objeto antes e depois da transformação.

3\. **Exercício de Rotação**:
   - Aplique uma rotação de acordo com a matriz de rotação.
   - Plotar a figura rotacionada em relação à original.

4\. **Exercício de Reflexão**:
   - Aplique a matriz de reflexão em relação ao eixo \(x\) ou \(y\).
   - Plotar o objeto antes e depois da reflexão.

5\. **Exercício de Cisalhamento**:
   - Aplique a matriz de cisalhamento aos vértices.
   - Plotar o objeto antes e depois da transformação.

6\. **Composição de Transformações**:
   - Aplique uma sequência de transformações (translação, rotação e escala) e observe como a figura muda.
   - Plotar cada passo da transformação para visualizar cada alteração.

### Ajustes Específicos para Cada Exercício:

- **Exercícios de Polígonos (quadrado, triângulo)**: Definir as coordenadas iniciais dos vértices do polígono.
- **Exercícios de Ponto Simples**: Usar a função `plt.scatter()` para plotar um ponto antes e depois da transformação.

### Exemplo Completo (Escala e Translação):

```python
import numpy as np
import matplotlib.pyplot as plt

# Função para translação
def translate(points, translation):
    return points + translation

# Função para escala
def scale(points, factor):
    return points * factor

# Exemplo: Triângulo
triangle = np.array([[1, 1], [3, 1], [2, 4]])

# Aplicar translação e escala
translated_triangle = translate(triangle, [2, 1])
scaled_triangle = scale(triangle, 1.5)

# Plotar o triângulo original, transladado e escalado
plt.figure()
plt.plot(*zip(*triangle, triangle[0]), label="Original")
plt.plot(*zip(*translated_triangle, translated_triangle[0]), label="Transladado", linestyle="--")
plt.plot(*zip(*scaled_triangle, scaled_triangle[0]), label="Escalado", linestyle="-.")
plt.title("Transformações em um Triângulo")
plt.legend()
plt.grid(True)
plt.show()
```


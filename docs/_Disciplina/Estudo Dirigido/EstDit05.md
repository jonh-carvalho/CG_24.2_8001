# **Estudo Dirigido 05**

---

## **Atividade: Iluminação e Animação**

---

### **Cena Noturna de Estudo**

#### **Objetivo**

Criar um cenário noturno em que um abajur ilumina uma mesa de estudo. O objetivo é aplicar o modelo de iluminação para destacar luzes difusas, luzes especulares, sombras e reflexões, simulando uma cena realista em um ambiente de baixa luz.

#### **Instruções**

1. **Configuração da Cena e Modelagem Básica**:

   - **Plano de Mesa**: Adicione um plano de 10x5 unidades para representar a superfície da mesa.
   - **Livro**: Adicione um cubo fino (altura baixa) para simular um livro. Posicione-o próximo ao centro da mesa e incline-o levemente.
   - **Copo**: Adicione um cilindro alto e fino ao lado do livro, simulando um copo ou caneca.
   - **Lápis**: Crie um cilindro fino e comprido para simular um lápis, posicionado diagonalmente sobre o livro.
2. **Criando o Abajur**:

   - **Base**: Adicione um cilindro pequeno e baixo no final da mesa para representar a base do abajur.
   - **Cúpula**: Adicione uma esfera cortada pela metade (ou um cilindro com topo arredondado) acima da base para simular a cúpula do abajur.
   - **Lâmpada**: Coloque uma **luz do tipo Point** dentro da cúpula do abajur. Ajuste a intensidade da luz para que ilumine suavemente os objetos ao redor, simulando o efeito de uma lâmpada noturna.
3. **Componentes de Iluminação**:

   - **Luz Difusa**: Ajuste a **luz do tipo Point** dentro do abajur com um valor de intensidade difusa médio, para iluminar suavemente a área em volta.
   - **Reflexão Especular**: Aumente o valor especular na superfície da mesa e no copo para que eles reflitam levemente a luz do abajur.
   - **Luz Ambiente**: Configure uma luz ambiente muito baixa, com um tom azulado escuro, para simular a iluminação do ambiente noturno.
   - **Sombras**: Ative as sombras na luz do abajur para criar um contraste realista, com sombras mais intensas dos objetos que estão na mesa.
4. **Materiais e Reflexões**:

   - **Mesa**: Use um material levemente refletivo para o plano da mesa (como madeira escura) com reflexões difusas altas e uma leve reflexão especular.
   - **Livro**: Aplique um material fosco com uma cor neutra e um tom levemente desgastado (amarelo ou bege claro).
   - **Copo**: Dê ao copo uma reflexão especular mais forte, com uma leve transparência (como vidro fosco).
   - **Lápis**: Use uma cor sólida como vermelho ou azul, com baixa reflexão especular.
5. **Configurações de Renderização**:

   - Posicione a câmera de um ângulo levemente acima da mesa, focando no livro e no abajur.
   - Ative o sombreamento suave nos objetos para evitar bordas marcadas.
   - Aumente a qualidade de amostragem para capturar detalhes de luzes e reflexões.

#### **Objetivo Final**

- **Análise dos Resultados**:
  - Observe como a **luz difusa** do abajur ilumina os objetos ao redor, criando uma atmosfera de leitura noturna.
  - A **luz especular** no copo e na mesa realça o realismo ao refletir a iluminação da lâmpada.
  - A **luz ambiente** em tom azulado ajuda a dar profundidade ao cenário e cria o efeito de uma noite tranquila.

#### **Desafio Avançado**

Experimente aplicar uma textura que confira um efeito de metal a superficie da mesa.

## Animação

1\. Animação da Lâmpada Piscando

Descrição: Simule a lâmpada do abajur piscando levemente, como se fosse uma lâmpada antiga, o que adiciona um pouco de suspense e dá mais realismo à cena.

- Como Fazer: Use keyframes na intensidade da luz Point do abajur para variar entre valores próximos da intensidade original (por exemplo, de 100% a 80%) por alguns segundos.

2\. Animação da Câmera

Descrição: Um movimento de câmera suave, com um zoom gradual ou uma leve rotação em torno dos objetos, pode criar uma visão mais imersiva.

- Como Fazer: Use keyframes para mover a câmera lentamente, fazendo um zoom-in ou uma leve rotação em torno da mesa.

3\. Proponha uma animação de qualquer tipo a algum dos objetos na cena.

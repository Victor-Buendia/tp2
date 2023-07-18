# Portabilidade

## Descrição

Segundo Goodliffe (2006, p. 252), a portabilidade no design de software refere-se à capacidade de um programa **se adaptar** e funcionar em diferentes plataformas e/ou sistemas, sem exigir grandes alterações. No entanto, nem todos os programas precisam ser portáteis. Isto é, depende dos requisitos específicos do código. É essencial encontrar um equilíbrio entre alcançar a portabilidade apropriada e evitar comprometer desnecessariamente o design do código.

Frequentemente, os desenvolvedores se deparam com situações em que seu código, originalmente projetado para um ambiente específico, precisa ser adaptado para funcionar em uma plataforma diferente devido a circunstâncias imprevistas. Se o código não foi inicialmente projetado com a portabilidade em mente, esse processo pode se tornar complicado e confuso, resultando em um design confuso cheio de declarações condicionais específicas para cada plataforma.

Para evitar tais situações, é fundamental tomar boas decisões sobre a estrutura das seções de código que dependem de sistemas operacionais ou hardware específicos. Ao criar uma camada de abstração de plataforma no início do design, os desenvolvedores podem encapsular funcionalidades específicas da plataforma, facilitando a implementação de diferentes versões dessa camada, para cada plataforma.

Além disso, consoante Goodliffe (2007, p. 252), durante a fase de design, é fundamental gerenciar a portabilidade, porque adaptar a portabilidade em código existente pode ser bastante custoso e demorado. Ao considerar a portabilidade desde o início, os desenvolvedores podem projetar um código mais limpo e de fácil manutenção, que pode ser facilmente adaptado a diferentes ambientes no futuro.

## Relação com maus cheiros de código

Tendo em vista os maus cheiros de código definidos por Martin Flower (1999), é possível definir os principais problemas provenientes da ausência de portabilidade em um software:

1. Código duplicado: Código repetido pode dificultar a adaptação a diferentes plataformas, uma vez que cada duplicação pode conter implementações específicas de cada plataforma, tornando a manutenção e evolução mais complexas.

2. Método longo: Métodos longos podem conter lógica específica para uma plataforma em particular, tornando-os difíceis de serem adaptados para outras plataformas e prejudicando a portabilidade.

3. Classe inchada: Classes muito extensas e com muitas responsabilidades podem conter funcionalidades específicas de uma plataforma, dificultando a migração para outras plataformas.

4. Lista de parâmetros longa demais: Muitos parâmetros podem indicar dependências específicas de uma plataforma, dificultando a reutilização ou adaptação do código para diferentes ambientes.

5. Mudanças divergentes: Mudanças que afetam diferentes plataformas de forma distinta podem indicar falta de abstração e dificultar a manutenção e portabilidade do código.

6. Cirurgia com rifle: Alterações espalhadas por todo o código para lidar com diferentes plataformas podem introduzir complexidade e tornar o código menos portátil.

7. Inveja de recursos: O uso excessivo de recursos específicos de uma plataforma pode indicar dependências não adequadas e dificultar a migração para outras plataformas.

8. Aglomerados de dados: Grupos de dados específicos de uma plataforma que aparecem em várias partes do código podem dificultar a adaptação a outras plataformas.

9. Obsessão primitiva: O uso excessivo de tipos primitivos em vez de abstrações apropriadas pode levar a dependências específicas de plataforma e prejudicar a portabilidade.

10. Instruções switch: Uso excessivo de instruções "switch" para tratar casos específicos de plataforma pode dificultar a adaptação a diferentes ambientes.

## Técnicas de Refatoração

Para melhorar a portabilidade, é necessário realizar refatorações que lidem com os maus cheiros supracitados. Aqui estão algumas técnicas de refatoração que podem ser aplicadas em cada um dos maus cheiros:

1. Código duplicado:
    1.1. Extrair método: Identificar o código duplicado e extrair a lógica repetida para um novo método, que pode ser chamado em vários locais.

2. Método longo:
    2.1. Extrair método: Identificar partes do método que realizam funcionalidades distintas e extrair essas partes para métodos menores e mais específicos.
    2.2. Introduzir objeto-parâmetro: Se o método longo envolver grupos de parâmetros, criar um objeto que represente esses parâmetros e passá-lo para o método extraído.

3. Classe inchada:
    3.1. Extrair classe: Identificar responsabilidades distintas na classe e criar novas classes para tratar essas responsabilidades separadamente.
    3.2. Extrair interface: Extrair interfaces que representem diferentes aspectos da classe para permitir que ela seja mais facilmente adaptável a diferentes contextos.

4. Lista de parâmetros longa demais:
    4.1. Substituir parâmetro por método: Quando um método usa um parâmetro para obter um valor específico, substituí-lo por um método que retorne esse valor diretamente.
    4.2. Introduzir objeto-parâmetro: Agrupar parâmetros relacionados em um objeto e passá-lo como um único parâmetro.

5. Mudanças divergentes:
    5.1. Extrair classe: Identificar partes do código que mudam para diferentes plataformas e agrupá-las em classes separadas.

6. Cirurgia com rifle:
    6.1. Mover método: Mover métodos relacionados a diferentes plataformas para as classes que contêm as funcionalidades específicas de cada plataforma.

7. Inveja de recursos:
    7.1. Mover método: Mover métodos que usam recursos específicos de uma plataforma para a classe que detém esses recursos.

8. Aglomerados de dados:
    8.1. Introduzir objeto-parâmetro: Agrupar dados relacionados em um objeto e passá-lo como um único parâmetro nos métodos que precisam desses dados.

9. Obsessão primitiva:
    9.1. Trocar dado por objeto: Substituir o uso excessivo de tipos primitivos por objetos que encapsulem os dados relacionados.

10. Instruções switch:
    10.1. Substituir condicional por polimorfismo: Substituir as instruções "switch" por uma hierarquia de classes com comportamentos específicos para cada plataforma.
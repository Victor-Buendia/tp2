# Ausência de Duplicidades

## Descrição

A característica de "Ausência de duplicidades" é fundamental para um bom projeto de *software* na medida em que evita a repetição desnecessária de código em uma aplicação. Isso quer dizer que o código precisa ser projetado de forma a eliminar duplicações ou trechos idênticos ou similares, substituindo-os por apenas uma única implementação reutilizável.

Um projeto de *software* que não possui código duplicado apresenta uma vantagem na sua **estrutura**, já que, sem duplicidades, cada trecho de código tem uma única responsabilidade e é colocado no lugar apropriado. Dessa maneira, o código se torna mais organizado e coeso, facilitando a manutenção e a evolução do código.

Programas sem duplicidade de código também são mais **coesos**. A coesão refere-se à organização lógica e funcional das partes de um programa. Eliminando a duplicidade de código, a modularização dele é feita de forma a agrupar o código relacionado em um único local, criando uma função ou componente com uma responsabilidade específica. Isso torna o código mais modular e facilita a compreensão das relações entre os diferentes componentes do sistema.

Além disso, a redução de duplicidades também ajuda a **diminuir o acoplamento** entre os diferentes módulos ou componentes do código. O acoplamento refere-se ao grau de dependência entre as partes do programa. Ao eliminar duplicidades, o código se torna mais independente e menos propenso a efeitos colaterais indesejados, já que a alteração é feita apenas em um local específico que reflete em todos os locais em que a função, método ou componente é utilizado.

Outro benefício que a eliminação de duplicidades traz é tornar o código mais legível e compreensível. Com um código organizado a partir do ponto de vista lógico e funcional, torna-se mais fácil entender e modificar o código, garantindo sua consistência e clareza.

Por fim, não ter duplicidade no código viabiliza sua reutilização, já que componentes ou funções são chamadas de diferentes partes do código, promovendo a modularidade e beneficiando a manutenção e o desenvolvimento posterior. Além disso, a reutilização de código reduz a quantidade total de código necessário, resultando em programas mais enxutos e eficientes.

## Relação com maus cheiros de código

Os maus cheiros definidos por Martin Fowler são indicadores de problemas no design e qualidade do código, são pontos em que há possibilidades para aplicação de refatoração. Sendo assim, podemos relaconar diretamente a característica de ausência de duplicidades à eliminação de maus cheiros definidos por Martin, podendo destacar:

1. Código duplicado: A ausência de duplicidades elimina diretamente esse mau cheiro, porque uma vez que exista duplicação, sabemos que partes similares ou idênticas do código estão em partes diferentes do programa. Eliminando a duplicidade, promovemos a reutilização de código e aumentamos sua clareza e coesão.

2. Método longo: Os métodos longos geralmente são compostos de muitas linhas de códigos e uma mistura confusa de funcionalidades, muitas vezes com códigos com lógica e função parecidas em sua extensão (código duplicado). Assim, remover a duplicidade ajudar a combater esse mau cheiro, pois, ao identificar trechos de código semelhantes em um método longo, é possível extrair esses trechos duplicados e criar métodos auxiliares reutilizáveis.

3. Classe inchada: A classe inchada geralmente é uma classe que acumula várias responsabilidades e possui um número grande de atributos e métodos. Garantindo a ausência de duplicidade, podemos reduzir o tamanho dessas classes inchadas, já que podemos criar classes auxiliares mais especializadas, por exemplo, para redistribuir as responsabilidades e aumentar a coesão do código.

4. Lista de parâmetros longa demais: Um método com uma lista longa de parâmetros indica um comportamento muito generalizado e aumenta a ocorrência de erros em seu uso por parte dos programadores. Normalmente, esses métodos possuem código duplicado para gerar múltiplos comportamentos distintos. Assim, extrair esses trechos e criar métodos auxiliares reduz a necessidade de passar vários parâmetros para apenas um método.

## Técnicas de Refatoração

Há algumas importantes técnicas de refatoração que podem ajudar a alcançar a característica de "Ausência de duplicidades" no projeto de código. Dentre elas, cabe mencionar:

1. Extrair Método: Se há código duplicado em um programa, é possível extraí-lo para um novo método e chamá-lo ao longo do código em vez de repetir código. Isso remove a duplicidade e aumenta a reutilização.

2. Extrair Classe: Quando encontra-se um conjunto de atributos e métodos que são frequentemente usados em conjujunto em partes distintas do código, é possível extrair esses elementos para uma nova classe. Isso centraliza a lógica relacionada e elimina a duplicação desses elementos.

3. Extrair Constante: Caso *strings* ou números (ou outros valores literais) sejam repetidamente usadas em múltiplas partes do código, o ideal é extraí-los para constantes para eliminar a duplicação e facilitar a manutenibilidade e legibilidade do código.

4. Polimorfismo: Em situações nas quais várias partes do código possuem uma lógica parecida mas algumas pequenas partes variam, pode ser interessante usar polimorfismo para eliminar a duplicidade. Isso envolveria a criação de uma hierarquia de classes, na qual cada classe implementa a lógica específica para seu contexto. Assim, o código duplicado é substituído por chamadas polimórficas.

5. Usar Funções de Biblioteca: Atualmente há uma gama de bibliotecas e funções prontas que podem substituir um comportamento alcançado por um código que é duplicado em um programa. Portanto, você pode eliminar a duplicação e aproveitar soluções já testadas e otimizadas ao utilizar bibliotecas e suas funções.

No geral, o objetivo das refatorações supracitadas no contexto de "Ausência de duplicidade" é identificar padrões duplicados e encontrar maneiras de reutilizar, extrair ou substituir o código duplicado.

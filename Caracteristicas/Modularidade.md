# Modularidade

## Descrição

Modularidade se dá pela característica da elaboração de software onde é criada uma divisão do sistema construído em componentes (ou módulos) com papéis independentes. Busca-se, para esses módulos, que tenham alta coesão e baixo acoplamento como principal objetivo.
Dessa maneira, a modularidade afeta as seguintes características do código da seguinte forma:

- Coesão: Um dos principais objetivos da modularidade é a obtenção de uma alta coesão. Os módulos criados, quando bem elaborados, apresentaram alto nível dessa característica. A alta coesão corrobora para que funcionalidades relacionadas estejam agrupadas e que a manutenção seja simplificada, já que, a alteração em módulos dificilmente afetará outras partes do sistema.

- Acoplamento: Juntamente à alta coesão, o baixo nível de acoplamento é um objetivo da modularização. A utilização de módulos estruturados a partir de interfaces claras e corretamente definidas ajuda, não somente no aspecto da padronização de utilização dos módulos, mas também na facilitação da modificação dos mesmos, à medida que é mais simples a alteração dos mesmos sem que haja impactos em outros módulos. O conjunto dessas características reflete na flexibilidade de reutilização de código.

- Claridade: A modularidade ajuda na compreensão do código na medida em que, através da separação do sistema em módulos, a leitura e compreensão das funcionalidades é simplificada.

- Estrutura: A estrutura de um código modularizado torna-se mais organizado, uma vez que, os módulos oferecem uma visão abstraída de cada parte do sistema e cada uma de suas responsabilidades.


## Relação com os maus-cheiros de código

Dentre os maus cheiros de código apresentados por Martin Fowler em sua obra "Refactoring: Improving the Design of Existing Code", os seguintes são relacionados a um código que falha na utilização da modularidade: Cirurgia com rifle, Código duplicado e Classe grande.  

- Código duplicado: A ausência da modularização resulta na repetição de trechos de código múltiplas vezes em um sistema. Como as funcionalidades não são modularizadas corretamente, acabam por não serem reutilizadas ao longo do código.

- Classe grande: A falta da característica pode acarretar na utilização de classes com múltiplas responsabilidades além do que deveriam (baixa coesão).


- Cirurgia com rifle: A ausência da característica de modularidade pode fazer com que o code smell seja recorrente, já que por não seguir uma estrutura de módulos com responsabilidades definidas o código pode ser afetado em múltiplos lugares desconectados  por alterações.



## Operações de refatoração para atingir a característica

Dentre as operações de refatoração que podem ajudar a atingir a modularidade, temos as seguintes:

- Extrair Método: Operação utilizada para extrair um trecho de código para um novo método. A operação pode ser usada para separar trechos de códigos em métodos mais coesos e reutilizáveis.

- Extrair Classe: Operação utilizada quando uma parte do código contempla um comportamento e atributos relacionados. Ao extrair esses comportamentos e atributos para uma nova classe, contribui-se para a criação de um novo módulo com uma responsabilidade própria.

- Mover Método: A operação consiste em mover um método de uma classe para outra, quando o método é mais frequentemente utilizado em outra classe. Ao mover tais métodos para as classes corretas, melhora-se a coesão e pode-se diminuir o acoplamento entre as classes, o que contribui para a modularidade do código.

- Introduzir Objeto de Parâmetro: Tal operação consiste em juntar vários parâmetros relacionados em um único objeto. Esse objeto é parâmetro ao invés de múltiplos parâmetros individuais. Isso reduz a dependência de múltiplos parâmetros e torna as interfaces mais claras e coesas. Por consequência, melhora-se a modularidade.

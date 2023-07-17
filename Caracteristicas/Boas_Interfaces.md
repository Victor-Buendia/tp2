# Boas Interfaces

## Descrição 

O tema específico abordado no livro "Pete Goodliffe - Code Craft" é sobre a criação de interfaces de qualidade, intitulada "Good Interfaces". O autor destaca a importância de interfaces bem projetadas como a fachada pública de um módulo, através das quais a funcionalidade do módulo é disponibilizada e acessada.

O livro sugere uma abordagem passo a passo para criar uma boa interface:
- Identificar o cliente e suas necessidades: É importante compreender o que o cliente deseja realizar através da interface.
- Identificar o fornecedor e sua capacidade: É necessário identificar o que o fornecedor é capaz de fornecer para atender às necessidades do cliente.
- Inferir o tipo de interface necessário: Determinar se é uma função, uma classe, um protocolo de rede ou outro tipo de interface, dependendo do contexto. Às vezes, é possível encapsular uma interface em diferentes formas, como envolver um objeto CORBA em uma biblioteca para disponibilizar sua funcionalidade em uma rede de computadores colaboradores.
- Determinar a natureza da operação: Identificar a funcionalidade essencial que precisa ser fornecida, levando em consideração se é mais geral do que o requisito específico do cliente. Muitas vezes, dentro de uma função, há uma operação mais útil esperando para ser extraída.

O livro também explora alguns princípios importantes para garantir a qualidade das interfaces:
1. Particionamento: Uma interface define uma linha de separação e ponto de contato entre o cliente e o implementador. O objetivo é estabelecer uma comunicação definida e evitar interações ad hoc.
2. Abstração: A abstração permite que o usuário se concentre nas decisões importantes, ignorando seletivamente certos detalhes. É importante escolher cuidadosamente o que é importante para o usuário e o que pode ser ocultado.
3. Compressão: A capacidade de uma interface de representar uma operação complexa de maneira mais simples. Isso é frequentemente alcançado através de boas abstrações, mas abstrações inadequadas podem levar o código a ficar mais verboso.
4. Substitutabilidade: A possibilidade de substituir uma implementação de interface por outra, desde que atenda ao mesmo contrato. Isso permite flexibilidade na escolha de diferentes implementações que possam ser trocadas sem afetar o comportamento visível através da interface.

## Relação com maus cheiros de código

Em relação aos "maus-cheiros de código" definidos por Fowler, o livro mostra como uma interface mal projetada pode levar a problemas como:
- Má estrutura: Uma interface ruim pode colocar as operações no lugar errado, dificultando o acompanhamento da lógica da aplicação e tornando a extensão do design mais difícil.
- Falta de clareza: Interfaces mal definidas podem levar à falta de compreensão sobre quem são os atores principais no sistema e o que eles devem fazer, resultando em interfaces pouco eficazes.
- Alto acoplamento: Uma interface mal projetada pode aumentar o acoplamento entre os módulos, tornando o código menos flexível e mais difícil de modificar.
- Baixa coesão: Interfaces inadequadas podem levar a uma redução da coesão, pois não estão focadas em fornecer apenas a funcionalidade necessária para um cliente específico.

## Técnicas de Refatoração

No contexto de alcançar "Boas Interfaces" no projeto de código, existem algumas técnicas de refatoração que podem ser úteis. Dentre elas temos:

- Implementação de Padrões de Projeto: Alguns padrões de projeto, podem ser aplicados para refatorar interfaces existentes e melhorar sua estrutura e flexibilidade. Esses padrões ajudam a separar as responsabilidades, promovendo a coesão e a baixo acoplamento entre os módulos.
- Remoção de Código Duplicado: A duplicação de código pode levar a interfaces confusas e redundantes. Ao identificar trechos de código duplicados, é possível criar métodos ou classes reutilizáveis e substituir as duplicações, tornando as interfaces mais coesas e concisas.
- Renomeação de Métodos e Classes: Nomes claros e descritivos são essenciais para interfaces de qualidade. Ao refatorar, é importante revisar os nomes de métodos e classes existentes, garantindo que eles transmitam adequadamente a intenção e a funcionalidade dos componentes. Isso ajuda na compreensão e na utilização correta das interfaces.
- Extração de Classe: Se uma classe está se tornando grande e complexa, é possível extrair parte de suas responsabilidades em uma nova classe. Essa técnica ajuda a dividir as interfaces em unidades mais coesas e a reduzir o acoplamento entre os módulos, melhorando a estrutura geral do código.

## Conclusão

Em resumo, o capítulo "Good Interfaces" do livro "Pete Goodliffe - Code Craft" enfatiza a importância de interfaces bem projetadas para melhorar a estrutura, clareza, coesão, acoplamento e outros aspectos do código. Ele fornece diretrizes e princípios para criar interfaces de qualidade, além de destacar a relação dessas interfaces com os maus-cheiros de código definidos por Fowler.

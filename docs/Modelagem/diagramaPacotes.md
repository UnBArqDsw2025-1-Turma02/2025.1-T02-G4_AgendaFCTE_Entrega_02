## Introdução

O diagrama de pacotes é um dos diagramas estruturais da UML utilizados para representar a organização e a divisão de um sistema em pacotes lógicos. Esses pacotes agrupam elementos relacionados, como classes, interfaces e outros artefatos, facilitando a compreensão da arquitetura geral do sistema. Através da visualização hierárquica, é possível identificar claramente as dependências e relacionamentos entre diferentes partes do software.

Esse tipo de diagrama é permite uma modelagem modular e escalável. Ao representar as interações entre os pacotes, o diagrama contribui para uma melhor organização do código-fonte e promove práticas de desenvolvimento orientadas à separação de responsabilidades e reutilização de componentes.

## Camadas

### Model
É a parte responsável pela lógica de negócio do projeto e pelo gerenciamento dos dados da aplicação. Atua como intermediária entre o banco de dados e a camada de visualização (View). Sua principal função é permitir a criação, leitura, atualização e exclusão (CRUD) de informações, garantindo a integridade e consistência dos dados durante essas operações.

### View
É responsável pela apresentação das informações ao usuário. Ela recebe os dados processados pela Model e os formata para exibição, utilizando templates apropriados para renderizar a resposta. A View não deve conter lógica de negócio, mas sim controlar como os dados são apresentados, funcionando como uma ponte entre a Model e a interface do usuário.

### Template
É encarregado da estrutura e do layout visual da interface. Contém os arquivos HTML, CSS e, quando aplicável, frameworks como Bootstrap para estilização. Os templates são utilizados pela View para renderizar o conteúdo visual de forma consistente, separando a lógica de apresentação da estrutura de design.


## Elementos


## Resultados



## Histórico de Versões

| Versão | Data       | Descrição               | Autor                                             | Revisor                                                | Comentário do Revisor |
| ------ | ---------- | ----------------------- | ------------------------------------------------- | ------------------------------------------------------ | --------------------- |
| `1.0`    | 17/04/2025 | Elaboração do esqueleto para entrega 2    |[Thales Euflauzino](https://github.com/thaleseuflauzino) | [Víctor Schmidt](https://github.com/moonshinerd)  | Aprovação do PR, ótimo trabalho |
| `1.1`    | 29/04/2025 | Introdução e  Camadas MVT |[Pedro Lopes](https://github.com/pLopess) |  |  |
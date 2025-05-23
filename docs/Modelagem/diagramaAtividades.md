# Diagrama de Atividades

## Introdução

O diagrama de atividades é utilizado para modelar o fluxo de trabalho ou de processos dentro de um sistema. Ele descreve a sequência de ações realizadas, decisões tomadas e caminhos possíveis durante a execução de uma atividade, sendo útil tanto para representar processos de negócios quanto comportamentos de sistemas ou algoritmos.

Alguns dos componentes mais comuns de um diagrama de atividade incluem:

- Ações : uma etapa da atividade em que o usuário ou software realiza uma determinada tarefa, indicados por retângulos de cantos arredondados.
- Nó de decisão : um ramo condicional no fluxo representado por um diamante. Inclui uma única entrada e duas ou mais saídas.
- Fluxos de controle : outro nome dado aos conectores que mostram o fluxo entre as etapas no diagrama.
- Nó inicial : simboliza o início da atividade, representado por um círculo preto.
- Nó final : representa a etapa final da atividade, representado por um círculo preto delineado.

## Resultados

### Diagrama de atividades - fluxo de busca, navegação e inscrição

**Versão Inicial**

<center>
 <p><b>Figura 1 - Fluxo de busca, navegação e inscrição</b></p>
 
 <img src="./assets/diagrama-atividades/diagrama-atividades.jpg" alt="diagramaAtividade" width="100%">
 
 <font size="2"><p style="text-align: center"><b>Autor: <a href="https://github.com/AlexandreLJr">Alexandre Junior</a></b></p></font>
 </center>
 
 <br>

A figura 2 representa o Diagrama de Atividades que cobre a busca, navegação e inscrição em um evento. O fluxo já começa com a decisão de se logar/cadastrar ou não no site. Depois de tomar essa decisão, os dois caminhos são bem parecidos: o usuário deve escolher buscar um evento ou navegar pelo site. Ao escolher buscar, caso não ache o que procura, ele volta para a tomada de decisão anterior, se achar, ele visualiza o evento. Ao escolher navegar, ao encontrar algo de interesse, ele visualiza o evento. Ao visualizar, ele deverá escolher se irá se inscrever no evento ou não. Caso escolha a segunda opção, ele volta para a tomada de decisão anterior. Ao decidir se inscrever, o caminho varia dependendo se ele está logado. Se o usuário já tiver logado, ele poderá se inscrever no evento direto e, assim, chegar ao fim do fluxo. Se ele não estiver logado, ao escolher se inscrever, ele deverá fazer o login/cadastro, para então voltar a ver o evento e conseguir se inscrever, e, enfim, finalizar o fluxo.

<center>

<a id="fig2">**Figura 2 – Fluxo de busca, navegação e inscrição**</a>

![Figura1](../assets/diagrama-atividades/diagrama-atividades-busca.png)  
<font size="2"><p style="text-align: center"><b>_Autores: <a href="https://github.com/AlexandreLjr">Alexandre Junior, </a><a href="https://github.com/manu-sgc">Manoela Garcia</a>_</b></p></font>

</center>

A Figura 3 apresenta o Diagrama de Atividades que descreve o fluxo de busca, navegação e inscrição em um evento. O processo se inicia com a decisão do usuário sobre realizar ou não o login/cadastro na plataforma. A partir dessa escolha, os caminhos são semelhantes: o usuário pode optar por buscar diretamente um evento ou navegar livremente pelo site.
Caso escolha a busca, ele poderá encontrar ou não o evento desejado. Se não encontrar, retornará ao ponto anterior de decisão. Se encontrar, visualizará os detalhes do evento. Já ao optar por navegar, o usuário poderá eventualmente encontrar um evento de interesse e, então, acessará sua visualização.
Na tela de visualização do evento, o usuário terá a opção de se inscrever ou não. Se decidir não se inscrever, voltará à etapa anterior (de busca ou navegação). Ao optar pela inscrição, o fluxo seguirá caminhos diferentes conforme o estado de autenticação do usuário: se já estiver logado, poderá se inscrever diretamente, concluindo o processo. Caso contrário, será necessário realizar o login ou cadastro antes de retornar à visualização do evento e concluir a inscrição, encerrando então o fluxo.

<center>

<a id="fig2">**Figura 3 – Fluxo de incrição em eventos**</a>

![alt text](../assets/diagrama-atividades/visualizar-eventos.png)
<font size="2"><p style="text-align: center"><b>_Autor: <a href="https://github.com/maykonjuso">Maykon Soares</a>_</b></p></font>

</center>

## Bibliografia

> FAKHROUTDINOV Kirill. Activity Diagrams. uml-diagrams.org. Disponível em: <https://www.uml-diagrams.org/activity-diagrams.html>. Acesso em: 30 abr. 2025.

## Histórico de Versões

| Versão | Data       | Descrição                                             | Autor                                                    | Revisor                                          | Comentário do Revisor           |
| ------ | ---------- | ----------------------------------------------------- | -------------------------------------------------------- | ------------------------------------------------ | ------------------------------- |
| `1.0`  | 17/04/2025 | Elaboração do esqueleto para entrega 2                | [Thales Euflauzino](https://github.com/thaleseuflauzino) | [Víctor Schmidt](https://github.com/moonshinerd) | Aprovação do PR, ótimo trabalho |
| `1.1`  | 30/04/2025 | Adicionando introdução e bibliografia                 | [Alexandre Junior](https://github.com/AlexandreLjr)      |  [Victor Bernardes](https://github.com/VHbernardes) | Revisado, ótimo trabalho                   |
| `1.2`  | 30/04/2025 | Adicionando versão 1 do diagrama de atividades        | [Alexandre Junior](https://github.com/AlexandreLjr)      |   [Victor Bernardes](https://github.com/VHbernardes)        |   Revisado, ótimo trabalho   |
| `1.3`  | 07/05/2025 | Adicionando diagrama com fluxo de busca e navegação   | [Manoela Garcia](https://github.com/manu-sgc)            |        [Victor Bernardes](https://github.com/VHbernardes)      |  Revisado, ótimo trabalho    |
| `1.3`  | 07/05/2025 | Adicionando diagrama com fluxo de incrição em eventos | [Maykon Soares](https://github.com/maykonjuso)           |    [Victor Bernardes](https://github.com/VHbernardes)        |   Revisado e aprovado, ótimo trabalho    |

## Introdução

O diagrama de sequência é utilizado principalmente para mostrar as interações entre objetos na ordem em que ocorrem. Embora muitos desenvolvedores acreditem que esses diagramas são feitos apenas para eles, esses diagramas são úteis tanto para análise de requisitos quanto para design e documentação de sistemas, novos ou existentes ([BELL, 2023](#ref1)).

## Diagrama de Sequência

### Fluxo de Busca e Inscrição em Evento

Na primeira imagem, representamos tanto o fluxo de inscrição em um evento, o qual o usuário precisa estar logado, quanto o de busca por um evento. O diagrama apresenta duas seções do sistema, Navegador (representando as principais views) e Controladora, as quais o usuário interage e realiza requisições. É possível notar que há um loop como fluxo alternativo, em que o usuário pode filtrar os eventos dentro da plataforma. Também, é possível o usuário requisitar a visualização de detalhes de um evento, para que assim possa se inscrever nele.

Outrossim, destaca-se que todo esse fluxo já considera a existência de uma classe Usuário, a qual não apresenta dependência alguma com os outros elementos do diagrama.

<center>

<a id="fig1">**Figura 1 - Fluxo de Busca e Inscrição em Evento**</a>

![Figura1](../assets/diagrama-sequencia/diagrama_sequencia_victorio.png)  
<font size="2"><p style="text-align: center"><b>*Autor: <a href="https://github.com/Victor-oss">Victório Lázaro</a>*</b></p></font>
</center>

### Fluxo de Favoritar, Visualizar Favoritos e Recomendar Eventos

Na segunda imagem, representamos o fluxo de favoritar eventos, visualizar favoritos e receber recomendações, ações que exigem que o usuário esteja logado. O diagrama é dividido entre Navegador e Controladora, refletindo a interação do usuário com a interface e a lógica do sistema.

Esse fluxo inicia com o usuário favoritando um evento, podendo depois acessar sua lista de favoritos e obter sugestões com base nesses interesses. Importante destacar que o diagrama foca apenas nessas funcionalidades privadas. Ações públicas como visualizar, filtrar ou acessar detalhes de eventos não exigem login e, por isso, não estão representadas aqui.

<center>

<a id="fig2">**Figura 2 - Favoritar, Visualizar Favoritos e Recomendar Eventos**</a>

![Figura2](../assets/diagrama-sequencia/diagrama_favoritos.png)  
<font size="2"><p style="text-align: center"><b>*Autor: <a href="https://github.com/rayenealmeida">Rayene Almeida</a>*</b></p></font>
</center>


### Fluxo de Cadastrar Eventos

Na terceira imagem, representamos o fluxo de cadastro de eventos, funcionalidade exclusiva do perfil de organizador. O diagrama está dividido entre Navegador, Controladora e Entidades, refletindo o caminho que os dados percorrem desde a interface até o armazenamento no sistema.

Esse fluxo se inicia quando o organizador acessa a tela de cadastro e preenche as informações do evento. Após o envio, os dados são validados e, se estiverem corretos, o evento é persistido no banco de dados. Notificações automáticas podem ser disparadas para usuários interessados.



<center>

<a id="fig3">**Figura 3 - Cadastrar Eventos**</a>

![Figura3](../assets/diagrama-sequencia/diagrama_cadastro.png)  
<font size="2"><p style="text-align: center"><b>*Autor: <a href="https://github.com/pLopess">Pedro Lopes</a>*</b></p></font>
</center>




## Referências Bibliográficas

> [<a id='ref1'>1</a>] BELL, Donald. *Explore the UML sequence diagram*. IBM Developer, 09 out. 2023. Disponível em: <https://developer.ibm.com/articles/the-sequence-diagram/?mhsrc=ibmsearch_a&mhq=sequence%20diagram&mhp=0/>. Acesso em: 21 abr. 2025.

> [<a id='ref2'>2</a>] SOUZA, Gildásio; CAVALCANTE, Eduardo. Apostila UML. [s.l.]: [s.n.], 2023. Disponível em: <https://aprender3.unb.br/mod/page/view.php?id=1368333>. Acesso em: 22 abr. 2025.

> [<a id='ref3'>3</a>] BARCELAR, Ricardo Rodrigues. Módulo 3 – Modelagem de Sistemas Orientada a Objetos com UML. Brasília: [s.n.], 2023. Disponível em: <https://aprender3.unb.br/mod/page/view.php?id=1368333>. Acesso em: 22 abr. 2025.

## Histórico de Versões

| Versão | Data       | Descrição               | Autor                                             | Revisor                                                | Comentário do Revisor |
| ------ | ---------- | ----------------------- | ------------------------------------------------- | ------------------------------------------------------ | --------------------- |
| `1.0`    | 17/04/2025 | Elaboração do esqueleto para entrega 2    |[Thales Euflauzino](https://github.com/thaleseuflauzino) | [Víctor Schmidt](https://github.com/moonshinerd)  | Aprovação do PR, ótimo trabalho |
| `1.1`    | 21/04/2025 | Adição do diagrama de esquema para busca e inscrição de eventos   |[Victório Lázaro](https://github.com/Victor-oss) | [Manoela Garcia](https://github.com/manu-sgc) | Só corrigir o que necessita de login |
| `1.2`    | 22/04/2025 | Adição do diagrama de esquema para favoritos e recomendações de eventos   |[Rayene Almeida](https://github.com/rayenealmeida) | [Manoela Garcia](https://github.com/manu-sgc) | Só adicionar o texto explicativo |
| `1.3`    | 23/04/2025 | Correção do diagrama de esquema para busca e inscrição de eventos   |[Victório Lázaro](https://github.com/Victor-oss) | [Manoela Garcia](https://github.com/manu-sgc) | Ficou muito bom!! |
| `1.4`    | 23/04/2025 | Adição da especificação das funcionalidades no diagrama que precisam de login  |[Rayene Almeida](https://github.com/rayenealmeida) | [Manoela Garcia](https://github.com/manu-sgc) | Tá ótimo! Aprovação do PR |
| `1.5`    | 02/05/2025 | Adição do diagrama de cadastro de eventos  |[Pedro Lopes](https://github.com/pLopess) | [Manoela Garcia](https://github.com/manu-sgc) | Muito bom!!!! Aprovação do PR |
## Introdução

Os diagramas de máquina de estados são uma ferramenta fundamental na modelagem de software baseada em UML, empregados para capturar o comportamento dinâmico de sistemas orientados a objetos ao representar os diferentes estados pelos quais um elemento pode passar durante seu ciclo de vida e as transições acionadas por eventos e condições específicas (HAREL, 1987; BOOCH; RUMBAUGH; JACOBSON, 1999). Conforme a especificação da [Object Management Group (OMG)](#ref2), essa notação, derivada dos statecharts de Harel, oferece suporte à hierarquia de estados, paralelismo de regiões e ações associadas a entradas, saídas e transições, garantindo formalidade e clareza na representação do comportamento interno dos componentes e suportando ainda a análise sistemática de consistência por meio de matrizes de transição e diagramas de superestados ([CLARKE; GRUMBERG; PELED, 1999](#ref3)).

Ao estruturar graficamente o fluxo de controle e as reações a estímulos externos, os diagramas de estados facilitam a comunicação entre equipes de desenvolvimento e a detecção precoce de inconsistências ou comportamentos não desejados, sendo amplamente utilizados em sistemas reativos e embarcados de alta criticidade e adotados como padrão em metodologias de desenvolvimento ágil e formal. Além disso, a formalização das semânticas de execução possibilita a aplicação de técnicas de verificação automática e teste de modelos, contribuindo para a robustez e confiabilidade das soluções de software ([OBJECT MANAGEMENT GROUP, 2011](#ref4)).


<font size="3"><p style="text-align: center"><b>Tabela 1</b>: Elementos do Diagrama de Estados</p></font>

| Nome | Função | Elemento
|------|------|:-------:
| Estado | ​A caixa de estados representa uma situação específica em que um objeto pode estar durante seu ciclo de vida, mostrando como ele reage a eventos e transita entre estados.  | <figure style="width: 100%; display: flex; justify-content: center; background-color: white; padding: 5px;"> ![estado](../assets/diagrama-estados/estado.png) </figure>
| Seta de Transição | ​A seta de transição indica a mudança de um estado para outro, acionada por um evento ou condição específica.​ | <figure style="width: 100%; display: flex; justify-content: center; background-color: white; padding: 10px;"> ![seta-transicao](../assets/diagrama-estados/seta-transicao.png) </figure>
| Estado Inicial | O estado inicial em um diagrama de estados representa o ponto de partida do ciclo de vida de um objeto ou sistema, indicando onde tudo começa. É simbolizado por um círculo sólido com uma seta apontando para o primeiro estado.​ | <figure style="width: 100%; display: flex; justify-content: center; background-color: white; padding: 10px;"> ![estado-inicial](../assets/diagrama-estados/estado-inicial.png) </figure>
| Exterminador (Estado Final) | ​O estado final representa o término do ciclo de vida de um objeto ou processo, indicando que ele não responderá mais a eventos futuros. É simbolizado por um círculo com outro círculo preenchido no centro.  | <figure style="width: 100%; display: flex; justify-content: center; background-color: white; padding: 10px;"> ![estado-final](../assets/diagrama-estados/estado-final.png) </figure>
| Estado Composto | ​O estado composto representa um estado que contém outros estados, permitindo modelar comportamentos complexos ou paralelos dentro de um único estado.   | <figure style="width: 100%; display: flex; justify-content: center; background-color: white; padding: 10px;"> ![estado-final](../assets/diagrama-estados/estado-composto.png) </figure>
| Ação | Uma ação é uma operação executável e atômica que ocorre durante uma transição ou dentro de um estado, como chamar uma função ou enviar um sinal.   | <figure style="width: 100%; display: flex; justify-content: center; background-color: white; padding: 10px;"> ![acao](../assets/diagrama-estados/acao.png) </figure>

<font size="2"><p style="text-align: center"><b>*Autor: <a href="https://github.com/moonshinerd">Víctor Schmidt*</a></b></p></font>

## Diagrama de Estados

<a id="diagrama1" href="https://app.diagrams.net/#G1dj738qSWtRH6K0qWtVimGE9OIRKDBL8L#%7B%22pageId%22%3A%2258cdce13-f638-feb5-8d6f-7d28b1aa9fa0%22%7D" style="display: block; text-align: center;">
  <b>Diagrama 1</b> – Diagrama de Estados
</a>


<iframe frameborder="0" style="width:100%;height:749px;" src="https://viewer.diagrams.net/?tags=%7B%7D&lightbox=1&highlight=0000ff&edit=https%3A%2F%2Fapp.diagrams.net%2F%23G1dj738qSWtRH6K0qWtVimGE9OIRKDBL8L%23%257B%2522pageId%2522%253A%252258cdce13-f638-feb5-8d6f-7d28b1aa9fa0%2522%257D&layers=1&nav=1&title=diagrama-estados.drawio&dark=0#Uhttps%3A%2F%2Fdrive.google.com%2Fuc%3Fid%3D1dj738qSWtRH6K0qWtVimGE9OIRKDBL8L%26export%3Ddownload"></iframe>

### Registro 1
Este registro descreve a modelagem dos fluxos referentes aos requisitos:

- [RF01](https://unbarqdsw2025-1-turma02.github.io/2025.1-T02-_G4_AgendaFCTE_Entrega_01/#/./Base/1.5.3.PriorizacaoMosCoW?id=rf1) – Integração com outros sites ou apps de eventos, permitindo sincronizar informações e compromissos.  
- [RF02](https://unbarqdsw2025-1-turma02.github.io/2025.1-T02-_G4_AgendaFCTE_Entrega_01/#/./Base/1.5.3.PriorizacaoMosCoW?id=rf2) – Integração com redes sociais e outros canais (Instagram, WhatsApp, e-mail, murais etc.) para compartilhamento e divulgação de eventos.  
- [RF03](https://unbarqdsw2025-1-turma02.github.io/2025.1-T02-_G4_AgendaFCTE_Entrega_01/#/./Base/1.5.3.PriorizacaoMosCoW?id=rf3) – Integração com agendas e mapas (Google Agenda, Outlook etc.), permitindo adicionar eventos e visualizar localização. 
- [RF04](https://unbarqdsw2025-1-turma02.github.io/2025.1-T02-_G4_AgendaFCTE_Entrega_01/#/./Base/1.5.3.PriorizacaoMosCoW?id=rf4) – Visualização de eventos com informações como data, hora, local, descrição, link de inscrição e contato.  
- [RF05](https://unbarqdsw2025-1-turma02.github.io/2025.1-T02-_G4_AgendaFCTE_Entrega_01/#/./Base/1.5.3.PriorizacaoMosCoW?id=rf5) – Cadastro, edição e exclusão de eventos pelos organizadores, com definição de detalhes como data, local, categoria e regras.  
- [RF06](https://unbarqdsw2025-1-turma02.github.io/2025.1-T02-_G4_AgendaFCTE_Entrega_01/#/./Base/1.5.3.PriorizacaoMosCoW?id=rf6) – Sugerir novos eventos, com possibilidade de moderação.
- [RF09](https://unbarqdsw2025-1-turma02.github.io/2025.1-T02-_G4_AgendaFCTE_Entrega_01/#/./Base/1.5.3.PriorizacaoMosCoW?id=rf9) – Busca de eventos por nome, local, data, tipo, categoria e tags.  
- [RF10](https://unbarqdsw2025-1-turma02.github.io/2025.1-T02-_G4_AgendaFCTE_Entrega_01/#/./Base/1.5.3.PriorizacaoMosCoW?id=rf10) – Filtrar e organizar eventos por tipo, data, localização, categoria, popularidade, hype e avaliações.  
- [RF14](https://unbarqdsw2025-1-turma02.github.io/2025.1-T02-_G4_AgendaFCTE_Entrega_01/#/./Base/1.5.3.PriorizacaoMosCoW?id=rf14) – Permitir favoritar eventos para acompanhar novidades e receber notificações.  
- [RF15](https://unbarqdsw2025-1-turma02.github.io/2025.1-T02-_G4_AgendaFCTE_Entrega_01/#/./Base/1.5.3.PriorizacaoMosCoW?id=rf15) – Oferecer sistema de comentários para interação entre usuários e organizadores, com moderação.  
- [RF18](https://unbarqdsw2025-1-turma02.github.io/2025.1-T02-_G4_AgendaFCTE_Entrega_01/#/./Base/1.5.3.PriorizacaoMosCoW?id=rf18) – Inscrição e resgate/compra de ingressos para eventos. 
- [RF21](https://unbarqdsw2025-1-turma02.github.io/2025.1-T02-_G4_AgendaFCTE_Entrega_01/#/./Base/1.5.3.PriorizacaoMosCoW?id=rf21) – Criação de perfis e autenticação dos usuários, inclusive por e-mail.  
- [RF26](https://unbarqdsw2025-1-turma02.github.io/2025.1-T02-_G4_AgendaFCTE_Entrega_01/#/./Base/1.5.3.PriorizacaoMosCoW?id=rf26) – Permitir que usuários curtam eventos.  

Ele registra o que foi feito na versão `1.1` e `1.2` pelo membro [Víctor Schmidt](https://github.com/moonshinerd) quanto ao diagrama de estados.

<center>

<a id="fig1">**Figura 1 - Registro 1**</a>

![Figura1](../assets/diagrama-estados/registro/registro1.jpg)  
<font size="2"><p style="text-align: center"><b>*Autor: <a href="https://github.com/moonshinerd">Víctor Schmidt</a>*</b></p></font>
</center>


## Referência Bibliográfica

> [<a id='ref1'>1</a>] LUCID SOFTWARE INC. _O que é um diagrama de máquina de estados?_ Lucidchart, 2025. Disponível em: https://www.lucidchart.com/pages/pt/o-que-e-diagrama-de-maquina-de-estados-uml. Acesso em: 21 abr. 2025.
>
> [<a id='ref2'>2</a>] OBJECT MANAGEMENT GROUP. *Unified Modeling Language® – Superstructure*. Version 2.5.1, Formal/2017‑12‑05. OMG, 2017. Disponível em: <https://www.omg.org/spec/UML/2.5.1/PDF>. Acesso em: 21 abr. 2025.
>
> [<a id='ref3'>3</a>] CLARKE, Edmund M.; GRUMBERG, Orna; PELED, Doron A. *Model Checking*. Cambridge, MA: MIT Press, 1999.
>
> [<a id='ref4'>4</a>] OBJECT MANAGEMENT GROUP. *Semantics of a Foundational Subset for Executable UML Models (fUML)*. Version 1.1, Formal/2011‑08‑05. OMG, 2011. Disponível em: <https://www.omg.org/spec/FUML/1.1>. Acesso em: 21 abr. 2025.

## Histórico de Versões

| Versão | Data | Descrição | Autor | Revisor | Comentário do Revisor |
| -- | -- | -- | -- | -- | -- |
| `1.0`    | 17/04/2025 | Elaboração do esqueleto para entrega 2    |[Thales Euflauzino](https://github.com/thaleseuflauzino) | [Víctor Schmidt](https://github.com/moonshinerd)  | Aprovação do PR, ótimo trabalho |
| `1.1`    | 21/04/2025 | Adicionando introdução, referências bibliográficas e tabela 1 com os elementos do diagrama de estados    | [Víctor Schmidt](https://github.com/moonshinerd) |   |  |
| `1.2`    | 22/04/2025 | Adicionando registro 1 e os requisitos trabalhados nesse registro dentro do diagrama de estados | [Víctor Schmidt](https://github.com/moonshinerd) |   |  |
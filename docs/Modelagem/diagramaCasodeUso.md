## Introdução

Um caso de uso detalha como o sistema é acionado em um contexto específico, descrevendo passo a passo a interação entre os usuários (atores) e o sistema até a realização de um objetivo pré‑definido. Seu principal papel é orientar o desenvolvimento, deixando claros os requisitos funcionais: o que o usuário pode fazer e como o sistema deve responder em cada etapa ([JACOBSON et al., 1992](#ref1)). 

## Metodologia

Para mapear as funcionalidades do sistema, usamos o diagrama de caso de uso, uma representação visual que destaca atores (usuários ou sistemas externos) e os casos de uso (ações que o sistema executa) ([SOMMERVILLE, 2011](#ref2)). 

Além disso, adotamos a persona [**Camila Duarte**](https://unbarqdsw2025-1-turma02.github.io/2025.1-T02-_G4_AgendaFCTE_Entrega_01/#/./Base/1.1.5.1.PerfilDeUsuarioEPersonas?id=camila-duarte) para alinhar cada caso de uso às necessidades reais dos usuários. Isso garante cenários mais verossímeis, levando em conta expectativas e desafios do perfil representado pela persona ([PRUITT; GRUDIN, 2002](#ref3)). 

A seguir, a Tabela 1 resume os principais elementos de um diagrama de caso de uso:

<font size="3"><p style="text-align: center"><b>Tabela 1</b>: Elementos do diagrama de casos de uso</p></font>

| Nome | Função | Elemento
|------|------|:-------:
| Ator | Representam os diversos tipos de usuários externos que interagem com o sistema. | <figure style="width: 40%; display: flex; justify-content: center; background-color: white; padding: 5px;"> ![boneco](../assets/casos-de-uso/bonecodepalito.png) </figure>
| Elipse (Caso de Uso) | É utilizada para representar os casos de uso em um diagrama, destacando funcionalidades ou ações específicas que o sistema realiza em resposta às interações dos atores. A elipse identifica cada caso de uso, exibindo o nome correspondente em seu interior. | <figure style="width: 40%; display: flex; justify-content: center; background-color: white; padding: 10px;"> ![elipse](../assets/casos-de-uso/elipse.png) </figure>
| Retângulo (Sistema) | É utilizado para representar o sistema ou o componente em análise, agrupando os casos de uso e os atores associados a ele. | <figure style="width: 40%; display: flex; justify-content: center; background-color: white; padding: 10px;"> ![retangulo](../assets/casos-de-uso/retangulo.png) </figure>
| Flecha (Relações) | As setas são utilizadas para ilustrar as relações ou interações entre os atores e os casos de uso no diagrama. | <figure style="width: 40%; display: flex; justify-content: center; background-color: white; padding: 10px;"> ![flecha](../assets/casos-de-uso/flecha.png) </figure>

<font size="2"><p style="text-align: center"><b>*Autor: <a href="https://github.com/moonshinerd">Víctor Schmidt*</a></b></p></font>

### Detalhamento adicional

No diagrama de casos de uso, você também pode explicitar:

- **Requisitos externos**: funcionalidades essenciais que o sistema deve oferecer para satisfazer demandas dos usuários.  
- **Funcionalidades do sistema**: capacidades internas necessárias para atender essas demandas de forma eficiente.  
- **Requisitos ambientais**: condições ou restrições do ambiente onde o sistema opera, incluindo integrações e dependências externas.  

## Diagrama de Casos de Uso

<center> 

**Diagrama 1** - <a id='quadro-caso-de-uso' href='https://app.diagrams.net/#G1OvxKGUKmt6cI1kB4XkXkrmrW_aqWq1Q3#%7B%22pageId%22%3A%22cuc-KDw1VMoB7bZAWTw1%22%7D'>Quadro de Casos de Uso no Draw.io</a>

</center>


<div style="border: 1px solid #ccc; border-radius: 8px; padding: 10px; box-shadow: 0 2px 6px rgba(0,0,0,0.1);">
  <iframe frameborder="0" style="width:100%;height:514px;" src="https://viewer.diagrams.net/?tags=%7B%7D&lightbox=1&highlight=0000ff&layers=1&nav=1&title=use-cases.drawio&dark=0#Uhttps%3A%2F%2Fdrive.google.com%2Fuc%3Fid%3D1OvxKGUKmt6cI1kB4XkXkrmrW_aqWq1Q3%26export%3Ddownload"></iframe>
</div>

## Referências Bibliográficas

> [<a id='ref1'>1</a>] JACOBSON, Ivar; CHRISTERSON, Magnus; JONSSON, Patrik; ÖVERGAARD, Gunnar. **Object‑oriented software engineering: a use case driven approach**. New York; Wokingham, Eng.; Reading, Mass.: ACM Press; Addison‑Wesley, 1992. Disponível em: <https://archive.org/details/ivar-jacobson-object-oriented-software-engineering-a-use-case-driven-approach-ac>. Acesso em: 19 abr. 2025.
>
> [<a id='ref2'>2</a>] SOMMERVILLE, Ian. *Software Engineering*. 9. ed. Boston: Addison‑Wesley, 2011. Cap. 5: System Modelling. Disponível em: <https://archive.org/details/sommerville-ian-engenharia-de-software-2011>. Acesso em: 19 abr. 2025.
>
> [<a id='ref3'>3</a>] PRUITT, John; GRUDIN, Jonathan. *Personas, Participatory Design and Product Development: An Infrastructure for Engagement*. In: BINDER, Thomas; GREGORY, Judith; WAGNER, Ina (eds.). Proceedings of the Participatory Design Conference, 7., 23–25 jun. 2002, Malmö, Sweden. Palo Alto, CA: CPSR, 2002. p. 144–161. Disponível em: <https://ojs.ruc.dk/index.php/pdc/article/view/249/241>. Acesso em: 19 abr. 2025. 

## Histórico de Versões

| Versão | Data | Descrição | Autor | Revisor | Comentário do Revisor |
| -- | -- | -- | -- | -- | -- |
| `1.0`    | 17/04/2025 | Elaboração do esqueleto para entrega 2    |[Thales Euflauzino](https://github.com/thaleseuflauzino) | [Víctor Schmidt](https://github.com/moonshinerd)  | Aprovação do PR, ótimo trabalho |
| `1.1`    | 19/04/2025 | Adicionando quadro de casos de uso no Draw.io para elaborar os casos de uso, adicionando introdução, metodologia e referências bibliográficas. Adicionando também tabela de Elementos do diagrama de casos de uso | [Víctor Schmidt](https://github.com/moonshinerd) |  |  |
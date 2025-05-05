## Introdução

O diagrama de implementação/implantação descreve a implementação física de informações geradas pelo programa de software em componentes de hardware. As caixas tridimensionais conhecidas como nódulos, representam os elementos básicos de software ou hardware, ou nódulos no sistema. As linhas de nódulo a nódulo indicam relacionamentos e as formas menores contidas dentro das caixas representam os artefatos de software empregados ([LUCIDCHART, s.d.](#ref1)).

## Diagrama de Implantação

Esse diagrama foi feito com base nas tecnologias escolhidas após elaboração do [Quadro de Conhecimentos da Equipe](./Modelagem/quadroConhecimento.md), com o MySQL escolhido para ser o SGBD usado pela equipe, o Django para desenvolvimento da API e o React para elaboração do frontend da aplicação.

<center>
<p><b>Figura 1 - Versão 1 - Diagrama de Implantação</b></p>

![Diagrama de Implantação](../assets/diagrama-implantacao/diagrama_implantacao.png)

<font size="2"><p style="text-align: center"><b>*Autor: <a href="https://github.com/Victor-oss">Victório Lázaro</a>*</b></p></font>
</center>

Após analisar e revisar o Diagrama 1, [Manoela Garcia](https://github.com/manu-sgc) e [Victor Bernardes](https://github.com/VHbernardes) concluíram que seria importante representar de forma mais precisa o ambiente de produção da aplicação. Por isso, decidiram adicionar o Gunicorn ao diagrama, uma vez que esse componente atua como servidor WSGI, sendo responsável por executar a aplicação Django de maneira eficiente e segura.

<center>
<p><b>Figura 2 - Versão 2 - Diagrama de Implantação</b></p>

![Diagrama de Implantação - Versão 2](../assets/diagrama-implantacao/diagrama_implantacao2.png)

<font size="2"><p style="text-align: center"><b>*Autores: <a href="https://github.com/manu-sgc">Manoela Garcia, </a><a href="https://github.com/VHbernardes">Victor Bernardes</a>*</b></p></font>
</center>


#### 1. PC e Dispositivo Mobile
- Representam os clientes finais (usuários) acessando a aplicação via navegadores (Browser).
- Ambos se conectam à aplicação através do protocolo HTTPS, garantindo uma comunicação segura com o servidor.

#### 2. Frontend Web
- É o servidor que hospeda a interface gráfica da aplicação desenvolvida com React.
- Comunica-se com os usuários via HTTPS.
- Também se comunica com o Backend API por HTTPS, solicitando ou enviando dados.

#### 3. Backend API
- É o servidor que executa a lógica da aplicação, baseado no framework Django.
- Usa o servidor Gunicorn como WSGI HTTP server, que serve de intermediário entre o Django e os pedidos HTTP.
- Recebe requisições do frontend por HTTPS.
- Se comunica com o banco de dados via protocolo TCP.

#### 4. Servidor Banco de Dados
- Armazena os dados da aplicação utilizando o MySQL como SGBD.
- Fornece e recebe dados da API via TCP, sem expor esse acesso diretamente aos clientes ou ao frontend.


## Referências Bibliográficas

> [<a id='ref1'>1</a>] LUCIDCHART. *O que é um diagrama de implementação?*. s.l., s.d. Disponível em: <https://www.lucidchart.com/pages/pt/o-que-e-diagrama-de-implementacao-uml>. Acesso em: 01 mai. 2025.
> [<a id='ref2'>2</a>] UML DIAGRAMS. *Package Diagrams Overview. UML Diagrams*, 2009. Disponível em: <https://www.uml-diagrams.org/deployment-diagrams-overview.html>. Acesso em: 31 abr. 2025.

## Histórico de Versões

| Versão | Data       | Descrição               | Autor                                             | Revisor                                                | Comentário do Revisor |
| ------ | ---------- | ----------------------- | ------------------------------------------------- | ------------------------------------------------------ | --------------------- |
| `1.0`    | 17/04/2025 | Elaboração do esqueleto para entrega 2    |[Thales Euflauzino](https://github.com/thaleseuflauzino) | [Víctor Schmidt](https://github.com/moonshinerd)  | Aprovação do PR, ótimo trabalho |
| `1.1`    | 01/05/2025 | Adição do diagrama de implantação  |[Victório Lázaro](https://github.com/Victor-oss) |[Rayene Almeida](https://github.com/rayenealmeida) | Não foi necessário correções, PR Aprovado|
| `1.2`    | 03/05/2025 | Adição da segunda versão do diagrama  |[Manoela Garcia](https://github.com/manu-sgc) | [Rayene Almeida](https://github.com/rayenealmeida)  | Não foi necessário correções, PR Aprovado |
| `1.3`    | 04/05/2025 | Adição da explicação dos elementos do Diagrama  |[Victor Bernardes](https://github.com/VHbernardes) | [Rayene Almeida](https://github.com/rayenealmeida)  | Não foi necessário correções, PR Aprovado |
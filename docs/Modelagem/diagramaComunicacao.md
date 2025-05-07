## Introdução

Durante a modelagem de um produto de software, é importante que o funcionamento lógico do sistema esteja organizado e coeso, afim não apenas de que a leitura do código do sistema seja intuitiva, como também que ele esteja funcionando de forma otimizada, aumentando o seu desempenho e reduzindo o uso de memória. Com esse objetivo, surge o Diagrama de Comunicação, para determinar como os objetos de um sistema mantém comunicação, usando as funções adequadas nos momentos solicitados e também salvando dados nos locais e momentos adequados. 
Esse documento busca representar a troca de mensagens, chamadas de funções e envio de informações entre diferentes objetos do sistema: AgendaFCTE.
É importante ressaltar, que esse diagrama foi montado idealizando um sistema orientado a objetos.



# 📘 Especificação Suplementar – Diagrama de Comunicação

## 🗂 Funcionalidade: Cadastro de Evento (RF05)

---

## 🎯 Objetivo do Diagrama
Demonstrar como os objetos interagem para realizar o **cadastro de um novo evento** pelo **Organizador de Eventos** no sistema **AgendaFCTE**.

---

## 🧩 Objetos Envolvidos

| Objeto                    | Tipo        | Descrição                                                                 |
|---------------------------|-------------|---------------------------------------------------------------------------|
| `OrganizadorEvento`       | Ator        | Usuário com permissão para criar, editar ou excluir eventos.              |
| `Interface`               | Interface   | Tela ou formulário de cadastro de eventos.                                |
| `EventoController `       | Controlador | Lida com as requisições da interface, coordena a validação e o salvamento.|
| `RepositorioDeEventos`    | Repositório | Responsável por persistir o evento no banco de dados.                     |

---

## 🔁 Mensagens Trocadas

| Nº  | Remetente                | Destinatário            | Mensagem / Método                                 | Descrição                                               |
|-----|--------------------------|--------------------------|----------------------------------------------------|-----------------------------------------------------------|
| 1   | `OrganizadorEvento`      | `Interface` | `preencherDadosEvento()`                          | Organizador insere os dados no formulário.                |
| 2   | `Interface`| `EventosController`       | `enviarFormulario(dadosEvento)`                   | Interface envia os dados preenchidos.                    |
| 3   | `EventosController`      | `RepositorioDeEventos`       | `salvarEvento(dadosEvento)`                       | Dados validados são enviados para persistência.          |             |
| 4   | `RepositorioDeEventos`      | `Interface` | `exibirMensagem("Evento cadastrado com sucesso")` |  Retorna status para interface.                |

---

## 📷 Representação Visual


<center>

<a id="fig1">**Figura 1**</a>

![Figura1](docs\assets\diagrama-comu\diagramaDeComu.png)  
<font size="2"><p style="text-align: center"><b>*Autor: <a href="https://github.com/joaolucas102">João Lucas Costa</a>*</b></p></font>
</center>




## Histórico de Versões

| Versão | Data       | Descrição               | Autor                                             | Revisor                                                | Comentário do Revisor |
| ------ | ---------- | ----------------------- | ------------------------------------------------- | ------------------------------------------------------ | --------------------- |
| `1.0`    | 17/04/2025 | Elaboração do esqueleto para entrega 2    |[Thales Euflauzino](https://github.com/thaleseuflauzino) | [Víctor Schmidt](https://github.com/moonshinerd)  | Aprovação do PR, ótimo trabalho |
| `1.1`    | 06/05/2025 | Diagrama RF05    |[João Lucas](https://github.com/joãolucas102) |   |   |

## Introdução

A **Especificação de Caso de Uso** tem como objetivo traduzir requisitos funcionais em um documento estruturado, assegurando que cada interação entre atores e o sistema esteja claramente definida. Ela detalha:

- **Breve Descrição**: descreve o propósito do caso de uso e o valor entregue ao negócio ou ao usuário.
- **Atores**: identifica todos os perfis (usuários ou sistemas externos) envolvidos na execução.
- **Fluxo Básico de Eventos**: documenta o **Fluxo Principal** (cenário de sucesso) e os **Fluxos Alternativos** ou **Exceções** (tratamento de erros e condições especiais).
- **Pré-Condições** e **Pós-Condições**: definem estados obrigatórios antes da execução e garantem consistência ao término.
- **Requisitos Especiais** e **Regras de Negócio**: estabelecem restrições, validações e critérios de aceitação.
- **Pontos de Extensão**: criam ganchos para futuras melhorias sem impactar o fluxo principal.

> “A especificação de caso de uso é a ponte entre o problema de negócio e a solução técnica, garantindo que todos os stakeholders compartilhem uma visão única do comportamento do sistema” ([JACOBSON et al., 1992](#ref1)).

---

## Metodologia

Para elaborar as especificações dos casos de uso da **Agenda FCTE**, seguimos:

1. **Levantamento de Requisitos**  
   Entrevistas com stakeholders e análise de documentos de negócio para capturar necessidades.

2. **Modelagem com Diagramas UML**  
   Criação de diagramas de caso de uso para visualizar atores, relacionamentos e pacotes de funcionalidades ([SOMMERVILLE, 2011](#ref2)).

3. **Construção de Personas**  
   Perfis como **Camila Duarte** para validar fluxos e antecipar exceções reais ([PRUITT & GRUDIN, 2002](#ref3)).

4. **Preenchimento do Template de Especificação**  
   Utilizamos um template padronizado que contempla:
   - Título, versão e histórico de revisão
   - Breve Descrição
   - Atores
   - Fluxo Principal e Alternativos
   - Pré/Pos-Condições
   - Requisitos Especiais, Regras de Negócio e Pontos de Extensão

## Especificação de Caso de Uso: Adicionar Evento à Minha Agenda

### 1. Breve Descrição

Permite ao participante (aluno ou usuário autenticado) incluir um evento concluído ou futuro em sua agenda pessoal dentro do site Agenda FCTE, para receber notificações e organizar seu cronograma.

---

### 2. Atores

- **Participante** (aluno ou usuário autenticado)
- **Sistema de Agenda FCTE**

---

### 3. Fluxo Básico de Eventos

**Início:** Usuário visualiza detalhes de um evento e clica em **“Adicionar à Minha Agenda”**.

1. O sistema apresenta botão **Adicionar à Minha Agenda** na tela de detalhes do evento.
2. O participante clica em **Adicionar à Minha Agenda**.
3. O sistema verifica se o evento ainda não está na agenda do participante. **[RN01]**
4. O sistema adiciona o evento ao calendário interno do usuário (data, hora, local).
5. O sistema agenda notificações (pré-evento). **[RN02]**
6. O sistema exibe mensagem de confirmação:
   > “Evento adicionado à sua agenda com sucesso.”
7. Caso de uso encerrado.

---

### 4. Fluxos Alternativos

#### 4.1 FE01 – Evento já adicionado

- **Quando:** No passo 3, se o evento já estiver na agenda.
- **Fluxo:**
  1. O sistema exibe mensagem:
     > “Este evento já está na sua agenda.”
  2. Oferece opções:
     - **Ver Agenda** (direciona para lista de eventos salvos)
     - **Cancelar**
  3. Caso de uso encerrado.

#### 4.2 FE02 – Conflito de horário

- **Quando:** No passo 4, se o horário do evento conflitar com outro já agendado.
- **Fluxo:**
  1. O sistema detecta sobreposição de horários.
  2. Exibe alerta:
     > “Conflito de horário com Evento X. Deseja prosseguir?”
  3. Participante escolhe:
     - **Sim** → sistema adiciona mesmo assim (retorna a 4).
     - **Não** → sistema cancela inclusão (encerrado).

---

### 5. Pré-Condições

1. Participante autenticado no sistema.
2. Evento disponível para visualização de detalhes.

---

### 6. Pós-Condições

1. Evento inserido no calendário do participante.
2. Notificações configuradas.
3. Operação registrada em log de auditoria.

---

### 7. Pontos de Extensão

- **Extensão de “Visualizar Evento” (RF04):**  
  O botão **Adicionar à Minha Agenda** surge como opção estendida ao visualizar detalhes de qualquer evento.

---

### 8. Requisitos Especiais

1. Interface acessível (leitores de tela, alto contraste).

---

## Especificação de Caso de Uso: Emitir Certificado de Participação

### 1. Breve Descrição

Este caso de uso permite ao participante de um evento (aluno ou usuário autenticado) emitir seu certificado de participação em PDF, após confirmação de presença. O sistema verifica o status de participação, gera o documento no padrão da Agenda FCTE e o disponibiliza para download.

---

### 2. Atores

- **Participante** (aluno ou usuário autenticado no Site)
- **Sistema de Agenda FCTE**

---

### 3. Fluxo Básico de Eventos

**Início:** Usuário clica em “Emitir Certificado” na interface de eventos concluídos.

1. O sistema lista todos os eventos concluídos com presença confirmada e exibe botão **Emitir Certificado** para cada um.
2. O participante seleciona o evento desejado.
3. O sistema valida presença registrada do participante. **[RN01]**
4. O sistema gera o certificado em PDF (A4 paisagem, texto selecionável), com:
   - Nome do participante
   - Título do evento
   - Data do evento
   - Carga horária
   - Logotipo e assinatura digital  
     **[RN02]**
5. O sistema oferece opção de **Download**.
6. O participante faz download.
7. Caso de uso encerrado.

---

### 4. Fluxos Alternativos

#### 4.1 FE01 – Participação não confirmada

- **Quando:** No passo 3.3, se não houver registro de presença.
- **Fluxo:**
  1. O sistema exibe mensagem:
     > “Certificado indisponível. Participação não confirmada.”
  2. Caso de uso encerrado.

#### 4.2 FE02 – Erro na geração do certificado

- **Quando:** No passo 3.4, se a geração do PDF falhar.
- **Fluxo:**
  1. O sistema exibe mensagem:
     > “Erro ao gerar certificado. Tente novamente mais tarde.”
  2. O participante pode:
     - Voltar à lista de eventos (retornar a 3.1)
     - Encerrar o caso de uso

---

### 5. Pré-Condições

1. Participante autenticado no sistema.
2. Evento selecionado já concluído.

---

### 6. Pós-Condições

1. Certificado gerado e disponibilizado.
2. Operação registrada em log de auditoria.

---

### 7. Pontos de Extensão

- **Extensão de “Visualizar Evento” (RF04):**  
  A partir da visualização do histórico do evento, o usuário pode acionar diretamente a emissão do certificado.

---

### 8. Requisitos Especiais

1. Layout padrão da Agenda FCTE (cores, fonte, logotipo).
2. Certificado deve conter assinatura digital auditável.

---

### 9. Informações Adicionais

- **RN01 – Validação de presença:** apenas participantes com status “Presente” podem emitir.
- **RN02 – Formato do PDF:** A4, orientação paisagem, margens de 2 cm.
- Campos obrigatórios:
  - Nome do participante
  - Título do evento
  - Data do evento
  - Carga horária
  - Assinatura digital

--

## Especificação de Caso de Uso: Buscar evento

### 1. Breve Descrição

Permite ao usuário, esteja ele logado ou não, visualizar os eventos disponíveis na agenda da FCTE.


---

### 2. Atores

- **Pessoa da Comunidade ou Aluno da FCTE**
- **Sistema de Agenda FCTE**

---

### 3. Fluxo Básico de Eventos

**Início:** Usuário clica em **“Visualizar Eventos”**.

1. O sistema apresenta botão **Visualizar Eventos** na tela inicial.
2. O participante clica em **Visualizar Eventos**.
3. O sistema leva o usuário à uma nova tela mostrado um calendário do mês atual e sem nenhum outro filto aplicado.
4. Caso de uso encerrado.

---

### 4. Requisitos Especiais

1. Interface acessível (leitores de tela, alto contraste).

---

## Especificação de Caso de Uso: Buscar evento por nome, data e categorias

### 1. Breve Descrição

Permite ao usuário, logado ou não, só visualizar os eventos que atendem certos pré-requisitos.

---

### 2. Atores

- **Pessoa da Comunidade ou Aluno da FCTE**
- **Sistema de Agenda FCTE**

---

### 3. Fluxo Básico de Eventos

**Início:** Usuário está na tela com o calendário de eventos

1. O sistema apresenta os campos para escrever o nome do eventou ou selecionar a categoria do evento, além dele poder trocar o mês e ano do calendário visualizado.
2. O participante pode mudar os valores dos campos de nome e categorias.
3. Quando ele clica em um dos dias do calendário, o sistema exibe uma lista dos eventos desse dia na tela e os eventos devem respeitar os filtros selecionados.
4. Caso de uso encerrado.

---

### 4. Fluxos Alternativos

#### 4.1 FE01 – Usuário muda os filtros com dia no calendário selecionado

- **Quando:** Depois do passo 3.
- **Fluxo:**
  1. O usuário altera os campos de nome e categorias quando um dia já foi selecionado e já está sendo exibido na tela uma lista com os eventos de um dia
  2. O sistema deve atualizar a lista de eventos para só mostrar os eventos que respeitam os filtros definidos.
  3. Caso de uso encerrado.

---

### 5. Pré-Condições

1. Mês e ano escolhidos para mostrar o calendário

---

### 6. Requisitos Especiais

1. Interface acessível (leitores de tela, alto contraste).

---

## Referências Bibliográficas

> [<a id='ref1'>1</a>] JACOBSON, Ivar; CHRISTERSON, Magnus; JONSSON, Patrik; ÖVERGAARD, Gunnar. **Object-oriented software engineering: a use case driven approach**. New York; Wokingham, Eng.; Reading, Mass.: ACM Press; Addison-Wesley, 1992. Disponível em: <https://archive.org/details/ivar-jacobson-object-oriented-software-engineering-a-use-case-driven-approach-ac>. Acesso em: 19 abr. 2025.

> [<a id='ref2'>2</a>] SOMMERVILLE, Ian. _Software Engineering_. 9. ed. Boston: Addison-Wesley, 2011. Cap. 5: System Modelling. Disponível em: <https://archive.org/details/sommerville-ian-engenharia-de-software-2011>. Acesso em: 19 abr. 2025.

> [<a id='ref3'>3</a>] PRUITT, John; GRUDIN, Jonathan. _Personas, Participatory Design and Product Development: An Infrastructure for Engagement_. In: BINDER, Thomas; GREGORY, Judith; WAGNER, Ina (eds.). Proceedings of the Participatory Design Conference, 7., 23–25 jun. 2002, Malmö, Sweden. Palo Alto, CA: CPSR, 2002. p. 144–161. Disponível em: <https://ojs.ruc.dk/index.php/pdc/article/view/249/241>. Acesso em: 19 abr. 2025.

## Histórico de Versões

| Versão | Data       | Descrição                                                           | Autor                                                    | Revisor                                          | Comentário do Revisor           |
| ------ | ---------- | ------------------------------------------------------------------- | -------------------------------------------------------- | ------------------------------------------------ | ------------------------------- |
| `1.0`  | 17/04/2025 | Elaboração do esqueleto para entrega 2                              | [Thales Euflauzino](https://github.com/thaleseuflauzino) | [Víctor Schmidt](https://github.com/moonshinerd) | Aprovação do PR, ótimo trabalho |
| `1.1`  | 03/05/2025 | Introdução sobre especificação e inclusão de primeira especificação | [Maykon Soares](https://github.com/maykonjuso)           |                                                  |                                 |
| `1.2`  | 05/05/2025 | Inclusão de casos de uso "Adicionar Evento à Minha Agenda"          | [Maykon Soares](https://github.com/maykonjuso)           |                                                  |                                 |
| `1.3`  | 06/05/2025 | Inclusão de casos de uso "Emitir Certificado de Participação"       | [Maykon Soares](https://github.com/maykonjuso)           |                                                  |                                 |
| `1.4`  | 06/05/2025 | Inclusão de casos de uso "Buscar evento" e "Buscar evento por nome, data e categorias" | [Victório Lázaro](https://github.com/Victor-oss)           |                                                  |                                 |
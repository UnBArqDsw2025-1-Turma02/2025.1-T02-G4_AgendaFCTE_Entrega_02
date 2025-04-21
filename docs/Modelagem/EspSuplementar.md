# Especificação Suplementar

## Introdução

A Especificação Suplementar objetiva descrever requisitos adicionais do sistema da FCTE em linguagem natural, incluindo características relacionadas à usabilidade, confiabilidade, desempenho, capacidade de suporte e outras qualidades do produto. Ela complementa os Casos de Uso ao especificar pontos não abordados diretamente neles.

## Metodologia

O modelo adotado para definir os requisitos do sistema foi o **FURPS+**, que categoriza os requisitos em: Funcionalidade, Usabilidade, Confiabilidade, Desempenho e Suportabilidade.

## Definições da Especificação Suplementar

### 1. Funcionalidades

As funcionalidades principais do sistema estão descritas nos documentos de elicitação e Casos de Uso:

- [Elicitação de Requisitos](./Modelagem/requisitos.md)
- [Casos de Uso](./Modelagem/diagramaCasodeUso.md)

---

### 2. Usabilidade

**Tabela 1: Requisitos de usabilidade**

| Requisito | Código | Descrição |
|-----------|--------|-----------|
| [RNF01](https://unbarqdsw2025-1-turma02.github.io/2025.1-T02-_G4_AgendaFCTE_Entrega_01/#/./Modelagem/requisitos) | BRFN01, QS16, QS17, EN10, EN11 | O sistema deve possuir uma interface intuitiva, limpa e responsiva, adaptável a diferentes dispositivos móveis, tablets e desktops. |
| [RNF08](https://unbarqdsw2025-1-turma02.github.io/2025.1-T02-_G4_AgendaFCTE_Entrega_01/#/./Modelagem/requisitos) | BRFN08 | O sistema deve seguir diretrizes de acessibilidade, como as WCAG, permitindo o uso por pessoas com diferentes deficiências. |
| [RNF09](https://unbarqdsw2025-1-turma02.github.io/2025.1-T02-_G4_AgendaFCTE_Entrega_01/#/./Modelagem/requisitos) | QS19 | O sistema deve apresentar um design atrativo, moderno e alinhado com a identidade visual da FCTE. |

<font size="3"><p style="text-align: center">Autor:<a href="https://github.com/thaleseuflauzino">Thales Euflauzino</a>, 2025</p></font>

---

### 3. Confiabilidade

**Tabela 2: Requisitos de confiabilidade**

| Requisito | Código | Descrição |
|-----------|--------|-----------|
| [RNF03](https://unbarqdsw2025-1-turma02.github.io/2025.1-T02-_G4_AgendaFCTE_Entrega_01/#/./Modelagem/requisitos) | BRFN03 | O sistema deve garantir segurança robusta com autenticação e autorização adequadas, protegendo os dados dos usuários e das operações realizadas. |
| [RNF04](https://unbarqdsw2025-1-turma02.github.io/2025.1-T02-_G4_AgendaFCTE_Entrega_01/#/./Modelagem/requisitos) | BRFN04, EN12 | O sistema deve garantir a proteção dos dados pessoais dos usuários, estando em conformidade com a LGPD e utilizando criptografia quando necessário. |
| [RNF10](https://unbarqdsw2025-1-turma02.github.io/2025.1-T02-_G4_AgendaFCTE_Entrega_01/#/./Modelagem/requisitos) | QS21 | O sistema deve garantir a confiabilidade das informações exibidas. |

<font size="3"><p style="text-align: center">Autor:<a href="https://github.com/thaleseuflauzino">Thales Euflauzino</a>, 2025</p></font>

---

### 4. Suportabilidade

**Tabela 3: Requisitos de suportabilidade**

| Requisito | Código | Descrição |
|-----------|--------|-----------|
| [RNF05](https://unbarqdsw2025-1-turma02.github.io/2025.1-T02-_G4_AgendaFCTE_Entrega_01/#/./Modelagem/requisitos) | BRFN05, QS20 | O sistema deve ter código modular e bem documentado, permitindo fácil manutenção e futuras atualizações pelos organizadores. |
| [RNF06](https://unbarqdsw2025-1-turma02.github.io/2025.1-T02-_G4_AgendaFCTE_Entrega_01/#/./Modelagem/requisitos) | BRFN06 | O sistema deve implementar mecanismos de monitoramento e registro (logs) das atividades. |
| [RNF07](https://unbarqdsw2025-1-turma02.github.io/2025.1-T02-_G4_AgendaFCTE_Entrega_01/#/./Modelagem/requisitos) | BRFN07 | O sistema deve ser compatível com diversos navegadores e dispositivos, assegurando uma experiência consistente para todos os usuários. |

<font size="3"><p style="text-align: center">Autor:<a href="https://github.com/thaleseuflauzino">Thales Euflauzino</a>, 2025</p></font>

---

### 5. Performance

**Tabela 4: Requisitos de performance**

| Requisito | Código | Descrição |
|-----------|--------|-----------|
| [RNF02](https://unbarqdsw2025-1-turma02.github.io/2025.1-T02-_G4_AgendaFCTE_Entrega_01/#/./Modelagem/requisitos) | BRFN02, QS18, EN13 | O tempo de resposta para operações como busca, filtragem e carregamento de eventos deve ser de no máximo 4 segundos, mesmo com grande volume de dados. |
| [RNF11](https://unbarqdsw2025-1-turma02.github.io/2025.1-T02-_G4_AgendaFCTE_Entrega_01/#/./Modelagem/requisitos) | QS22 | O sistema deve ter boa escalabilidade, mantendo desempenho mesmo com aumento da demanda. |

<font size="3"><p style="text-align: center">Autor:<a href="https://github.com/thaleseuflauzino">Thales Euflauzino</a>, 2025</p></font>

---

### 6. Outros

**Tabela 5: Outros requisitos complementares**

| Requisito | Código | Descrição |
|-----------|--------|-----------|
| [RNF12](https://unbarqdsw2025-1-turma02.github.io/2025.1-T02-_G4_AgendaFCTE_Entrega_01/#/./Modelagem/requisitos) | QS23 | O sistema deve enviar notificações automáticas conforme a preferência configurada pelo usuário. |

<font size="3"><p style="text-align: center">Autor:<a href="https://github.com/thaleseuflauzino">Thales Euflauzino</a>, 2025</p></font>

## Bibliografia

> GAMBLE, S. Example: Supplementary Specification. [S. l.]: Pace University, 21 dez. 1998. Disponível em: https://csis.pace.edu/~marchese/SE616_New/Samples/Example%20%20Supplementary%20Specification.htm. Acesso em 21 de abril de 2025.
>
> SERRANO Milene; SERRANO Mauricio. Requisitos - Aula 13. Disponível na plataforma Aprender3. Acesso em 21 de abril de 2025.

## Histórico de Versões

| Versão | Data       | Descrição               | Autor                                             | Revisor                                                | Comentário do Revisor |
| ------ | ---------- | ----------------------- | ------------------------------------------------- | ------------------------------------------------------ | --------------------- |
| `1.0`    | 17/04/2025 | Elaboração do esqueleto para entrega 2    |[Thales Euflauzino](https://github.com/thaleseuflauzino) | [Víctor Schmidt](https://github.com/moonshinerd)  | Aprovação do PR, ótimo trabalho |
| `1.1`    | 21/04/2025 | Elaboração de todo o documento no modelo FURPS+    |[Thales Euflauzino](https://github.com/thaleseuflauzino) | [Víctor Schmidt](https://github.com/moonshinerd) | Artefato muito bem feito e ótimas referências, PR aprovado. |

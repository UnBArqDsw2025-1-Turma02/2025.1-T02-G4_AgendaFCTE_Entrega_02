## Introdução
O NFR Framework é uma abordagem para representar e analisar Requisitos Não-Funcionais (RNFs), que tem como objetivo implementar soluções específicas. Esse método leva em consideração as características gerais do sistema e de seu domínio. No contexto do NFR Framework, utiliza-se o modelo Softgoal Interdependency Graph (SIG).

## Softgoal Interdependency Graph

O [*Softgoal Interdependency Graph (SIG)*](#ref1) é uma ferramenta visual que ilustra como o NFR Framework opera. Ele apresenta, de forma gráfica e clara, as decisões tomadas pela equipe de desenvolvimento em relação aos softgoals e destaca as interdependências entre eles.

### Tipos de Softgoal

Para entender o *Softgoal Interdependency Graph (SIG)*, é fundamental compreender o conceito de  NFR Softgoal. Um *softgoal* refere-se a um objetivo que não possui definição precisa e cujos critérios de satisfação são vagos. Em outras palavras, trata-se de uma característica abstrata que pode ser analisada e avaliada posteriormente para determinar seu cumprimento. 

Os softgoals podem ser de diferentes tipos. Quando são *operacionalizados, assumem uma forma concreta, transformando-se em funcionalidades claras. Já os  softgoals de afirmação* são descritos em linguagem natural, servindo como registros adicionais e argumentativos que podem ser incorporados ao modelo. A Figura 1 ilustra os [diferentes tipos de softgoals.](#ref1)


<font size="3"><p style="text-align: center"><b>Figura 1</b> - Tipos de Softgoal</p></font>

<center>

![TIPOS](../assets/nfr/nfr_tipos.png)
</center>

<font size="3"><p style="text-align: center"> Fonte: [SILVA, 2019](#ref1)</p></font>

## Interdependências  
As interdependências representam as relações entre softgoals, que podem ser classificadas em decomposições e contribuições.
<font size="3"><p style="text-align: center"><b>Figura 2</b> - Tipos de Softgoal</p></font>

<center>

![DECOMPOSIÇÃO](../assets/nfr/nfr_decomp.png)
</center>

<font size="3"><p style="text-align: center">  Fonte: [SILVA, 2019](#ref1)</p></font>

### Decomposições  
As decomposições descrevem como um softgoal pode ser subdividido em outros, podendo ocorrer em diferentes níveis de abstração:  
1.  Softgoals de NFR (Requisitos Não Funcionais)   
2.  Softgoals de Operacionalização   
3.  Softgoals de Afirmação 

De acordo com [SILVA (2019)](#ref1), as decomposições ajudam a detalhar os softgoals em elementos mais específicos, reduzindo ambiguidades e facilitando a priorização. Os principais tipos são:  

-  Decomposição NFR:  Divide questões fundamentais em partes menores, auxiliando na priorização e clareza.  
-  Decomposição de Operacionalização:  Refina soluções amplas em alternativas mais específicas.  
-  Decomposição de Afirmação:  Fornece justificativas ou contraposições para decisões específicas.  
-  Decomposição de Priorização:  Um softgoal é refinado para outro do mesmo tipo e tópico, atribuindo uma prioridade específica.  

### Contribuições  
No  NFR Framework , as especializações de softgoals podem contribuir de maneira variada para outros softgoals: positiva ou negativa, total ou parcial. Os tipos de contribuições incluem:  

-  AND:  Todos os softgoals derivados devem ser satisfeitos para que o softgoal principal também seja.  
-  OR:  Basta que um dos softgoals derivados seja satisfeito para que o principal também o seja.  
-  MAKE (++):  Uma contribuição totalmente positiva, garantindo a satisfação do softgoal original.  
-  BREAK (--):  Uma contribuição totalmente negativa, levando à negação do softgoal original.  
-  HELP (+):  Contribuição parcialmente positiva, refletindo positivamente no softgoal original.  
-  HURT (-):  Contribuição parcialmente negativa, impactando de forma negativa o softgoal original.  
-  UNKNOWN (?):  Relação incerta ou indefinida.  
-  EQUALS:  Indica que as satisfações do softgoal derivado e do principal são idênticas.  
-  SOME:  A contribuição é conhecida, mas sua intensidade é desconhecida.  

### Propagação de Impactos  
A propagação de impactos no  NFR Framework  considera como mudanças em um requisito não funcional podem afetar outros requisitos relacionados. Para isso, é essencial identificar dependências e compreender as interações entre os requisitos, avaliando prioridades e possíveis compromissos (trade-offs).  

As diferentes formas de impacto são:  
-  ✓ (Satisfeito):  O requisito contribui positivamente para outro.  
-  𝒲+ (Fracamente satisfeito):  A relação é positiva, mas menos intensa.  
-  X (Negado):  O requisito impacta negativamente outro, impossibilitando sua realização.  
-  𝒲- (Fracamente negado):  Relação negativa, mas com menor intensidade.  
-  🗲 (Conflitante):  Existe conflito, com impactos positivos e negativos simultâneos.  
-  u (Indeterminado):  Relação desconhecida devido à falta de informações.  

Compreender essas interdependências e seus impactos é crucial para tomar decisões informadas e gerenciar os efeitos colaterais de mudanças nos requisitos.

## Metodologia
Neste documento, serão apresentados 3 NFRs, com requisitos vindo dos [requisitos elicitados não funcionais](https://unbarqdsw2025-1-turma02.github.io/2025.1-T02-G4_AgendaFCTE_Entrega_02/#/./Modelagem/requisitos?id=rnf1). Para cada categoria, foi feito um SIG (Softgoal Interdependency Graph), um diagrama da propagação de impactos e um cartão de especificação, que possui informações sobre o NFR, como a descrição, a categoria, os conflitos, a origem, os critérios e outras informações. 


## NFR 01 - Desempenho

<font size="3"><p style="text-align: center"><b>Figura 3</b> - NFR de Desempenho</p></font>

<center>

![Desempenho](../assets/nfr/nfr_desempenho.png)
</center>

<font size="2"><p style="text-align: center"> Autores: [Pedro Lopes](https://github.com/pLopess) e [Victor Hugo](https://github.com/VHbernardes)</p></font>


###  Impactos Desempenho 

<font size="3"><p style="text-align: center"><b>Tabela 1</b>: Impactos Desempenho</p></font>

<div style="display: flex; justify-content: center;">
  <table>
    <thead>
      <tr>
        <th><strong>NFR</strong></th>
        <th><strong>Impacto</strong></th>
        <th><strong>Avaliador</strong></th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>Desempenho</td>
        <td>✓</td>
        <td><a href="https://github.com/pLopess">Pedro Lopes</a></td>
      </tr>
      <tr>
        <td>Rapidez</td>
        <td>𝒲+</td>
        <td><a href="https://github.com/pLopess">Pedro Lopes</a></td>
      </tr>
      <tr>
        <td>Resposta em 4ms</td>
        <td>✓</td>
        <td><a href="https://github.com/pLopess">Pedro Lopes</a></td>
      </tr>
      <tr>
        <td>Manutenibilidade</td>
        <td>𝒲+</td>
        <td><a href="https://github.com/pLopess">Pedro Lopes</a></td>
      </tr>
      <tr>
        <td>Código Modular</td>
        <td>𝒲−</td>
        <td><a href="https://github.com/pLopess">Pedro Lopes</a></td>
      </tr>
      <tr>
        <td>Código bem documentado</td>
        <td>𝒲+</td>
        <td><a href="https://github.com/pLopess">Pedro Lopes</a></td>
      </tr>
      <tr>
        <td>Escalabilidade</td>
        <td>𝒲+</td>
        <td><a href="https://github.com/pLopess">Pedro Lopes</a></td>
      </tr>
      <tr>
        <td>Manter desempenho em alta demanda</td>
        <td>✓</td>
        <td><a href="https://github.com/pLopess">Pedro Lopes</a></td>
      </tr>
    </tbody>
  </table>
</div>

<font size="2"><p style="text-align: center"> Autores: [Pedro Lopes](https://github.com/pLopess) e [Victor Hugo](https://github.com/VHbernardes)</p></font>


### Cartão de Especificação - Desempenho

<font size="3"><p style="text-align: center"><b>Tabela 2</b>: Cartão de Especificação - Desempenho</p></font>


| **ID do NFR**     | **Classificação: Desempenho**                                         |
|-------------------|------------------------------------------------------------------------|
| **Descrição:**    | Refere-se à capacidade do sistema de entregar respostas rápidas, com manutenção facilitada e desempenho consistente mesmo sob alta demanda. |
| **Justificativa:**| Um sistema com bom desempenho melhora a experiência do usuário, facilita a manutenção e garante escalabilidade sem degradação perceptível. |
| **Origem dos Requisitos:** | Os requisitos [RNF02](https://unbarqdsw2025-1-turma02.github.io/2025.1-T02-G4_AgendaFCTE_Entrega_02/#/./Modelagem/requisitos?id=rnf2), [RNF05](https://unbarqdsw2025-1-turma02.github.io/2025.1-T02-G4_AgendaFCTE_Entrega_02/#/./Modelagem/requisitos?id=rnf5) e [RNF11](https://unbarqdsw2025-1-turma02.github.io/2025.1-T02-G4_AgendaFCTE_Entrega_02/#/./Modelagem/requisitos?id=rnf11).                        |
| **Dependências:** | - |
| **Prioridade:**   | Alta                                                                  |
| **Conflitos:**    | Potencial conflito entre modularidade e desempenho (trade-off entre RNF05 e RNF02). |

<font size="2"><p style="text-align: center"> Autores: [Pedro Lopes](https://github.com/pLopess) e [Victor Hugo](https://github.com/VHbernardes)</p></font>


## NFR 02 - Segurança

<font size="3"><p style="text-align: center"><b>Figura 4</b> - NFR de Segurança</p></font>

<center>

![Segurança](../assets/nfr/nfr_seguranca.png)
</center>

<font size="2"><p style="text-align: center"> Autores: [Pedro Lopes](https://github.com/pLopess) e [Victor Hugo](https://github.com/VHbernardes)</p></font>

###  Impactos Segurança 

<font size="3"><p style="text-align: center"><b>Tabela 3</b>: Impactos Segurança </p></font>

<div style="display: flex; justify-content: center;">
  <table>
    <thead>
      <tr>
        <th><strong>NFR</strong></th>
        <th><strong>Impacto</strong></th>
        <th><strong>Avaliador</strong></th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>Segurança</td>
        <td>✓</td>
        <td><a href="https://github.com/pLopess">Pedro Lopes</a></td>
      </tr>
      <tr>
        <td>Proteção aos Usuários</td>
        <td>𝒲+</td>
        <td><a href="https://github.com/pLopess">Pedro Lopes</a></td>
      </tr>
      <tr>
        <td>Conformidade com a LGPD</td>
        <td>𝒲+</td>
        <td><a href="https://github.com/pLopess">Pedro Lopes</a></td>
      </tr>
      <tr>
        <td>Uso de Criptografia</td>
        <td>𝒲+</td>
        <td><a href="https://github.com/pLopess">Pedro Lopes</a></td>
      </tr>
      <tr>
        <td>Autenticação e Autorização</td>
        <td>𝒲+</td>
        <td><a href="https://github.com/pLopess">Pedro Lopes</a></td>
      </tr>
      <tr>
        <td>Informações</td>
        <td>𝒲+</td>
        <td><a href="https://github.com/pLopess">Pedro Lopes</a></td>
      </tr>
      <tr>
        <td>Confiabilidade dos dados exibidos</td>
        <td>✓</td>
        <td><a href="https://github.com/pLopess">Pedro Lopes</a></td>
      </tr>
      <tr>
        <td>Controle</td>
        <td>𝒲+</td>
        <td><a href="https://github.com/pLopess">Pedro Lopes</a></td>
      </tr>
      <tr>
        <td>Monitoramento e logs</td>
        <td>✓</td>
        <td><a href="https://github.com/pLopess">Pedro Lopes</a></td>
      </tr>
    </tbody>
  </table>
</div>


<font size="2"><p style="text-align: center"> Autores: [Pedro Lopes](https://github.com/pLopess) e [Victor Hugo](https://github.com/VHbernardes)</p></font>


### Cartão de Especificação - Segurança

<font size="3"><p style="text-align: center"><b>Tabela 4</b>: Cartão de Especificação - Segurança </p></font>


| **ID do NFR**     | **Classificação: Segurança**                                           |
|-------------------|------------------------------------------------------------------------|
| **Descrição:**    | Refere-se à capacidade do sistema de proteger usuários e informações por meio de controle de acesso, conformidade legal e mecanismos de rastreabilidade. |
| **Justificativa:**| Um sistema seguro preserva a integridade, confidencialidade e rastreabilidade dos dados, além de proteger os usuários e a organização contra riscos legais e operacionais. |
| **Origem dos Requisitos:** | Os requisitos [RNF03](https://unbarqdsw2025-1-turma02.github.io/2025.1-T02-G4_AgendaFCTE_Entrega_02/#/./Modelagem/requisitos?id=rnf3), [RNF04](https://unbarqdsw2025-1-turma02.github.io/2025.1-T02-G4_AgendaFCTE_Entrega_02/#/./Modelagem/requisitos?id=rnf4), [RNF06](https://unbarqdsw2025-1-turma02.github.io/2025.1-T02-G4_AgendaFCTE_Entrega_02/#/./Modelagem/requisitos?id=rnf6) e [RNF10](https://unbarqdsw2025-1-turma02.github.io/2025.1-T02-G4_AgendaFCTE_Entrega_02/#/./Modelagem/requisitos?id=rnf10).               |
| **Dependências:** | - |
| **Prioridade:**   | Alta                                                                  |
| **Conflitos:**    | Nenhum identificado.                                                   |

<font size="2"><p style="text-align: center"> Autores: [Pedro Lopes](https://github.com/pLopess) e [Victor Hugo](https://github.com/VHbernardes)</p></font>

## NFR 03 - Usabilidade

<font size="3"><p style="text-align: center"><b>Figura 5</b> - NFR de Usabilidade </p></font>

<center>

![Usabilidade](../assets/nfr/nfr_usabilidade.png)
</center>

<font size="2"><p style="text-align: center"> Autores: [Pedro Lopes](https://github.com/pLopess) e [Victor Hugo](https://github.com/VHbernardes)</p></font>

### Impactos Usabilidade 

<font size="3"><p style="text-align: center"><b>Tabela 5</b>: Impactos Usabilidade </p></font>

<div style="display: flex; justify-content: center;">
  <table>
    <thead>
      <tr>
        <th><strong>NFR</strong></th>
        <th><strong>Impacto</strong></th>
        <th><strong>Avaliador</strong></th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>Interface do usuário</td>
        <td>𝒲+</td>
        <td><a href="https://github.com/VHbernardes">Victor Bernardes</a></td>
      </tr>
      <tr>
        <td>Acessibilidade</td>
        <td>𝒲+</td>
        <td><a href="https://github.com/VHbernardes">Victor Bernardes</a></td>
      </tr>
      <tr>
        <td>Experiência do usuário</td>
        <td>𝒲+</td>
        <td><a href="https://github.com/VHbernardes">Victor Bernardes</a></td>
      </tr>
      <tr>
        <td>Intuitiva</td>
        <td>✓</td>
        <td><a href="https://github.com/VHbernardes">Victor Bernardes</a></td>
      </tr>
      <tr>
        <td>Limpa</td>
        <td>✓</td>
        <td><a href="https://github.com/VHbernardes">Victor Bernardes</a></td>
      </tr>
      <tr>
        <td>Responsiva</td>
        <td>✓</td>
        <td><a href="https://github.com/VHbernardes">Victor Bernardes</a></td>
      </tr>
      <tr>
        <td>Design atrativo alinhado à identidade visual</td>
        <td>𝒲+</td>
        <td><a href="https://github.com/VHbernardes">Victor Bernardes</a></td>
      </tr>
      <tr>
        <td>Diretrizes WCAG</td>
        <td>✓</td>
        <td><a href="https://github.com/VHbernardes">Victor Bernardes</a></td>
      </tr>
      <tr>
        <td>Notificações conforme preferências</td>
        <td>𝒲+</td>
        <td><a href="https://github.com/VHbernardes">Victor Bernardes</a></td>
      </tr>
    </tbody>
  </table>
</div>

<font size="2"><p style="text-align: center"> Autores: [Pedro Lopes](https://github.com/pLopess) e [Victor Hugo](https://github.com/VHbernardes)</p></font>

### Cartão de Especificação - Usabilidade

<font size="3"><p style="text-align: center"><b>Tabela 6</b>: Cartão de Especificação - Usabilidade </p></font>


| **ID do NFR**     | **Classificação: Usabilidade**                                           |
|-------------------|--------------------------------------------------------------------------|
| **Descrição:**    | Refere-se à facilidade com que os usuários podem interagir com o sistema de forma intuitiva, acessível e satisfatória. Envolve aspectos como design limpo, responsividade, aderência a diretrizes de acessibilidade e experiência geral do usuário.                                     |
| **Justificativa:**| Um sistema com boa usabilidade melhora a adoção pelos usuários, reduz erros, aumenta a eficiência e promove uma experiência positiva, além de atender a normas de acessibilidade. |
| **Origem dos Requisitos:** | Os requisitos [RNF01](https://unbarqdsw2025-1-turma02.github.io/2025.1-T02-G4_AgendaFCTE_Entrega_02/#/./Modelagem/requisitos?id=rnf1), [RNF08](https://unbarqdsw2025-1-turma02.github.io/2025.1-T02-G4_AgendaFCTE_Entrega_02/#/./Modelagem/requisitos?id=rnf8), [RNF09](https://unbarqdsw2025-1-turma02.github.io/2025.1-T02-G4_AgendaFCTE_Entrega_02/#/./Modelagem/requisitos?id=rnf9) e [RNF12](https://unbarqdsw2025-1-turma02.github.io/2025.1-T02-G4_AgendaFCTE_Entrega_02/#/./Modelagem/requisitos?id=rnf12). |
| **Dependências:** | -                                                                           |
| **Prioridade:**   |Alta                                                                         |
| **Conflitos:**    | Nenhum identificado.                                                        |

<font size="2"><p style="text-align: center"> Autores: [Pedro Lopes](https://github.com/pLopess) e [Victor Hugo](https://github.com/VHbernardes)</p></font>

## Referências Bibliográficas

> [<a id='ref1'>1</a>] SILVA, Reinaldo Antônio. NFR4ES: Um Catálogo de Requisitos Não-Funcionais para Sistemas Embarcados. Centro de Informática UFPE, Recife, 2019. Disponível em: <https://repositorio.ufpe.br/handle/123456789/34150>. Acesso em: 22/05/2023.

> SERRANO, Milene. Requisitos – Aula 17. 2017. Apresentação de slides. Disponível em: [https://aprender3.unb.br/pluginfile.php/2972516/mod_resource/content/1/Requisitos%20-%20Aula%20019a.pdf](https://aprender3.unb.br/pluginfile.php/2972516/mod_resource/content/1/Requisitos%20-%20Aula%20019a.pdf). Acesso em: 16 de Dez. 2024.

> NFR Framework. Repositório da disciplina de Requisitos de Software da Universidade de Brasília, 2023. Disponível em: [https://requisitos-de-software.github.io/2023.1-BilheteriaDigital/modelagem/agil/nfrframework/](https://requisitos-de-software.github.io/2023.1-BilheteriaDigital/modelagem/agil/nfrframework/). Acesso em: 16 de Dez. 2024.

## Histórico de Versões

| Versão | Data       | Descrição               | Autor                                             | Revisor                                                | Comentário do Revisor |
| ------ | ---------- | ----------------------- | ------------------------------------------------- | ------------------------------------------------------ | --------------------- |
| `1.0`    | 17/04/2025 | Elaboração do esqueleto para entrega 2    |[Thales Euflauzino](https://github.com/thaleseuflauzino) | [Víctor Schmidt](https://github.com/moonshinerd)  | |
| `1.1`    | 07/05/2025 | Adição dos tipos de Softgoal, contribuições e impactos |[Victor Bernardes](https://github.com/VHbernardes) | [Pedro Lopes](https://github.com/pLopess) | Ótimo conteúdo |
| `1.2`    | 07/05/2025 | Adição dos NFR de Desempenho e Segurança, tabelas de impactos e cartões de especificação |[Pedro Lopes](https://github.com/pLopess) | [Manoela Garcia](https://github.com/manu-sgc) | Ótimo trabalho!! |
| `1.3`    | 07/05/2025 | Adição do NFR de Usabilidade, tabela de impacto e cartão de especificação |[Victor Bernardes](https://github.com/VHbernardes) | [Manoela Garcia](https://github.com/manu-sgc) | Muito bom!!! Aprovação do PR |
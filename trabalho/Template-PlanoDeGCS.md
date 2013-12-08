<SISACAD>
=================
Plano de Gerenciamento de Configuração
======================================
Versão 1.0
------------------

Histórico de Versões
--------------------

|Data                |Versão       |Descrição               |Autor          |
|--------------------|-------------|------------------------|---------------|
|04/12/2013|1.0|Versão inicial|Jackson Uchoa|
|_&lt;dd/mm/aaaa&gt;_|_&lt;1.1&gt;_|_&lt;Outra versão&gt;_  |_&lt;autor&gt;_|



1. Introdução
==============

O Plano de Gerenciamento de Configuração descreve todas as atividades do Gerenciamento de Controle de Configuração e Mudança que serão executadas durante o ciclo de vida do produto. Suas atividades envolvem identificar a configuração do software, manter sua integridade durante o projeto e controlar sistematicamente as mudanças.

1.1 Finalidade
---------------
A finalidade deste documento é criar um padrão a ser seguido por todos os membros da equipe com o intuito de garantir o maior controle do produto no decorrer do projeto. 

Para que isso aconteça serão detalhados os recursos necessários (equipes, ferramentas e computadores), as responsabilidades atribuídas e o cronograma de atividades.

1.2 Escopo
----------
Este Plano de Gerenciamento de Configuração é destinado para todos os integrantes da equipe responsável pelo desenvolvimento do sistema SISACAD, e abrange todo o controle e gerenciamento da configuração do projeto SISACAD – Sistema Acadêmico. 

1.3 Definições, Acrônimos e Abreviações
---------------------------------------
| Termo        | Significado            |
| ------------- |:---------------------:|
| SCRUM      | É um processo ágil que permite manter o foco na entrega do maior valor de negócio, no menor tempo possível. |
| GC      | Gerência de Configuração      |
| CCM | Comitê para o Controle de Mudanças.      |
| RH | Recursos Humanos      |
| Baseline | Conjunto de itens de configuração que conseguiram um estado comprovado de estabilidade.      |

1.4 Referências
---------------
_[Esta subseção apresenta uma lista completa de todos os documentos mencionados no Plano de Gerenciamento de Configuração. Identifique os documentos por título, número de relatório (se aplicável), data e organização responsável pela publicação. Especifique as fontes a partir das quais as referências podem ser obtidas. Essas informações podem ser fornecidas por um anexo ou outro documento.]_

1.5 Visão Geral
---------------
As próximas seções deste documento estão divididas conforme a tabela abaixo.

| Seção        | Descrição            |
| ------------- |:---------------------:|
| 2 | São relacionados os papéis, as responsabilidades das atividades e as ferramentas dentro da GC da Fábrica. |
| 3 | É apresentado como serão criadas e controladas as Baselines. |
| 4 | São abordados os detalhes sobre quando o Plano de Gerenciamento de Configuração deve ser atualizado. |
| 5 | Descreve as ferramentas de software, o pessoal e o treinamento necessários para implementar as atividades de CM especificadas. |
| 6 | Descreve de que forma o software desenvolvido fora do ambiente do projeto será incorporado. |



2. Gerenciamento de Configuração de Software
============================================

2.1 Organização, Responsabilidades e Interfaces
------------------------------------------------
| Seção        | Descrição            | Responsabilidade        |
| ------------- |:---------------------:|:----------------:
| Gerente de configuração | Jackson Uchoa | Estabelecer Políticas de GC, Escrever Plano de GC, Configurar Ambiente de GC, Criar Espaços de Trabalho de Integração, Criar Baselines, Promover Baselines |
| Comitê de Controle de Mudanças | Jackson Uchoa, Yago Melo | Estabelecer Processo de Controle de Mudanças, Revisar Solicitação de Mudança |
| Desenvolvedor | Yago Melo | Seguir os padrões e procedimentos definidos no Plano de Gerência de Configuração |
| Permissões Gerais | Jackson Uchoa, Yago Melo | Enviar Solicitação de Mudança, Atualizar Solicitação de Mudança |

2.2 Ferramentas, Ambiente e Infra-estrutura
-------------------------------------------
| Ferramenta        | Tipo            | Descrição        | Versão    |
| ------------- |:---------------------:|:----------------:|:------------:
| Github.com |  | Projeto de hospedagem que permite o controle de versão de artefatos |  |
| Git | Controle de Versão | Sistema de controle de versão. | 1.8.5.1 |
| Jira | Gestão de projetos e defeitos | Ferramenta para controle de atividades e defeitos. | 6.1 |
| JUnit | Gestão de testes unitários | Ferramenta para manutenção de testes unitários. | 4.0 |
| Maven | Integração Continua | Ferramenta para controle continuo do código desenvolvido | 2 |
 


3. O Programa de Gerenciamento de Configuração
==============================================

3.1 Identificação da Configuração
---------------------------------
### 3.1.1 Métodos de Identificação
----------------------------------

<b> [ SISACAD ][ AAA ][ TextoLivre ].[ EXT ]  Ou  [ SISACAD ][ AA ][ TextoLivre ].[ EXT ] </b>

| Parte da Linha      | Descrição        |
| ------------- |:---------------------:|
| [ SISACAD ] | Identifica o sistema. “SISACAD - Sistema de Controle Acadêmico” |
| [ AAA ] / [ AA ] | Significa o acrônimo de três letras (TLA) dos vários tipos de artefatos utilizados na criação do sistema. |
| [ TextoLivre ] | Significa texto Livre para a melhor identificação do documento.  |
| [ EXT ] | Extensão do arquivo do documento. |

Exemplo: <b>SISACADMCUUC0001-ManterAlunos.doc</b> – Modelo de caso de manter Alunos

### 3.1.2 Itens de Configuração
_[Relacionar os artefatos ou grupos de artefatos, separando por tipo, modulo ou subsistema, responsável ou momento em que deverão ser incluídos em baselines._
* _“Inclusão em Baseline” em branco significa que o grupo de artefatos não participará de baseline. Pode ser expresso como uma data ou identificador de uma baseline, fase ou ponto de controle_
* _“Responsável”: indicar nominalmente, sempre que possível]_

| Item (ou Tipo de Item)                 | Responsável na equipe	     | Inclusão em Baseline |
|----------------------------------------|-----------------------------|----------------------|
|_&lt;grupo de itens de configuração&gt;_|_&lt;nome do responsável&gt;_|_&lt;momento a partir do qual o conjunto de artefatos será incluído em baseline&gt;_|


### 3.1.3 Baselines do Projeto

_[As baselines funcionam como um padrão oficial no qual os trabalhos subseqüentes são baseados. Somente mudanças autorizadas podem ser efetuadas nas baselines._
_Descreva em que pontos do ciclo de vida do projeto ou produto as baselines devem ser estabelecidas. As baselines mais comuns devem ser definidas ao final de cada uma das fases de Iniciação, Elaboração, Construção e Transição. Elas também podem ser geradas no final de iterações ocorridas dentro das várias fases ou com freqüência ainda maior._
_Descreva quem autoriza uma baseline e o que ela contém.]_

### 3.1.4 Estrutura do Repositório de Versões
_[Descreva a organização de diretórios do seu repositório e que itens/arquivos devem ser armazenados em cada diretório.]_

3.2 Controle de Configuração e Mudança
--------------------------------------

### 3.2.1 Processamento e Aprovação de Solicitações de Mudança
_[Descreva o processo pelo qual os problemas e as mudanças são submetidos, revisados e dispostos. Inclua como funciona a transição de estados de uma solicitação de mudança]_

### 3.2.2 Comitê de Controle de Mudança (CCB)
_[Descreva a participação e os procedimentos para processar solicitações e aprovações de mudança a serem seguidos pelo CCB. Informe quem são os membros do CCB e suas responsabilidades.]_



4. Padrões e Procedimentos
==========================
_[Descreva os padrões e procedimentos que devem ser seguidos no projeto. Crie subseções se achar necessário, para organizá-los melhor.]_



5. Treinamento e Recursos
=========================
_[Descreva as ferramentas de software, o pessoal e o treinamento necessários para implementar as atividades de CM especificadas.]_



6. Auditorias de Configuração
=============================
_[Descreva o cronograma das auditorias de configuração e o que será verificado. Informe também como serão reportados os problemas encontrados e onde sera feito o acompanhamento dos itens corretivos.]_

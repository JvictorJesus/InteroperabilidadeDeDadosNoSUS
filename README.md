# Desafios para Integração da interoperabilidade nos sistemas de Saúde Publica

## Integrantes
João Victor de Jesus Silva | [GitHub](https://github.com/JvictorJesus) | Engenharia de Dados | 48134872  
Integrante (ordem alfabética) | GitHub | Área de carreira | RGM  
Integrante (ordem alfabética) | GitHub | Área de carreira | RGM  
Integrante (ordem alfabética) | GitHub | Área de carreira | RGM  
Integrante (ordem alfabética) | GitHub | Área de carreira | RGM  

**Dossiê:** Nº6 Interoperabilidade de dados no SUS  
**Recorte:** Usuários do SUS no Brasil que dependem exclusivamente da rede pública e sofrem prejuízo pela falta de acesso às próprias informações de saúde (histórico, exames, tratamentos e etc). Essa população é a mais afetada pela fragmentação dos sistemas, e tem menor capacidade de contornar o problema por meios privados.

## 1. Análise do problema
**1.1 Quem é afetado, onde e quando?**

A falta de interoperabilidade afeta pacientes, profissionais e instituições de saúde, tanto públicas quanto privadas.

O problema ocorre quando o paciente transita entre diferentes estabelecimentos e seus dados clínicos não estão disponíveis para consulta. Isso pode acontecer entre unidades do próprio SUS ou na transição entre serviços públicos e privados.

Os principais prejudicados são os pacientes que dependem de diferentes instituições para consultas, exames e tratamentos, especialmente quando não conseguem disponibilizar seu histórico médico de maneira integrada.

**1.2 Quais são as causas tecnológicas?**

- Acesso restrito: a consulta e o compartilhamento de informações na RNDS dependem de autenticação, autorização e permissões específicas. Esse processo pode limitar a disponibilidade dos dados entre instituições.  
- Fragmentação dos sistemas: diferentes estabelecimentos utilizam softwares e padrões de armazenamento que nem sempre conseguem se comunicar.  
- Integração incompleta: nem todas as instituições públicas e privadas estão efetivamente conectadas à rede, dificultando a distribuição das informações.  
- Dependência de infraestrutura: unidades sem equipamentos, conexão ou profissionais especializados enfrentam dificuldades para registrar e compartilhar informações.  
- Limitações de acesso institucional: mesmo quando os dados existem, isso não significa que estejam disponíveis para consulta nos sistemas utilizados pelos profissionais de saúde.

**1.3. O que já existe e por que não basta?**

O Brasil possui a Rede Nacional de Dados em Saúde (RNDS), responsável por integrar e compartilhar informações clínicas, e o Meu SUS Digital, que permite aos cidadãos consultar e administrar informações disponibilizadas em seu histórico.

Entretanto, essas iniciativas ainda enfrentam limitações de integração e distribuição. A existência de uma rede nacional não garante que todos os estabelecimentos estejam conectados ou consigam consultar as informações necessárias.

Além disso, a necessidade de autorizações e processos de acesso pode dificultar o compartilhamento entre instituições, principalmente na relação entre serviços públicos e privados.

A falta de interoperabilidade gera consequências práticas:  
- Repetição desnecessária de exames já realizados.
- Atrasos no atendimento devido à ausência de informações.
- Risco de diagnósticos incorretos ou incompletos.
- Descontinuidade de tratamentos por falta de histórico clínico.
- Maior dificuldade para acompanhar a evolução do paciente.

## 2. Proposta tecnológica
**2.1 A solução do ponto de vista do usuário**

A solução proposta consiste em ampliar e facilitar o acesso às informações da Rede Nacional de Dados em Saúde (RNDS), responsável por integrar e compartilhar informações clínicas, utilizando o Meu SUS Digital como uma das principais ferramentas de acesso para os cidadãos.

Atualmente, essas informações ainda são pouco conhecidas pela população e, muitas vezes, não são devidamente disponibilizadas ou aproveitadas pelas instituições de saúde. Além de promover a conscientização dos pacientes sobre a existência dessa rede, a proposta busca facilitar o acesso às informações clínicas, permitindo que pacientes e profissionais de saúde consultem um histórico mais completo e integrado.

Mesmo dentro do próprio SUS, existem situações em que exames são repetidos por falta de consulta aos registros anteriores, prolongando tratamentos e aumentando o sofrimento dos pacientes.

A proposta de aprimoramento desse fluxo consiste nas seguintes etapas:

1. Disponibilização de informações pelo paciente: o cidadão poderá consultar suas informações de saúde no Meu SUS Digital e disponibilizar documentos complementares, como exames realizados em instituições que ainda não estejam integradas à rede.  
2. Acesso dos profissionais de saúde: médicos e demais profissionais autorizados deverão ter acesso facilitado ao histórico clínico dos pacientes, permitindo consultar informações anteriores e registrar novos atendimentos.  
3. Conscientização da população: promover gradualmente o conhecimento sobre a existência e utilização da RNDS e do Meu SUS Digital, incentivando os cidadãos a acompanharem suas próprias informações de saúde.  
4. Integração com instituições privadas: ampliar a integração dos sistemas de hospitais, clínicas e laboratórios particulares à rede nacional, reduzindo obstáculos técnicos e operacionais ao compartilhamento de informações.  
5. Acompanhamento integrado: permitir que pacientes e profissionais autorizados acompanhem as informações clínicas disponíveis de maneira centralizada e acessível, contribuindo para a continuidade dos tratamentos.  

**2.2 Arquitetura**

A arquitetura proposta [Mermaid](https://mermaid.ai/app/projects/7c60d26e-5e11-40ba-8f77-b6224b6bc216/diagrams/d2c570b7-29bb-4bac-bb1a-8d4cc405d437/share/invite/eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkb2N1bWVudElEIjoiZDJjNTcwYjctMjliYi00YmFjLWJiMWEtOGQ0Y2M0MDVkNDM3IiwiYWNjZXNzIjoiVmlldyIsInB1cnBvc2UiOiJzaGFyZS1pbnZpdGUiLCJpYXQiOjE3OTQxNjA0NzEsImV4cCI6MTc5Njc1MjQ3MX0.iMt04q4yDiLnCc6v_QUOPW0IbmHnRW808ivMWgxoXQg?entryPoint=share-modal) representa o fluxo de informações entre pacientes, instituições públicas e privadas e a Rede Nacional de Dados em Saúde.

Os dados são produzidos durante consultas, exames e tratamentos, enviados pelos sistemas das instituições integradas e disponibilizados na RNDS. Os pacientes podem consultar suas informações pelo Meu SUS Digital, enquanto os profissionais autorizados podem acessá-las conforme suas permissões.

Quando uma instituição ainda não estiver integrada, o paciente poderá disponibilizar documentos complementares para auxiliar o atendimento, sem substituir a validação e o registro oficial pelos profissionais responsáveis.

**2.3 O trabalho de cada área do grupo e como se complementam**

- **Engenharia de Dados:** responsável pela coleta, organização, integração e orquestração dos dados necessários ao funcionamento do sistema. Também atua na preparação das informações para estatísticas, análises e pesquisas.

- **Ciência de Dados:** responsável por analisar e correlacionar os dados coletados, identificando padrões, inconsistências e possíveis problemas. Pode contribuir com estudos que auxiliem na identificação de gargalos e oportunidades de melhoria no atendimento.

- **Cloud Computing:** responsável pela infraestrutura de armazenamento e processamento em nuvem, garantindo disponibilidade, escalabilidade e capacidade de processamento das informações.

- **Cibersegurança:** uma das áreas mais importantes, considerando a sensibilidade das informações médicas e dos dados pessoais dos pacientes e profissionais. Atua na proteção dos dados, controle de acesso, prevenção de invasões e garantia da confidencialidade e integridade das informações.

- **Redes:** responsável por estabelecer e manter a comunicação entre os sistemas envolvidos, garantindo a conectividade e a transmissão das informações entre a RNDS e as instituições públicas e privadas.

Integração entre as áreas: enquanto Engenharia de Dados organiza e prepara as informações, Ciência de Dados analisa seu conteúdo. Cloud Computing fornece a infraestrutura necessária para armazená-las e processá-las, Cibersegurança protege os dados e Redes garante a comunicação entre os diferentes sistemas. Dessa forma, todas as áreas trabalham em conjunto para garantir o funcionamento de uma estrutura integrada e segura.

**2.4 O que a tecnologia não resolve**

Embora a tecnologia possa contribuir para melhorar a eficiência do SUS, existem problemas estruturais que não podem ser solucionados exclusivamente por ferramentas tecnológicas ou inteligência artificial.

1. Subfinanciamento
Problema: recursos financeiros insuficientes, distribuição inadequada do orçamento e defasagem na remuneração de procedimentos médicos, comprometendo a capacidade de atendimento e manutenção dos serviços.  
Limitação tecnológica: ferramentas digitais podem auxiliar no controle e na análise da distribuição dos recursos, mas não conseguem solucionar a insuficiência de investimentos financeiros ou substituir decisões políticas e orçamentárias.

2. Longas filas de espera
Problema: demora excessiva para conseguir consultas com especialistas, realizar exames e passar por cirurgias, prejudicando o diagnóstico e o início dos tratamentos.  
Limitação tecnológica: sistemas inteligentes podem auxiliar na organização das filas, priorização de casos e otimização dos agendamentos, mas não resolvem a falta de profissionais, especialistas e capacidade de atendimento.

3. Má gestão e falhas administrativas
Problema: distribuição inadequada de recursos, falhas logísticas, dificuldade no controle de medicamentos e falta de integração entre os diferentes níveis de gestão do SUS.  
Limitação tecnológica: sistemas informatizados podem melhorar o controle e a transparência administrativa, mas não substituem uma gestão eficiente, planejamento adequado e decisões administrativas responsáveis.

4. Falta de leitos e superlotação
Problema: quantidade insuficiente de leitos em hospitais e unidades de emergência, dificultando o atendimento, principalmente durante epidemias e períodos de aumento da demanda.  
Limitação tecnológica: ferramentas de monitoramento podem auxiliar no acompanhamento da ocupação e na organização dos encaminhamentos, mas não criam novos leitos, hospitais ou ampliam a capacidade física das unidades.

5. Falta de medicamentos
Problema: indisponibilidade periódica de medicamentos essenciais nas Unidades Básicas de Saúde, prejudicando a continuidade dos tratamentos dos pacientes.  
Limitação tecnológica: sistemas de controle e inteligência artificial podem auxiliar na previsão da demanda e no gerenciamento dos estoques, mas não resolvem problemas de aquisição, financiamento, fabricação e distribuição de medicamentos.

## 3. Análise ética
3.1 Matriz de riscos (mínimo 5 riscos)  
3.2 Decisão (implantar / com controles / não implantar ainda) + justificativa ≤ 10 linhas  
3.3 Controles antes de produção (mínimo 6, cobrindo: transparência, revisão humana, minimização de dados, segurança, teste de viés, canal de contestação)  
3.4 LGPD (tabela de dados pessoais)  
3.5 Comunicado público (≤ 600 caracteres, estilo LinkedIn) + contagem

## 4. Acessibilidade e inclusão digital
4.1 Quem pode ficar de fora + o que a solução faz por cada grupo  
4.2 Requisitos concretos de acessibilidade (WCAG)

## 5. Sustentabilidade
5.1 Impacto ambiental da solução  
5.2 Sustentabilidade do projeto (quem mantém, quem paga, depois do 1º ano)

## 6. Impacto esperado
6.1 Indicadores mensuráveis com meta  
6.2 Como os usuários serão ouvidos antes de ampliar  
6.3 Se a solução não pegar

## 7. Quadro de decisões (mínimo 5)
Tabela: Decisão | Alternativas | Por que escolhemos esta

## 8. Capítulos individuais
### 8.1 [Seu Nome Completo | Sua Área]

**Papel no projeto:**

[Descreva aqui o que você ficou responsável e o que produziu de concreto no trabalho. Ex: pesquisa e escrita da análise do problema, definição da solução, diagramas, revisão do texto etc.]

**Plano de desenvolvimento**

| Competência | Tipo | Situação atual | Meta (6 a 12 meses) |
|---|---|---|---|
| [Ex: Modelagem de dados / Integração de sistemas] | Técnica | Já tenho / Em desenvolvimento / Não tenho | [Meta SMART] |
| [Ex: Comunicação técnica com o grupo] | Comportamental | Já tenho / Em desenvolvimento / Não tenho | [Meta SMART] |
| [Ex: Análise de requisitos de privacidade (LGPD)] | Técnica | Já tenho / Em desenvolvimento / Não tenho | [Meta SMART] |
| [Ex: Organização e cumprimento de prazos] | Comportamental | Já tenho / Em desenvolvimento / Não tenho | [Meta SMART] |
| [Ex: Inglês básico] | Meta | Já tenho / Em desenvolvimento / Não tenho | [Meta SMART] |


**Feedback dos colegas**

**[Nome do integrante | Área de carreira]**  
- **Pontos positivos**:  
- **Pontos a melhorar**:  
- **Sugestões**:

**[Nome do integrante | Área de carreira]**  
- **Pontos positivos**:  
- **Pontos a melhorar**:  
- **Sugestões**:

**[Nome do integrante | Área de carreira]**  
- **Pontos positivos**:  
- **Pontos a melhorar**:  
- **Sugestões**:

**[Nome do integrante | Área de carreira]**  
- **Pontos positivos**:  
- **Pontos a melhorar**:  
- **Sugestões**:

### 8.2 [Seu Nome Completo | Sua Área]

**Papel no projeto:**

[Descreva aqui o que você ficou responsável e o que produziu de concreto no trabalho. Ex: pesquisa e escrita da análise do problema, definição da solução, diagramas, revisão do texto etc.]

**Plano de desenvolvimento**

| Competência | Tipo | Situação atual | Meta (6 a 12 meses) |
|---|---|---|---|
| [Ex: Modelagem de dados / Integração de sistemas] | Técnica | Já tenho / Em desenvolvimento / Não tenho | [Meta SMART] |
| [Ex: Comunicação técnica com o grupo] | Comportamental | Já tenho / Em desenvolvimento / Não tenho | [Meta SMART] |
| [Ex: Análise de requisitos de privacidade (LGPD)] | Técnica | Já tenho / Em desenvolvimento / Não tenho | [Meta SMART] |
| [Ex: Organização e cumprimento de prazos] | Comportamental | Já tenho / Em desenvolvimento / Não tenho | [Meta SMART] |
| [Ex: Inglês básico] | Meta | Já tenho / Em desenvolvimento / Não tenho | [Meta SMART] |


**Feedback dos colegas**

**[Nome do integrante | Área de carreira]**  
- **Pontos positivos**:  
- **Pontos a melhorar**:  
- **Sugestões**:

**[Nome do integrante | Área de carreira]**  
- **Pontos positivos**:  
- **Pontos a melhorar**:  
- **Sugestões**:

**[Nome do integrante | Área de carreira]**  
- **Pontos positivos**:  
- **Pontos a melhorar**:  
- **Sugestões**:

**[Nome do integrante | Área de carreira]**  
- **Pontos positivos**:  
- **Pontos a melhorar**:  
- **Sugestões**:

### 8.3 [Seu Nome Completo | Sua Área]

**Papel no projeto:**

[Descreva aqui o que você ficou responsável e o que produziu de concreto no trabalho. Ex: pesquisa e escrita da análise do problema, definição da solução, diagramas, revisão do texto etc.]

**Plano de desenvolvimento**

| Competência | Tipo | Situação atual | Meta (6 a 12 meses) |
|---|---|---|---|
| [Ex: Modelagem de dados / Integração de sistemas] | Técnica | Já tenho / Em desenvolvimento / Não tenho | [Meta SMART] |
| [Ex: Comunicação técnica com o grupo] | Comportamental | Já tenho / Em desenvolvimento / Não tenho | [Meta SMART] |
| [Ex: Análise de requisitos de privacidade (LGPD)] | Técnica | Já tenho / Em desenvolvimento / Não tenho | [Meta SMART] |
| [Ex: Organização e cumprimento de prazos] | Comportamental | Já tenho / Em desenvolvimento / Não tenho | [Meta SMART] |
| [Ex: Inglês básico] | Meta | Já tenho / Em desenvolvimento / Não tenho | [Meta SMART] |


**Feedback dos colegas**

**[Nome do integrante | Área de carreira]**  
- **Pontos positivos**:  
- **Pontos a melhorar**:  
- **Sugestões**:

**[Nome do integrante | Área de carreira]**  
- **Pontos positivos**:  
- **Pontos a melhorar**:  
- **Sugestões**:

**[Nome do integrante | Área de carreira]**  
- **Pontos positivos**:  
- **Pontos a melhorar**:  
- **Sugestões**:

**[Nome do integrante | Área de carreira]**  
- **Pontos positivos**:  
- **Pontos a melhorar**:  
- **Sugestões**:

### 8.4 [Seu Nome Completo | Sua Área]

**Papel no projeto:**

[Descreva aqui o que você ficou responsável e o que produziu de concreto no trabalho. Ex: pesquisa e escrita da análise do problema, definição da solução, diagramas, revisão do texto etc.]

**Plano de desenvolvimento**

| Competência | Tipo | Situação atual | Meta (6 a 12 meses) |
|---|---|---|---|
| [Ex: Modelagem de dados / Integração de sistemas] | Técnica | Já tenho / Em desenvolvimento / Não tenho | [Meta SMART] |
| [Ex: Comunicação técnica com o grupo] | Comportamental | Já tenho / Em desenvolvimento / Não tenho | [Meta SMART] |
| [Ex: Análise de requisitos de privacidade (LGPD)] | Técnica | Já tenho / Em desenvolvimento / Não tenho | [Meta SMART] |
| [Ex: Organização e cumprimento de prazos] | Comportamental | Já tenho / Em desenvolvimento / Não tenho | [Meta SMART] |
| [Ex: Inglês básico] | Meta | Já tenho / Em desenvolvimento / Não tenho | [Meta SMART] |


**Feedback dos colegas**

**[Nome do integrante | Área de carreira]**  
- **Pontos positivos**:  
- **Pontos a melhorar**:  
- **Sugestões**:

**[Nome do integrante | Área de carreira]**  
- **Pontos positivos**:  
- **Pontos a melhorar**:  
- **Sugestões**:

**[Nome do integrante | Área de carreira]**  
- **Pontos positivos**:  
- **Pontos a melhorar**:  
- **Sugestões**:

**[Nome do integrante | Área de carreira]**  
- **Pontos positivos**:  
- **Pontos a melhorar**:  
- **Sugestões**:

### 8.5 [Seu Nome Completo | Sua Área]

**Papel no projeto:**

[Descreva aqui o que você ficou responsável e o que produziu de concreto no trabalho. Ex: pesquisa e escrita da análise do problema, definição da solução, diagramas, revisão do texto etc.]

**Plano de desenvolvimento**

| Competência | Tipo | Situação atual | Meta (6 a 12 meses) |
|---|---|---|---|
| [Ex: Modelagem de dados / Integração de sistemas] | Técnica | Já tenho / Em desenvolvimento / Não tenho | [Meta SMART] |
| [Ex: Comunicação técnica com o grupo] | Comportamental | Já tenho / Em desenvolvimento / Não tenho | [Meta SMART] |
| [Ex: Análise de requisitos de privacidade (LGPD)] | Técnica | Já tenho / Em desenvolvimento / Não tenho | [Meta SMART] |
| [Ex: Organização e cumprimento de prazos] | Comportamental | Já tenho / Em desenvolvimento / Não tenho | [Meta SMART] |
| [Ex: Inglês básico] | Meta | Já tenho / Em desenvolvimento / Não tenho | [Meta SMART] |


**Feedback dos colegas**

**[Nome do integrante | Área de carreira]**  
- **Pontos positivos**:  
- **Pontos a melhorar**:  
- **Sugestões**:

**[Nome do integrante | Área de carreira]**  
- **Pontos positivos**:  
- **Pontos a melhorar**:  
- **Sugestões**:

**[Nome do integrante | Área de carreira]**  
- **Pontos positivos**:  
- **Pontos a melhorar**:  
- **Sugestões**:

**[Nome do integrante | Área de carreira]**  
- **Pontos positivos**:  
- **Pontos a melhorar**:  
- **Sugestões**:

## 9. Referências
Fontes dos últimos 2 anos (a partir de nov/2024) + leis/normas vigentes. Com link.

# Desafios para Integração da interoperabilidade nos sistemas de Saúde Publica

## Integrantes
Alison Belen | [GitHub](https://github.com/alison97-ciber) | Cibersegurança | 48012327  
Ana Julia de Aquino Silva | [GitHub](https://github.com/aquinoana1109-lgtm) | Engenharia de Dados| 47784105.  
Arthur Costa de Paula | [GitHub](https://github.com/artcpaula2007-creator) | Engenharia de Dados | 48108014  
João Victor de Jesus Silva | [GitHub](https://github.com/JvictorJesus) | Engenharia de Dados | 48134872  
Rafael Christian de Araujo Costa | [GitHub](https://github.com/Rafael44Christian) | Cibersegurança | 47926597    

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
**3.1 Matriz de riscos**

A integração de informações de saúde exige cuidados éticos e técnicos, pois envolve dados pessoais sensíveis. A falta de proteção adequada pode causar prejuízos aos pacientes, comprometer a confiança no SUS e dificultar a continuidade dos atendimentos.

| Risco identificado | Probabilidade | Impacto | Medidas de prevenção |
|--------------------|---------------|---------|----------------------|
| Acesso não autorizado aos prontuários | Média | Muito alto | Autenticação multifator, controle de permissões e acesso restrito aos profissionais autorizados. |
| Vazamento de dados pessoais e médicos | Média | Muito alto | Criptografia dos dados, monitoramento de acessos, testes de segurança e plano de resposta a incidentes. |
| Alteração ou inconsistência das informações médicas | Média | Alto | Validação dos dados recebidos, identificação da instituição responsável e registro do histórico de alterações. |
| Indisponibilidade dos sistemas | Média | Alto | Backups, redundância de infraestrutura, monitoramento e plano de recuperação de serviços. |
| Uso indevido das informações por instituições | Média | Muito alto | Definição de finalidades permitidas, auditoria, responsabilização e fiscalização dos acessos. |
| Discriminação ou decisões baseadas em dados incompletos | Média | Alto | Revisão humana, testes de viés e proibição de decisões clínicas exclusivamente automatizadas. |
| Exclusão de pessoas com dificuldades de acesso digital | Alta | Alto | Manutenção de atendimento presencial, linguagem simples e alternativas de acesso às informações. |
| Envio de documentos falsos ou incorretos pelo paciente | Média | Alto | Identificação da origem dos documentos e validação por profissionais antes de incorporá-los ao histórico oficial. |

**3.2 Decisão: implantar com controles**

A decisão é implantar a solução com controles rigorosos de segurança, privacidade e transparência. A integração pode melhorar a continuidade do atendimento, reduzir a repetição de exames e facilitar o acesso ao histórico médico. Entretanto, como envolve dados pessoais sensíveis, sua implantação deverá ocorrer gradualmente, com testes de segurança, controle de permissões e auditoria. Os profissionais de saúde continuarão responsáveis pelas decisões clínicas, sem depender exclusivamente de processos automatizados. A solução também deverá respeitar a LGPD e garantir que o cidadão tenha conhecimento sobre o uso de suas informações.

**3.3 Controles antes de produção**

Antes da disponibilização da solução, deverão ser implementadas as seguintes medidas:

- Transparência: informar aos pacientes quais dados são coletados, por que são utilizados, quais instituições podem acessá-los e quais são seus direitos.  
- Revisão humana: garantir que informações clínicas importantes e documentos complementares sejam avaliados por profissionais habilitados, sem permitir que sistemas automatizados substituam decisões médicas.  
- Minimização de dados: coletar e compartilhar somente as informações necessárias para cada finalidade, evitando o acesso a todo o histórico médico quando isso não for necessário  
- Segurança da informação: utilizar criptografia durante o armazenamento e a transmissão dos dados, autenticação multifator, controle de acesso por função e monitoramento de atividades suspeitas.  
- Teste de viés: avaliar periodicamente se os dados utilizados em análises ou ferramentas automatizadas apresentam distorções que possam prejudicar determinados grupos de pacientes.  
- Canal de contestação: disponibilizar um canal para que os cidadãos solicitem correções de informações, esclareçam dúvidas e contestem acessos ou utilizações indevidas de seus dados.  
- Auditoria e rastreabilidade: registrar quem acessou as informações, quando ocorreu o acesso, qual instituição realizou a consulta e quais alterações foram feitas.  
- Plano de resposta a incidentes: estabelecer procedimentos para identificar, conter e comunicar incidentes de segurança, seguindo as exigências da LGPD e da Resolução CD/ANPD nº 15/2024.  
- Controle de integração: verificar a identidade e a autorização das instituições conectadas à RNDS, além de validar a origem e a estrutura dos dados recebidos.

**3.4 LGPD – Tabela de dados pessoais**

A proposta envolve o tratamento de dados pessoais comuns e sensíveis, principalmente informações relacionadas à saúde. Por isso, o projeto deverá respeitar os princípios da finalidade, adequação, necessidade, transparência, segurança e prevenção previstos na Lei Geral de Proteção de Dados Pessoais (Lei nº 13.709/2018).

| Dados tratados | Classificação | Finalidade do tratamento | Proteção necessária |
|----------------|---------------|--------------------------|---------------------|
| Nome completo | Dado pessoal | Identificar corretamente o paciente. | Controle de acesso e armazenamento seguro. |
| CPF e Cartão Nacional de Saúde (CNS) | Dado pessoal | Confirmar a identidade e relacionar os registros médicos ao paciente correto. | Criptografia e acesso restrito. |
| Data de nascimento e dados de contato | Dado pessoal | Identificação e comunicação com o cidadão. | Acesso limitado e utilização somente quando necessário. |
| Diagnósticos, doenças e histórico médico | Dado pessoal sensível | Permitir a continuidade do atendimento e o acompanhamento clínico. | Criptografia, permissões específicas e auditoria. |
| Resultados de exames e prescrições | Dado pessoal sensível | Auxiliar os profissionais na avaliação e no acompanhamento do paciente. | Compartilhamento restrito e validação das informações. |
| Vacinas, medicamentos e tratamentos | Dado pessoal sensível | Consultar procedimentos realizados e evitar interrupções ou repetições desnecessárias. | Proteção contra acessos e alterações não autorizadas. |
| Identificação dos profissionais de saúde | Dado pessoal | Verificar quem realizou o atendimento e controlar as permissões de acesso. | Autenticação e registro de atividades. |
| Registros de acesso ao sistema | Dado pessoal, quando identificável | Garantir rastreabilidade, auditoria e investigação de possíveis incidentes. | Armazenamento protegido e acesso restrito. |

Bases legais e responsabilidades:

- Para dados pessoais comuns, poderão ser aplicadas as hipóteses legais do artigo 7º da LGPD, especialmente o cumprimento de políticas públicas pela administração pública, quando cabível.  
- Para dados pessoais sensíveis, deverão ser observadas as hipóteses específicas do artigo 11, como o tratamento necessário à execução de políticas públicas previstas em leis e regulamentos e à tutela da saúde, conforme o contexto e os agentes envolvidos.  
- O tratamento não deverá utilizar o consentimento como justificativa genérica para qualquer compartilhamento. A base legal deverá ser definida e documentada conforme a finalidade de cada operação.  
- Os dados deverão ser mantidos somente pelo período necessário, respeitando as obrigações legais e os prazos de guarda aplicáveis.  
- Os cidadãos deverão ter acesso a informações sobre o tratamento de seus dados e aos mecanismos legais para solicitar correções e exercer seus direitos.

**3.5 Comunicado público (estilo LinkedIn)**

A proposta busca facilitar o acesso ao histórico de saúde por meio da integração entre instituições e a Rede Nacional de Dados em Saúde (RNDS), com consulta pelo Meu SUS Digital e por profissionais autorizados. O uso será limitado às finalidades legítimas, com acesso controlado, registro de consultas e proteção conforme a LGPD. O cidadão receberá informações claras sobre seus dados e terá canal para solicitar correções, esclarecer dúvidas ou contestar usos indevidos. A implantação será gradual, após testes de segurança e avaliação dos resultados.

## 4. Acessibilidade e inclusão digital
**4.1 Quem pode ficar de fora + o que a solução faz por cada grupo**

A integração dos dados dos pacientes pelo aplicativo do SUS busca facilitar o acesso aos serviços de saúde. Porém, algumas pessoas podem enfrentar dificuldades para utilizar a tecnologia.
Idosos: podem ter dificuldade com aplicativos. A solução deve oferecer uma interface simples, com letras grandes e navegação fácil.  
Pessoas com deficiência visual: o aplicativo deve ser compatível com leitores de tela e permitir aumentar o tamanho das letras.  
Pessoas com deficiência auditiva: disponibilizar informações por escrito, notificações visuais e instruções claras.  
Pessoas com baixa alfabetização digital: oferecer instruções simples, ícones intuitivos e orientação para utilizar o aplicativo.  
Pessoas sem acesso à internet: permitir que o atendimento presencial continue disponível nas unidades de saúde.  
Pessoas com deficiência motora: oferecer navegação por comandos de voz e compatibilidade com tecnologias assistivas.  
A proposta é garantir que todos os pacientes consigam acessar suas informações de saúde, independentemente de suas limitações ou condições de acesso à tecnologia.

**4.2 Requisitos concretos de acessibilidade (WCAG)**

Os requisitos concretos de acessibilidade WCAG (Web Content Accessibility Guidelines) são diretrizes internacionais que estabelecem critérios para tornar sites e aplicativos acessíveis a todas as pessoas, incluindo aquelas com deficiência visual, auditiva, motora ou cognitiva. Essas diretrizes foram desenvolvidas pelo W3C (World Wide Web Consortium) e têm como objetivo garantir que todos possam acessar e utilizar os recursos digitais com autonomia, segurança e igualdade de condições.  

As WCAG são organizadas em quatro princípios fundamentais: perceptível, operável, compreensível e robusto. O princípio perceptível determina que as informações devem ser apresentadas de maneira que todos consigam identificá-las, como utilizar textos com contraste adequado, permitir o aumento das letras e oferecer descrições para imagens e ícones. O princípio operável estabelece que as funcionalidades devem ser acessíveis e fáceis de utilizar, permitindo, por exemplo, a navegação por teclado ou por tecnologias assistivas. O princípio compreensível determina que as informações, instruções e mensagens sejam claras e simples, facilitando o entendimento dos usuários. Já o princípio robusto garante que o aplicativo seja compatível com diferentes dispositivos e tecnologias assistivas, como leitores de tela.  

No aplicativo Meu SUS Digital, esses requisitos são importantes porque a plataforma disponibiliza informações e serviços relacionados à saúde da população, como carteira de vacinação, histórico clínico, resultados de exames, medicamentos e documentos de saúde. Portanto, é necessário garantir que pessoas com diferentes necessidades consigam utilizar essas funcionalidades sem enfrentar barreiras digitais.  

Na prática, a acessibilidade pode ser aplicada permitindo que pessoas com deficiência visual utilizem leitores de tela para identificar botões, menus e informações sobre vacinas e exames. Também é importante oferecer contraste adequado entre textos e fundos, permitir o aumento do tamanho das letras e garantir que os ícones tenham descrições compreensíveis. Para pessoas com deficiência auditiva, os conteúdos em vídeo devem possuir legendas e as notificações não devem depender exclusivamente de sons. Para pessoas com deficiência motora, os botões devem ter tamanho adequado, ser bem distribuídos na tela e permitir o uso de tecnologias assistivas. Já para pessoas com deficiência cognitiva, é importante utilizar linguagem simples, instruções objetivas, menus organizados e mensagens de erro fáceis de compreender.  

Outro aspecto importante é a aplicação dos níveis de conformidade WCAG, classificados em A, AA e AAA. O nível A contempla requisitos básicos de acessibilidade; o nível AA apresenta critérios mais abrangentes e é uma referência recomendada para serviços digitais públicos; e o nível AAA reúne requisitos mais rigorosos. Para o aplicativo do SUS, buscar a conformidade com o nível AA é uma medida importante para ampliar o acesso da população aos serviços digitais.  

Dessa forma, a aplicação dos requisitos WCAG no Meu SUS Digital contribui para garantir os princípios de universalidade e equidade do SUS, pois permite que todos os cidadãos tenham condições de acessar informações e serviços de saúde, independentemente de suas limitações físicas, sensoriais ou cognitivas. Assim, a acessibilidade digital não deve ser considerada apenas um recurso adicional, mas uma necessidade para assegurar inclusão, autonomia e igualdade no acesso à saúde.

## 5. Sustentabilidade
5.1 Impacto ambiental da solução  

A criação de um sistema que permita compartilhar as informações dos pacientes do SUS pode trazer benefícios não só para a nossa saúde, mas também para o meio ambiente.
Com as informações armazenadas de forma digital, será possível diminuir o uso do papel, já que muito documentos e históricos médico poderá de ser consultados pelo próprio sistema. Além disso, quando o resultado dos exames estiverem disponíveis para diferentes unidades de saúde, poderá diminuir a repetição de exames que já foram realizados.

5.2 Sustentabilidade do projeto (quem mantém, quem paga, depois do 1º ano)

Para que o projeto continue funcionando depois do primeiro ano, será necessário que o Governo Federal, junto com os estados e municípios, fique responsável pela manutenção e pelos investimentos necessários.
Os custos poderão ser mantidos por meio de recursos públicos destinados à saúde e à tecnologia. Esse investimento será utilizado para atualizar o sistema, corrigir possíveis erros, manter os servidores funcionando e garantir a segurança das informações dos pacientes.
Também será necessário contar com profissionais da área de TI para acompanhar o funcionamento da plataforma, realizar melhorias e resolver problemas que possam surgir durante sua utilização.
Uma forma de evitar gastos desnecessários seria aproveitar estruturas que já existem, como a Rede Nacional de Dados em Saúde (RNDS) e o Meu SUS Digital, realizando melhorias nos sistemas em vez de desenvolver tudo novamente.
Na nossa visão, para que o projeto continue funcionando por muitos anos, não basta apenas criar uma solução tecnológica. É necessário investir em manutenção, segurança e profissionais capacitados. Assim, será possível oferecer aos usuários do SUS um acesso mais fácil às suas informações de saúde, independentemente da unidade em que forem atendidos.

## 6. Impacto esperado
A implementação de uma solução tecnológica voltada à interoperabilidade de dados no Sistema Único de Saúde (SUS) tem como objetivo melhorar a integração e o compartilhamento de informações entre instituições de saúde, proporcionando maior agilidade nos atendimentos, redução de falhas administrativas e melhor organização dos dados dos pacientes.

Com o auxílio da inteligência artificial, espera-se também otimizar processos, identificar padrões de demanda e auxiliar os profissionais na tomada de decisões, contribuindo para uma gestão mais eficiente dos recursos disponíveis.

6.1 Indicadores mensuráveis com meta  
Para avaliar a eficiência da solução proposta, serão utilizados indicadores que permitam acompanhar os resultados durante sua implementação.

- Integração de informações: alcançar pelo menos 80% de integração dos registros das unidades participantes do projeto-piloto.
- Agilidade no acesso aos dados: reduzir em 30% o tempo necessário para localizar informações dos pacientes.
- Redução de retrabalho: diminuir em 20% a duplicidade de cadastros e registros de informações.
- Satisfação dos usuários: alcançar pelo menos 80% de avaliações positivas entre pacientes e profissionais participantes.
- Segurança das informações: garantir o cumprimento das normas da LGPD e monitorar possíveis falhas de segurança e acessos não autorizados.
As metas são estimativas iniciais para o projeto-piloto e poderão ser ajustadas conforme os resultados obtidos.

6.2 Como os usuários serão ouvidos antes de ampliar
  Antes de ampliar a implementação da solução, serão realizadas pesquisas de satisfação, entrevistas e avaliações com pacientes, médicos, enfermeiros e profissionais administrativos das unidades de saúde participantes.
O objetivo será identificar dificuldades de utilização, problemas de acessibilidade, possíveis falhas no compartilhamento de informações e necessidades de melhorias.
Também serão analisadas sugestões dos profissionais responsáveis pelo atendimento, garantindo que a tecnologia realmente contribua para facilitar suas atividades e melhorar a experiência dos pacientes.
Somente após a avaliação dos resultados e a realização dos ajustes necessários será considerada a expansão da solução para outras unidades de saúde.

6.3 Se a solução não pegar
  Caso a solução não apresente os resultados esperados, será realizada uma análise para identificar as principais causas, como dificuldades de integração entre sistemas, falta de capacitação dos profissionais, problemas técnicos ou resistência à utilização da ferramenta.

A partir dessa avaliação, poderão ser adotadas medidas como:
 Revisão e aprimoramento do sistema de integração de dados;
 Capacitação dos profissionais responsáveis pela utilização da plataforma;
 Melhorias na infraestrutura tecnológica das unidades participantes;
 Reavaliação das ferramentas de inteligência artificial utilizadas;
 Manutenção de procedimentos convencionais e registros alternativos para evitar a interrupção dos atendimentos.

Caso a tecnologia não demonstre benefícios suficientes, sua implementação poderá ser reduzida ou reformulada, priorizando soluções administrativas e operacionais que contribuam para a melhoria do atendimento público de saúde.

## 7. Quadro de decisões (mínimo 5)

Durante o desenvolvimento da proposta, foram avaliadas diferentes alternativas para melhorar a interoperabilidade entre os sistemas de saúde. As decisões foram tomadas considerando a facilidade de acesso às informações, a segurança dos dados, a inclusão dos pacientes e a viabilidade da solução.

| Decisão | Alternativas | Por que escolhemos esta |
|---|---|---|
| Utilizar a RNDS como base para integração dos dados | Criar uma plataforma independente; utilizar a RNDS; integrar somente sistemas locais. | Escolhemos utilizar a RNDS porque ela já é a estrutura nacional destinada à integração e ao compartilhamento de informações de saúde, evitando criar uma rede paralela. |
| Utilizar o Meu SUS Digital como ferramenta de acesso para os cidadãos | Criar um aplicativo próprio; utilizar o Meu SUS Digital; disponibilizar somente acesso presencial. | Escolhemos o Meu SUS Digital porque já é uma ferramenta disponibilizada pelo Ministério da Saúde e permite que os cidadãos consultem informações de saúde sem precisar utilizar outro aplicativo. |
| Permitir a integração de instituições públicas e privadas | Integrar somente unidades públicas; permitir integração de instituições públicas e privadas; manter sistemas separados. | Escolhemos ampliar a integração para ambos os setores, pois o paciente pode realizar consultas e exames em diferentes instituições e precisa ter continuidade no atendimento. |
| Permitir o envio de documentos complementares pelos pacientes | Bloquear documentos externos; permitir o envio com validação; incorporar automaticamente todos os documentos ao histórico oficial. | Escolhemos permitir o envio com validação profissional, pois isso ajuda pacientes que realizam exames em instituições ainda não integradas, sem comprometer a confiabilidade das informações médicas. |
| Adotar controles rigorosos de segurança e privacidade | Acesso amplo às informações; acesso restrito por autorização; compartilhamento sem registro. | Escolhemos o acesso controlado e auditável, com autenticação, criptografia e registro de atividades, para proteger os dados pessoais e médicos conforme a LGPD. |
| Realizar a implantação de forma gradual | Implantação imediata em todas as instituições; implantação por etapas e testes; adiar completamente o projeto. | Escolhemos a implantação gradual porque permite identificar falhas, avaliar a segurança, corrigir problemas e melhorar a integração antes de ampliar o uso da solução. |
| Manter alternativas de atendimento para pessoas com dificuldades digitais | Utilizar somente o aplicativo; oferecer acesso digital e suporte presencial; restringir o acesso aos usuários com dispositivos modernos. | Escolhemos combinar o acesso digital com alternativas presenciais, garantindo que idosos, pessoas com deficiência e cidadãos sem acesso à internet também possam consultar e utilizar suas informações de saúde. |

As decisões foram definidas buscando equilibrar inovação, segurança, acessibilidade e viabilidade. Dessa forma, a proposta aproveita estruturas já existentes no SUS e procura melhorar a integração das informações sem deixar de lado a proteção e os direitos dos pacientes.

## 8. Capítulos individuais
### 8.1 Rafael Christian de Araujo Costa | Cibersegurança

#### Papel no projeto

Minha participação no projeto foi voltada principalmente à área de Cibersegurança, contribuindo diretamente para o desenvolvimento das seções 3 (Análise Ética) e 7 (Quadro de Decisões).

Na seção 3, fui responsável por desenvolver a análise dos riscos relacionados ao compartilhamento de informações de saúde, identificando possíveis problemas como vazamento de dados, acessos não autorizados, alterações indevidas de informações médicas e uso inadequado dos dados dos pacientes. Também trabalhei na definição de medidas preventivas, considerando a criptografia, autenticação, controle de acesso, auditoria e os requisitos da Lei Geral de Proteção de Dados (LGPD).

Além disso, desenvolvi a tabela de dados pessoais, relacionando as informações que podem ser utilizadas pelo sistema, suas finalidades e as formas necessárias de proteção. Também participei da definição da decisão de implantação da solução com controles de segurança, transparência e privacidade.

Na seção 7, contribuí para o quadro de decisões do projeto, apresentando as alternativas avaliadas e justificando as escolhas realizadas pelo grupo. Entre elas estão a utilização da RNDS como base de integração, o uso do Meu SUS Digital para acesso dos cidadãos, a integração entre instituições públicas e privadas, a validação de documentos complementares enviados pelos pacientes e a implantação gradual da solução.

Minha principal contribuição foi demonstrar que a integração dos dados do SUS precisa ir além da comunicação entre sistemas. É necessário garantir que as informações dos pacientes sejam protegidas, utilizadas corretamente e compartilhadas somente de acordo com as finalidades permitidas.

Também fiquei responsável por reunir e organizar as referências bibliográficas do projeto, desenvolvendo a seção 9. Realizei pesquisas em fontes oficiais, como o Ministério da Saúde, a ANPD, a legislação brasileira e organizações responsáveis por padrões de tecnologia. Essa etapa foi importante para fundamentar as decisões do grupo, principalmente nas questões relacionadas à interoperabilidade, segurança da informação, acessibilidade e proteção de dados pessoais.

Com isso, minha contribuição envolveu não apenas a análise dos riscos e as decisões de segurança, mas também a pesquisa de informações confiáveis para dar embasamento ao desenvolvimento da proposta.

#### Plano de desenvolvimento

| Competência | Tipo | Situação atual | Meta (6 a 12 meses) |
|---|---|---|---|
| Segurança da informação | Técnica | Em desenvolvimento | Estudar os fundamentos de segurança da informação e aplicar conhecimentos de criptografia, autenticação e controle de acesso em pelo menos dois projetos ou laboratórios práticos. |
| Proteção de dados e LGPD | Técnica | Em desenvolvimento | Aprofundar meus conhecimentos na LGPD e desenvolver pelo menos um checklist de segurança e privacidade para aplicar em um projeto acadêmico. |
| Redes e infraestrutura | Técnica | Em desenvolvimento | Estudar protocolos, redes, firewalls e mecanismos de proteção, realizando pelo menos dois exercícios práticos de configuração e segurança de redes. |
| Análise de riscos e vulnerabilidades | Técnica | Em desenvolvimento | Aprender técnicas de identificação de vulnerabilidades e realizar pelo menos dois laboratórios práticos em ambientes controlados. |
| Comunicação e trabalho em equipe | Comportamental | Em desenvolvimento | Melhorar minha comunicação técnica, participar das decisões dos projetos e apresentar pelo menos um trabalho relacionado à tecnologia durante os próximos 12 meses. |
| Inglês técnico | Meta | Em desenvolvimento | Estudar inglês por pelo menos 20 minutos, quatro vezes por semana, durante seis meses, buscando melhorar a compreensão de documentações e conteúdos de Cibersegurança. |

**Feedback dos colegas**

**[Arthur Costa| Engenharia de Dados]**  
- **Pontos positivos**:
- Apresenta metas claras para desenvolver conhecimentos em segurança da informação, redes, LGPD e análise de vulnerabilidades.
- **Pontos a melhorar**:
- Buscar maior contato com ferramentas utilizadas na área de Cibersegurança, como Wireshark, Linux e ferramentas de análise de vulnerabilidades.
- **Sugestões**:
- Estudar a LGPD na prática: Elaborar checklists de privacidade e segurança para aplicar em projetos acadêmic

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

### 8.2 [Ana Julia de Aquino Silva | Engenharia de Dados]

**Papel no projeto:**

Minha participação no projeto foi ajudar na pesquisa sobre o problema de falta de informações entre o sistema de saúde. Também ajudei organizar os textos e entender as dificuldades enfrentadas pelos pacientes e profissionais, pensando em possíveis soluções para ambos lados.

**Plano de desenvolvimento**

| Competência | Tipo | Situação atual | Meta (6 a 12 meses) |
|---|---|---|---|
|Banco de Dados e SQL / | Técnica | Em desenvolvimento /| Aprender a criar, consultar e organizar bancos de dados, praticando comandos SQL pelo menos duas vezes por semana |
| Integração de Dados | Técnica |  Não tenho | Entender como funciona a integração de informações entre diferentes sistemas e desenvolver um pequeno projeto prático até o final de 12 meses |
| Python para análise de dados | Técnica | Em desenvolvimento | Aprender os principais comandos de Python e desenvolver atividades simples para organizar e analisar dados. |
| Comunicação com o grupo | Comportamental Em desenvolvimento | Melhorar minha comunicação, participar mais das atividades em grupo e compartilhar minhas ideias durante os trabalhos. |
| Inglês básico  | Meta | Em desenvolvimento 
| Aprender palavras e expressões em inglê, estudando pelo menos 20 minutos por dia. |


**Feedback dos colegas**

**[Rafael Christian | Cibersegurança]**  
- **Pontos positivos**:  Demonstrou dedicação na elaboração da sua parte individual e contribuiu para ampliar a visão do grupo sobre o tema. Seu trabalho apresenta informações relevantes e mostra preocupação em relacionar os conhecimentos da sua área com a proposta de melhoria do SUS.
- **Pontos a melhorar**:  Poderia aprofundar um pouco mais a relação entre sua área profissional e a solução tecnológica proposta, detalhando como suas habilidades poderiam ser aplicadas na prática.
- **Sugestões**:  Continuar desenvolvendo seus conhecimentos técnicos, buscar experiências práticas relacionadas à sua área e procurar aplicar esses conhecimentos em projetos que envolvam tecnologia e saúde.

**[Arthur Costa | Engenharia de Dados]**  
- **Pontos positivos**:
- Ela apresenta metas específicas para desenvolver competências técnicas e comportamentais ao longo de 6 a 12 meses.
- **Pontos a melhorar**:
- Trabalhar a confiança para apresentar ideias, tirar dúvidas e participar mais ativamente das decisões em grupo.
- **Sugestões**:
- Utilizar aplicativos como Duolingo e assistir a vídeos com legendas em inglês para melhorar a compreensão.

**[Nome do integrante | Área de carreira]**  
- **Pontos positivos**:  
- **Pontos a melhorar**:  
- **Sugestões**:

**[Nome do integrante | Área de carreira]**  
- **Pontos positivos**:  
- **Pontos a melhorar**:  
- **Sugestões**:

## 8.3 Alison Belen | Cibersegurança

**Papel no projeto:**

Fui responsável pela avaliação individual do tópico 4 — Acessibilidade e Inclusão Digital. Durante essa etapa, identifiquei os grupos que poderiam enfrentar dificuldades no acesso aos serviços digitais, como idosos, pessoas com deficiência e pessoas com pouca familiaridade com a tecnologia.

Como proposta de solução, sugeri a integração dos dados dos pacientes por meio do aplicativo do SUS, utilizando uma interface simples e acessível. A proposta inclui recursos como letras ampliadas, compatibilidade com leitores de tela, navegação intuitiva e atendimento presencial como alternativa para pessoas que não possuem acesso à internet.

Além disso, considerei requisitos de acessibilidade baseados nas diretrizes WCAG, buscando contribuir para uma solução mais inclusiva, acessível e eficiente para todos os pacientes.

## Plano de desenvolvimento

| Competência | Tipo | Situação atual | Meta (6 a 12 meses) |
| --- | --- | --- | --- |
| Programação | Técnica | Em desenvolvimento | Fortalecer os conhecimentos de programação por meio de estudos regulares e desenvolver pelo menos 2 projetos práticos, publicando-os no GitHub com descrição. |
| Cibersegurança | Técnica | Em desenvolvimento | Estudar os fundamentos de cibersegurança durante os próximos 12 meses e concluir pelo menos 1 curso ou trilha introdutória. |
| Banco de dados e redes | Técnica | Em desenvolvimento | Praticar conceitos de banco de dados e redes e desenvolver pelo menos 1 atividade ou projeto acadêmico que aplique esses conhecimentos. |
| Comunicação técnica com o grupo | Comportamental | Em desenvolvimento | Participar das atividades em grupo e apresentar ou explicar pelo menos 1 projeto ou conteúdo técnico ao longo dos próximos 6 a 12 meses. |
| Organização e cumprimento de prazos | Comportamental | Em desenvolvimento | Planejar semanalmente as tarefas acadêmicas e cumprir os prazos de entrega das atividades durante os próximos 6 meses. |
| Inglês básico | Meta | Em desenvolvimento | Estudar inglês por 20 minutos, 3 vezes por semana, durante 12 meses, para melhorar a compreensão de conteúdos e materiais da área de tecnologia. |

## Feedback dos colegas

**[João Victor de Jesus Silva | Engenharia de dados]**  
- **Pontos positivos**: Metas de desenvolvimento bem direcionadas à área de interesse em Ciber-segurânça. A pesquisa incluí grupos diversos, ampliando a capacidade de inclusão da solução inicial.  
- **Pontos a melhorar**: Maior especificação nos critérios concretos da WCAG, que não especifica exatamente quais mecanismos devem estar presentes na solução para cada grupo.  
- **Sugestões**: Aprimorar a proposta de inclusão da solução, aprofundando os requisitos de inclusão conforme a WCAG.

**[Rafael Christian | Cibersegurança]** 
- **Pontos positivos**:  Demonstrou preocupação com a inclusão digital e conseguiu identificar diferentes grupos que podem enfrentar dificuldades para utilizar os serviços digitais do SUS. Também apresentou boas sugestões de acessibilidade, relacionando a proposta às diretrizes WCAG.
- **Pontos a melhorar**:  Poderia aprofundar um pouco mais a parte prática da acessibilidade, detalhando como os recursos sugeridos seriam aplicados no Meu SUS Digital.
- **Sugestões**:  Buscar exemplos de aplicações das diretrizes WCAG em sistemas reais e desenvolver propostas ainda mais específicas para melhorar a experiência dos usuários.

**[Arthur Costa | Engenheira de Dados]**  
- **Pontos positivos**:
 Busca desenvolver conhecimentos em diferentes áreas da TI, o que pode proporcionar uma formação profissional mais completa.
- **Pontos a melhorar**:
- Como apresenta objetivos em diferentes áreas da tecnologia, seria interessante identificar uma área para aprofundar os conhecimentos e direcionar melhor sua carreira.
- **Sugestões**:
- Criar pelo menos dois projetos de programação e publicá-los no GitHub, explicando suas funcionalidades e tecnologias utilizadas.

**[Nome do integrante | Área de carreira]**  
- **Pontos positivos**:  
- **Pontos a melhorar**:  
- **Sugestões**:

### 8.4 [ Arthur Costa de Paula | Engenharia de Dados]

**Papel no projeto:**
Fui responsável pela pesquisa e análise dos principais desafios enfrentados pelo Sistema Único de Saúde (SUS), identificando suas causas e consequências para a população. Além disso, busquei compreender as dificuldades enfrentadas pelos usuários do sistema e desenvolvi propostas de soluções para os problemas identificados, considerando tanto a aplicação da Inteligência Artificial (IA) quanto alternativas convencionais que não dependem do uso dessa tecnologia, com o objetivo de contribuir para a melhoria da qualidade e da eficiência dos serviços de saúde pública.


**Plano de desenvolvimento**

| Competência | Tipo | Situação atual | Meta (6 a 12 meses) |
|---|---|---|---|
| Desenvolvimento de sistemas | Técnica |  Em desenvolvimento  | Procuro aperfeiçoar o desenvolvimento de sistemas, dependendo menos da IA , e poder fazer mais alguns projetos utilizando Python e Java |
| Comunicação técnica com o grupo | Comportamental | Já tenho | Busco sempre a melhor forma possível de me expressar para meus colegas , entenderem e compreenderem minha linha de raciocínio, para que sempre estejamos na mesma pagina e continuar um bom trabalho   |
| Organização e cumprimento de prazos| Comportamental | Em desenvolvimento | Sempre é bom prestar atençao nos prazos preciso aprender a usar isso a meu favor fazendo ja uma grande parte do trabalho antes para que a finalização não seja corrida e no final não atenda as expectativas|
| Inglês básico | Meta | Em desenvolvimento  | Cursos de inglês finalizados eu já tenho o que falta é aperfeiçoar a parte da conversa, conversar totalmente em ingles sem travar ou ficar confuso com a pronuncia por isso buscar fazer sempre coisas como , trabalhos em inglês para que minha mente decore e estude a língua  |


**Feedback dos colegas**

**[Alison Belen | Cibersegurança]**  
- **Pontos positivos**: Demonstra iniciativa, boa capacidade de pesquisa e análise, além de preocupação em propor soluções para os problemas identificados.  
- **Pontos a melhorar**: Aprimorar a organização dos prazos e desenvolver maior autonomia na programação, reduzindo a dependência da IA.  
- **Sugestões**: Desenvolver projetos práticos com Python e Java, organizar melhor as tarefas e praticar conversação em inglês para fortalecer suas habilidades profissionais.

**[João Victor de Jesus Silva | Engenharia de Dados]**  
- **Pontos positivos**: Muito interessante destacar que, apesar de ainda precisar do uso de IA para o desenvolvimento de algumas atividades, segue buscando maior independência da ferramenta. A pesquisa foi essêncial para o desenvolvimento do projeto.  
- **Pontos a melhorar**: Pequena falta de detalhamento em relação ás propostas em alternativa ao uso de IA, considerando as falhas de gestão, filas e falta de remedios.  
- **Sugestões**: Desenvolvimento de um portifólio, mesmo que com projetos feitos a partir de IA, que servirão como base para destacar a evolução. Aprimoramento das soluções não tecnológicas.

**[Rafael Christian | Cibersegurança]**  
- **Pontos positivos**:  Demonstrou boa capacidade de pesquisa e iniciativa ao identificar diferentes problemas enfrentados pelo SUS. Também foi interessante considerar soluções que não dependem exclusivamente da inteligência artificial.
- **Pontos a melhorar**:  Poderia detalhar melhor como as soluções propostas seriam colocadas em prática e aprofundar a relação entre suas pesquisas e a proposta tecnológica do grupo.
- **Sugestões**: Desenvolver projetos práticos utilizando Python e Java, além de buscar formas de relacionar seus conhecimentos de programação e engenharia de dados aos problemas apresentados no projeto.

**[Nome do integrante | Área de carreira]**  
- **Pontos positivos**:  
- **Pontos a melhorar**:  
- **Sugestões**:

### 8.5 João Victor de Jesus Silva | Engenharia de dados

**Papel no projeto:**

Fui responsável pela realização de pesquisas, análise do problema relacionado à interoperabilidade de dados no sistema de saúde e contribuição na elaboração de uma proposta de solução. Minha participação envolveu investigar as dificuldades de integração e compartilhamento de informações entre instituições de saúde, considerando aspectos como acessibilidade, segurança e organização dos dados.

**Plano de desenvolvimento**

| **Competência** | **Tipo** | **Situação atual** | **Meta (6 a 12 meses)** |
|---|---|---|---|
| Programação e desenvolvimento de sistemas | Técnica | Já tenho | Desenvolver pelo menos dois projetos práticos utilizando Java ou Python, aplicando boas práticas de programação e versionamento com Git. |
| Banco de dados e análise de informações | Técnica | Em desenvolvimento | Aprofundar conhecimentos em SQL e modelagem de dados, desenvolvendo pelo menos um projeto que envolva consultas, relacionamentos e organização de informações. |
| Análise de problemas e levantamento de requisitos | Técnica | Já tenho | Aplicar técnicas de análise de requisitos em pelo menos dois projetos acadêmicos ou pessoais, documentando problemas identificados e possíveis soluções. |
| Comunicação e trabalho em equipe | Comportamental | Em desenvolvimento | Melhorar minha comunicação em atividades coletivas, participando ativamente de reuniões, apresentando ideias e contribuindo nas decisões dos projetos. |
| Inglês | Meta | Em desenvolvimento | Desenvolver o inglês até alcançar o nível básico-intermediário, estudando pelo menos 30 minutos por dia e praticando leitura, escrita e conversação. |
| Inserção profissional na área de tecnologia | Meta | Em desenvolvimento | Conquistar uma oportunidade de estágio ou emprego na área de TI nos próximos 12 meses, mantendo o currículo atualizado, aprimorando o LinkedIn e realizando candidaturas frequentes. |


**Feedback dos colegas**

**[Arthur Costa de Paula| Engenharia de Dados]**  
- **Pontos positivos**:A página está dividida em seções bem definidas, facilitando a compreensão das informações; O plano apresenta metas com prazos de 6 a 12 meses, permitindo acompanhar sua evolução;Demonstra preocupação em aprimorar conhecimentos em programação,banco de dados e análise de informações;Inclui competências comportamentais, como comunicação e trabalho em equipe, que são importantes no mercado profissional; Apresenta interesse em ingressar no mercado de tecnologia e conquistar uma oportunidade na área. 
- **Pontos a melhorar**: A meta poderia especificar quais conhecimentos técnicos em inglês pretende desenvolver, considerando a importância da língua na área de tecnologia; Algumas metas poderiam apresentar resultados mais concretos e critérios para avaliar se foram alcançadas.
- **Sugestões**:Explicar melhor como sua pesquisa contribuiu para a proposta de solução; Definir objetivos relacionados à conquista de estágio em Engenharia de Dados; Criar projetos práticos e disponibilizá-los no GitHub para demonstrar seus conhecimentos.

**[Alison Belen | Cibersegurança]**  
- **Pontos positivos**: Apresenta boa organização, metas claras e interesse em desenvolver conhecimentos técnicos e profissionais.  
- **Pontos a melhorar**: Aprofundar conhecimentos em ferramentas específicas de Engenharia de Dados e tornar algumas metas mais mensuráveis.  
- **Sugestões**: Desenvolver projetos práticos com Python e SQL, publicar no GitHub e buscar oportunidades de estágio na área.

**[Rafael Christian | Cibersegurança]**  
- **Pontos positivos**:  Apresentou uma boa análise sobre a interoperabilidade dos dados no SUS e demonstrou preocupação com a integração das informações entre diferentes instituições. Também apresentou metas de desenvolvimento bem organizadas e relacionadas à sua área profissional.
- **Pontos a melhorar**:   Poderia detalhar um pouco mais sua participação na construção da solução tecnológica, mostrando quais conhecimentos de Engenharia de Dados foram aplicados ou poderiam ser utilizados no projeto.
- **Sugestões**:  Aprofundar os conhecimentos em SQL, integração de sistemas e modelagem de dados, desenvolvendo projetos práticos que possam demonstrar sua evolução e contribuir para sua entrada no mercado de tecnologia.

**[Nome do integrante | Área de carreira]**  
- **Pontos positivos**:  
- **Pontos a melhorar**:  
- **Sugestões**:

## 9. Referências

As referências abaixo foram utilizadas para fundamentar as pesquisas, decisões técnicas, análises éticas e propostas apresentadas neste projeto.

1. **GITHUB.** Interoperabilidade de Dados no SUS – Repositório do projeto. Disponível em: https://github.com/JvictorJesus/InteroperabilidadeDeDadosNoSUS. Acesso em: 9 nov. 2026.

2. **BRASIL. Ministério da Saúde.** Rede Nacional de Dados em Saúde (RNDS). Apresenta a plataforma oficial de interoperabilidade e o compartilhamento de informações de saúde. Disponível em: https://www.gov.br/saude/pt-br/composicao/seidigi/rnds/rnds. Acesso em: 9 nov. 2026.

3. **BRASIL. Ministério da Saúde.** Meu SUS Digital. Informações sobre os serviços digitais, histórico de saúde e acesso dos cidadãos aos seus dados. Disponível em: https://www.gov.br/saude/pt-br/composicao/seidigi/meususdigital. Acesso em: 9 nov. 2026.

4. **BRASIL. Ministério da Saúde.** Guia de Implementação da Rede Nacional de Dados em Saúde (RNDS). Documentação técnica sobre integração dos sistemas e utilização do padrão HL7 FHIR R4. Disponível em: https://fhir.saude.gov.br/. Acesso em: 9 nov. 2026.

5. **BRASIL.** Decreto nº 12.560, de 23 de julho de 2025. Dispõe sobre a Rede Nacional de Dados em Saúde e sobre as Plataformas SUS Digital. Disponível em: https://www.planalto.gov.br/ccivil_03/_ato2023-2026/2025/decreto/d12560.htm. Acesso em: 9 nov. 2026.

6. **BRASIL.** Lei nº 13.709, de 14 de agosto de 2018. Lei Geral de Proteção de Dados Pessoais (LGPD). Disponível em: https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm. Acesso em: 9 nov. 2026.

7. **AUTORIDADE NACIONAL DE PROTEÇÃO DE DADOS (ANPD).** Resolução CD/ANPD nº 15, de 24 de abril de 2024. Regulamento de Comunicação de Incidente de Segurança. Disponível em: https://www.gov.br/anpd/pt-br/acesso-a-informacao/institucional/atos-normativos/regulamentacoes_anpd/. Acesso em: 9 nov. 2026.

8. **WORLD WIDE WEB CONSORTIUM (W3C).** Web Content Accessibility Guidelines (WCAG) 2.2. Diretrizes internacionais para acessibilidade de conteúdos e aplicações digitais. Disponível em: https://www.w3.org/WAI/standards-guidelines/wcag/. Acesso em: 9 nov. 2026.

9. **HL7 INTERNATIONAL.** FHIR (Fast Healthcare Interoperability Resources). Padrão internacional para troca e integração de informações em saúde. Disponível em: https://hl7.org/fhir/R4/. Acesso em: 9 nov. 2026.

10. **BRASIL.** Lei nº 8.080, de 19 de setembro de 1990. Dispõe sobre as condições para a promoção, proteção e recuperação da saúde e a organização e o funcionamento dos serviços correspondentes. Disponível em: https://www.planalto.gov.br/ccivil_03/leis/l8080.htm. Acesso em: 9 nov. 2026.

11. **PÁGINA DA FIOCRUZ , Escola Politécnica de Saúde Joaquim Venâncio** https://www.epsjv.fiocruz.br/noticias/reportagem/falta-de-integracao-e-distribuicao-das-bases-de-dados-fragiliza-sistemas-de?utm_source

12. **PÁGINA DA TCU , TRIBUNAL DE CONTAS DA UNIÃO** https://portal.tcu.gov.br/imprensa/noticias/tcu-avalia-programa-agora-tem-especialistas-do-ministerio-da-saude?utm_source

13. **PORTAL CFM , CONSELHO FEDERAL DE MEDICINA** https://portal.cfm.org.br/noticias/em-13-anos-brasil-perde-25-mil-leitos-de-internacao-do-sus/?utm_source

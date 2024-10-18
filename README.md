# Case Técnico - Gabriela_Gazola_DDF_TECH_102024

# Introdução ao case

Como Profissional de Dados na Dadosfera, você irá construir projetos de implementação da plataforma Dadosfera SaaS, em uma empresa, buscando centralizar diversas fontes de dados para aprimorar a tomada de decisões, eficiência operacional e análise estratégica. Após um kickoff bem-sucedido com o cliente, é hora de dar sequência à execução do projeto, enfrentando os desafios específicos delineados pelo cliente.

Seu cliente, uma grande empresa de e-commerce, está com um projeto de contruir uma Plataforma de Dados, com o objetivo de entregar análises descritivas e prescritivas com maior agilidade, menor custo, em todas as áreas da empresa.

# Item 0 - Sobre Agilidade e Planejamento

Crie um artefato que represente todas as etapas do projeto, desde a concepção até a implementação, seguindo as melhores práticas do PMBOK. Pode ser, tanto um gantt chart, um fluxograma, um checklist de tarefas ou um kanban board com as tarefas planejadas. Adicione esse fluxograma na documentação do case.

Avançado: Incluir análises de risco, estimativas de custos, e alocação de recursos. Avançado: Representar interdependências e pontos críticos do projeto.

Link Trello: https://trello.com/invite/b/670d7d63e9e164f58c364c13/ATTI2586c0f1e0699813360efad3d9583ca4ECD62110/case-tecnico-dadosfera

![Captura de Tela (392)](https://github.com/user-attachments/assets/eb1b5a61-c1e2-448a-8bdf-52b72cbc15e7)


# Item 1 - Sobre a Base de Dados

Seguindo o cenário proposto na definição do Case, pesquise e sugira uma base de dados para fazer todo case ponta a ponta.

Para escolher a base foi utilizado o site Kaggle, e como base de dados sugeridas pelo site de acordo com o tema do case, foi selecionado a base de dados disponibilizada no link: https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce


# Item 2.1 - Sobre a Dadosfera - Integrar

Vamos iniciar com o carregamento e posterior análise descritiva dos dados propostos. Utilizando o módulo de Coleta da Dadosfera, conecte a sua base de dados proposta e suba esses dados para a Plataforma.

Lembre-se: você deve carregar, pelo menos, 100.000 registros para que seu case seja avaliado por completo.

**Resposta**

A base de dados escolhida foi carregada com sucesso para a plataforma, podemos acessar pelo link: https://app.dadosfera.ai/pt-BR/collect/pipelines

# Item 3 - Sobre a Dadosfera - Explorar

Usando os seus conhecimentos da documentação da Dadosfera, faça a carga desse dataset, catalogue-o com as informações mais relevantes, seguindo boas práticas de Dicionário de Dados.

**Resposta**

Os datasets foram catalogados, podemos acessar pelo link: https://app.dadosfera.ai/pt-BR/catalog/data-assets

![Captura de Tela (393)](https://github.com/user-attachments/assets/12945e04-7a3c-49bf-bb52-242dd7b2c002)

![Captura de Tela (395)](https://github.com/user-attachments/assets/0068fc6f-b470-43b1-bb1d-c595a4b7b4c4)


# Item 4 - Sobre Data Quality

Após a integração e exploração dos dados do site de e-commerce, você identificou várias inconsistências e dados faltantes que podem impactar negativamente a performance dos modelos de IA e a experiência de compra dos clientes. Como você abordaria a melhoria da qualidade desses dados utilizando as ferramentas e práticas recomendadas pela Dadosfera?

**Resposta**

Para melhorar a qualidade dos dados no e-commerce e otimizar a performance de modelos de IA, é essencial realizar uma análise detalhada para identificar inconsistências, erros e dados ausentes, seguida de uma limpeza, removendo registros duplicados ou incorretos e padronizando formatos para garantir consistência. Ferramentas específicas de validação, enriquecimento e deduplicação devem ser usadas para automatizar esse processo. Além disso, é fundamental treinar os colaboradores sobre boas práticas de entrada e manutenção de dados, enquanto se implementa um monitoramento contínuo, com auditorias regulares e acompanhamento de métricas de qualidade, assegurando melhorias constantes.

Gere um relatório de qualidade dos dados usando uma biblioteca apropriada - great-expectations ou soda-core - para identificar inconsistências e dados faltantes.

Relatório se encontra em: https://github.com/gabrielagazola/Gabriela_Gazola_DDF_TECH_102024/blob/main/report_quality_date.ipynb

# Item 5 - Sobre o uso de GenAI e LLMs - Processar

Traga um dataset desestruturado e, utilizando IA, gere features em cima desses dados.

**Resposta**

As features podem ser acessadas no documento pelo link: https://github.com/gabrielagazola/Gabriela_Gazola_DDF_TECH_102024/blob/main/item5-features.md

![Captura de Tela (397)](https://github.com/user-attachments/assets/209d1fe8-4ee2-410a-8a02-4d1abd40a445)



# Item 6 - Sobre Modelagem de Dados

Com os dados importados, precisamos propor uma modelagem de dados que seja condizente com o cenário dos dados e do cliente.

Crie um modelagem seguindo os princípios de Kimball, Data Vault ou outro - que deve ser explicado e justificado - com 2 visões finais dos dados.

Resposta no link: https://github.com/gabrielagazola/Gabriela_Gazola_DDF_TECH_102024/blob/main/item6.md

# Item 7 - Sobre Análise de Dados - Analisar

Crie uma Coleção com o formato - <mes_ano> assim como no exemplo:

Crie um dashboard que mostre uma análise das categoria e uma análise de série-temporal. Salve a Query SQL utilizada e também o print do resultado da query no documento markdown deste teste. Crie, pelo menos, 5 visualizações/questões em cima dos dados, utilizando 5 tipos de visualizações diferentes.

**Resposta**

As respostas para esse item podem ser encontradas no documento https://github.com/gabrielagazola/Gabriela_Gazola_DDF_TECH_102024/blob/main/item7.md

# Item 8 - Sobre Pipelines

Uma das etapas essenciais de um projeto de Dados é a criação de Pipelines de Dados. Desde o processo de criação de modelos inteligentes, utilizando-se de Machine Learning, até a Engenharia de Dados, com Pipelines de Transformação e Limpeza de Dados.

Agora você tem que criar um pipeline para processar os dados anteriores. Para criar um pipeline, acesse nosso módulo de inteligência e siga este guia na nossa documentação.

# Item 9 - Sobre Data Apps

Agora você tem que criar um Data App utilizando Streamlit para explorar os dados anteriores. Para criar um Data App, acesse nosso módulo de inteligência e siga este guia na nossa documentação.

# Item 10 - Apresentação do Case

Após a primeira reunião com nossa equipe de vendas, você deve fornecer uma solução técnica que atenda às exigências e se encaixe na arquitetura deles. Aqui está o diagrama da arquitetura atual deles:

Você deve mostrar, com base nos seus estudos sobre a Documentação da Dadosfera, a viabilidade de substituirmos essa solução pelo case construído.

Aula 4 – DevOps: pipelines, CI/CD e testes automatizados

Na Aula 4 de DevOps, estudamos o conceito de pipelines e o papel delas nos processos de Integração Contínua (CI) e de Entrega ou Implantação Contínua (CD). O conteúdo mostrou como várias etapas do desenvolvimento de software podem ser automatizadas, desde a alteração do código e a execução de testes até a geração de artefatos e, conforme a configuração, a implantação da aplicação.

Um dos principais conceitos apresentados foi o de pipeline, que pode ser entendida como uma sequência automática de etapas executadas para validar, construir, testar e, depois, disponibilizar uma aplicação. Assim, tarefas que antes seriam feitas manualmente passam a rodar sozinhas sempre que certas condições são cumpridas, como um novo commit ou um pull request.

Aprendemos também sobre os arquivos de configuração no formato .yml ou .yaml, usados para definir as etapas que a pipeline vai executar. Neles é possível configurar os eventos que disparam a execução, os ambientes, os comandos, as dependências entre etapas, as ferramentas empregadas, os testes, os builds e outras ações necessárias para automatizar o desenvolvimento e a entrega.

Ao longo da aula, usamos o GitHub Actions como exemplo prático. Pudemos acompanhar diretamente no GitHub a execução de uma pipeline, vendo cada etapa e conferindo os resultados mostrados pela plataforma. A demonstração ajudou a entender melhor a relação entre o código guardado no repositório, o arquivo .yml e a execução automática das tarefas.

Outro ponto estudado foi o encadeamento de pipelines e de etapas. Uma pipeline pode ter várias etapas que precisam seguir uma ordem determinada. Por exemplo, primeiro se instalam as dependências, depois a aplicação é compilada, em seguida os testes são executados e, só se tudo isso terminar com sucesso, acontece a implantação. Esse processo cria uma sequência de validações antes que uma versão do software seja liberada.

Também se discutiu a possibilidade de ter mais de um arquivo .yml no mesmo projeto. Isso é permitido e pode ser útil quando há processos diferentes a automatizar. Por exemplo, um arquivo pode cuidar dos testes, outro do build e outro do deploy. Dessa forma, o projeto passa a ter diferentes workflows, cada um com uma finalidade específica.

Outra dúvida levantada na aula foi sobre a execução simultânea de pipelines. Workflows ou etapas diferentes também podem rodar em paralelo, desde que não haja dependência exigindo que uma espere o término da outra. A execução paralela pode diminuir o tempo total de processamento, sobretudo quando existem vários testes independentes que podem ser feitos ao mesmo tempo.

Além das pipelines, estudamos a importância dos testes automatizados dentro do CI/CD. Com eles, os problemas são identificados automaticamente antes que uma alteração seja integrada ou chegue aos usuários. Dessa maneira, a pipeline também funciona como uma barreira de qualidade, impedindo que alterações com falhas avancem para as etapas seguintes.

Entre os principais tipos de testes abordados, estão os testes unitários, os testes de integração e os testes de performance.

Os testes unitários servem para verificar pequenas partes isoladas da aplicação. Um exemplo seria testar separadamente uma função que faz um cálculo ou valida um dado. Por serem menores e mais específicos, costumam ser rápidos e podem ser executados com frequência durante o desenvolvimento.

Os testes de integração verificam como diferentes componentes do sistema funcionam juntos. Um exemplo seria conferir se uma aplicação consegue se comunicar corretamente com um banco de dados ou se um serviço consegue consumir uma API sem problemas. Esse tipo de teste é importante porque uma aplicação pode ter componentes que funcionam bem sozinhos, mas dão problema quando usados em conjunto.

Já os testes de performance buscam analisar o comportamento da aplicação quanto ao desempenho. Podem ser usados para medir o tempo de resposta, o número de requisições suportadas, o consumo de recursos e o comportamento do sistema sob diferentes níveis de carga.

Usar esses testes na pipeline permite descobrir problemas mais cedo. Em vez de encontrar um erro apenas depois que a aplicação foi publicada, o processo de CI/CD pode rodar as verificações automaticamente e interromper o fluxo quando uma etapa importante falhar.

A aula também mostrou que CI/CD não significa somente fazer o deploy de forma automática. O conceito envolve montar um processo confiável e repetível para validar e entregar software. A pipeline pode incluir várias etapas, como análise do código, instalação de dependências, compilação, execução de testes, geração de artefatos, verificações de segurança e implantação.

Como atividade da Aula 4, foi proposta uma pesquisa com base no artigo acadêmico "Practical Comparison Between the CI/CD Platforms Azure DevOps and GitHub", de Vladislav Manolov, Daniela Gotseva e Nikolay Hinov, publicado na revista Future Internet, volume 17, número 4, em 2025. O artigo traz uma comparação prática entre Azure DevOps e GitHub, analisando suas características e seu uso em processos de CI/CD.

O objetivo da atividade é identificar as ferramentas e tecnologias citadas pelos autores e fazer uma análise comparativa entre as plataformas, considerando características, funcionalidades, vantagens, limitações e as situações em que cada solução pode ser mais indicada. Na pesquisa, esse material foi organizado em seções sobre as ferramentas abordadas, o Azure DevOps, o GitHub e o GitHub Actions, a comparação entre Azure Pipelines e GitHub Actions, a integração contínua, a segurança, os testes automatizados, a escalabilidade e o desempenho, os custos e os critérios para escolher entre as plataformas.

O artigo compara principalmente o Azure DevOps e o GitHub. O Azure DevOps é apresentado como uma suíte completa de ferramentas de DevOps mantida pela Microsoft, com recursos como Azure Pipelines, Azure Repos, Azure Boards, Azure Test Plans e Azure Artifacts, além do Azure DevOps Server, que pode ser instalado na infraestrutura da própria organização, e do TFVC, um sistema de controle de versão centralizado. No GitHub, o principal recurso para CI/CD é o GitHub Actions, usado para automatizar workflows, complementado por itens como GitHub Advanced Security, Dependabot, GitHub Enterprise Cloud, GitHub Enterprise Server e GitHub Marketplace. O artigo cita ainda outras tecnologias que costumam estar integradas a essas plataformas, como Docker, Kubernetes, AWS, Google Cloud, NUnit, xUnit, Selenium e Azure Active Directory.

A comparação feita pelos autores considera diversos aspectos, como automação de CI/CD, controle de versão, segurança, testes automatizados, escalabilidade e desempenho, integração com serviços de nuvem, custos e experiência de uso. O Azure DevOps tem uma abordagem mais estruturada e voltada a ambientes corporativos, reunindo código, pipelines, gestão de projetos, testes e artefatos em um só lugar. O GitHub, por sua vez, é mais simples e centrado no Git, nos repositórios e na experiência do desenvolvedor, e usa o GitHub Actions para automatizar workflows definidos em arquivos YAML dentro do próprio repositório.

Um dos pontos importantes da pesquisa é entender que não existe uma única ferramenta que seja a melhor para todos os projetos. A escolha depende das necessidades da organização, do tamanho da equipe, da infraestrutura disponível, dos requisitos de segurança, do nível de controle exigido, do orçamento e da estratégia de DevOps adotada.

O Azure DevOps tende a ser mais indicado para empresas de grande porte e projetos corporativos, principalmente quando há uso do ecossistema Microsoft, necessidade de governança rigorosa, vários ambientes de implantação ou exigência de infraestrutura híbrida ou on-premises. O GitHub costuma ser a escolha mais natural para equipes pequenas ou médias, projetos open source e times que já trabalham com fluxos baseados em Git e querem configurar o CI/CD com rapidez. Os autores destacam justamente que a escolha entre as plataformas deve considerar fatores como estratégia de desenvolvimento, segurança, escalabilidade, infraestrutura e orçamento.

Assim, a Aula 4 uniu a teoria de DevOps a uma aplicação prática. Primeiro, foram apresentados os conceitos de pipelines, arquivos .yml, execução de etapas, testes automatizados e encadeamento de processos. Depois, esses conceitos foram observados na prática com o GitHub Actions. Por fim, a atividade proposta amplia o conteúdo da aula ao exigir uma análise acadêmica das principais plataformas usadas para implementar processos de CI/CD, o que ajuda a perceber que há soluções diferentes e que cada uma tem características, vantagens e limitações próprias.

Referência da atividade:

MANOLOV, Vladislav; GOTSEVA, Daniela; HINOV, Nikolay. Practical Comparison Between the CI/CD Platforms Azure DevOps and GitHub. Future Internet, v. 17, n. 4, p. 153, 2025. DOI: https://doi.org/10.3390/fi17040153. Disponível em: https://www.mdpi.com/1999-5903/17/4/153. Acesso em: 5 set. 2026.

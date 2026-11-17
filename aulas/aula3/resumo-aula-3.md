Resumo da aula 3 — dependências e ci/cd

Na aula de hoje, ampliamos o que sabíamos sobre dependências e compreendemos melhor o papel delas no desenvolvimento de um projeto. Também retomamos os conceitos de CI/CD, em especial a ideia de automatizar processos para facilitar a integração, os testes e a entrega do código.

Ao longo da aula, clonamos um repositório do GitHub para observar, na prática, como um projeto se comporta quando é baixado e executado em outro ambiente. Com isso, percebemos que um projeto não é formado só pelo código que escrevemos: ele também precisa de várias bibliotecas, pacotes e ferramentas para rodar corretamente.

Um dos pontos mais importantes foi perceber que as versões das dependências podem gerar problemas. Uma aplicação pode funcionar sem falhas no computador de uma pessoa e dar erro em outro, se as versões das bibliotecas forem diferentes ou se alguma dependência estiver ausente. Por isso, é essencial definir e controlar bem as dependências usadas no projeto, para que todos trabalhem com uma configuração compatível.

Vimos também a importância dos arquivos de configuração, como o package.json, que guarda informações relevantes do projeto e de suas dependências. Ao clonar o repositório, por exemplo, não é preciso baixar uma a uma as bibliotecas utilizadas: basta rodar o npm install, que instala o que o projeto precisa conforme suas configurações.

Depois de instalar as dependências, executamos o projeto com o npm start e conferimos se ele funcionava direito. A experiência mostrou, na prática, como o código pode ser compartilhado por meio de um repositório e, depois, configurado e executado por outra pessoa.

Além disso, entendemos melhor por que enviar o código para um repositório é tão importante. A finalidade não é só guardar o código, mas permitir que outras pessoas acessem o projeto, o clonem, instalem suas dependências e deem continuidade ao desenvolvimento. Isso se liga diretamente ao uso de CI/CD, já que, em um fluxo de desenvolvimento, o código enviado ao repositório pode passar por processos automáticos de instalação, testes e validação.

Ao final da aula, ficou mais clara a relação entre código, dependências, versões, GitHub e CI/CD, e a percepção de que manter as dependências organizadas e as versões sob controle é fundamental para evitar problemas e garantir que o projeto funcione de forma consistente em ambientes diferentes.

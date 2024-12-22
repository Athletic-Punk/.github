# Athletic Punk - Saúde nos Esportes
## Organização do projeto
Para manter um trabalho organizado usando o [GitHub](https://github.com/), iremos usar as seguintes práticas:

## Commits
- **Commits frequentes**: Faça commits frequentes com mudanças pequenas e específicas.
- **Mensagens de commit descritivas**: Escreva mensagens de commit claras e descritivas que expliquem o que foi alterado e por quê.
    - Exemplo: `STYLE: Continuação da responsividade` ou `FEAT: Implementando página de contato`

***OS COMMITS DEVEM SER ESCRITOS EM INGLÊS NO FORMATO ACIMA***

#

### Padrões de commit
- Padrões de commit ajudam a manter um histórico de commits claro e consistente, facilitando a compreensão das mudanças no projeto. Usaremos os padrões da **Conventional Commits**.
- Como dito anteriormente, o commit deve ter a seguinte estrutura: `<PADRÃO_DE_COMMIT>: <descrição>`

### Tipos de commit
- **FEAT**: Utilizado para introdução de uma nova funcionalidade.
    - Exemplo: `FEAT: adiciona página de login`
- **FIX**: Utilizado para correção de bugs
    - Exemplo: `FIX: corrige erro de carregamento de página`
- **DOCS**: Utilizado para mudanças na documentação
    - Exemplo: `DOCS: atualiza README com instruções de instalação`
- **STYLE**: Utilizado para mudanças que não afetam o significado do código (espaços em branco, formatação, ponto e vírgula, etc)
    - Exemplo: `STYLE: formata código de acordo com o padrão ESLint`
- **REFACTOR**: Utilizado para mudanças no código que não corrigem bugs nem adicionam funcionalidades
    - Exemplo: `REFACTOR: renomeia variáveis para melhorar legibilidade`
- **PERF**: Utilizado para mudanças que melhoram a performance
    - Exemplo: `PERF: otimiza função de busca`
- **TEST**: Utilizado para adição ou correção de testes
    - Exemplo: `TEST: adiciona testes unitários para a função de login`
- **BUILD**: Utilizado para mudanças que afetam o sistema de build ou depêndencias externas (como npm)
    - Exemplo: `BUILD: atualiza dependências do projeto`
- **CI**: Utilizado para mudanças em arquivos e scripts de configuração
    - Exemplo: `CI: adiciona configuração do GitHub Actions`
- **CHORE**: Utilizado para mudanças em tarefas de manutenção do projeto que não alteram o código fonte ou testes
    - Exemplo: `CHORE: limpa arquivos temporários`
- **REVERT**: Utilizado para reverter um commit anterior
    - Exemplo: `REVERT: reverte commit 123455`


## Issues
- **Gerenciamento de tarefas**: Usaremos as issues para registrar bugs, solicitações de funcionalidades e tarefas.
- **Labels e assignees**: Utlizaremos as labels (categorias) para categorizar as issues e atribui-lás para aassignees (responsáveis) para garantir o adequado gerenciamento das tasks.

## Branches
- **Uso de branches**: Criação de branches para diferentes funcionalidades, correções de bugs ou experimentos. 
    - **main**: Branch de produção;
    - **dev**: Branch de desenvolvimento;
    - **funcionalidades específicas**: Branchs FEAT, FIX, etc.
- **Nomenclatura consistente**: Utilize convenções de nomenclatura clara e consistente para as branches, como, por exemplo: `FEAT: nome-da-funcionalidade` ou `FIX: descrição-do-bug`

***OS TÍTULOS DAS BRANCHES DEVEM SER ESCRITAS EM INGLÊS NO FORMATO ACIMA***

## Pull Requests (PRs)
- **Revisão de código**: Use pull requests para revisarmos e discutirmos antes de mesclá-lo na branch dev.
- **Descrições detalhadas**: Inclua descrições detalhadas nos PRs para explicar as mudanças e o contexto. Tipos de descrições:
    - Funcionalidades implementadas
    - Bugs corrigidos
    - Melhorias de código
    - Refatorações
- **Resumo**: Apresente uma descrição breve sobre o propósito e impacto do Pull Request.

***O TÍTULO, A DESCRIÇÃO E O RESUMO DOS PULL REQUESTS DEVEM SER ESCRITAS EM INGLÊS SEGUINDO O PADRÃO DO COMMIT PRINCIPAL REALIZADO DURANTE A IMPLEMENTAÇÃO***

Exemplo: 

Título: `FIX: refatoração das rotas`

Descrição: ` Branch criada para a resolver o bug nas rotas...`

### Informações Adicionais
- **Reviewers**: pessoas responsáveis pela revisão das alterações realizas **(Adiconar Nicole como reviewer)**
- **Assignees**: pessoas responsáveis pelas alterações realizadas
- **Label**: categoria relacionada às mudanças realizadas:
    - FRONTEND
    - BACKEND
    - DESIGN
    - DOCS

#

### COMO FAZER UM PULL REQUEST ?
1. **Atualize sua branch local**
    - Antes de começar a trabalhar, atualize sua branch local para garantir que você tenha as últimas mudanças da branch principal.
    ```
    git checkout dev
    git pull origin dev
    git checkout -b minha-branch
    ```
2. **Faça commits pequenos e descritivos**
    - Faça commits frequentes e com mensagens descritivas que expliquem claramente o que foi alterado.
    ***OS COMMITS DEVEM SER ESCRITOS EM INGLÊS NO FORMATO ABAIXO***
    ```
    git add .
    git commit -m "PADRÃO_DE_COMMIT": mensagem de commit
    ```

3. **Resolva conflitos de merge**
    - Antes de abrir o PR, atualize sua branch com as últimas mudanças da branch principal para resolver possíveis conflitos.
    ```
    git checkout dev
    git pull origin dev
    git checkout minha-branch
    git merge dev
    ```

4. **Crie o Pull Request**
    - Envie sua branch para o repositório remoto e crie o PR.
    ```
    git push origin minha-branch
    ```
    - No GitHub, vá para a página do repositório, clique em "Pull Requests" e depois em "New pull request". Selecione sua branch e a branch dev e clique em "Create Pull Request".

5. **Preencha a descrição do PR**
    - Forneça uma descrição detalhada do que foi alterado, incluindo o contexto, a razão das mudanças e qualquer informação relevante.
    - Adicione referência as issues, usando #número-da-issue.

6. **Solicite revisões**
    - Adicione a Nicole como revisora do PR, para a revisão e fornecimento de um feedback sobre o código.

7. **Responda o Feedback**
    - Esteja preparado para fazer mudanças adicionais com base no feedback dos revisores. Faça os ajustes necessários e atualize o PR.
    ```
    git add .
    git commit -m ""PADRÃO_DE_COMMIT": mensagem de commit"
    git push origin minha-branch
    ```

8. **Rebase, se necessário**
    - Se a dev tiver avançado, será necessário fazer um rebase para garantir que seu PR esteja atualizado.
    ```
    git fetch origin
    git rebase origin/dev
    ```

9. **Mescle o PR**
    - Após a aprovação dos revisores e a passagem de todos os testes, você pode mesclar o PR. No GitHub, você tem três principais opções de merge para mesclar pull requests (PRs) em um repositório: **Merge Commit, Squash and Merge, e Rebase and Merge**, mas usaremos a Rebase and Merge.
        - Rebase and merge:
            - **Como funciona?**: Reaplica os commits de uma branch sobre a base da branch de destino, criando uma linha de tempo linear.
            - **Como usar?**
            ```
            git checkout minha-branch
            git rebase dev
            ```
            **Resolva os conflitos e continue**
            ```
            git checkout dev
            git merge minha-branch
            ```

## Documentação
- **README.md**: Iremos manter o arquivo [README.md](./profile/README.md) atualizado com as informações e objetivos do projeto.
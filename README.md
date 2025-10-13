# Artefatos

[Artefatos de Programação](https://www.notion.so/Artefatos-de-Programa-o-110256ceaea780d48619d28b60bc9150?pvs=21)

- **Semana 02**
    
    [Análise Exploratória Avançada dos Dados com Jupyter + Poetry E criação de Data Lake](https://www.notion.so/An-lise-Explorat-ria-Avan-ada-dos-Dados-com-Jupyter-Poetry-E-cria-o-de-Data-Lake-110256ceaea780dda353d27861021435?pvs=21)
    
    [Arquitetura de Dados com UML de Componentes (Arquitetura Medalhão) E Precificação](https://www.notion.so/Arquitetura-de-Dados-com-UML-de-Componentes-Arquitetura-Medalh-o-E-Precifica-o-110256ceaea7809c9218f0dbbac25b21?pvs=21)

---

# Diretrizes do Módulo 8

Este documento estabelece diretrizes claras para a utilização de boas práticas no desenvolvimento de software, visando a organização e a qualidade do código. Todos os alunos devem seguir as instruções abaixo:

## **Uso de Conventional Commits**

- **Padrão Obrigatório**: Todos os commits devem seguir a especificação dos **Conventional Commits**. Isso implica que cada mensagem de commit deve ser estruturada da seguinte forma:Exemplos de tipos incluem:
    
    `text<tipo>[escopo opcional]: <descrição curta>
    
    [descrição mais detalhada opcional]`
    
    - **`feat`**: nova funcionalidade
    - **`fix`**: correção de bug
    - **`docs`**: alterações na documentação
    - **`refactor`**: refatoração do código
    - **`test`**: adição ou alteração de testes.
- **Proibições**: Não serão aceitos emojis nas mensagens de commit, nem commits que não sigam o padrão estabelecido. Mensagens vagas ou genéricas, como "melhorias" ou "atualizações", são inaceitáveis.

## **Documentação**

- **Formatos Aceitos**: A documentação deve ser apresentada em duas plataformas: **MkDocs** e no padrão do escritório de projetos. Os alunos podem copiar e colar informações entre essas plataformas, mas devem ajustar o conteúdo para garantir clareza e adequação ao formato requerido.

## **Análise de Entregas**

- **Revisão na Main**: Todas as entregas de sprint serão analisadas diretamente na branch **main** do repositório. É imprescindível que os alunos sigam o padrão **GitFlow**, que é um modelo de branching que organiza o desenvolvimento em diferentes tipos de branches.

## **O que é GitFlow?**

É uma estratégia popular de branching do Git, introduzida por Vincent Driessen em 2010, que visa simplificar o gerenciamento de lançamentos. Ele utiliza várias branches principais e define papéis específicos para cada uma delas:

1. **Main**: Contém o código pronto para produção.
2. **Develop**: Serve como uma branch de integração onde novas funcionalidades são combinadas antes de serem lançadas.
3. **Feature Branches**: Criadas a partir da branch develop para trabalhar em novas funcionalidades.
4. **Release Branches**: Usadas para preparar novas versões antes do lançamento final.
5. **Hotfix Branches**: Criadas a partir da main para corrigir problemas críticos rapidamente.

O fluxo típico do GitFlow envolve criar uma branch develop a partir da main, adicionar novas funcionalidades em feature branches, e quando tudo estiver pronto, mesclar essas alterações na develop e, eventualmente, na main.

## **Qualidade do Código**

- **Código Limpo**: O código deve ser escrito de maneira que não necessite de comentários extensivos para ser compreendido. Isso significa que todos devem seguir rigorosamente o padrão de **programação orientada a objetos**, aplicando princípios como encapsulamento, herança e polimorfismo nos pacotes e ETLs (Extract, Transform, Load).

Ao seguir estas diretrizes, garantimos um ambiente de desenvolvimento mais organizado e colaborativo, facilitando a comunicação entre os membros da equipe e melhorando a qualidade do produto final.
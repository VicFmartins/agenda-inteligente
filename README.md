# Agenda Inteligente

Aplicacao web em .NET 8 com Blazor para organizacao de compromissos, tarefas e rotinas pessoais em uma interface simples, moderna e pronta para evolucao.

## Visao geral

O projeto nasce como uma base para uma agenda digital inteligente, com foco em produtividade, clareza visual e possibilidade de crescimento para recursos como notificacoes, categorizacao de compromissos, prioridades e automacoes.

Nesta versao, o repositorio entrega uma base web funcional em Blazor Server, organizada para servir como ponto de partida de produto e portfolio.

## Objetivo do produto

O Agenda Inteligente busca resolver um problema comum: centralizar compromissos, tarefas e contexto do dia em uma experiencia unica, leve e de facil manutencao.

O direcionamento do projeto aponta para:

- gestao de compromissos e eventos;
- acompanhamento de prioridades;
- visao diaria e semanal;
- evolucao futura para lembretes e automacoes;
- interface web simples de operar e facil de expandir.

## Stack utilizada

- .NET 8
- ASP.NET Core
- Blazor Server com Razor Components interativos
- CSS isolado + estilos globais
- Visual Studio / CLI `dotnet`

## Estrutura do projeto

```text
.
|- AgendaInteligente.Web.sln
|- AgendaInteligente.Web.csproj
|- Program.cs
|- appsettings.json
|- Components
|  |- App.razor
|  |- Routes.razor
|  |- Layout
|  `- Pages
`- wwwroot
   |- app.css
   `- bootstrap
```

## Arquitetura atual

O projeto esta estruturado como uma aplicacao web server-side em Blazor:

1. `Program.cs` configura o pipeline HTTP e os servicos do app.
2. `App.razor` define a base HTML e os assets globais.
3. `Routes.razor` centraliza o roteamento.
4. `Components/Layout` concentra o shell visual da aplicacao.
5. `Components/Pages` contem as paginas principais.

Essa organizacao deixa a base enxuta e adequada para evoluir por features sem acoplamento desnecessario.

## Funcionalidades atuais

- pagina inicial institucional do produto;
- pagina com visao funcional do fluxo da agenda;
- pagina com arquitetura e roadmap tecnico;
- layout navegavel e responsivo;
- pipeline padrao de execucao com HTTPS, antiforgery e static files.

## Como executar localmente

### Requisitos

- SDK do .NET 8 instalado

### Executando com CLI

```bash
dotnet restore
dotnet build
dotnet run --project AgendaInteligente.Web.csproj
```

Aplicacao padrao:

- `https://localhost:7xxx`
- `http://localhost:5xxx`

As portas exatas dependem do perfil local do ASP.NET Core.

## Configuracao

Os arquivos `appsettings.json` e `appsettings.Development.json` ja contem a configuracao basica de logging.

Se o projeto evoluir para integracoes externas, o recomendado e:

- manter segredos fora do codigo;
- usar variaveis de ambiente;
- separar configuracoes por ambiente.

## Estado atual do projeto

O projeto esta limpo para publicacao inicial:

- compila sem erros;
- nao depende de segredos hardcoded;
- nao inclui artefatos desnecessarios do Visual Studio no versionamento;
- possui base visual coerente com o nome do produto.

## Proximos passos recomendados

- adicionar modelo de dominio para compromissos, categorias e usuarios;
- integrar persistencia com Entity Framework Core;
- criar CRUD de eventos e tarefas;
- incluir autenticacao, notificacoes e filtros por periodo;
- adicionar testes automatizados.

## Publicacao no GitHub

Depois de criar o repositorio remoto, basta conectar o projeto local:

```bash
git init
git add .
git commit -m "feat: initial Agenda Inteligente web application"
git remote add origin <URL_DO_REPOSITORIO>
git branch -M main
git push -u origin main
```

## Posicionamento para portfolio

Este projeto comunica bem:

- base moderna com .NET 8;
- preocupacao com organizacao de interface e estrutura;
- ponto de partida claro para um produto de produtividade;
- capacidade de transformar um template cru em uma base de produto mais apresentavel.

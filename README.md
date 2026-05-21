# Web OS Tool Installer

Repositório de pacotes para o **Web OS** — sistema operacional rodando no navegador.

## Como usar

1. Abra o Web OS no seu navegador
2. Abra o aplicativo **Instalador de Ferramentas**
3. Clique em **Atualizar** para buscar os pacotes disponíveis
4. Clique em **Instalar** nos aplicativos que desejar

## Pacotes disponíveis

| Pacote | Descrição |
|--------|-----------|
| Calculator | Calculadora básica |
| Notepad | Bloco de notas |
| Computer | Explorador de drives |
| About | Sobre o sistema |
| Settings | Configurações do sistema |
| Task Manager | Gerenciador de tarefas |
| Browser | Navegador web com abas |
| File Manager | Gerenciador de arquivos virtual |

## Estrutura

```
web_toolinstaller/
  README.md
  packages.json          # Manifesto com lista de pacotes
  packages/              # Arquivos JSON dos aplicativos
    calculator.json
    notepad.json
    ...
  icons/                 # Ícones SVG dos aplicativos
    calculator.svg
    notepad.svg
    ...
```

## Desenvolvimento

Para adicionar um novo pacote:

1. Crie o arquivo `.json` do app em `packages/`
2. Adicione o ícone SVG em `icons/`
3. Adicione a entrada no `packages.json`
4. Faça push para o repositório

O formato do JSON do pacote segue o padrão do Web OS:

```json
{
  "id": "meuapp",
  "name": "Meu App",
  "icon": "meuapp",
  "width": 500,
  "height": 400,
  "css": "...",
  "js": "AppManager.register('meuapp',{init:function(b){...}})"
}
```

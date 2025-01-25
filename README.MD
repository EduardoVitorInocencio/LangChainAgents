# Projeto de Estudo sobre LangChain Agents

## Estrutura do Projeto

- `main.py`: Contém a lógica principal para invocar a função `agent_chain` e realizar a consulta.

## Dependências

Este projeto depende das seguintes bibliotecas:
- `dotenv`: Para carregar variáveis de ambiente a partir de um arquivo `.env`.
- `langchain`: Para utilizar agentes e ferramentas de linguagem.
- `langchain_openai`: Para utilizar o modelo de linguagem `ChatOpenAI`.

## Como Executar

1. Certifique-se de ter o Python instalado em sua máquina.
2. Instale as dependências necessárias.
3. Execute o script `main.py`.

### Passos para Execução

1. **Clone o repositório:**

    ```bash
    git clone <URL_DO_REPOSITORIO>
    cd <NOME_DO_REPOSITORIO>
    ```

    Este comando clona o repositório do projeto para sua máquina local e navega até o diretório do projeto.

2. **Instale as dependências:**

    ```bash
    pip install -r requirements.txt
    ```

    Este comando instala todas as dependências listadas no arquivo [requirements.txt](http://_vscodecontentref_/1).

3. **Execute o script:**

    ```bash
    python main.py
    ```

    Este comando executa o script `main.py`.

## Explicação do Código

### Carregando Variáveis de Ambiente

```python
from dotenv import load_dotenv, find_dotenv

load_dotenv(find_dotenv())
```

• load_dotenv(): Carrega as variáveis de ambiente a partir de um arquivo .env.
• find_dotenv(): Encontra automaticamente o arquivo .env no diretório atual ou em diretórios superiores.

### Importando Bibliotecas

``` python
from langchain.agents import load_tools
from langchain_openai import ChatOpenAI
from langchain.agents import AgentType
```
• load_tools: Função para carregar ferramentas específicas.
• ChatOpenAI: Classe para utilizar o modelo de linguagem ChatOpenAI.
• AgentType: Enumeração para tipos de agentes.

### Configurando o Modelo de Linguagem

```python
llm = ChatOpenAI(model="gpt-4o-mini")
```

• ChatOpenAI(model="gpt-4o-mini"): Inicializa o modelo de linguagem ChatOpenAI com o modelo gpt-4o-mini.

### Carregando Ferramentas

```python
tool_names = ["llm-math"]
tools = load_tools(tool_names, llm=llm)
```

• tool_names: Lista de nomes de ferramentas a serem carregadas.
• load_tools(tool_names, llm=llm): Carrega as ferramentas especificadas utilizando o modelo de linguagem llm.

### Invocando a Função agent_chain

```python
agent_chain.invoke(input="Which is the most famous singer from there?")
```

• agent_chain.invoke(input="..."): Invoca a função agent_chain com a entrada especificada para consultar o cantor mais famoso de uma localidade.

### Exemplo de Uso

O script main.py contém a seguinte linha de código:


Esta linha invoca a função agent_chain para consultar o cantor mais famoso de uma localidade específica.

# Contribuição

Se você deseja contribuir com este projeto, por favor, siga os passos abaixo:

1. Faça um fork do repositório.
2. Crie uma nova branch (git checkout -b feature/nova-feature).
3. Faça suas alterações e commit (git commit -m 'feat: Adicione nova feature').
4. Envie para o branch (git push origin feature/nova-feature).
5. Abra um Pull Request.

Licença
Este projeto está licenciado sob a Licença MIT. Veja o arquivo LICENSE para mais detalhes.
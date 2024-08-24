Olá, repositório criado por mim para contemplar práticas de git, github e python e ambiente virtual do python, aulas ministradas pelo professor **Juliano Marcelino**.

Ambiente: Windows, utilizando PowerShell, VSCode e Python3

<details><summary><h2>Criando a pasta de trabalho via PS</h2></summary>

1) Abra o cmd e execute o comando powershell em modo admin:
```sh
powershell start-process powershell -verb runas
```
2) Acesse via PS a pasta documentos local
```sh
PS C:\> cd .\Users\Diego\Documents\
```
3) Execute o comando **mkdir** para criar o diretório com o nome do ambiente virtual desejado
```sh
PS C:\Users\Diego\Documents> mkdir firstVenv
```
Agora temos a pasta para configurar o ambiente virtual.
</details>

<details><summary><h2>Alterar a politica de execução de scripts do PS</h2></summary>
Para executar o script de ativação do ambiente virtual do python3 é preciso alterar a politica de execução de script do Windows que por padrão está desabilitada, faça isso executando o comando abaixo no PS.

```sh
PS C:\Users\Diego\Documents> Set-ExecutionPolicy AllSigned
```
**OBS**: Quando solicitado permitir a alteração da política de execução de scripts, digite "A" para aceitar a alteração e assim poder prosseguir com a execução do script para ativar o ambiente virtual python3 via PS.
</details>
<details><summary><h2>Criar ambiente virtual via PS</h2></summary>
Certifique que a permissão para executar scripts está habilitada conforme o tópico anterior, agora iremos criar o ambiente virtual com o comando a seguir na pasta que criada ./firstVenv via PS:

```sh
PS C:\Users\Diego\Documents> python -m venv .\firstVenv\
```
Se o comando for executado corretamente, listando a estrutura da pasta ficará da seguinte forma:

```sh
Mode                 LastWriteTime         Length Name
d-----        24/08/2024     14:53                Include
d-----        24/08/2024     14:53                Lib
d-----        24/08/2024     14:53                Scripts
-a----        24/08/2024     14:53            193 pyvenv.cfg
```
</details>
<details><summary><h2>Ativar o ambiente virtual via PS</h2></summary>
Ambiente criado corretamente, basta ativar para começar a trabalhar no projeto de forma isolada. Faça isso executando o script de ativação com o comando abaixo.

```sh
PS C:\Users\Diego\Documents\firstVenv> .\firstVenv\Scripts\Activate.ps1
```
Se até aqui tudo ocorrer bem, você pode incluir seus arquivos do projeto em python em um ambiente virtual isolado e seguro.

**OBS**: Suba seus arquivos para o .github, configure o  arquivo .gitignore e envie apenas o que for necessário, documente os passos criando um arquivo README.md de fácil compreensão.
</details>

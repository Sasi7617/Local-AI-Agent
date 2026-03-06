Initially installed Ollama and satrt running it on cmd through command "ollama" and "Ollama list" will help you see what all llm models are currently available in your system.

"Ollama pull <llm-model-name>" will help you pull the particular llm model into your system for ex, 
"ollama pull llama3.2"

To pull the embedding model use commmand "ollama pull mxbai-embed-large"

1.On VS code terminal, initially get into virtual env through command 
python -m venv venv  

2.Now activtae the virtual env through
.\venv\Scripts\activate

3.Now install a;; the dependencies required as mentioned in requirements.txt
pip install ollama langchain pandas langchain-chroma langchain-ollama

4.To run the python code through teerminal use command 
python .\main.py



Here since the version conflict issue occurred due to ollama libraries require python 3.12 version instead of python 3.14(updated) version I used following method to ensure python 3.12 version is used particularly for this project

In terminal run below cmds,
$uvPath = "$env:USERPROFILE\.local\bin"
if ($env:Path -notlike "*$uvPath*") {
    [Environment]::SetEnvironmentVariable("Path", [Environment]::GetEnvironmentVariable("Path", "User") + ";$uvPath", "User")
    $env:Path += ";$uvPath"
    Write-Host "Success! uv has been added to your Path." -ForegroundColor Green
} else {
    Write-Host "uv is already in your Path, try restarting your terminal again." -ForegroundColor Yellow
}

The above command will install uv 

Once uv installed create new venv and activate it using below cmds,
uv venv --python 3.12
.\.venv\Scripts\activate

now install required dependencies using cmd(make sure you are in venv),
uv pip install ollama pandas 


project github Url ---> https://github.com/techwithtim/LocalAIAgentWithRAG/blob/main/README.md
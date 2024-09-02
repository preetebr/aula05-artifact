# CI/CD Impacta -Aula 05


#### 1) Dentro de sua conta pessoal no GitHub, no repo criado no exercício da aula citado acima (aula-05-artifact), acrescentar no arquivo de workflow criado (go-example.yml) um scheduler de execução do evento push presente no arquivo, que seja trigado a cada 15 min, de segunda à sábado

#### 2) Acrescentar dois novos jobs no workflow existente (go-example.yml), com a dependência de execução e conclusão do job criado no exercício da aula (identificador build-go). Além disso, os jobs devem ter as seguintes características:

###### 1º JOB

- Identificador: download-and-run-linux
- Name: Download and run Linux
- Runner: ubuntu (última versão)
- Primeiro Step: usar a action de checkout no repo
- Segundo Step: usar a action de download do artefato, passando como argumento o nome do artefato chamado linux, gerado durante o exercício
- Terceiro Step: executar no S.O o comando para ler as opções do script run.sh (comando: source ./run.sh)



###### 2º JOB


- Identificador: download-only-windows
- Name: Download Windows
- Runner: windows (última versão)
- Primeiro Step: usar a action de checkout no repo
- Segundo Step: usar a action de download do artefato, passando como argumento o nome do artefato chamado windows, gerado durante o exercício


#### 3) Fazer os devidos commits e executar os workflows. Compartilhar o link do repositório com o professor com as evidências de criação e execução do workflow
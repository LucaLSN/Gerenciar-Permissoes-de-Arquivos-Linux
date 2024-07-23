# Comandos Para USO BÁSICO do Linux via Command Line
------
Os comandos abaixo são recomendáveis para maninupulação básica
de arquivos e repositórios, neste caso foi utilizado como base: 
Linux Mint que é uma distribuição Linux orientada pela comunidade baseada no Ubuntu (que, por sua vez, é baseada no Debian),
fornecida com uma variedade de aplicativos gratuitos e de código aberto.
------
### mkdir
  - criar diretório(pasta)
### rmdir 
  - remover diretório(pasta)
### touch
  - criar arquivo(especificar o tipo, exemplo: .txt)
### rm 
  - remover arquivo
### grep 
  - filtrar algo dentro do arquivo (geralmente strigs)
  -  exemplo de uso: grep "OS" logs.txt
  -  não ser case sensitive: grep -i "OS" logs.txt
### mv 
  - mover um arquivo de um local para outro
  - exemplo: mv arquivo.txt pastamover -- comando move o arquivo.txt para a pastamover (se no mesmo diretório)
---------
# Gestão BÁSICA de Permissões Linux via Command Line
No Linux as permissões são mostradas como uma string sequência de 10 digitos
"**drwxrwxrwx**"

Onde:
**d** = refere-se as permissões de um diretório. Se for **-** refere-se a um arquivo

**r** = refere-se a permissão de leitura.(read)

**w** = refere-se a permissão de escrita.(write)

**x** = refere-se a permissão de executar.(execute)

Primeiro sequência de 3 digítos: **rwx** refere-se as permissões do usuário. (u)

Segundo sequência de 3 digítos: **rwx** refere-se as permissões do grupo. (g)

Terceira sequência de 3 digítos: **rwx** refere-se as permissões de outros.(o)
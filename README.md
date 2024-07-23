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

## Explorando as permissões existentes

Durante a mudança das permissões de acesso, leitura e execução é importante visualizar quais permissões já estão habilitadas ou desabilitadas.

Algumas pastas e arquivos no Linux se mantém ocultos por via de regra para evitar acessos acidentais, você pode mostrar os arquivos ocultos utilizando o comando:

**ls -a** : Exibe arquivos ocultos. Os arquivos ocultos começam com um ponto (.) no início.

Outros comandos para visualizar as permissões:

**ls -l** : Exibe permissões de arquivos e diretórios. Também exibe outras informações adicionais, incluindo o nome do proprietário, o grupo, o tamanho do arquivo e a hora da última modificação.

**ls -la** : Exibe permissões de arquivos e diretórios, incluindo arquivos ocultos. Essa é uma combinação das outras duas opções.

## Realizar a mudança de permissões

Ao realizar qualquer mudança significativa deve-se observar o princípio de **privilégio mínimo**, ou seja, conceder acesso apenas o acesso e autorizações mínimas para executar determinada tarefa.

Usamos o comando **chmod** para alterar as permissões de **rwx** 

Existem duas formas de realizar a mudança:
Utilizar "**+**" e o "**-**" (atribuição indereta) 
ou utilizar "**=**" (atribuição direta/exata)

1°: para exemplo **arquivo.txt** podemos usar **chmod u+rw, g-wx arquivo.txt**

Neste exemplo acima estamos concedendo as seguintes permissões: Para o (usuário(u)) adicionamos a leitura e escrita do arquivo. Para o (grupo(g)) removemos a escrita execução.




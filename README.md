# Comandos Para Uso Básico do Linux via Command Line

Os comandos abaixo são recomendáveis para a manipulação básica de arquivos e repositórios. Este guia foi elaborado com base no Linux Mint, uma distribuição Linux orientada pela comunidade e baseada no Ubuntu (que, por sua vez, é baseado no Debian). O Linux Mint é fornecido com uma variedade de aplicativos gratuitos e de código aberto.

### mkdir
  - Criar diretório (pasta)
  
### rmdir 
  - Remover diretório (pasta)
  
### touch
  - Criar arquivo (especificar o tipo, exemplo: .txt)
  
### rm 
  - Remover arquivo
  
### grep 
  - Filtrar algo dentro do arquivo (geralmente strings)
  - Exemplo de uso: `grep "OS" logs.txt`
  - Não ser case sensitive: `grep -i "OS" logs.txt`
  
### mv 
  - Mover um arquivo de um local para outro
  - Exemplo: `mv arquivo.txt pastamover` (move o arquivo.txt para a pastamover, se no mesmo diretório)

# Gestão Básica de Permissões Linux via Command Line

No Linux, as permissões são mostradas como uma string de sequência de 10 dígitos "**drwxrwxrwx**"

Onde:
**d** = refere-se às permissões de um diretório. Se for **-**, refere-se a um arquivo

**r** = refere-se à permissão de leitura (read)

**w** = refere-se à permissão de escrita (write)

**x** = refere-se à permissão de execução (execute)

Primeira sequência de 3 dígitos: **rwx** refere-se às permissões do usuário (u)

Segunda sequência de 3 dígitos: **rwx** refere-se às permissões do grupo (g)

Terceira sequência de 3 dígitos: **rwx** refere-se às permissões de outros (o)

## Explorando as Permissões Existentes

Durante a mudança das permissões de acesso, leitura e execução, é importante visualizar quais permissões já estão habilitadas ou desabilitadas.

Algumas pastas e arquivos no Linux se mantêm ocultos por regra para evitar acessos acidentais. Você pode mostrar os arquivos ocultos utilizando o comando:

- **ls -a**: Exibe arquivos ocultos. Os arquivos ocultos começam com um ponto (.) no início.

Outros comandos para visualizar as permissões:

- **ls -l**: Exibe permissões de arquivos e diretórios. Também exibe outras informações adicionais, incluindo o nome do proprietário, o grupo, o tamanho do arquivo e a hora da última modificação.

- **ls -la**: Exibe permissões de arquivos e diretórios, incluindo arquivos ocultos. Essa é uma combinação das outras duas opções.

## Realizar a Mudança de Permissões

Ao realizar qualquer mudança significativa, deve-se observar o princípio de **privilégio mínimo**, ou seja, conceder apenas o acesso e as autorizações mínimas necessárias para executar determinada tarefa.

Usamos o comando **chmod** para alterar as permissões de **rwx**.

Existem duas formas de realizar a mudança:
1. Utilizar "**+**" e "**-**" (atribuição indireta)
2. Utilizar "**=**" (atribuição direta/exata)

1. Para o exemplo **arquivo.txt**, podemos usar:
   - `chmod u+rw,g-wx arquivo.txt`

Neste exemplo, estamos concedendo as seguintes permissões: Para o usuário (u), adicionamos a leitura e escrita do arquivo. Para o grupo (g), removemos a escrita e execução.

Se você quiser retirar todas as permissões, pode usar:

- `chmod u-rwx,g-rwx,o-rwx arquivo.txt`

Outra maneira de atribuir essas permissões é usar o sinal de igual (=) no primeiro argumento:

- `chmod u=r,g=rw,o=- arquivo.txt`

**Observação:** Quando houver alterações de permissão para mais de um tipo de proprietário, serão necessárias vírgulas para separar as alterações para cada tipo de proprietário. Não deve haver espaços após essas vírgulas.
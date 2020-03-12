# Criando Repositórios no Redmine
Por repositório entende-se “um espaço que é usado para armazenar/guardar/arquivar coisas diferentes.Atualmente costuma-se fazer referência às bases de dados digitais e a diversos sistemas informáticos como repositórios.”

Este tutorial irá mostrar como criar um repositório Git no Redmine. Lembre-se que você poderá armazenar **imagens, documentos, planilhas, códigos ou outros tipos de arquivos** neste repositório.

1) Depois de logado no redmine, Clique em 'Configurações' -> 'Repositórios' -> 'Novo repositório'

2) No terminal, execute o seguinte comando para acessar o contêiner através do docker 

```
$ sudo docker container exec -it nome-do-seu-contêiner bash
```
Caso não saiba o nome do seu contêiner, utilize o comando abaixo. O nome estará na coluna **REPOSITORY**

```
$ sudo docker images
```

Lembre-se que um contêiner é como se fosse uma 'mini máquina virtual'. Se quiser, você pode verificar os arquivos existentes no contêiner digitando '-ls'

3) Agora que você está acessando o contêiner, você poderá utilizar comandos do Git normalmente. Você pode, por exemplo, criar um novo repositório utilizando 'git init' ou clonar um já existente com o 'git clone'. Exemplo:

```
git clone https://github.com/LucasIFNMG/redmine
```
Verifique se foi criada a nova pasta utilizando o '-ls' .

4) Dentro do repositório, utilize o comando abaixo para verificar o diretório dele.

```
pwd
```
*Dica: você pode acessar pastas pelo terminal através do comando cd nome-da-pasta . Experimente digitar cd + primeiras letras da pasta + TAB*

5) Agora você tem tudo em mãos! Volte no redmine e, na aba de criação de um Novo Repositório, preencha os dados.

**IMPORTANTE: no 'Caminho para o repositório', adicione /.git no final do diretório.** No meu caso:

```
/usr/src/redmine/repositorio/.git
```
6) Finalize a criação do repositório. Perceba que será exibido uma lista dos seus repositórios, na qual você poderá editar/excluir qualquer um deles. Lembre-se que você pode ter vários repositórios no redmine. Para acessá-los, vá na aba 'Repositório'.


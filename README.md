# Melhorando documentação dos conhecimentos no Git

O objetivo aqui é criar um indice evolutivo das documentações dos conceitos estudados

Antes, deixa eu registrar os comandos de inicialização que as vezes eu esqueço por usar pouco

```
echo "# gitComTags" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/msilva1610/gitComTags.git
git push -u origin main
```

Para criar os links sitados no bloco capitulo, não é necessário:
* Branches
* Tags

Apenas precisa executar o comit do código, com um bom comentário, obviamente. Depois digitar `git log` para pegar o id do commit.

Exemplo:

```git
PS E:\Arquivos\Vagrant\git> git log
commit 764e66e9adca0ed3f7c8bf73d333780fcaa2ea5b (HEAD -> main, origin/main)
Author: msilva1610 <msilva1610@gmail.com>
Date:   Tue Jan 5 23:10:23 2021 -0300

    Acertando o link

commit 413df72bae8f0ee22eb3accc6a530fe6cb7a05fc
Author: msilva1610 <msilva1610@gmail.com>
Date:   Tue Jan 5 23:08:34 2021 -0300

    Criando o primeiro link

commit 03e44c97b9439e4b35bef9810ca1da89829cbb85
Author: msilva1610 <msilva1610@gmail.com>
Date:   Tue Jan 5 22:51:08 2021 -0300

    01 - inicio

commit 0647754fa5401cab77333939273bc143db3da4f8
Author: msilva1610 <msilva1610@gmail.com>
Date:   Tue Jan 5 22:47:17 2021 -0300

    01 - inicio
```

Perceba que cada commit tem um ID, exemplo: 0647754fa5401cab77333939273bc143db3da4f8

Utilizar esse ID com as meta tags abaixo:

```
[Titulo do link](../../tree/0647754fa5401cab77333939273bc143db3da4f8)
```

A sintaxe acima permitirá que um link  para o commit local. O ID também servirá para recuperar um código nesse mesmo ponto na linha do tempo.

Entre um link e outro é necessário criar uma linha em branco. Casso contrário o link ficará na mesma linha.

Uma outra forma curiosa é colocr um link para uma imagem. Exemplo:

```
![Try Django 1.11 Logo](https://cfe2-static.s3-us-west-2.amazonaws.com/media/projects/try-django-111/images/share/try_django_1_11_share.png)
```

O ponto de exclamção no inicio informa que aparecerá apenas a imagem e o texto do link será omitido.


## Recuperar parte do trabalho a partir de um commit

Para issso execute é necessário identiifcar o id do commit e depois usar o comando:
```
git checkout 0647754fa5401cab77333939273bc143db3da4f8
```

Fazer isso em um outro diretório para um teste de temporário ou para desfazer um ponto do trabalho.

Vide links:

* https://pt.stackoverflow.com/questions/45077/como-recuperar-o-commit-anterior

## Cápitulos

[01 - Criando o primeiro link](../../tree/0647754fa5401cab77333939273bc143db3da4f8) 

[02 - Usando link](../../tree/764e66e9adca0ed3f7c8bf73d333780fcaa2ea5b) 

[03 - Usando link corretamente](../../tree/6a1a1a2dbf03a1be7c32059579e9998ad3de41fb) 

[04 - Notas finais](../../tree/44abec7449eb126cf4ed3fed156a0acd0af833db) 


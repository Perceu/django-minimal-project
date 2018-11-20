# Django minimal Project

Nesse repositorio tem um modelo de template minimo para o django,
Mostrando que e possivel mudar a arquitetura base do startproject do django para 
modelo diferenciado, ja com uma nova arquitetura de arquivos/pastas


usando o comando :
```shell
django-admin startproject [nome do projeto] --template=django-minimal
```

> O template do django direciona a uma pasta, então por exemplo, se tu clonar esse repositorio e quiser usar uma dentro de um outra pasta basta direcionar para a pasta django-minimal

#### Exemplo

```shell
django-admin startproject site_do_batata --template=../django-minimal-project/django-minimal
```

#### para rodar o projeto minimo 

```shell
python site_do_batata/site_do_batata.py runserver
```

> Basta acessar o 127.0.0.1:8000


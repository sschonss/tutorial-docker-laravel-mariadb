# Docker & Laravel
## _Laravel + MariaDB_
---

# Introdução :page_facing_up:


Esse tutorial vai ajudar você a criar um projeto Laravel usando Docker.

Meu objetivo é ajudar você a criar um projeto Laravel com Docker da maneira mais fácil.

Eu decidi escrever esse tutorial porque eu tinha algumas dificuldades em criar um projeto Laravel com Docker e eu quero ajudar você contornar essas dificuldades.

Seguindo a documentação é um bom caminho para aprender, mas as vezes você precisa ler um tutorial para entender melhor.

No entanto, eu aprendi muito escrevendo esse tutorial, então é uma via de mão dupla.

Se você tem alguma pergunta, pode entrar em contato comigo pelo [LinkedIn](https://www.linkedin.com/in/luiz-schons/) ou [GitHub](https://github.com/sschonss).

---
# Instalação :whale:

## Docker
- [Docker](https://docs.docker.com/get-docker/)

Para Windows, você precisa instalar [WSL2](https://docs.microsoft.com/en-us/windows/wsl/install-win10) e [Docker Desktop](https://docs.docker.com/docker-for-windows/install/)

## Docker Compose
- [Docker Compose](https://docs.docker.com/compose/install/)
---

# Usando os recursos :rocket:

## Clone o docker-compose.yml
```sh
mkdir ~/myapp && cd ~/myapp
curl -LO https://raw.githubusercontent.com/bitnami/containers/main/bitnami/laravel/docker-compose.yml
```

## Atenção :warning:

Você precisa alterar as variáveis de ambiente no arquivo docker-compose.yml para os seus próprios valores.

As vezes, você precisa alterar as portas no arquivo docker-compose.yml para evitar conflitos com outros serviços.

Talvez você precise abrir o seu projeto `~/myapp` no seu IDE ou editor de texto para editar o seu arquivo .env.

Lembre-se de alterar a variável DB_HOST no seu arquivo .env para o nome do serviço definido no arquivo docker-compose.yml.

Podem ser necessárias alterações nas permissões do diretório `~/myapp`, porque o container vai criar arquivos nesse diretório e talvez você não consiga editar esses arquivos.


## Iniciar os serviços :muscle:
```sh
docker-compose up
```

Uma dica: Você pode usar a flag -d para executar os containers em segundo plano:
```sh
docker-compose up -d
```

Eu recomendo que você não use a flag -d quando você iniciar os containers pela primeira vez, porque você pode ver os logs dos containers e verificar se tudo está funcionando corretamente.

## Parando os serviços :stop_sign:
```sh
docker-compose down
```

## Dicas :bulb:

### Verificar o status dos containers
```sh
docker-compose ps
```

### Verificar os logs dos containers
```sh
```sh
docker-compose logs
```

### Verificar os logs de um container específico
```sh
docker-compose logs <container-name>
```

### Verificar os logs de um container específico em tempo real
```sh
docker-compose logs -f <container-name>
```

## Acessar a aplicação :computer:

No seu terminal, você pode ver a URL da sua aplicação.

Normalmente, a URL é http://localhost:8000 se você não alterar as portas no arquivo docker-compose.yml.


## Acessar o banco de dados :floppy_disk:

Eu recomendo que você use o [DBeaver](https://dbeaver.io/) ou [DataGrip](https://www.jetbrains.com/datagrip/) para acessar o banco de dados.

Você pode usar as credenciais definidas no arquivo docker-compose.yml.

## Acessar o container :package:

Você pode acessar o container usando o seguinte comando:
```sh
docker-compose exec <container-name> bash
```

Se você usa Windows, você pode abrir o Docker Desktop e clicar no nome do container para abrir um terminal.

## Considerações finais :memo:

Eu recomendo que você leia a documentação do [Bitnami Laravel](https://hub.docker.com/r/bitnami/laravel/) para aprender mais sobre essa imagem.

Você pode usar essa imagem [Bitnami Laravel](https://hub.docker.com/r/bitnami/laravel/) em produção, mas você precisa alterar as variáveis de ambiente no arquivo docker-compose.yml para os seus próprios valores.

Eu escrevi esse tutorial para ajudar você, mas eu não sei tudo sobre Docker e Laravel, eu também estou aprendendo.

Eu espero que esse tutorial ajude você. :smile:

[LinkedIn](https://www.linkedin.com/in/luiz-schons/)
[GitHub](https://github.com/sschonss)

---

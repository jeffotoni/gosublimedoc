#Sublime para Go

Vamos configurar o Sublime para reconhecer a linguagem de programação Go.

Vou descrever os plugins e o que configurei para o Sublime reconhecer Go e vou deixar meus arquivos e configuração meu config do sublime-text para que possa copia-lo e usa-lo caso desejar e não irá precisar e ter todo trabalho de configura-lo.

Como eu gosto de escovar bits as vezes vou deixar a documentação como instalei e configurei o sublime pkg por pgk.

Já irá esclarecer muitas coisas para configurar o Sublime para reconhecer a linguagem Go.

### Instalando Sublime em linux 

<h1 align="center">
  <br />
  <img src="https://github.com/jeffotoni/gosublimedoc/blob/master/sublime-go.jpg" alt="logo" width="700" />
  <br />
  <br />
  <br />
</h1>

Para instalarmos o sublime em linux basta seguir os passos abaixo:


Instalando as dependências necessárias para adicionar um novo repositório HTTPS:
```bash

sudo apt update
sudo apt install dirmngr gnupg apt-transport-https ca-certificates software-properties-common

```

Importando o repositorio GPG key da api sublime sublime:
```bash

curl -fsSL https://download.sublimetext.com/sublimehq-pub.gpg | sudo apt-key add -
sudo add-apt-repository "deb https://download.sublimetext.com/ apt/stable/"

```

Instalar o Sublime Text 3:
```bash

sudo apt install sublime-text

```


### Copiando config do sublime para você usa-lo em sua máquia

Estou disponibilizando meu config do sublime para que possa copiar e colar e utiliza-lo sem ter que instalar e configurar tudo novamente, irá pegar tudo prontinho para usar.

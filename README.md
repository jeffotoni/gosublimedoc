#Sublime para Go

Vamos configurar o Sublime para reconhecer a linguagem de programação Go.

Vou descrever os plugins e o que configurei para o Sublime reconhecer Go e vou deixar meus arquivos e configuração meu config do sublime-text para que possa copia-lo e usa-lo caso desejar e não irá precisar e ter todo trabalho de configura-lo.

Como eu gosto de escovar bits as vezes vou deixar a documentação como instalei e configurei o sublime pkg por pgk.

Já irá esclarecer muitas coisas para configurar o Sublime para reconhecer a linguagem Go.


Antes de iniciarmos no univeso do Sublime, vamos instalar e configurar a famigerada linguagem Go.

## Instalando Go no Linux

<h1 align="center">
  <br />
  <img src="https://github.com/jeffotoni/gosublimedoc/blob/master/install_go.png" alt="logo" width="700" />
  <br />
  <br />
  <br />
</h1>

Install Go neste link terá o passo a passo de como instalar em diversos Sistemas Operacionais mas vou deixar aqui a instalação no Linux.

Se você tiver uma versão anterior do Go instalada, certifique-se de removê-la antes de instalar, vamos baixar a versão go1.15.6 mas pode entrar no site e pegar a última versão se preferir.

#### Confira o passo a passo 

1. Remova o Go caso esteja instalado

```bash

$ sudo rm -rf /usr/local/go

```
1. Baixe o arquivo [clicando aqui](https://golang.org/dl/go1.15.6.linux-386.tar.gz) 

2. Extraia-o em **/usr/local** com o seguinte comando

```bash

$ sudo tar -C /usr/local -xzf go1.15.6.linux-386.tar.gz

```

3. Adicione **/usr/local/go/bin** à PATH variável de ambiente.

```bash

$ export PATH=$PATH:/usr/local/go/bin

```

4. Para deixar o que fizemos acima global, ou seja toda vez que for entrar em seu terminal "go" seja executado você pode fazer isso adicionando a seguinte linha que mostrei acima ao seu $HOME/.profile ou /etc/profile (para uma instalação em todo o sistema) ou em seu **bash** ou o que estiver usando em seu ambiente Linux, no meu caso configuro o .zshrc, copie e cole os seus exports para dentro do seu arquivo:

```bash
$ echo "
\nexport GOPATH=$HOME/projeto/golang
\nexport PATH=$PATH:/usr/local/go/bin
\nexport PATH=$PATH:$GOPATH/bin
" >> ~/.bashrc

$ source ~/.bashrc

```

O arquivo acima colocamos o $GOPATH para facilitar as configurações quando formos usar o Sublime.


5. Agora vamos testar se tudo deu certo 

```bash

$ go version

```

Saída:
```bash

go version go1.15.6 linux/386

```

#### Hello World

Crie o arquivo main.go e edite o código abaixo:
```go

package main

func main() {
  
  println("Meu primeiro Hello World")

}

```

Vamos executar nosso programa:
```bash

$ go run main.go

```

Saída:
```bash

Meu primeiro Hello World

```

### Instalando Sublime em linux 

<h1 align="center">
  <br />
  <img src="https://github.com/jeffotoni/gosublimedoc/blob/master/sublime-go.jpg" alt="logo" width="700" />
  <br />
  <br />
  <br />
</h1>

Agora que temos nosso Go insalado e configurado vamos instalar o famigerado sublime em linux.


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


##### Baixar config Sublime

No link abaixo irá fazer download para sua máquna

[sublime-text-3.tar.bz2](https://jeffotoni.sfo2.digitaloceanspaces.com/sublime-text-3.tar.bz2)

Quando baixar só descompactar e copiar para dentro do seu .config no seu $HOME

```bash

$ tar xvjf sublime-text-3.tar.bz2
$ cp -r sublime-text-3 ~/.config

```

Quando trabalhamos com Go nas versões novas não precisamos mais do $GOPATH, mas para os editores vamos manter só para flexibilizar um pouco mais todo nosso trabalho.

Agora vamos configurar seu arquivo de configuração para que o Sublime consiga reconhecer seu $GOPATH e funcionar certinho.

Vamos criar um arquivo oculto em seu $HOME chamado .zprofile

```bash

$ touch ~/.zprofile

```
Agora cole ou copie para dentro do seu arquivo .zprofile suas configurações Go.

Exemplo:
```bash

export GOPATH=$HOME/projeto/golang
export PATH=$PATH:/usr/local/go/bin
export PATH=$PATH:$GOPATH/bin

```

Este é um exemplo, onde nosso $GOPATH está dentro de **"projeto/golang"** mas você pode definir o que achar melhor.

Agora é abrir o sublime e abrir seus projetos para ver como ficou..






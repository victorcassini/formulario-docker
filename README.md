# Formulário HTML com Docker

Este é um projeto simples contendo uma página HTML com um formulário visual, ideal para fins acadêmicos e para quem está aprendendo sobre Docker. O projeto utiliza a ferramenta `http-server` para servir os arquivos estáticos da aplicação dentro de um container Docker.

## ✨ O que o projeto faz?

Exibe uma página web com um formulário de contato contendo os seguintes campos:

- Nome  
- E-mail  
- Mensagem  

⚠️ *Este formulário é apenas visual. Os dados digitados não são enviados para nenhum servidor.*

---

## 🐳 Docker: como funciona aqui?

O container é configurado com base na imagem `node:18-alpine`, que é leve e adequada para rodar pequenos servidores. Dentro dele, utilizamos o `http-server` (instalado via npm) para servir os arquivos HTML.

---

## 🛠 Como rodar

Siga os passos abaixo para executar a aplicação localmente usando Docker:

### 1. Clonar o repositório

```bash
git clone https://github.com/SeuUsuario/formulario-docker.git
cd formulario-docker
```

### 2. Construir a imagem Docker

Este comando irá ler o `Dockerfile`, instalar as dependências e gerar uma imagem chamada `formulario-docker`.

```bash
docker build -t formulario-docker .
```

### 3. Subir a aplicação

Aqui estamos dizendo ao Docker para rodar a imagem criada e expor a porta `8080` do container para a máquina local:

```bash
docker run -p 8080:8080 formulario-docker
```

### 4. Acessar no navegador

Depois que o container estiver rodando, abra seu navegador e vá para:

[http://localhost:8080](http://localhost:8080)

Você verá a página com o formulário carregada e pronta para uso.

---

## 📁 Estrutura do Projeto

```
formulario-docker/
├── index.html        # Página HTML com o formulário
├── Dockerfile        # Instruções para criar a imagem Docker
├── package.json      # Arquivo opcional para descrever o projeto
├── style.css         # Arquivo opcional para estilização
└── README.md         # Este arquivo de instruções
```

---

## ✅ Requisitos

- Docker instalado e funcionando  
- Acesso ao terminal (Linux, macOS ou Windows com WSL/PowerShell)

---

criado por: Victor Alexandre Ferraz Cassini
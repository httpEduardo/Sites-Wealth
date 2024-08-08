# Guia Rápido: Como Configurar e Enviar um Repositório para o GitHub

## 1. Inicializar o Repositório Localmente

1. Navegue até o diretório no seu sistema onde você deseja criar o projeto.
2. Inicialize o repositório Git com o comando:

    ```bash
    git init
    ```

## 2. Vincular o Repositório Local ao Repositório Remoto

Para vincular seu repositório local ao repositório remoto no GitHub:

1. **Criar um repositório no GitHub (se ainda não tiver):**
   - Acesse o [GitHub](https://github.com), faça login e crie um novo repositório.
   - Copie o URL do repositório, que será algo como `https://github.com/usuario/repositorio.git`.

2. **Adicionar o repositório remoto ao Git:**

    No terminal, execute o seguinte comando, substituindo a URL com a do seu repositório:

    ```bash
    git remote add origin https://github.com/usuario/repositorio.git
    ```

   Isso configura o vínculo entre seu repositório local e o repositório remoto no GitHub.

## 3. Preparar os Arquivos para o Commit

Agora, adicione os arquivos que deseja commitar:

- **Adicionar arquivos específicos:**

    ```bash
    git add nome_do_arquivo.extensao
    ```

- **Adicionar todos os arquivos modificados:**

    ```bash
    git add .
    ```

## 4. Fazer o Commit

Depois de adicionar os arquivos ao stage, faça o commit com uma mensagem descritiva:

```bash
git commit -m "Descrição do que foi alterado"
 ```
## 5. Enviar o Commit para o Repositório Remoto

Para enviar o commit ao repositório remoto no GitHub, use o comando:

```bash
git push -u origin master
 ```

Exercício: Criação de um Repositório Local e Push para GitHub

Este exercício tem como objetivo praticar a criação de um repositório local, edição de arquivos, controle de versão com Git e envio do projeto para um repositório remoto no GitHub via SSH.

Passos do Exercício

1. Criar um Repositório Local e o Arquivo index.html
mkdir Exercicio_Git
cd Exercicio_Git
touch index.html

Edite o index.html conforme desejado.

2. Configuração Global do Git e Inicialização do Repositório
git config --global user.name "Seu Nome"
git config --global user.email "seuemail@example.com"
git init

3. Adicionar Arquivo ao Commit
git add index.html
git commit -m "Adiciona arquivo index.html"

4. Criar o Repositório no GitHub e Configurar o Remote

No GitHub, crie um novo repositório e copie a URL SSH.

Adicione o repositório remoto:
git remote add origin git@github.com:SeuUsuario/SeuRepositorio.git
git branch -M main
git push -u origin main

5. Configurar a Autenticação SSH e Fazer Push

Se ainda não configurou sua chave SSH, crie uma e adicione ao GitHub
ssh-keygen -t rsa -b 4096 -C "seuemail@example.com"
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_rsa
cat ~/.ssh/id_rsa.pub # Copie e adicione no GitHub

Teste a conexão:
ssh -T git@github.com

Se a conexão estiver correta, faça o push:
git push origin main

Agora seu repositório está no GitHub! 🚀

6. Criação do Ficheiro README.md do Exercício e Fazer um Push no GitHub

Crie o arquivo README.md e adicione ao repositório:
nano README.md
git add README.md
git commit -m "Adiciona README.md"
git push origin main

Agora seu repositório está no GitHub! 🚀

# Sobre

Tenho um caderno com os principais comandos anotados que consulto no dia a dia. Depois de uma conversa muito interessante com uma pessoa experiente, fui apresentada ao ciclo do **Learn Public**, onde *Todo ensino precisa ser: aprendido, adquirido e compartilhado*. Então resolvi transferir minhas anotações para esse arquivo e torná-lo público. 

ps: estou partindo do princípio que vc já conhece/usa o Git. Caso seja iniciante, recomendo que leia esse [artigo](https://rogerdudler.github.io/git-guide/index.pt_BR.html)


## Subindo mudanças pro Git
1. `git commit -m "sua_mensagem"`: envia as mudanças nos arquivos do repositório local para o remoto
2. `git add *`: envia os arquivos alterados
3. `git pull origin <sua_branch>`: pega todas as alterações da <sua_branch> remota e mescla localmente
4. `git pull`: baixa o conteúdo remoto e atualiza localmente, deixando os conteúdos iguais
5. `git push`: sobe os commits do repo local para o remoto

## Trabalhando com Branches
1. `git branch <nome_da_branch>`: cria uma branch 
2. `git branch`: lista todas as branches disponíveis localmente e marca a que vc está trabalhando
3. `git checkout <nome_da_branch`: muda da branch atual para <nome_da_branch>
4. `git checkout -b <nome_da_branch`: cria uma branch e já muda pra ela
5. `git reset --hard origin/<nome_da_branch>`: reseta a branch para a versão remota
6. `git fetch <remote>`: baixa todas as branches do repositório remoto 
7. `git fetch <remote> <nome_da_branch>`: baixa a branch especificada
8. `git branch -D <nome_da_branch>`: deleta uma branch

## Fazendo deploy/subindo pra produção
1. `git pull origin <sua_branch>`: pega todas as alterações da <sua_branch> remota e mescla localmente
2. `git push`: sobe os commits do repo local para o remoto
3. `git fetch origin <sua_branch_trabalhada>`: atualiza a branch de acordo com a origin
4. `git pull origin master-staging`: envia os códigos para a branch master-staging (onde se encontra o código em produção)
5. `git merge master-staging`: une todas as alterações na master-sataging
6. `git tag -a 2.3.4.5 -m "identificação do que a tag faz" <noma_da_branch>`: sempre que for incluído novas funcionalidades no seu software, é lançada uma nova versão/release do seu produto. Assim sendo, é necessário subir uma tag. A tag serve para "marcar" esse ponto importante. Note que nesse exemplo, "subimos" a versão 2.3.4.5 com a breve identificação dessa versão. 
7. `git tag`: lista as tags existentes
8. Acessa a sua plataforma de deploy e aperta o botão mágico **Promote to Production** ou similar e voilà 





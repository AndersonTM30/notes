# Principais Comandos para Git Flow

## Inicialização do Repositório e Criação de Branches Principais
Inicializar o repositório Git:
```bash 
git init
```
Adicionando o readme:
```bash 
git add README.md
```
Criando o commit inicial:
```bash 
git commit -m "initial commit"
```
Alterando a branch master para a main:
```bash 
git branch -M main
```
Adicionando o projeto no Github:
```bash 
git remote add origin https://github.com/user/project.git
```
Subindo a primeira alteração para o Github:
```bash 
git push -u origin main
```
Criar a branch develop a partir da main:
```bash 
git checkout -b develop
git push -u origin develop
```
## Desenvolvimento de Funcionalidades
Criar uma branch feature a partir da develop:
```bash 
git checkout -b feature/nova-funcionalidade develop
```
Trabalhar na feature e fazer commits:
```bash 
git add .
git commit -m "feat: descrição da nova funcionalidade"
```
Fazer merge da branch feature na develop após conclusão:
```bash 
git checkout develop
git merge feature/nova-funcionalidade
git branch -d feature/nova-funcionalidade
git push origin develop
```
## Preparação para Release
Criar uma branch release a partir da develop:
```bash 
git checkout -b release/v1.0 develop
```
Trabalhar em correções e ajustes finais na release branch:
```bash 
git add .
git commit -m "fix: correções finais para release v1.0"
```
Fazer merge da branch release na main e develop, e criar uma tag:
```bash 
git checkout main
git merge release/v1.0
git tag -a v1.0 -m "Release v1.0"
git push origin main --tags

git checkout develop
git merge release/v1.0
git push origin develop
```
Deletar a branch release:
```bash 
git branch -d release/v1.0
```
## Correções Rápidas em Produção (Hotfix)
Criar uma branch hotfix a partir da main:
```bash 
git checkout -b hotfix/corrige-bug main
```
Realizar correções na branch hotfix e fazer commits:
```bash 
git add .
git commit -m "fix: correção de bug crítico em produção"
```
Fazer merge da branch hotfix na main e develop, e criar uma tag:
```bash 
git checkout main
git merge hotfix/corrige-bug
git tag -a v1.0.1 -m "Hotfix v1.0.1"
git push origin main --tags

git checkout develop
git merge hotfix/corrige-bug
git push origin develop
```
Deletar a branch hotfix:
```bash 
git branch -d hotfix/corrige-bug
```


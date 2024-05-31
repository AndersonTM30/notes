## Conventional Commits
O Conventional Commits é uma convenção para escrever mensagens de commit que cria um histórico explícito e bem documentado, que facilita a automação de versões, geração de changelogs e outros processos.  
## Principais Prefixos de Conventional Commits
- `feat`: Adição de uma nova funcionalidade.
- `fix`: Correção de um bug.
- `docs`: Mudanças na documentação.
- `style`: Mudanças que não afetam a lógica do código (espaços em branco, formatação, etc).
- `refactor`: Mudança no código que não corrige um bug nem adiciona uma funcionalidade.
- `perf`: Mudança que melhora a performance.
- `test`: Adição ou modificação de testes.
- `build`: Mudanças que afetam o sistema de build ou dependências externas (ferramentas de compilação, pacotes npm, etc).
- `ci`: Mudanças em arquivos e scripts de configuração de CI (continous integration).
- `chore`: Outras mudanças que não modificam o src ou arquivos de teste.
- `revert`: Reverter um commit anterior.
## Exemplos de Mensagens de Commit
Adicionar uma nova funcionalidade:
```bash
git commit -m "feat: adicionar funcionalidade de login"
```
Corrigir um bug:
```bash
git commit -m "fix: corrigir erro no botão de envio"
```
Atualizar a documentação:
```bash
git commit -m "docs: atualizar README com instruções de instalação"
```
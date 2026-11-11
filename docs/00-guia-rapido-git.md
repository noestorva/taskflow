# 🧭 Guia Rápido de Git e Fluxo de Trabalho

Este guia contém apenas os comandos essenciais que você usará durante toda a disciplina. **Nunca trabalhe diretamente na branch `main`.**

---

## 1️⃣ Configuração Inicial (Fazer apenas 1 vez no computador)

Abra o terminal e informe seu nome e o mesmo e-mail cadastrado no GitHub:

```bash
git config --global user.name "Seu Nome"
git config --global user.email "seu.email@exemplo.com"
```

---

## 2️⃣ Baixando o Projeto (Fazer apenas 1 vez)

Copie a URL do repositório da sua equipe no GitHub e execute:

```bash
git clone <cole-a-url-do-repositorio-aqui>
cd <nome-da-pasta-do-projeto>
```

---

## 3️⃣ O Ciclo Diário de Trabalho (Repetir a cada nova tarefa)

### Passo 1: Atualizar a `main` local
Antes de começar qualquer tarefa nova, garanta que você tem a versão mais recente do projeto:

```bash
git checkout main
git pull origin main
```

### Passo 2: Criar uma branch para a sua tarefa
Crie uma branch nova a partir da `main` usando o número da *Issue* que você pegou no quadro:

```bash
git checkout -b feature/issue-1-tela-login
```
*(Dica: use `feature/` para funcionalidades novas e `fix/` para correção de bugs).*

### Passo 3: Salvar seu progresso (Add e Commit)
Após escrever seu código, verifique o que foi alterado e salve um ponto na história do projeto:

```bash
# 1. Veja os arquivos modificados
git status

# 2. Adicione todos os arquivos modificados para o pacote de envio
git add .

# 3. Salve o pacote com uma mensagem clara do que foi feito
git commit -m "feat: cria estrutura html da tela de login"
```

### Passo 4: Enviar para o GitHub (Push)
Envie a sua branch para o repositório online:

```bash
git push -u origin feature/issue-1-tela-login
```
*(Nos próximos commits da mesma branch, basta digitar `git push`).*

---

## 4️⃣ Finalizando a Tarefa (No site do GitHub)

1. Acesse o repositório da equipe no GitHub.
2. Clique no botão verde **"Compare & pull request"** que aparecerá no topo.
3. No campo de descrição, escreva `Closes #1` (trocando o `1` pelo número da sua *Issue*).
4. Avise um colega da equipe para revisar o código.
5. Após a aprovação do colega, clique em **"Merge pull request"** e depois em **"Delete branch"**.
6. Volte para o **Passo 1** para pegar a próxima tarefa!

---

## 🆘 Comandos de Emergência

* **Esqueci em qual branch estou:**
  ```bash
  git branch
  ```
* **Alterei um arquivo e quero desfazer tudo (voltar ao último commit):**
  ```bash
  git checkout -- nome-do-arquivo.ext
  ```
* **Fiz alterações na `main` por engano antes de criar a branch:**
  ```bash
  git checkout -b feature/nome-da-nova-branch
  ```
  *(Isso move suas alterações para a branch nova e deixa a `main` limpa).*


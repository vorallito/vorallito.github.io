# Regras para publicar neste repositório (vorallito.github.io)

Mais de um agente publica aqui (Claude Code e ChatGPT/Codex). Siga estas regras para ninguém apagar o trabalho do outro.

## Antes de mexer

1. **Puxe as mudanças primeiro:** `git pull --rebase origin main`.
2. Se o pull reclamar de mudanças locais, faça commit do seu trabalho e rode o pull de novo. Nunca descarte o que não é seu.

## Enquanto trabalha

3. **Cada projeto na sua pasta.** Não apague, não renomeie e não sobrescreva pastas ou arquivos de outro projeto.
4. **Donos atuais:**

| Caminho | Projeto | Como é gerado |
|---|---|---|
| `index.html`, `en/`, `img/`, `capa.png`, `Farmacia_de_Skills_Vorallito.pdf`, `revisao-semanal.zip` | Farmácia de Skills (Claude Code) | `python3 build.py --site --en` na pasta `vorallito_handoff/`. Não edite à mão. |
| `chatgpt/` | Farmácia do ChatGPT | derivada da adaptação GPT-6; preserve como página própria |
| `chatgpt-gpt6/` | Guia GPT-6 (ChatGPT/Codex) | pelo próprio projeto |
| `AGENTS.md`, `CLAUDE.md`, `.nojekyll`, `.gitignore` | regras do repositório | à mão, com cuidado |

5. Projeto novo: crie uma pasta nova e acrescente uma linha na tabela acima no mesmo commit.

## Ao publicar

6. **Autor dos commits:** `Vorallito <334010285+vorallito@users.noreply.github.com>`. Nunca use nome ou e-mail reais: o Vorallito é um pseudônimo.
7. Antes do commit, confira que nenhum arquivo traz nome real, e-mail pessoal ou dados de clientes. O `.gitignore` bloqueia segredos, rascunhos, HANDOFF e exportações de assinantes; não use `git add -f` para contorná-lo. Rode `gitleaks git .` antes do push.
8. **Nunca sobrescreva o histórico remoto** (push forçado) nem reescreva o histórico de `main`.
9. Se o push for recusado, rode `git pull --rebase origin main` e tente de novo. Se houver conflito num arquivo de outro projeto, pare e pergunte ao operador.
10. Depois do push, confira que a sua página responde (HTTP 200) e que as páginas dos outros projetos continuam no ar.

# DEPLOY GITHUB PAGES - rotterdamsolutions.com
Domínio: rotterdamsolutions.com (DNS no Wix: ns14/ns15.wixdns.net)
E-mail destino: rotterdamsolutions@outlook.com
WhatsApp: (11) 93924-6289
LinkedIn: https://www.linkedin.com/company/rotterdam-solutions/about/?viewAsMember=true

## ✅ PACOTE JÁ PRONTO PARA GITHUB PAGES
Este pacote já contém:
- index.html (site v12 final com e-mail rotterdamsolutions@outlook.com)
- CNAME (com rotterdamsolutions.com)
- .nojekyll (para GitHub não processar como Jekyll)
- assets/ (logo oficial 100%)

## PASSO 1: Criar repositório no GitHub (2 min)
1. github.com → New repository
2. Nome: rotterdam-solutions-site (ou rotterdamsolutions.com)
3. Marque Private ou Public (recomendo Private no começo)
4. NÃO marque "Add README" (já temos)
5. Create repository

## PASSO 2: Push do código (2 min)
Descompacte o ZIP e no terminal dentro da pasta:

```bash
git init
git add .
git commit -m "Rotterdam Solutions v12 - GitHub Pages - Email Outlook + WhatsApp + LinkedIn"
git branch -M main
git remote add origin https://github.com/SEU_USUARIO/rotterdam-solutions-site.git
git push -u origin main
```
Substitua SEU_USUARIO pelo seu usuário do GitHub.

## PASSO 3: Ativar GitHub Pages (1 min)
1. No GitHub, vá no seu repo → Settings → Pages (no menu lateral)
2. Build and deployment:
   - Source: Deploy from a branch
   - Branch: main | / (root) | Save
3. Custom domain: digite rotterdamsolutions.com e clique Save
4. Marque "Enforce HTTPS" (após alguns minutos ficará disponível)
5. O GitHub vai criar um commit com CNAME automaticamente (já temos, mas ele confirma)

## PASSO 4: Configurar DNS no Wix (3 min) - SEU CASO ATUAL
Seu DNS atual no Wix:
- A: rotterdamsolutions.com → 185.230.63.171 / .186 / .107 (Wix)
- CNAME: www.rotterdamsolutions.com → cdn3.wixdns.net (Wix)
- NS: ns14.wixdns.net / ns15.wixdns.net

Vá em Wix → Domínios → rotterdamsolutions.com → Gerenciar registros DNS:

### REMOVER (Wix):
- Delete: A rotterdamsolutions.com → 185.230.63.171 (TTL 1h)
- Delete: A rotterdamsolutions.com → 185.230.63.186
- Delete: A rotterdamsolutions.com → 185.230.63.107
- Delete: CNAME www.rotterdamsolutions.com → cdn3.wixdns.net

### ADICIONAR (GitHub Pages - IPs oficiais):
Adicione 4 registros A (todos para o apex rotterdamsolutions.com):

1. Tipo: A | Host: rotterdamsolutions.com | Valor: 185.199.108.153 | TTL: 1 hora
2. Tipo: A | Host: rotterdamsolutions.com | Valor: 185.199.109.153 | TTL: 1 hora
3. Tipo: A | Host: rotterdamsolutions.com | Valor: 185.199.110.153 | TTL: 1 hora
4. Tipo: A | Host: rotterdamsolutions.com | Valor: 185.199.111.153 | TTL: 1 hora

Adicione 1 CNAME para www:

5. Tipo: CNAME | Host: www.rotterdamsolutions.com | Valor: SEU_USUARIO.github.io | TTL: 1 hora
   Substitua SEU_USUARIO pelo seu usuário GitHub
   Ex: se seu usuário é rotterdamsolutions, fica rotterdamsolutions.github.io

### NÃO MEXER EM:
- NS ns14.wixdns.net / ns15.wixdns.net
- MX / TXT (se tiver para e-mail)

## PASSO 5: Aguardar propagação (até 1h)
- GitHub Pages leva de 5 min a 1h para validar o domínio
- Em Settings → Pages vai aparecer "DNS check in progress" e depois "Active" com cadeado verde
- Teste: https://rotterdamsolutions.com e https://www.rotterdamsolutions.com
- Marque Enforce HTTPS quando liberar

## PASSO 6: Ativar formulário (primeira vez)
1. Acesse https://rotterdamsolutions.com
2. Preencha o formulário de contato com teste
3. Abra rotterdamsolutions@outlook.com
4. Você receberá e-mail do FormSubmit.co: "Confirm your email"
5. Clique em "Confirm" / "Activate"
6. Pronto! Todas as próximas solicitações chegam no Outlook com modal "Solicitação enviada com sucesso!"

## CHECKLIST FINAL
- [ ] Repo criado e push feito
- [ ] GitHub Pages ativado em Settings → Pages
- [ ] Custom domain rotterdamsolutions.com salvo
- [ ] DNS no Wix alterado (4 A + 1 CNAME)
- [ ] DNS check Active no GitHub
- [ ] https://rotterdamsolutions.com funcionando com SSL
- [ ] Logo 100% aparecendo nítido
- [ ] 3 dashboards portfólio carregando
- [ ] Formulário enviando para rotterdamsolutions@outlook.com
- [ ] Modal de confirmação aparecendo
- [ ] WhatsApp (11) 93924-6289 e LinkedIn funcionando
- [ ] Teste no celular

## DÚVIDAS COMUNS
- Se ainda mostrar site do Wix após 1h: limpe cache, teste no modo anônimo, ou aguarde TTL
- Se GitHub Pages mostrar "Not served": verifique se os 4 A records estão corretos
- Se formulário não chegar: verifique spam em rotterdamsolutions@outlook.com e se clicou no link de ativação do FormSubmit

## Suporte
- GitHub Pages Docs: https://docs.github.com/pt/pages/configuring-a-custom-domain-for-your-github-pages-site
- Wix DNS: https://support.wix.com/pt/article/dom%C3%ADnios-gerenciando-registros-dns

Tudo pronto para GitHub Pages!

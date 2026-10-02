# Fisio+ — Prontuários de Fisioterapia

PWA em HTML5/CSS3/JavaScript Vanilla, pensado para GitHub Pages e funcionamento offline.

## Segurança
Os dados clínicos são armazenados em IndexedDB como blobs criptografados com AES-GCM. A chave é derivada da senha por PBKDF2-SHA-256. A senha não é armazenada. O hash do e-mail é usado apenas para localizar a conta local.

Não existe recuperação de senha: perder a senha significa perder a capacidade de descriptografar os dados. GitHub Pages também não fornece sincronização entre dispositivos.

## EmailJS
O envio de boas-vindas está desativado por padrão. No `app.js`, preencha `CONFIG.emailjs` e inclua o SDK do EmailJS no `index.html` quando desejar ativá-lo. O envio exige internet no momento do cadastro; o prontuário continua offline.

## Backup
O JSON exportado contém os registros já criptografados. Para importar, selecione o arquivo e informe a senha original da conta. Guarde o backup em local seguro.

## Uso clínico
Antes de usar com pacientes reais, valide segurança, privacidade, LGPD, política institucional, retenção e backup. O sistema especialista é apenas referencial/educacional e não diagnostica nem prescreve.

## GitHub Pages
Publique estes arquivos na raiz do repositório e ative Settings → Pages → Deploy from a branch. O Service Worker exige HTTPS e funciona no GitHub Pages.

# HERYTA – Gestão Contabilística (PWA GitHub Pages)

Versão inicial para publicação no GitHub Pages e utilização em Android e computador.

## Funcionalidades desta fase
- PWA com manifesto e service worker.
- Interface responsiva.
- Base de dados local IndexedDB.
- Cadastro de várias empresas.
- Cadastro de vários utilizadores no mesmo navegador/perfil.
- Autenticação local com PBKDF2 e Web Crypto.
- Estrutura inicial reservada para contas e lançamentos.

## Publicar no GitHub Pages
1. Crie um repositório público, por exemplo `heryta-contabilidade`.
2. Carregue todos os ficheiros e pastas desta pasta para a raiz do repositório.
3. No GitHub, abra **Settings → Pages**.
4. Em **Build and deployment**, escolha **Deploy from a branch**.
5. Escolha a branch `main` e a pasta `/ (root)`, depois grave.
6. Aguarde a publicação e abra o endereço indicado pelo GitHub Pages.

Não renomeie `index.html`, `manifest.json` ou `service-worker.js`. Os caminhos relativos (`./`) permitem publicar também em repositório de projeto.

## Instalar
- Android: abra o endereço HTTPS publicado no Chrome. Use o menu do navegador e escolha **Instalar aplicação** ou **Adicionar ao ecrã principal**, conforme a opção apresentada.
- Computador: abra o endereço publicado num navegador compatível e utilize o ícone/opção de instalação quando disponível.

## Utilização offline
Abra a aplicação uma primeira vez com internet para carregar os ficheiros e registar o service worker. Depois, volte a abrir a aplicação instalada ou o mesmo endereço no mesmo navegador. O conteúdo da aplicação fica em cache; os registos ficam na IndexedDB do navegador.

## Limitações importantes
- GitHub Pages apenas hospeda ficheiros estáticos. Não é servidor de base de dados.
- Os dados ficam no armazenamento local do navegador, neste dispositivo e perfil. Não sincronizam entre Android e computador nem entre utilizadores/dispositivos.
- Limpar dados do navegador, desinstalar ou perder o dispositivo pode apagar os registos. Exportação/restauro de cópias de segurança será implementada antes de uso real.
- A versão PWA usa IndexedDB; não usa o SQLite nativo do pacote Android anterior.
- A gestão de permissões por empresa ainda é básica; nesta fundação os perfis existem, mas regras completas de acesso serão adicionadas.
- Não guardar dados contabilísticos reais até implementar backups, exportação/restauro, bloqueio de sessões e auditoria completa.
- O motor de partidas dobradas, Plano de Contas, Diário, Razão e demonstrações financeiras pertencem às fases seguintes.
- Para PWA, HTTPS é necessário; GitHub Pages fornece HTTPS.

## Primeiro acesso
Crie o administrador no ecrã inicial. Escolha uma palavra-passe forte. Não existe palavra-passe padrão no código.

## Testes recomendados
1. Criar administrador.
2. Sair e entrar novamente.
3. Registar duas empresas.
4. Criar utilizadores com perfis diferentes.
5. Fechar e reabrir o navegador.
6. Testar modo avião depois de a primeira visita online.

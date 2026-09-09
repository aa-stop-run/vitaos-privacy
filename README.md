# VitaOS — Política de Privacidade

Este repositório existe por uma razão só: alojar publicamente a política de
privacidade do **VitaOS**, porque a Google Play exige um URL público e
acessível sem autenticação, e o repositório da aplicação é privado.

**Publicado em:** https://aa-stop-run.github.io/vitaos-privacy/

O código-fonte do VitaOS **não** está aqui.

## Conteúdo

| Ficheiro | O que é |
|---|---|
| `index.html` | A política de privacidade. HTML autónomo — sem CSS externo, sem tipos de letra externos, sem scripts, sem pedidos de rede. |
| `.nojekyll` | Diz ao GitHub Pages para servir os ficheiros como estão, sem os processar com Jekyll. |

## Como manter sincronizado

A fonte da verdade é `PRIVACY_POLICY.md`, no repositório privado do VitaOS,
e `public/privacy.html` é a mesma política em HTML. Quando a política mudar
lá, copia-se o HTML para aqui como `index.html` e faz-se um commit.

Duas coisas a não esquecer quando isso acontecer:

1. **Atualizar a data** de *Última atualização* no topo.
2. **Reconferir a tabela de permissões contra o manifesto fundido** da AAB de
   release — não contra `android/app/src/main/AndroidManifest.xml`. As
   bibliotecas acrescentam permissões que não estão no manifesto de origem
   (`INTERNET` e `ACCESS_NETWORK_STATE` vêm da Google Play Billing, `VIBRATE`
   vem da biblioteca de notificações). É o manifesto fundido que a Google
   recebe, e é com ele que a política e o formulário de *Data safety* têm de
   bater certo.

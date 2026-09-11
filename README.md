# VitaOS — Privacy Policy / Política de Privacidade

Este repositório existe por uma razão só: alojar publicamente a política de
privacidade do **VitaOS**, porque a Google Play exige um URL público e
acessível sem autenticação, e o repositório da aplicação é privado.

**Publicado em:** https://aa-stop-run.github.io/vitaos-privacy/ — em inglês,
e em [português](https://aa-stop-run.github.io/vitaos-privacy/pt/),
[espanhol](https://aa-stop-run.github.io/vitaos-privacy/es/),
[alemão](https://aa-stop-run.github.io/vitaos-privacy/de/) e
[francês](https://aa-stop-run.github.io/vitaos-privacy/fr/).

O código-fonte do VitaOS **não** está aqui.

## Conteúdo

| Ficheiro | O que é |
|---|---|
| `index.html` | A política em inglês — o URL que vai para a Play Console. |
| `pt/`, `es/`, `de/`, `fr/` | A mesma política nas outras línguas da app. Cada página liga às outras quatro. |
| `.nojekyll` | Diz ao GitHub Pages para servir os ficheiros como estão, sem os processar com Jekyll. |

Páginas HTML autónomas: sem CSS externo, sem tipos de letra externos, sem
scripts, sem pedidos de rede.

## Como manter sincronizado

**Não editar estas páginas à mão.** A fonte é
`assets/privacy/politica_privacidade.json`, no repositório privado do VitaOS —
o mesmo texto que a app vai mostrar nas Definições. As páginas geram-se de lá:

```powershell
cd D:\Projetos_IA\vitaOS
flutter build appbundle --release
python scripts\generate_privacy_policy.py --copia D:\Projetos_IA\vitaos-privacy
```

e depois faz-se commit e push aqui.

O gerador recusa-se a escrever se as cinco línguas não tiverem a mesma
estrutura, ou se o manifesto fundido da AAB de release declarar permissões
diferentes das da tabela. Por isso se constrói a AAB primeiro: a tabela diz
"todas, sem exceção", e é o manifesto fundido — com as permissões que as
bibliotecas acrescentam — que a Google recebe. Não esquecer de mudar também a
data de atualização, nas cinco línguas.

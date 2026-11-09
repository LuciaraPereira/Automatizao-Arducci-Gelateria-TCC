# Arquitetura atual do protótipo

HTML, CSS e JavaScript estáticos, publicados no GitHub Pages. Navegação e armazenamento no navegador simulam o sistema; não há backend bancário, fiscal ou autenticação real.

```mermaid
flowchart LR
 U[Usuário: mobile, tablet ou desktop] --> B[Navegador]
 G[GitHub Pages: arquivos estáticos] --> B
 B --> T[Telas cliente, visitante e administrativo]
 T --> S[Estado e armazenamento local do navegador]
```

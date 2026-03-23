# JFynzo — Controle de Despesas 📱

App de controle financeiro pessoal com SQLite local, lançamentos recorrentes, tema claro/escuro e geração de relatório PDF.

## Como gerar o APK via GitHub

### 1. Suba o repositório no GitHub

```bash
git init
git add .
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/SEU_USUARIO/jfynzo.git
git push -u origin main
```

### 2. O GitHub Actions roda automaticamente

A cada push na branch `main`, o workflow `.github/workflows/build-apk.yml` executa e gera:

- **JFynzo-debug-apk** — APK de debug pronto para instalar
- **JFynzo-release-unsigned-apk** — APK de release sem assinatura

### 3. Baixar o APK

1. Vá em **Actions** no seu repositório
2. Clique no workflow mais recente
3. Role até **Artifacts**
4. Baixe o **JFynzo-debug-apk**

### Instalar no Android

1. No celular: **Configurações → Segurança → Fontes desconhecidas → Ativar**
2. Transfira o `.apk` para o celular
3. Abra o arquivo e instale

---

## Estrutura do projeto

```
jfynzo/
├── www/
│   └── index.html          ← App completo (HTML único)
├── android/                ← Gerado pelo Capacitor (não edite manualmente)
├── .github/
│   └── workflows/
│       └── build-apk.yml   ← Pipeline de build
├── capacitor.config.json   ← Configurações do Capacitor
├── package.json
└── .gitignore
```

## Desenvolvimento local

```bash
npm install
npx cap add android       # primeira vez
npx cap sync android      # após editar www/index.html
npx cap open android      # abre no Android Studio
```

---

Desenvolvido por **JFSistemas**

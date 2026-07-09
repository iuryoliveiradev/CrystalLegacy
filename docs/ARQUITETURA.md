# 🏛️ Arquitetura do Crystal Legacy

**Versão:** 0.1 Alpha

Este documento descreve a organização do projeto. Seu objetivo é facilitar a manutenção, o crescimento e a colaboração futura.

---

## Filosofia

Cada pasta deve possuir uma responsabilidade clara.

Organização é uma funcionalidade do projeto.

---

## Estrutura

```text
CrystalLegacy/
│
├── README.md
├── LICENSE
│
├── docs/
│   ├── CONSTITUICAO.md
│   ├── ROADMAP.md
│   ├── ARQUITETURA.md
│   ├── DESIGN.md
│   └── CHANGELOG.md
│
├── assets/
├── grub/
├── plymouth/
├── sddm/
├── kde/
├── wallpapers/
├── icons/
├── cursors/
├── sounds/
├── scripts/
├── packages/
├── installer/
└── src/
```

---

## Responsabilidade das Pastas

### docs/

Documentação oficial do projeto.

### assets/

Arquivos de apoio utilizados em documentação, protótipos e desenvolvimento.

### grub/

Tema e documentação relacionados ao GRUB.

Conteúdo previsto:

- `theme.txt`
- imagens
- fontes
- ícones
- documentação de instalação e rollback

### plymouth/

Tela de carregamento do sistema.

### sddm/

Tela de login.

### kde/

Configurações e personalizações do KDE Plasma.

### wallpapers/

Papéis de parede oficiais.

### icons/

Ícones próprios do Crystal Legacy.

### cursors/

Cursores personalizados.

### sounds/

Sons oficiais do sistema.

### scripts/

Scripts de automação.

### packages/

Arquivos relacionados a empacotamento e lista de pacotes.

### installer/

Arquivos relacionados ao futuro instalador do Crystal Legacy.

### src/

Código-fonte dos programas desenvolvidos pelo projeto.

---

## Convenções

- Documentação em Português (Brasil).
- Comentários de código preferencialmente em português no início do projeto.
- Nomes de pastas em letras minúsculas.
- Documentos principais em letras maiúsculas quando estiverem na raiz ou em `docs/`.
- Organização antes de implementação.

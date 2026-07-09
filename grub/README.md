# 🧭 GRUB — Crystal Legacy

**Versão:** 0.1 Alpha

Este documento registra o planejamento, os cuidados e a estrutura inicial do tema GRUB do Crystal Legacy.

---

## Objetivo

Personalizar o menu de boot do sistema com a identidade visual do Crystal Legacy, mantendo segurança, clareza e possibilidade de recuperação caso algo dê errado.

O GRUB será a primeira tela visual do Crystal Legacy após a UEFI.

---

## O que é o GRUB?

O **GRUB** é o carregador de boot usado para iniciar o sistema operacional.

Ele permite escolher entre:

- Crystal Legacy / Arch Linux
- Windows
- Opções avançadas do Linux
- Entradas de recuperação

---

## Fluxo

```text
UEFI
↓
GRUB
↓
Kernel Linux
↓
Sistema operacional
```

---

## Papel do GRUB no Crystal Legacy

O GRUB será responsável por apresentar o primeiro contato visual com o sistema.

Ele deverá transmitir:

- nostalgia;
- clareza;
- identidade;
- segurança;
- simplicidade.

O visual deve lembrar uma tela de seleção inspirada em RPG clássico, sem comprometer a legibilidade.

---

## Regras de Segurança

1. Nunca alterar o GRUB real sem backup.
2. Nunca remover entradas funcionais.
3. Sempre manter uma forma de acessar o Windows.
4. Sempre testar alterações com cuidado.
5. Sempre documentar o que foi alterado.
6. Visual bonito nunca deve prejudicar a leitura.
7. O tempo de escolha deve ser suficiente para o usuário decidir.

---

## Estrutura Planejada

```text
grub/
├── README.md
├── theme.txt
├── background.png
├── icons/
│   ├── crystal-linux.png
│   └── windows.png
└── fonts/
```

---

## Arquivos Principais

### theme.txt

Arquivo principal do tema.

Define:

- fundo;
- fontes;
- cores;
- posição do menu;
- estilo da seleção;
- espaçamentos;
- elementos visuais.

### background.png

Imagem de fundo do menu.

Deve ser:

- leve;
- legível;
- em boa resolução;
- sem elementos protegidos por direitos autorais.

### icons/

Pasta com ícones das entradas do menu.

### fonts/

Pasta para fontes usadas pelo GRUB.

---

## Caminhos Reais do Sistema

No Arch Linux, os arquivos reais do GRUB geralmente ficam em:

```text
/boot/grub/
```

Temas podem ficar em:

```text
/boot/grub/themes/
```

Configurações principais podem envolver:

```text
/etc/default/grub
/etc/grub.d/
```

A geração do arquivo final normalmente é feita com:

```bash
sudo grub-mkconfig -o /boot/grub/grub.cfg
```

---

## Atenção

O arquivo `grub.cfg` não deve ser editado manualmente.

Ele é gerado automaticamente a partir das configurações do sistema.

---

## Backup Planejado

Antes de qualquer alteração real, deverão ser feitos backups de:

```text
/etc/default/grub
/etc/grub.d/40_custom
/boot/grub/grub.cfg
```

---

## Ideia Visual Inicial

O tema do GRUB deverá ter:

- fundo em pixel art original;
- menu centralizado;
- opções claras;
- destaque visual para a opção selecionada;
- tempo de escolha visível;
- estética de aventura;
- leitura fácil mesmo em telas grandes.

---

## Entradas Esperadas

```text
Crystal Legacy
Windows
Opções avançadas
```

---

## Status

Este documento é apenas o planejamento inicial.

Nenhuma alteração real no GRUB deve ser feita antes da criação de backup e revisão dos caminhos atuais do sistema.

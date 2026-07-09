# ⚙️ Fluxo de Boot do Crystal Legacy

**Versão:** 0.1 Alpha

Este documento explica como o Crystal Legacy inicia, desde o momento em que o computador é ligado até a área de trabalho.

---

## Objetivo

Entender e documentar o processo de inicialização antes de modificar qualquer parte do sistema.

O Crystal Legacy deve personalizar o boot com segurança, mantendo sempre a possibilidade de voltar atrás caso algo dê errado.

---

## Fluxo Geral

```text
Power
↓
UEFI
↓
GRUB
↓
Kernel Linux
↓
initramfs
↓
systemd
↓
Plymouth
↓
SDDM
↓
KDE Plasma
↓
Crystal Legacy Desktop
```

---

## 1. Power

O processo começa quando o computador é ligado.

A placa-mãe inicializa os componentes básicos, como processador, memória, armazenamento e vídeo.

---

## 2. UEFI

A UEFI é o firmware da placa-mãe.

Ela procura um carregador de boot registrado, como:

- GRUB
- Windows Boot Manager

No Crystal Legacy, a UEFI deverá carregar o GRUB.

---

## 3. GRUB

O GRUB é o menu de inicialização.

Ele permite escolher entre:

- Crystal Legacy / Arch Linux
- Windows
- Opções avançadas

No futuro, o GRUB receberá o primeiro tema visual do Crystal Legacy.

---

## 4. Kernel Linux

Depois da escolha no GRUB, o kernel Linux é carregado.

O kernel é o núcleo do sistema operacional.

Ele conversa diretamente com o hardware.

---

## 5. initramfs

O initramfs prepara o ambiente inicial necessário para o sistema conseguir montar a partição principal.

Ele é uma etapa temporária antes do sistema real assumir.

---

## 6. systemd

O systemd inicia os serviços principais do sistema.

Ele carrega rede, áudio, login, serviços internos e outros componentes.

---

## 7. Plymouth

O Plymouth exibe a tela de carregamento visual.

No Crystal Legacy, ele será responsável pela animação de boot.

---

## 8. SDDM

O SDDM é a tela de login.

No futuro, receberá um tema próprio do Crystal Legacy.

---

## 9. KDE Plasma

Após o login, o KDE Plasma carrega a área de trabalho.

Essa será a base inicial do Crystal Legacy Desktop.

---

## Regras de Segurança

1. Nunca modificar arquivos reais do boot sem backup.
2. Nunca testar tema GRUB diretamente sem cópia de segurança.
3. Sempre documentar cada alteração.
4. Sempre manter uma entrada funcional de boot.
5. Sempre manter o Windows acessível pelo menu ou pela UEFI.

---

## Próxima etapa

O próximo documento será dedicado ao GRUB:

```text
grub/README.md
```

Nele serão documentados:

- onde o GRUB fica instalado;
- onde ficam seus temas;
- como fazer backup;
- como testar alterações;
- como recuperar o boot se algo der errado.

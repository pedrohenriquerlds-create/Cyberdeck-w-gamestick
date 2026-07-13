# DIY Cyberdeck

**Em andamento**

Um cyberdeck construído a partir de um gamestick baseado em chip Rockchip, explorando os limites (e as dores de cabeça) de rodar Linux em hardware ARM de baixo custo.

## Sobre o projeto

Este repositório documenta o processo de construção de um cyberdeck caseiro, usando como base um gamestick com chip Rockchip. O objetivo é transformar um dispositivo barato e limitado em uma máquina Linux funcional, com uma interface de terminal personalizada e propósito prático, unindo hardware e software, algo que quero levar para a área de engenharia mecatrônica.

Este ainda não é um projeto finalizado. É um registro técnico: o que funcionou, o que não funcionou, e por quê.

## Hardware

- **Base:** Gamestick genérico, chip Rockchip (ARM), 2 GB RAM DDR3
- **Periféricos adicionados:**
  - Hub USB
  - Adaptador Wi-Fi USB
- **Planejado:**
  - Tela HDMI
  - Case impressa em 3D

## Software

- **Distro:** Slax Linux, baseada no Debian 12.2.0
- **Arquitetura da imagem:** x86 (32-bit)
- **Arquitetura do hardware:** ARM

## Problema atual: incompatibilidade de arquitetura

O maior obstáculo até agora: a imagem do Slax que estou usando é x86 (32-bit), mas o gamestick roda em ARM. Isso significa que o sistema não inicializa corretamente / não consegue rodar binários nativos, pois os conjuntos de instruções são incompatíveis (x86 usa CISC, ARM usa RISC; não dá pra simplesmente rodar um binário compilado para uma arquitetura na outra sem emulação).

- [ ] Encontrar uma imagem do Slax (ou outra distro leve) feita especificamente para ARM
- [ ] Verificar suporte oficial da Rockchip para essa variante do chip (identificar o modelo exato: RK3229? RK3288? RK3328?)
- [ ] Testar distros alternativas com builds ARM confirmadas (Armbian, DietPi, Debian ARM oficial)
- [ ] Considerar QEMU/emulação como último recurso (não recomendado para uso diário, apenas testes)
- [ ] Adicionar tela HDMI ao cyberdeck
- [ ] Projetar e imprimir uma case em 3D para o cyberdeck

## Log de progresso

| Data | O que foi feito | Resultado |
|------|------------------|-----------|
| 10/julho/2026 | Instalação inicial do Slax x86 | Falhou ao inicializar — suspeita de incompatibilidade de arquitetura |
| 11/julho/2026 | Adição do Hub USB e do adaptador Wi-Fi USB ao cyberdeck | Periféricos conectados com sucesso |

---

Projeto pessoal de Pedro Henrique Rocha Ladislau da Silva, parte dos estudos em TI (IFRO) e interesse em engenharia mecatrônica.

---

# DIY Cyberdeck EN 🇺🇸

**Work in Progress**

A cyberdeck built from a Rockchip-based gamestick, exploring the limits (and headaches) of running Linux on low-cost ARM hardware.

## About the project

This repository documents the process of building a homemade cyberdeck, using a gamestick with a Rockchip chip as the base. The goal is to turn a cheap, limited device into a functional Linux machine with a customized terminal interface and practical purpose combining hardware and software, which is something I want to carry into the mechatronics engineering field.

This isn't a finished project (yet). It's a technical log: what worked, what didn't, and why.

## Hardware

- **Base:** Generic gamestick, Rockchip chip (ARM), 2 GB RAM DDR3
- **Added peripherals:**
  - USB Hub
  - USB Wi-Fi adapter
- **Planned:**
  - HDMI display
  - 3D-printed case

## Software

- **Distro:** Slax Linux, based on Debian 12.2.0
- **Image architecture:** x86 (32-bit)
- **Hardware architecture:** ARM

## Current issue: architecture mismatch

The biggest obstacle so far: the Slax image I'm using is x86 (32-bit), but the gamestick runs on ARM. This means the system doesn't boot properly / can't run native binaries, because the instruction set architectures are incompatible (x86 uses CISC, ARM uses RISC; you can't just run a binary compiled for one on the other without emulation).

- [ ] Find a Slax (or other lightweight distro) image built specifically for ARM
- [ ] Check for official Rockchip support for this chip variant (identify the exact model: RK3229? RK3288? RK3328?)
- [ ] Try alternative distros with confirmed ARM builds (Armbian, DietPi, official Debian ARM)
- [ ] Consider QEMU/emulation as a last resort (not recommended for daily use, testing only)
- [ ] Add HDMI display to the cyberdeck
- [ ] Design and 3D-print a case for the cyberdeck

## Progress log

| Date | What was done | Result |
|------|----------------|--------|
| 10/July/2026 | Initial Slax x86 install | Failed to boot — suspected architecture mismatch |
| 11/July/2026 | Added USB Hub and USB Wi-Fi adapter to the cyberdeck | Peripherals connected successfully |

---

Personal project by Pedro Henrique Rocha Ladislau da Silva, part of ongoing IT studies (IFRO) and interest in mechatronics engineering.
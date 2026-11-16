# Pencil Car 🚗✏️

Desenhe a estrada e o carro faz o resto. Jogo em HTML/JS (arquivo único em `www/index.html`) empacotado como app Android com Capacitor 8 (Android 16 / API 36).

## APK
Cada envio para a branch `main` roda o GitHub Actions (**Actions → Build APK**) e publica o APK em **Releases**.
Link fixo da versão mais recente:
https://github.com/GabrielTrama/pencilcar/releases/latest/download/PencilCar.apk

## Detalhes do app
- Pacote: `com.gabriel.pencilcar`
- Tela cheia, sempre em paisagem; botão voltar do Android volta ao menu.
- Assinado com uma chave de teste fixa (`android/app/pencilcar-teste.keystore`) para que as atualizações instalem por cima sem perder o progresso.
- **Play Store:** não usar essa chave de teste. Para publicar, gerar uma chave de upload própria (guardada fora do repositório) e um AAB (`bundleRelease`).

## Ícone e abertura
- Ícones gerados com `npx capacitor-assets generate --android` a partir de `assets/icon-*.png`.
- A abertura nativa é `android/app/src/main/res/drawable/splash.xml` (logo centralizado, não estica). Não há `assets/splash.png` de propósito.

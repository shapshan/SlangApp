# Сленг IQ — Android APK

## Способ 1: без установки чего-либо (GitHub Actions)
1. Создайте новый репозиторий на github.com и загрузите в него все файлы из этой папки
   (включая скрытую папку `.github`).
2. Откройте вкладку **Actions** → дождитесь зелёной галочки (3–6 минут).
3. Откройте последний запуск → внизу **Artifacts** → скачайте `slang-iq-apk`.
4. Внутри архива `app-debug.apk` — перенесите на телефон и установите
   (разрешите установку из неизвестных источников).

## Способ 2: локально (нужны Node 20, JDK 17, Android SDK)
```
npm install
npm run css
npx cap add android
npx cap sync android
cd android && ./gradlew assembleDebug
```
APK: `android/app/build/outputs/apk/debug/app-debug.apk`

Для публикации в Google Play нужна подписанная release-сборка (AAB).

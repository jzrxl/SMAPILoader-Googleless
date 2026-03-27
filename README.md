# FORKED FOR ARCHIVE PURPOSES (ENG Translated)

# 📢 Manifest
I understand, of course. Work should be paid, and piracy is a criminal offense in some countries,
but mere mortals shouldn't have to suffer because of tilting at windmills. Especially users of Huawei phones without Google Play
and ideological opponents of Google (I, for example, wouldn't give them a dime even if I could),
who are completely deprived of the opportunity to play with mods due to someone's whim. They
may have been able to buy a game on their phone from Google Play at one point, but having switched to
Huawei/having gotten rid of Google, they will be forced to suffer without mods, getting punched in the face
without a shred of sympathy or a solution. Moreover, if you believe the internet, even previously purchased copies from Google Play can no longer be installed in Russia. Consequently, there isn't much choice.

![image](./img/windmills.png)

It's not my style to be offended by the mentally ill people that ardent copyright zealots are.
The game is DRM-free, so this repository and fork don't violate the original license, the game's license, or anyone else's rights, as it doesn't allow anything to circumvent the already absent license check in the pure game. Not doing something isn't prohibited by law,
just like creating a fork that doesn't do what the original did.

# 🛠️ SMAPI Launcher
![image](https://github.com/user-attachments/assets/09a5f3fa-0b99-4aae-8f47-2de9009d5209)

# 🌟 Features
- - Send logs to the SMAPI server with one button.
- Update SMAPI without reinstalling the game or loader.
- No labor-intensive manual manipulation required.
- Support for games installed from the Galaxy Store, Google Play, and via APK.
- Transparent build via GitHub Actions.
The APK is built directly from the contents of this repository in a clean and controlled virtual machine provided by GitHub. You can track the progress and download the latest build here:
  [![.NET](https://github.com/IvanKr08/SMAPILoader-Googleless/actions/workflows/publish.yml/badge.svg)](https://github.com/IvanKr08/SMAPILoader-Googleless/actions/workflows/publish.yml)


# 🕒 Plans
- [ ] Russification of SMAPI Launcher itself.
- [ ] Import/export/backup saves.
- [ ] Automatically download/update SMAPI.
- [x] ~~Automated build via GitHub Actions~~
- [x] ~~Android 5.~~ Currently confirmed to work on Android 5.1.
- [ ] ARM32, x86, and AMD64 support. Runtime patches have been written, but MonoMod hasn't been ported to ARM32 yet,
and I don't have native libraries for x86/AMD64. Furthermore, I'm not sure Stardew Valley even exists for these architectures. But if it does, please share the libraries from the APK.


# 📲 Установка
1. Скачать/собрать и установить [SMAPI Launcher](https://github.com/IvanKr08/SMAPILoader-Googleless/releases).
   Экспериментальные сборки есть в [GitHub Actions](https://github.com/IvanKr08/SMAPILoader-Googleless/actions).
2. Скачать SMAPI.4.x.x-(xxxx).zip [отсюда](https://github.com/NRTnarathip/SMAPI-Android-1.6/releases)
   **(автор перестал выпускать свежие сборки SMAPI в GitHub, только в таиландском Discord)**.
3. Запустить SMAPI Launcher.
4. "Install SMAPI From Zip", после чего выбрать архив со SMAPI.
5. Дождаться "Successfully Install SMAPI".
6. "Start Game", после чего SMAPI Launcher клонирует игру, внедрит SMAPI и запустит ее.
7. Убедиться, что игра работает, после чего установить желаемые моды через встроенный менеджер.

# ‼️ Известные проблемы
- Новое сохранение *не создается* и появляется сообщение "SMAPI Launcher не отвечает".
  - Не нажимать на экран после подтверждения создания персонажа, игра может думать вплоть до минуты.
	Если сообщение всё равно появляется, то сразу после попадания в мир нужно перезапустить игру.
    Загрузка существующего сохранения требует 5-10 секунд и не вызывает это сообщение.
- Мод N отключен из-за несовместимости. Обновите мод.
  - Большая часть модов, которые подписаны как "предназначено для Android",
    были созданы под мобильный SMAPI для 1.5 и несовместимы с новым форком.
    Чаще работает версия, которая предназначена для ПК.
- Мод якобы загружен, но на практике не работает или сыплет ошибками в консоль.
  - Мобильный SMAPI находится в зачаточном состоянии и некоторые внутренние аспекты игры
    отличаются от компьютерной версии. Можете написать автору мода с просьбой исправить его,
    но далеко не факт, что он будет в этом заинтересован/увидит физическую возможность.
    В противном случае придется либо отказаться от мода, либо исправлять его самостоятельно
    (после чего патч можно будет предложить автору).
    Требуется распаковать сборки игры из APK (файл assemblies.blob) и иметь базовые представления о C#,
    после чего существует 2 варианта:
      1. Скачать исходный код, подключить зависимости (конкретно StardewValley.dll и StardewModdingAPI.dll)
         и собрать его.
      2. Пропатчить несовместимости через dnSpyEx. В целом проще и быстрее, плюс позволяет исправлять моды
         с закрытым кодом, но несколько устарел и может серьезно напугать количеством непонятных вещей
         (которые вам не нужны). Еще очень желательно понимать, как работает стековая виртуальная машина,
         чтобы иметь возможность модифицировать MSIL напрямую. Код из декомпилятора не всегда собирается назад.
  - Более того, совместимость может ломаться между версий SMAPI. Попробуйте 4.1.&ast;, 4.2.&ast; и 4.3.&ast;.

# #️⃣ Связь
Discord-сервер оригинала - SMAPI Thailand: https://discord.com/invite/ETtycvcJjr

**Не ожидайте получить там помощь для данного форка. В лучшем случае вам ничего не ответят,
в худшем могут назвать очень плохими словами и даже забанить**

При любых проблемах или вопросах пишите в [Issues](https://github.com/IvanKr08/SMAPILoader-Googleless/issues)
и [Discussions](https://github.com/IvanKr08/SMAPILoader-Googleless/discussions).

Если у вас нет аккаунта GitHub, то на [4PDA](https://4pda.to/forum/index.php?showtopic=945283)
или [русском сервере Discord](https://discord.gg/XCka9TDaGx).
В двух последних случаях не забудьте пингануть меня (IvanKr08), ибо я их не читаю просто так.

# 📦 Самостоятельная сборка
1. Установить .NET SDK 8 и Android SDK (ничего не понимаю в Android, но ваш SDK обязан поддерживать API 29).
   Android SDK должен быть прописан в переменной ANDROID_HOME. Если вы используете Visual Studio,
   то нужно установить весь набор для MAUI
   (по какой-то причине иначе не появляется менеджер SDK, даже если поставить всё отдельно от MAUI).
2. Клонировать или скачать репозиторий.
3. Открыть cmd и перейти в папку с репозиторием.
4. "dotnet workload restore" (нужно 3+ гигабайт свободного места на системном разделе).
5. "dotnet run --project LibPatcher patch".
   Это автоматически пропатчит рантайм Mono. Если этого не сделать, то игра откажется запускаться из-за MethodAccessException
   (если вы не сразу его пропатчили, то обязательно удалите obj и bin перед повторной сборкой). [Больше информации](/LibPatcher).
6. Помолиться и выполнить "dotnet publish ./SMAPIGameLoader".
7. Если появились ошибки, то сообщить о них через [Issues](https://github.com/IvanKr08/SMAPILoader-Googleless/issues) или
   попытаться исправить самостоятельно.
8. Если сборка завершилась успешно, то можно устанавливать получившийся APK.

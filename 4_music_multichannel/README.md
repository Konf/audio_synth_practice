[Назад в оглавление](../README.md)

# Проигрывание простой музыки на двух звуковых каналах
Демонстрация проигрывания простой музыки на звуковом канале находится в папке `audio_synth_practice/4_music_multichannel`.

Чтобы запустить тестбенч, выполните в консоли Modelsim:
```
cd audio_synth_practice/4_music_multichannel
do make.do
```

Эта демонстрация добавляет к части 3 второй звуковой канал и простое микширование между двумя каналами.
Тестбенч построен так, что на обоих каналах играются одинаковые ноты, но разными генераторами, с целью получения более «интересного» звука.
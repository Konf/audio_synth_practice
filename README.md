# Цифровой звук - практическое занятие

Данный репозиторий содержит практические задания к занятию "Генерация звука в цифровых схемах. История развития звука в компьютерах" и пояснительную документацию к примерам.

## Список примеров со ссылками:
- [1.1. Генераторы простых форм сигнала - прямоугольная волна](1_wave_generators/1_square/README.md)
- [1.2. Генераторы простых форм сигнала - пила](1_wave_generators/2_saw/README.md)
- [1.3. Генераторы простых форм сигнала - обратная пила](1_wave_generators/3_saw_inv/README.md)
- [1.4. Генераторы простых форм сигнала - треугольная волна](1_wave_generators/4_triangle/README.md)
- [1.5. Генераторы простых форм сигнала - синусоида](1_wave_generators/5_sine/README.md)
- [1.6. Генераторы простых форм сигнала - шум](1_wave_generators/6_noise/README.md)
- [2. Звуковой канал](2_audio_channel/README.md)
- [3. Воспроизведение простой музыки](3_music/README.md)
- [4. Полифония](4_music_multichannel/README.md)
- [5.1. Частотная модуляция](5_modulation/1_frequency_modulation/README.md)
- [5.2. Амплитудная модуляция](5_modulation/2_amplitude_modulation/README.md)
- [6. Проигрывание сэмплов](6_samples/README.md)

## Структура testbench и основная информация
Суть практической части занятия заключается в изучении примеров генерации звука. Практическая часть выполняется в симуляторе Modelsim/Questa. Предложенный testbench генерирует .wav файлы со звуком, позволяя Вам услышать звук на своём компьютере, не используя отладочные стенды с FPGA.
В используемом на данном занятии testbench можно выделить следующие секции:
- Функции write_wav_number и write_wav – предназначены для записи wav файла
- Генерация опорной тактовой частоты 12.5 МГц, используемой во всех генераторах звука
- Генерация сброса
- Initial-блок c последовательностью действий и нот
- Логика, имитирующая работу АЦП с частотой 48 КГц. Эта логика захватывает выход генераторов и, используя SystemVerilog Queue, сохраняет звуковые отчеты для вывода в wav файл.

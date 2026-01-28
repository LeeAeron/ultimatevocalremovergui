## UVR5 models

## RUS


## 🧩 MDX-Net Models

## 🔰 MDX-Net v1/v2
Основаны на архитектуре Multi-Dilated Convolutional Networks (MDX).

Отличаются высокой точностью при разделении вокала и инструментов. 

Подходят для большинства жанров, особенно для чистых студийных записей.

Минус: относительно высокая нагрузка на GPU/CPU.

## 🔰 MDX23C
Оптимизированная версия MDX-Net с улучшенной скоростью и меньшими требованиями к памяти.

Добавлен режим denoise, который помогает убирать шумы и артефакты.

Хорошо работает на живых записях и сложных миксах.

## 🎛 UVR-MDX-NET Inst HQ 1–5
Назначение: Отделение инструментала от вокала.

HQ1–HQ5: Чем выше номер, тем выше качество и нагрузка.

HQ2/3 — лучше вытаскивают длинный вокал.

HQ4/5 — дают чуть чище результат, но медленнее.

Архитектура: Full-band MDX-Net.

## 🎚 UVR-MDX-NET Inst 1–3
Назначение: Более лёгкие модели для инструментала.

Особенности: Могут оставлять вокальный хвост, но звучат натуральнее.

Нагрузка: Ниже, чем HQ-серия.

## ⚖ UVR-MDX-NET Main / Inst Main
Назначение: Универсальные модели для вокал/инструментал.

Баланс: Хорошее качество при умеренной нагрузке.

Применение: Базовые модели для ансамблей.

## 🎤 UVR-MDX-NET Karaoke / Karaoke 2
Назначение: Удаление лид-вокала, сохранение фоновых голосов и инструментала.

Применение: Создание караоке.

## 🧪 Специализированные MDX-модели
Voc FT / Kim Vocal: Заточены на извлечение вокала.

Crowd HQ 1: Хорошо работает с концертами и "толпой".

Reverb HQ by FoxJoy: Подавление реверберации и эха.


## 🔄 Roformer Models

▪️RoFormer — это улучшенная архитектура Transformer, использующая встраивание вращающихся позиций (RoPE) для более эффективного кодирования позиций токенов в последовательности. Это позволяет моделям лучше учитывать как абсолютные, так и относительные зависимости между текстовыми элементами и масштабироваться до длинных последовательностей.

▪️RoFormer — это модификация стандартного Transformer, предложенная в 2021 году исследователями Цзяньлинем Су и его коллегами.

Главное нововведение — это встраивание вращающихся позиций (RoPE), метод, который кодирует позиционную информацию путем вращения входных векторов в двумерном пространстве.

▪️ Почему RoPE?
В классических Transformer позиционная информация добавляется с помощью фиксированных или обучаемых встраиваний.

▪️ RoPE позволяет:

Учитывать относительные позиции токенов, а не только абсолютные.

Моделировать естественное затухание зависимостей между токенами по мере увеличения расстояния.

Масштабироваться до длинных последовательностей без потери качества.

▪️ Приложения
Обработка текста: Повышение качества языковых моделей (например, в задачах машинного перевода и генерации текста).

Музыка и аудио: RoFormer адаптирован для задач разделения источников звука (например, вокала и инструментов), где важны временные зависимости.

Эффективные модели: RoPE хорошо работает с линейным самовниманием, что ускоряет обучение и вывод результатов.


## 🔰 BS-Roformer (Band-Split Roformer)

Использует архитектуру Roformer (Rotary Transformer), адаптированную для аудио.

Делит спектр на диапазоны (band-split), что повышает точность разделения.

Отличается лучшей обработкой длинных контекстов и сложных вокальных партий.

Минус: требует больше ресурсов, чем MDX23C.

## 🔰 ViperX Roformer

Вариант Roformer, оптимизированный для скорости.

Подходит для потоковой обработки и быстрой сегментации.

Чуть уступает BS-Roformer по качеству, но выигрывает в производительности.

## 🧬 MDX23C InstVoc HQ
Архитектура: Гибрид MDX + спектральная точность.

Назначение: Одновременное извлечение вокала и инструментала.

Качество: Один из лучших SDR на современных тестах.

## 🧠 BS-Roformer-Viperx (1297, 1296, 1053, 1143)
Архитектура: Band-Split Roformer.

Авторы: Viperx и др.

Особенности: Максимальное качество, высокая VRAM нагрузка.

1297: Часто в топе таблиц качества.

## 🎵 MelBand Roformer Kim
Варианты: InstV1/V2, InstVoc Duality, InstV1(E).

Назначение: Чистый инструментал или парное разделение.

Особенности: Разные параметры и тренировочные датасеты.


## 🎶 VR-Architecture Models

## VR Arch v1/v2/v3

Классическая линейка моделей UVR (Ultimate Vocal Remover).

Основаны на спектральных методах и CNN-архитектуре.

Отличаются стабильностью и низкими требованиями к ресурсам.

Хорошо подходят для слабых ПК и ноутбуков.

Минус: качество разделения ниже, чем у MDX-Net и Roformer.

## 🧰 VR Arch v1/v2/v3
Архитектура: Классическая CNN.

Назначение: Базовое разделение вокала/инструментала.

Нагрузка: Низкая, подходит для слабых ПК.

Качество: Ниже, чем у MDX и Roformer.

## 🧩 Kuielab Models

## 🔊 kuielab_a_vocals / bass / drums / other
Назначение: Разделение на 4 стема.

Качество: Хорошее, умеренная нагрузка.

##  🔊 kuielab_b_vocals / bass / drums / other
Назначение: Улучшенная серия.

Особенности: b_vocals — агрессивный экстрактор вокала.


## UVR5 Model Overview

| Модель                               | Назначение                 | Архитектура         | Качество     | Нагрузка      | Особенности                              |
|--------------------------------------|----------------------------|---------------------|--------------|---------------|------------------------------------------|
| UVR-MDX-NET Inst HQ 1–5              | Инструментал/вокал         | MDX-Net Full-band   | Очень высокое| Средне–высокая| HQ3/4 — лучший баланс                    |
| UVR-MDX-NET Inst 1–3                 | Инструментал               | MDX-Net             | Среднее      | Низкая        | Натуральное звучание                     |
| UVR-MDX-NET Main / Inst Main         | Универсальное разделение   | MDX-Net             | Хорошее      | Средняя       | Базовые модели для ансамблей             |
| UVR-MDX-NET Karaoke / Karaoke2       | Караоке                    | MDX-Net             | Среднее      | Средняя       | Сохраняет фоновые голоса                 |
| MDXNET_9482 / Voc FT / Kim Vocal     | Вокал                      | MDX-Net             | Высокое      | Средняя       | Адаптированы под вокал                   |
| Crowd HQ 1                           | Концертные записи          | MDX-Net             | Среднее      | Средняя       | Хорошо работает с "толпой"               |
| Reverb HQ by FoxJoy                  | Подавление реверберации    | MDX-Net             | —            | Средняя       | Удаляет эхо и реверб                     |
| MDX23C InstVoc HQ                    | Вокал+инструментал         | MDX23C (гибрид)     | Очень высокое| Высокая       | Лучший SDR на тестах                     |
| BS-Roformer-Viperx 1297 и др.        | Вокал/инструментал         | Band-Split Roformer | Максимальное | Очень высокая | Топ по качеству                          |
| MelBand Roformer Kim (V1/V2/Duality) | Вокал/инструментал         | MelBand Roformer    | Высокое      | Высокая       | Разные версии под задачи                 |
| VR Arch v1/v2/v3                     | Базовое разделение         | CNN                 | Среднее      | Низкая        | Подходит для слабых ПК                   |
| kuielab_a_vocals/bass/drums/other    | Стем-разделение            | CNN                 | Хорошее      | Средняя       | 4 канала: вокал, бас, ударные, остальное |
| kuielab_b_vocals/bass/drums/other    | Улучшенное стем-разделение | CNN                 | Очень хорошее| Средне–высокая| b_vocals — агрессивный экстрактор        |


## 💿 Что такое Apollo

Apollo — это метод моделирования полосовой последовательности для высококачественного восстановления звука.

Разработан исследователями из Университета Цинхуа и лаборатории искусственного интеллекта Tencent.

Основная цель: восстановление музыки, искаженной кодеками (особенно при низких битрейтах).

Работает в частотной области: разделяет спектрограмму на поддиапазоны, моделирует временные и спектральные зависимости и восстанавливает высокочастотные детали.

Модель ориентирована на музыку, а не на речь (для речи лучше использовать UVR или Demucs).


##ENG

## 🧩 MDX-Net Models

🔰 MDX-Net v1/v2
Based on the Multi-Dilated Convolutional Networks (MDX) architecture.

They are characterized by high accuracy in separating vocals and instruments.

Suitable for most genres, especially clean studio recordings.

Con: Relatively high GPU/CPU load.

## 🔰 MDX23C
Optimized version of MDX-Net with improved speed and lower memory requirements.

Added denoise mode, which helps remove noise and artifacts.

Works well on live recordings and complex mixes.

## 🎛 UVR-MDX-NET Inst HQ 1–5
Purpose: Separating instrumentals from vocals.

HQ1–HQ5: The higher the number, the higher the quality and load.

HQ2/3 — better at extracting long vocals.

HQ4/5 — produce slightly cleaner results, but slower.

Architecture: Full-band MDX-Net.

## 🎚 UVR-MDX-NET Inst 1–3
Purpose: Lighter models for instrumentals.

Features: May leave vocal tails, but sound more natural.

Power handling: Lower than the HQ series.

## ⚖ UVR-MDX-NET Main / Inst Main
Purpose: General-purpose models for vocals/instruments.

Balance: Good quality at moderate power handling.

Use: Basic models for ensembles.

## 🎤 UVR-MDX-NET Karaoke / Karaoke 2
Purpose: Removing lead vocals, preserving background vocals and instrumentals.

Application: Karaoke production.

## 🧪 Specialized MDX Models
Voc FT / Kim Vocal: Focused on vocal extraction.

Crowd HQ 1: Works well with concerts and crowds.

Reverb HQ by FoxJoy: Suppresses reverberation and echo.


## 🔄 Roformer Models

▪️RoFormer is an improved Transformer architecture that uses Rotary Position Embedding (RoPE) to more efficiently encode token positions in a sequence. This allows models to better account for both absolute and relative dependencies between text elements and scale to long sequences.

▪️RoFormer is a modification of the standard Transformer, proposed in 2021 by researchers Jianlin Su and colleagues.

The main innovation is Rotary Position Embedding (RoPE), a method that encodes positional information by rotating input vectors in two-dimensional space.

▪️ Why RoPE?
In classic Transformers, positional information is added through fixed or learnable embeddings.

▪️ RoPE allows you to:

Consider the relative positions of tokens, not just absolute ones.

Model the natural decay of dependencies between tokens as distance increases.

Scaling to long sequences without loss of quality.

▪️ Applications
Text processing: Improving the quality of language models (e.g., in machine translation and text generation tasks).

Music and audio: RoFormer is adapted for audio source separation tasks (e.g., vocals and instruments), where temporal dependencies are important.

Efficient models: RoPE works well with linear self-attention, which speeds up training and inference.


## 🔰 BS-Roformer (Band-Split Roformer)

Uses the Roformer (Rotary Transformer) architecture adapted for audio.

Divides the spectrum into bands (band-split), which improves separation accuracy.

Distinguished by better processing of long contexts and complex vocal parts.

Con: Requires more resources than the MDX23C.

## 🔰 ViperX Roformer

A speed-optimized Roformer variant.

Suitable for streaming processing and fast segmentation.

Slightly inferior to BS-Roformer in quality, but superior in performance.

## 🧬 MDX23C InstVoc HQ
Architecture: Hybrid MDX + spectral accuracy.

Purpose: Simultaneous extraction of vocals and instrumentals.

Quality: One of the best SDRs in modern tests.

## 🧠 BS-Roformer-Viperx (1297, 1296, 1053, 1143)
Architecture: Band-Split Roformer.

Creators: Viperx and others.

Features: Maximum quality, high VRAM load.

1297: Frequently at the top of quality charts.

## 🎵 MelBand Roformer Kim
Variants: InstV1/V2, InstVoc Duality, InstV1(E).

Purpose: Pure instrumental or paired separation.

Features: Various parameters and training datasets.

They are characterized by stability and low resource requirements.

Well suited for low-end PCs and laptops.

Cons: Separation quality is lower than that of MDX-Net and Roformer.

## 🧰 VR Arch v1/v2/v3
Architecture: Classic CNN.

Purpose: Basic vocal/instrumental separation.

Load: Low, suitable for low-end PCs.

Quality: Lower than MDX and Roformer.

## 🧩 Kuielab Models

## 🔊 kuielab_a_vocals / bass / drums / other
Purpose: Separation into 4 stems.

Quality: Good, moderate load.

## 🔊 kuielab_b_vocals / bass / drums / other
Purpose: Improved series.

Features: b_vocals is an aggressive vocal extractor.


## UVR5 Model Overview

| Model                                 | Purpose                   | Architecture        | Quality   | Load Capacity | Features                               |
|---------------------------------------|---------------------------|---------------------|-----------|--------------------------------------------------------|
| UVR-MDX-NET Inst HQ 1–5               | Instrumental/Vocal        | MDX-Net Full-band   | Very High | Medium-High   | HQ3/4 — Best Balance                   |
| UVR-MDX-NET Inst 1–3                  | Instrumental              | MDX-Net             | Medium    | Low           | Natural                                |
| UVR-MDX-NET Main / Inst Main          | Versatile Separation      | MDX-Net             | Good      | Average       | Basic Ensemble Models                  |
| UVR-MDX-NET Karaoke / Karaoke2        | Karaoke                   | MDX-Net             | Medium    | Medium        | Preserves background vocals            |
| MDXNET_9482 / Voc FT / Kim Vocal      | Vocals                    | MDX-Net             | High      | Medium        | Adapted for vocals                     |
| Crowd HQ 1                            | Live recordings           | MDX-Net             | Medium    | Medium        | Works well with crowds                 |
| Reverb HQ by FoxJoy                   | Reverb reduction          | MDX-Net             | —         | Medium        | Removes echo and reverb                |
| MDX23C InstVoc HQ                     | Vocals + Instruments      | MDX23C (Hybrid)     | Very High | High          | Best SDR in tests                      |
| BS-Roformer-Viperx 1297 and others    | Vocals/Instrumentals      | Band-Split Roformer | Maximum   | Very High     | Top quality                            |
| MelBand Roformer Kim (V1/V2/Duality)  | Vocals/Instruments        | MelBand Roformer    | High      | High          | Different versions for different tasks |
| VR Arch v1/v2/v3                      | Basic Separation          | CNN                 | Medium    | Low           | Suitable for low-end PCs               |
| kuielab_a_vocals/bass/drums/other     | Stem Separation           | CNN                 | Good      | Medium        | 4 channels: vocals, bass, drums, other |
| kuielab_b_vocals/bass/drums/other     | Enhanced Stem Separation  | CNN                 | Very Good | Medium-High   | b_vocals — Aggressive Extractor        |


## 💿 What is Apollo

Apollo is a band-sequence modeling method for high-quality audio restoration.

Developed by researchers from Tsinghua University and Tencent AI Lab.

The main goal: restoring music distorted by codecs (especially at low bitrates).

Works in the frequency domain: it divides the spectrogram into subbands, models temporal and spectral dependencies, and restores high-frequency details.

The model is focused on music, not speech (for speech, it is better to use UVR or Demucs).


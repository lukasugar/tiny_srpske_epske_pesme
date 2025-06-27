# tiny_epske_pesme
🤗 https://huggingface.co/datasets/alkibijad/tiny_srpske_epske_pesme 🤗

## 🇷🇸 Српска верзија `tiny shakespeare` скупа података
Када сам се играо сам тренирањем малих језичких модела и пратио неки од Карпатијевих видео, пало ми је на памет да уместо Шекспирових дела ([tiny_shakespeare](https://raw.githubusercontent.com/karpathy/char-rnn/master/data/tinyshakespeare/input.txt)) користим српске епске песме.

Разлози за то су:
- тренирање и тестирање над ћирилицом значи коришћење токена који су мање заступљени на интернету у односу на енглески језик
- јер ми архаични енглески није матерњи, и требало би да у раним епохама тренинга лакше уочим напредак модела на српском
- само ме је занимало како ће да ради 😅


### Коришћење
Уместо линка ка `tiny_shakespeare`, треба користити линк ка фајлу у овом репозиторијуму.
Нпр. у [nanoGPT](https://github.com/karpathy/nanoGPT/blob/93a43d9a5c22450bbf06e78da2cb6eeef084b717/data/shakespeare/prepare.py#L7-L11) пројекту:
```
input_file_path = os.path.join(os.path.dirname(__file__), 'input.txt')
if not os.path.exists(input_file_path):
    # data_url = 'https://raw.githubusercontent.com/karpathy/char-rnn/master/data/tinyshakespeare/input.txt'
    data_url = https://raw.githubusercontent.com/lukasugar/tiny_epske_pesme/refs/heads/main/data_final/sve_srpske_epske_pesme.txt?token=GHSAT0AAAAAACMY3KTXCGNFC6GWBS4U2YA42C4FIOQ
    with open(input_file_path, 'w', encoding='utf-8') as f:
        f.write(requests.get(data_url).text)
```

### 📊 Поређење величина скупова података

| Скуп података                | Број редова | Број карактера |
|------------------------------|:-----------:|:--------------:|
| Tiny Shakespeare             |   32,777    |   1,115,394    |
| Све српске епске песме       |   26,047    |    737,054     |


| Поређење                        | Вредност                |
|----------------------------------|-------------------------|
| Tiny Shakespeare је              | 151.33% величине „Све српске епске песме“ |
| „Све српске епске песме“ је      | 0.7x величине Tiny Shakespeare            |
| Апсолутна разлика                | -378,340 карактера      |


Ово показује да је нови скуп за око 30% мањи оригиналног `Tiny Shakespeare`, што није идеално, али требало би да је довољно за ”играрију” са малим моделима.




## 🇬🇧 Serbian version of the `tiny shakespeare` dataset

When I was playing around with training small language models and following one of Karpathy's videos, it occurred to me that instead of Shakespeare's works ([tiny_shakespeare](https://raw.githubusercontent.com/karpathy/char-rnn/master/data/tinyshakespeare/input.txt)), I could use Serbian epic poems.

The reasons for this are:
- Training and testing on Cyrillic means using tokens that are less represented on the internet compared to the English language
- Because archaic English is not my native language, I should be able to notice the model's progress in Serbian more easily during the early stages of training
- I was just curious to see how it would work 😅

### Usage
Instead of the link to `tiny_shakespeare`, you should use the link to the file in this repository.
For example, in the [nanoGPT](https://github.com/karpathy/nanoGPT/blob/93a43d9a5c22450bbf06e78da2cb6eeef084b717/data/shakespeare/prepare.py#L7-L11) project:
```
input_file_path = os.path.join(os.path.dirname(__file__), 'input.txt')
if not os.path.exists(input_file_path):
    # data_url = 'https://raw.githubusercontent.com/karpathy/char-rnn/master/data/tinyshakespeare/input.txt'
    data_url = https://raw.githubusercontent.com/lukasugar/tiny_epske_pesme/refs/heads/main/data_final/sve_srpske_epeske_pesme.txt?token=GHSAT0AAAAAACMY3KTXCGNFC6GWBS4U2YA42C4FIOQ
    with open(input_file_path, 'w', encoding='utf-8') as f:
        f.write(requests.get(data_url).text)
```

### 📊 Dataset Size Comparison

| Dataset                     | Number of Lines | Number of Characters |
|-----------------------------|:---------------:|:-------------------:|
| Tiny Shakespeare            |     32,777      |     1,115,394       |
| All Serbian Epic Poems      |     26,047      |      737,054        |


| Comparison                        | Value                    |
|------------------------------------|-------------------------|
| Tiny Shakespeare is                | 151.33% the size of "All Serbian Epic Poems" |
| "All Serbian Epic Poems" is        | 0.7x the size of Tiny Shakespeare           |
| Absolute difference                | -378,340 characters      |


This shows that the new dataset is about 30% smaller than the original `Tiny Shakespeare`, which is not ideal, but should be enough for "playing around" with small models.


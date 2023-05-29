# Poem-Generation-Project
A text generation project which crawls data from web and uses transformer architecture to create Vietnamese poem

# Dataset
Taking Haiku poetry data from first 10 pages at https://www.thivien.net/searchpoem.php?PoemType=16&ViewType=1&Country=2 

# Progamming language
Python

# Inference
```python
n_sentences = 3
results = ['đời này còn lại gì']
for idx in range(n_sentences):
    input_str = results[idx]
    text, output_tokens, attention_weights = generate_text(
        transformer, 
        tokenizer,
        input_str
    )
    results.append(text.replace('<start>', '').replace('<end>', '').strip())
results = list(map(lambda x: x.capitalize(), results))
print('\n'.join(results))
```
```
Đời này còn lại gì
Người ấy đến rất thơ
Từ sâu rừng xanh tận
Một tình yêu thương yêu
```






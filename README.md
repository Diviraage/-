from googletrans import Translator

# Зчитування тексту для перекладу
text = input("Введіть текст для перекладу: ")

# Ініціалізація об'єкту Translator
translator = Translator()

# Переклад тексту з української мови на англійську мову
translated_text = translator.translate(text, src='uk', dest='en').text

# Збереження перекладеного тексту в файл або виведення результату на екран
save_or_print = input("Ви бажаєте зберегти перекладений текст у файлі? (y/n): ")
if save_or_print.lower() == 'y':
    with open('translated_text.txt', 'w') as f:
        f.write(translated_text)
else:
    print(translated_text)

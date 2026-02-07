import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt

# Загрузка данных из файла JSON, размещённого на GitHub
url = 'https://raw.githubusercontent.com/<your_username>/<repo_name>/main/events.json'
df = pd.read_json(url)

# Просмотр первых строк датасета
print(df.head())

# Изучаем структуру данных
print("Структура данных:")
print(df.info())

# Группировка событий по типу ("signature")
event_counts = df['signature'].value_counts()

# Распечатываем количество каждого типа события
print("\nКоличество событий по каждому типу:")
print(event_counts)
# Создание графика распределения событий по типам
plt.figure(figsize=(10, 6))
sns.countplot(data=df, x='signature', order=df['signature'].value_counts().index)
plt.title('Распределение событий информационной безопасности')
plt.xlabel('Тип события')
plt.ylabel('Количество событий')
plt.xticks(rotation=45)
plt.show()

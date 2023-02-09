1. Инициализация локального репозитория:
```bash
$git init
```

2. Привязать локальный репозиторий к удаленному:
```bash
$git remote add origin <ссылка на удаленный репозиторий>
```

3. Смержит ветки локального и удаленного репозитория после привязки:
```bash
$git pull origin main --allow-unrelated-histories
```

4. Коммитим изменения:
```bash
$git commit -m "<Комментарий к коммиту>"
```

5. Сделает ветку `main` репозитория `origin` отслеживаемой и запушит вследующий раз без ее указания:
```bash
$git push --set-upstream origin main
```
или
```bash
$git push -u origin main
```

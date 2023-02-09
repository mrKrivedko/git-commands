 Установить notepad++ в качестве гит редактора:
```bash
$git config --global core.editor "'C:/Program Files/Notepad++/notepad++.exe' -multiInst -notabbar -nosession -noPlugin"
```

Покажет какие коммиты прибавились по сравнению с веткой мастер:
```bash
$git cherry -v master
```
Покажет сколько их:
```bash
$git cherry -v master | wc -l
```

Передвинуть  HEAD на 5 коммитов назад. (-i - это интерактивный режим):
```bash
$git rebase -i HEAD~5
```

Пушит принудительно игнорируя конфликты:
```bash
$git push --force
```

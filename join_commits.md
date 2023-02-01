```git config --global core.editor "'C:/Program Files/Notepad++/notepad++.exe' -multiInst -notabbar -nosession -noPlugin"``` - установить notepad++ в качестве гит редактора.

```git cherry -v master``` - покажет какие коммиты прибавились по сравнению с веткой мастер.

```git cherry -v master | wc -l``` - покажет сколько их.

```git rebase -i HEAD~5``` - передвинуть  HEAD на 5 коммитов назад. (-i - это интерактивный режим)

```git push --force``` - пушит принудительно игнорируя конфликты.

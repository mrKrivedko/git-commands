Добавление коллабораторов
В своём репозитории на GitHub тимлид должен перейти во вкладку Settings, затем в левом боковом меню выбрать Collaborators и на открывшейся странице нажать кнопку Add people.

В открывшемся окне необходимо указать данные разработчика, которому предоставляется доступ к репозиторию в качестве соразработчика: его никнейм, полное имя или адрес электронной почты пользователя GitHub.

Если пользователь найден, то его нужно выбрать и нажать на кнопку Select a collaborator above;
после этого ваш коллега получит приглашение в репозиторий, оно придёт на адрес электронной почты, привязанный к GitHub.

Просмотр и создание веток
Можно посмотреть на все ветки, которые есть в склонированном репозитории и узнать, в какой ветке вы находитесь в данный момент. Если вы предпочитаете работу через терминал, то воспользуйтесь командой ```git branch``:
    
    git branch  # Команда для просмотра веток.
    * master  # Основная и пока единственная ветка проекта, 
    # звёздочкой отмечено, что вы в ней. 
    
    git branch develop  # Создали новую ветку с именем develop.
    git branch  # Проверили, в какой ветке находимся.
    develop  # Появилась новая ветка.
    * master  # Но мы пока находимся в ветке master. 

Ветка создана, но разработчик останется в ветке ```master```. Чтобы переключиться в ветку ```develop```, нужно ввести команду ```git checkout develop```:
    
    git checkout develop  # Переключились в ветку develop.
    git branch #  Проверили: "Где я?".
    * develop #  Звездочкой отмечена выбранная ветка.
    master 
    Применять дополнительную команду не обязательно: можно создать ветку и сразу переключиться на неё:
    git checkout -b develop  # Создали ветку develop и сразу переключились на неё.

Но ветка ```develop``` создана и сохранена лишь в локальном репозитории тимлида, а в репозитории на GitHub её пока нет. Чтобы сделать её доступной для других разработчиков, тимлид должен выполнить команду: 
    
    git push --set-upstream origin develop

После этого новая ветка будет доступна на GitHub, а когда соразработчики склонируют репозиторий тимлида себе, то обе ветки станут локально видны и им. 
Если остальные участники команды уже склонировали репозиторий, в котором тимлид еще не успел создать новую ветку, то чтобы увидеть добавленную ветку в удалённом репозитории им необходимо будет выполнить команду ```git fetch```.

Чтобы новая ветка стала видна и доступна для других разработчиков, создатель ветки должен синхронизировать изменения с удалённым репозиторием при помощи команды
    
    git push --set-upstream origin <имя ветки> 

Чтобы объединить («смержить») ветки, нужно переключиться в ветку, куда должны попасть изменения; из этой ветки нужно выполнить команду на слияние. 

- переключиться на ветку, в которую будут залиты изменения:

    git checkout develop  # Переключились в develop.
   
- переместить все коммиты из feature/email-validation в ветку develop — смержить ветки:
     
    git merge feature/email-validation

   
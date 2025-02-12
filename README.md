# Binfor GUI
Это наша первая графическая библиотека.

# Загрузка библиотеки

```lua
local library = loadstring(game:HttpGet('https://raw.githubusercontent.com/Aucor-Limited/BinFor-GUI/refs/heads/main/source.lua'))()
```

# Создание окна

```lua
local gui, sidebar, mainContent = library:CreateMainGUI("BinFor GUI")
```

# Создание вкладки

```lua
local mainTab = library:CreateTab("Main", sidebar, mainContent)
```

# Создание кнопки

```lua
local button = library:CreateButton("Button Example", mainTab, function()
    print("touched")
end)
```

# Создание поля ввода

```lua
local createTextBox = library:CreateTextBox(mainTab, "Введите текст...")
createTextBox.FocusLost:Connect(function()
    print("Введенный текст:", createTextBox.Text)
end)
```

# Создание тумблера

```lua
local createToggle = library:CreateToggle("Тумблер 1", mainTab, function(state)
    print("Тумблер 1:", state and "Включен" or "Выключен")
end)
```

# Создание выпадающего меню

```lua
local dropdown = library:CreateDropdown("Выберите опцию", mainTab, {"Опция 1", "Опция 2", "Опция 3"}, function(selected)
    print("Выбрана опция:", selected)
end)
```

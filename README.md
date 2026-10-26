fmi-ml-courses
Курс: эффективный fine-tuning мультимодальных моделей (VLM).

Стек
Модель: Qwen2.5-VL-3B-Instruct (4-bit QLoRA)
Железо: GTX 1050 Ti 4GB, Windows 10, conda env fmi-cv
Инструменты: LLaMA-Factory (lab 09), Unsloth (lab 10+)
Лабораторные
Лаба	Тема	Статус
09	Fine-tuning VLM с LLaMA-Factory (QLoRA r8, манифест, resume)	✅ готово
10	Эффективный fine-tuning с Unsloth (ранг 8 vs 16)	✅ готово
11	Текущая лаба	🚧 в работе
Как воспроизвести
conda activate fmi-cvjupyter lab

---

## Шаг 5. Первый коммит и выкладка на GitHub (5 минут)

Выполняй построчно в PowerShell (в папке курса). Замени `<твой_юзернейм>` на реальный.

```powershell
# 1. Превратить папку в репозиторий (завести историю)
git init

# 2. Сложить ВСЁ в «корзину» для снимка (кроме того, что в .gitignore)
git add .

# 3. ПРОВЕРКА: топ-10 самых больших файлов, попавших в снимок
git ls-files | ForEach-Object { Get-Item $_ -ErrorAction SilentlyContinue } |
  Sort-Object Length -Descending | Select-Object -First 10 Name, @{n='MB';e={[math]::Round($_.Length/1MB,1)}}
```
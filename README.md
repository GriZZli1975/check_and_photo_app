# Публичный репозиторий только для APK и манифеста обновлений.
# Исходный код приложения и backend — в приватном репозитории check_and_photo.

# Check & Photo — релизы приложения

Здесь только:
- `app-update.json` — манифест для автообновления в приложении
- **Releases** — APK-файлы

Основной проект (бот, API, код) — **приватный**, сюда не попадает.

## Публикация новой версии

Из приватного репозитория `check_and_photo`:

```powershell
.\scripts\publish_android_release.ps1 -Version "0.1.14" -Build 14 -Notes "Что нового"
```

Скрипт соберёт APK, создаст GitHub Release в **этом** репозитории и обновит `app-update.json`.

## Первичная настройка (один раз)

```powershell
.\scripts\init_app_releases_repo.ps1
```

Создаст публичный репозиторий `check_and_photo_app` на GitHub и запушит этот каталог.

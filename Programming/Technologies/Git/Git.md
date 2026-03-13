#git
- `git clone` - provodnikda git banch here orqali git reponi papka ochish orqali olib kelib
- `git add` - commit uchun qo'shish (git add . -hammasini qo'shish)
- `git commit -m "Add title"` - commit qilish
- `git checkout` - shoxni almashtirish
- `git checkout -b` - shox yaratish va unga o'tish
- `git init` - initial (ilk) commit qilish
- `git merge` - shoxlarni birlashtirish
- `git branch -d` - shoxni o'chirish
- `git status` - proyekt holatini ko'rish
- `git pull origin feature` - shoxni ozimizga olib kelish
- `git branch -d "branch-name"` - shoxni o'chirish
- `git remote add teamlead repo-link` - teamlead reponi ozimizga ulash ulash
- `git origin -v` komandasi git repositoriyasining remote versiyalarini ko'rsatadi.
- `git push origin [branch-name]` - lokal repo'da qilingan o'zgarishlarni serverga yuborish
- `git fetch` - serverdagi yangiliklarni lokal repo'ga yuklash
- `git diff` - commitlar orasidagi farqni ko'rish
- `git log` - o'tgan commitlarni ko'rish
- `git revert [commit-id]` - qilingan commitni bekor qilish
- `git reset --hard [commit-id]` - commit tarixiga qaytish
- `git tag -v [tag-name]` - tagning versiyasini tekshirish
- `git stash` - ishlamoqda bo'lgan o'zgarishlarni saqlab qolish
- `git stash pop` - saqlangan o'zgarishlarni qayta yuklash
- `git cherry-pick [commit-id]` - biror commitni boshqa shoxga ko'chirish - provodnikda git banch here orqali git reponi papka ochish orqali olib kelib

**Шаблон для создания ветвь на git:**

- `feature/` – если это новая функция.
- `fix/` – если это исправление ошибки.
- `hotfix/` – для быстрых исправлений критических багов.
- `chore/` – для несвязанных с функционалом задач (например, рефакторинг, обновление зависимостей).
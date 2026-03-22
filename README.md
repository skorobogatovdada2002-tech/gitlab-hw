# Домашнее задание к занятию «GitLab» — Скоробогатов Евгений

---

## Задание 1

### Что было сделано

- Развернут GitLab локально через Vagrant
- Создан проект `sdvps-materials` в GitLab
- Запущен GitLab Runner в Docker
- Runner успешно зарегистрирован и переведен в статус `online`

### Скриншот

![Runner](runner.png)

---

## Задание 2

### Что было сделано

- В проект добавлен файл `.gitlab-ci.yml`
- Настроены стадии `test` и `build`
- Pipeline успешно выполнен
- Получены успешные сборки jobs

### Файл `.gitlab-ci.yml`

```yaml
stages:
  - test
  - build

default:
  tags:
    - docker

test_job:
  stage: test
  image: alpine:latest
  script:
    - echo "Test stage"

build_job:
  stage: build
  image: alpine:latest
  script:
    - echo "Build stage"
```
### Скриншоты

![Pipeline](pipeline.png)

![Job](job.png)

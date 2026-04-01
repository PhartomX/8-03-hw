# Домашнее задание к занятию "`GitLab`" - `Алексей Сидоров`

---

### Задание 1

Что нужно сделать:

Разверните GitLab локально, используя Vagrantfile и инструкцию, описанные в этом репозитории.
Создайте новый проект и пустой репозиторий в нём.
Зарегистрируйте gitlab-runner для этого проекта и запустите его в режиме Docker. Раннер можно регистрировать и запускать на той же виртуальной машине, на которой запущен GitLab.
В качестве ответа в репозиторий шаблона с решением добавьте скриншоты с настройками раннера в проекте.


![img1](https://github.com/PhartomX/8-03-hw/blob/main/img/img1.png)


---

### Задание 2

Что нужно сделать:
Запушьте репозиторий на GitLab, изменив origin. Это изучалось на занятии по Git.
Создайте .gitlab-ci.yml, описав в нём все необходимые, на ваш взгляд, этапы.
В качестве ответа в шаблон с решением добавьте:
файл gitlab-ci.yml для своего проекта или вставьте код в соответствующее поле в шаблоне;
скриншоты с успешно собранными сборками.


```
.gitlab-ci.yml:

stages:
  - test
  - build
 
test:
  stage: test
  image: golang:1.17
  script:
   - go test .
  tags: 
    - netology

build:
  stage: build
  image: docker:latest
  script:
   - docker build .
  tags: 
   - netology
```

Пушим репозиторий в GitLab:
![img2](https://github.com/PhartomX/8-03-hw/blob/main/img/img2.png)`

'Cкриншоты с успешно собранными сборками:

![img3](https://github.com/PhartomX/8-03-hw/blob/main/img/img3.png)`

![img4](https://github.com/PhartomX/8-03-hw/blob/main/img/img4.png)`

![img5](https://github.com/PhartomX/8-03-hw/blob/main/img/img5.png)`

---
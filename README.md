# Домашнее задание к занятию "`Домашнее задание к занятию «GitLab»`" - `Селиверстов Никита`

### Задание 1

Gitlab развернул на яндексе по инструкции.

Скриншот настройка раннера.
![alt text](https://github.com/nikdev96/sys-pattern-homework/blob/main/img/%231.png)
Раннера развернул на том же сервере в докере.
![alt text](https://github.com/nikdev96/sys-pattern-homework/blob/main/img/%232.png)

---

### Задание 2
Файл gitlab-ci.yml

![alt text](https://github.com/nikdev96/sys-pattern-homework/blob/main/img/%234.png)
```yaml
stages:
  - test
  - build

test:
  stage: test
  image: golang:1.17
  script: 
    - go test .

build:
  stage: build
  image: docker:latest
  script:
    - docker build . 


    
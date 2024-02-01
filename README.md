<br />
<div align="center">
  <a href="https://theraven.tech/">
    <img src="images/nomoc.png" alt="Logo" width="300" height="100">
  </a>

  <h3 align="center" >Тестове завдання по виправленню багів</h3>


    
  </p>
</div>









## Introduction 
Привіт мене звати Данііл, я викладаю Construct 2 уже три роки для дітей 13-16 років також займаюсь програмуванням на Java уже рік.
Є не один пет проект на цих технологіях. JavaScript в основному більше розуміння основ та структури ніж глибокі знання, писав скріпти та Rest Application.
Подобається працювати над іграми.


## About the project 

В проекті було виправлення 9 багів, в деяких рівнях для того щоб швидко перевірити функціонал я просто перемістив персонажа до фінішу.

## Important

Я не прибирав моменти дебагу та строчки які допомагали його реалізувати. Звісно в реальних проектах це все прибирається.

## Build with
* [![Construct][Construct]][Construct-url]
* [![JavaScript][JavaScript]][JavaScript-url]
* [![NodeJs][NodeJs]][NodeJs-url]


### Instalation 
1. Клонуйте репозиторій
   ```sh
     https://github.com/DaniilZotin/Construct-2-Dino.git
   ```
2. Запустіть локальний сервер, якщо не має скачайте

![image](https://github.com/DaniilZotin/Construct-2-Dino/assets/85665335/b446b61f-1f10-425f-b4cb-67dfba7c28ae)


перейдіть в папку з проектом

![image](https://github.com/DaniilZotin/Construct-2-Dino/assets/85665335/e8cad167-6bcc-47d7-a60c-a5c2997631f2)


запустіть сервер

![image](https://github.com/DaniilZotin/Construct-2-Dino/assets/85665335/a9cea033-69a6-454f-9ae7-4ba4d00aff91)


   
3. Перейти по локальній адресі

![image](https://github.com/DaniilZotin/Construct-2-Dino/assets/85665335/bd13c33d-82a4-408d-8f89-a2bfd94b4171)



4. Все готово, перевіряйте як працює гра






## Preview (Коротко описую як виправив баги)
### При виборі мови завжди вибирається англійська мова 
1. Надав глобальним змінним дефолтне значення англ мови
2. В einitialScreen виставив щоб текст залежав від глобальних змінних, вони були статичними
3. Далі програма автоматично запрацювала вірно тому що логіка присвоєння написана вірно
### На першому рівні не збираються золоті яйця
1. Скопіював з другого рівня блок взаємодії з яйцем(stars)
### На другому рівні монстри не вбиваються
Я не знайшов цього багу, в моїй програмі монстрів на другому рівні можна було вбити
### При оновленні сторінки браузера скидається весь прогрес проходження рівнів
Найскладнійший баг
Я міг реалізувати свою логіку переключення на рівні але вирів розібратись в тій що була.
Саме тому додаткових строчок коду не має(окрім тих за допомогою яких я дебажив їх можна видалити)
1. Потрібно було правильно порівнювати дані які приходять з localStorage, тому був використаний каст до int
після чого умова почала працювати.

![image](https://github.com/DaniilZotin/Construct-2-Dino/assets/85665335/4a9e486c-b549-4215-acab-1d73b0a50a82)


2. Використав правильну конкатинацію

![image](https://github.com/DaniilZotin/Construct-2-Dino/assets/85665335/b15d6c02-7a27-441d-b167-4a600b5bbb01)



### При виході до головного меню з рівнів зникає "продовжити"
1. Прибрав строки які відповідали за видалення тексту continue
2. Видалив переміщення позиції тексту

### Кнопка фулскрин не працює і її немає на андроїді є тільки на ПК повинна працювати і на ПК і на Андроїд
1. Видалив строки які відповідали за destroy кнопки fullscreen на андроїд та IOS

### Динозавр провалюється на 3м рівні з початку рівня
1. Була виключена колізія у блока який прикріплений до Dino

### 4й рівень не відкривається
Тут навіть було дуже весело ) 
Хвилин 30 після того як я побачив змінну Variable4 я думав навіщо вона, і коли дійшов до цього завдання то посміхнувся ) 
1. Виправлено умову, тепер вне залежності від того який це рівень можна на нього заходити і не має дискримінації цифри 4

### При відключенні звуків звуки продовжують програватись
1. Додав логіку включення та виключення музики
2. Зробив єдиний обробник змінної яка відповідає за звуки та музику

![image](https://github.com/DaniilZotin/Construct-2-Dino/assets/85665335/ba33f861-1de9-4d50-b4ee-58a5a3d14098)






[Construct]: https://img.shields.io/badge/construct2-2A7BA0?style=for-the-badge&logo=construct3&logoColor=white
[Construct-url]: https://spring.io/projects/spring-framework

[JavaScript]: https://img.shields.io/badge/javascript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=white
[JavaScript-url]: https://spring.io/projects/spring-framework

[NodeJs]: https://img.shields.io/badge/nodejs-339933?style=for-the-badge&logo=nodedotjs&logoColor=white
[NodeJs-url]: https://spring.io/projects/spring-framework

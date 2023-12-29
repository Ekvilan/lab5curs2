#  МИНИСТЕРСТВО НАУКИ И ВЫСШЕГО ОБРАЗОВАНИЯ РОССИЙСКОЙ ФЕДЕРАЦИИ ФЕДЕРАЛЬНОЕ ГОСУДАРСТВЕННОЕ БЮДЖЕТНОЕ ОБРАЗОВАТЕЛЬНОЕ УЧРЕЖДЕНИЕ ВЫСШЕГО ОБРАЗОВАНИЯ «САХАЛИНСКИЙ ГОСУДАРСТВЕННЫЙ УНИВЕРСИТЕТ»

## Лабораторная работа №6

### "Основы языка JavaScript"

Выполнил: Акимов И.В.

Проверил: Соболев Е. И.

г. Южно-Сахалинск
2023 год

### задачи
1.	Сделайте alert по нажатию на кнопку.

        function func1() {
            alert("Кнопка была нажата!");
          }
           <p>
              <button onclick="func1()">1 Задание</button>
          </p>

2.	Сделайте изменение текста в input по нажатию кнопки.

           function func2() {
              var input = document.getElementById('myInput');
              input.value = "Новый текст!";
            }
          	     	<p>
                    <button onclick="func2()">2 Задание</button>
                    <input type="text" id="myInput" value="ШАХ">
                </p>


4.	Сделайте вывод содержимого input по нажатию кнопки.


              function func3() {
                var input = document.getElementById('myyInput').value;
                alert(input);
              }
            	<p>
            <button onclick="func3()">3 Задание</button>
            <input type="text" id="myyInput" value="ЛЕРТ">
          </p>


5.	 Сделайте кнопку по нажатию на нее, она выводит alert содержимое input, возведенное в квадрат.
            
            function func4() {
                alert(Math.pow(document.getElementById('myyInputt').value, 2))
              }
              	 <p>
                <button onclick="func4()">4 Задание</button>
                <input type="number" id="myyInputt" value="3">
              </p>


6.	 Сделайте кнопку по нажатию, она осуществляет обмен содержимым между двумя input.

            function func5() {
                var temp = document.getElementById('input51').value; 
                document.getElementById('input51').value = document.getElementById('input52').value; 
                document.getElementById('input52').value = temp;
              }
              	 <p>
                <button onclick="func5()">5 Задание</button>
                <input type="text" id="input51" value="ЛАКА">
                <input type="text" id="input52" value="ЛАКЕЙ">
              </p>

7.	Сделайте кнопку по нажатию на нее поменяется ее текст.

            function func6() {
                this.innerHTML = 'Текст кнопки поменялся';
              }
                            <p>
                <button onclick="this.innerHTML = 'Текст поменялся'">6 Задание</button>
              </p>

8.	Сделайте кнопку по нажатию на нее, она меняет цвет текста в input, используя свойства CSS.

              function func7() {
                document.getElementById('Inputs').style.color = 'green'
                }
                	<p>
                <button onclick="func7()">7 Задание</button>
                <input type="text" id="Inputs" value="asfdhgjklт">
              </p>
              

9.	Сделайте кнопки по нажатию на них, одна из них блокирует input с помощью атрибута disabled, а другая разблокирует.

              function func8() {
                document.getElementById('Innput').disabled = true;
                  }
                  function func88() {
                    document.getElementById('Innput').disabled = false;
                      }
                  	<p>
                  <button onclick="func8()">8 Задание</button>
                  <button onclick="func88()">8 Задание</button>
                  <input type="text" id="Innput" value="asdfghjklsdg">
                </p>


10.	Сделайте кнопку при наведении на нее появляется alert.

  
              function func9() {
                    }
                    	<p>
                    <button onmouseover="alert('Вы навелись на кнопку')">9 Задание</button>
                  </p>


11.	 Сделайте кнопку при двойном на нее появляется alert.

              function func10() {   
                  }
                  <p>
                  <button ondblclick="alert('двойное нажатие')">10 Задание</button>
                </p>
                <style>
                  .a {
                   border: 2px double green; 
                   background-color: rgb(98, 196, 69);
                   width:130px;
                  }
                 </style>

12.	 Сделайте область с помощью div при наведении на нее появляется alert.
          
            function func11() {
              
                }
          <p>
            <div class="a" onmouseover="alert('Наведение ')">11 ЗАДАНИЕ</div>
          </p>

13.	Сделайте кнопку и картинку, при нажатии кнопки картинка меняется.
            
              function func12() {
                    document.getElementById('myImage').src = 'suz.jpg'
                  }
                      <p>
                  <button onclick="func12()">12 Задание</button><br>
                  <img id="myImage" src="qwe.jpg" width="200" height="200">
                </p>

14.	Сделайте alert по нажатию на кнопку. Используя this.

                 function func13() {
                       }
                   	<p>
                  <button onclick="alert(this.innerHTML)">13 Задание</button>
                </p>
    

15.	Сделайте изменение текста в input по нажатию кнопки. Используя this.

                  
                  function func14() {
                  }
                  <p>
                  <input type="text" id="Inputqq" value="sdadadsa">
                  <button onclick="this.previousElementSibling.value = 'Изменён'">14 Задание</button>
                </p>

16.	Сделайте кнопку, при нажатии кнопки кнопка блокируется.

                  function func15() {
                  }
                   	 <p>
                  <button onclick="this.disabled = true;">15 Задание</button>
                    </p>

17.	Сделайте кнопку, при нажатии кнопка считает количество нажатий на нее.
              
               function func16() {
                
                  clickCount++;
                  document.getElementById("clickCount").innerHTML = "Количество нажатий: " + clickCount;
                  }
                   	<p>
                    <button onclick="func16()">16 Задание</button>
                  <p id="clickCount">Количество нажатий: 0</p>
                  </p>

                  
18.	Сделайте кнопку, при нажатии курсор мышки должен измениться.

           function func17() {
            }
             	<p>
            <button onclick="this.style.cursor = 'pointer'">17 Задание</button>
            </p>
  
19.	Используя JavaScript, сделайте так, чтобы при клике на кнопку исчезал элемент с id=&quot;hide&quot

                <!DOCTYPE HTML>
                <html>
                <head>
                    <meta charset="utf-8">
                </head>
                <body>
                    <input type="button" id="hider" value="Нажмите, чтобы спрятать текст"/>
                    <div id="hide">Текст</div>
                <script>
                    /* ваш код */
                </script>
                </body>
                </html>

          function func18() {
          document.getElementById('hide').style.display = 'none';
            }
            <p>
              <button onclick="func18()">18 Задание</button>
              <p id="hide">id=hide</p>
            </p>

20.	Создайте кнопку, при клике на которую, она будет скрывать сама себя.

                function func19() {
                const massive = [10, 5, 20, 8, 15, 30, 25, 12];
                let minel = massive[0];
                let maxel = massive[0];
                let indexmin = 0;
                let indexmax = 0;
                for (let i = 1; i < massive.length; i++) {
                  if (massive[i] < minel) {
                    minel = massive[i];
                    indexmin = i;
                  }
                  if (massive[i] > maxel) {
                    maxel = massive[i];
                    indexmax = i;
                  }
                }
                const sumindex = indexmin + indexmax;
                alert('Сумма номеров минимального и максимального элементов: ' + sumindex);
                }
               	<p>
              <button onclick="this.style.display = 'none'">19 Задание</button>
            </p>

21.	Напишите простой калькулятор.

              function func20() {
                function calculate(num1, operator, num2) {
                  switch (operator) {
                    case '+':
                      return num1 + num2;
                    case '-':
                      return num1 - num2;
                    case '*':
                      return num1 * num2;
                    case '/':
                      if (num2 !== 0) {
                        return num1 / num2;
                      } else {
                        return 'Ошибка: Деление на ноль невозможно!';
                      }
                    default:
                      return 'Ошибка: Неверный оператор!';
                  }
                }
                const number1 = parseFloat(prompt('Введите первое число:'));
                const operator = prompt('Введите оператор (+, -, *, /):');
                const number2 = parseFloat(prompt('Введите второе число:'));
                const result = calculate(number1, operator, number2);
                alert(`Результат: ${result}`);
              }
              <p>
                <button onclick="func20()">20 Задание</button>
              </p>
  
## ВЫВОД
решил задачи с использованием Node.js, запустил node.js на 3 разных движках

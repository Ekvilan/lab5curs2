#  МИНИСТЕРСТВО НАУКИ И ВЫСШЕГО ОБРАЗОВАНИЯ РОССИЙСКОЙ ФЕДЕРАЦИИ ФЕДЕРАЛЬНОЕ ГОСУДАРСТВЕННОЕ БЮДЖЕТНОЕ ОБРАЗОВАТЕЛЬНОЕ УЧРЕЖДЕНИЕ ВЫСШЕГО ОБРАЗОВАНИЯ «САХАЛИНСКИЙ ГОСУДАРСТВЕННЫЙ УНИВЕРСИТЕТ»

## Лабораторная работа №5

### "Основы языка JavaScript"

Выполнил: Акимов И.В.

Проверил: Соболев Е. И.

г. Южно-Сахалинск
2023 год

### задачи

1.	Напишите код, выполнив задание из каждого пункта отдельной строкой:
-	Создайте пустой объект user.
-	Добавьте свойство name со значением John.
-	Добавьте свойство surname со значением Smith.
-	Измените значение свойства name на Pete.
-	Удалите свойство name из объекта.

              function func1() {
                  var user = {};
                  user.name = 'John';
                  user.surname = 'Smith';
                  user.name = 'Pete';
                  delete user.name;
                  alert(JSON.stringify(user));
                  }


2. Напишите функцию isEmpty(obj), которая возвращает true, если у объекта нет свойств, иначе false. Должно работать так:

let schedule = {};
alert( isEmpty(schedule) ); // true
schedule["8:30"] = "get up";
alert( isEmpty(schedule) ); // false

            function func2() {
            function isEmpty(obj) {
            for (let key in obj) {
            return false; // Если найдено хотя бы одно свойство, объект не пустой
            }
            return true; // Если цикл завершился, и свойств не найдено, объект пустой
            }
            let schedule = {};
            alert(isEmpty(schedule)); // true
            schedule["8:30"] = "get up";
            alert(isEmpty(schedule)); // false
            }


3. Можно ли изменить объект, объявленный с помощью const? Как вы думаете?
const user = {
  name: "John"
};
// это будет работать?
user.name = "Pete";


              function func3() {
              const user = {
              name: "John"
              };
            user.name = "Pete"; // Это сработает и изменит значение свойства name объекта.
            alert(user.name); 
          }



4. У нас есть объект, в котором хранятся зарплаты нашей команды:
let salaries = {
  John: 100,
  Ann: 160,
  Pete: 130
}
Напишите код для суммирования всех зарплат и сохраните результат в переменной sum. Должно получиться 390. Если объект salaries пуст, то результат должен быть 0.

            function func4() {
            let salaries = {
            John: 100,
            Ann: 160,
            Pete: 130
            };
            let sum = 0;
            for (let employee in salaries) {
            sum += salaries[employee];
            }
            if (sum === 0) {
            alert("Зарплаты отсутствуют в объекте.");
            } else {
            alert("Сумма зарплат: " + sum);
            }
            }

5. Создайте функцию multiplyNumeric(obj), которая умножает все числовые свойства объекта obj на 2.

Например:
// до вызова функции
let menu = {
  width: 200,
  height: 300,
  title: "My menu"
};

multiplyNumeric(menu);
// после вызова функции
menu = {
  width: 400,
  height: 600,
  title: "My menu"
};
Обратите внимание, что multiplyNumeric не нужно ничего возвращать. Следует напрямую изменять объект.

            function func5() {
            function multiplyNumeric(obj) {
            for (let key in obj) {
            if (typeof obj[key] === "number") {
            obj[key] *= 2;
            }
            }
            }
            let menu = {
            width: 200,
            height: 300,
            title: "My menu"
            };
            multiplyNumeric(menu);
            alert("После вызова функции:");
            alert("width: " + menu.width); // Выведет 400
            alert("height: " + menu.height); // Выведет 600
            alert("title: " + menu.title); // Останется без изменений ("My menu")
            }

6. Что выведет следующий код?

let fruits = ["Яблоки", "Груша", "Апельсин"];

// добавляем новое значение в "копию"
let shoppingCart = fruits;
shoppingCart.push("Банан");

// что в fruits?
alert( fruits.length ); // ?


              function func6() {
              let fruits = ["Яблоки", "Груша", "Апельсин"];
              // Добавляем новое значение в "копию" (на самом деле, это один и тот же массив)
              let shoppingCart = fruits;
              shoppingCart.push("Банан");
              // Длина массива fruits теперь равна 4
              alert(fruits.length); // Выведет 4
              }


7. Давайте произведём 5 операций с массивом.
·	Создайте массив styles с элементами «Джаз» и «Блюз».
·	Добавьте «Рок-н-ролл» в конец.
·	Замените значение в середине на «Классика». Ваш код для поиска значения в середине должен работать для массивов с любой длиной.
·	Удалите первый элемент массива и покажите его.
·	Вставьте «Рэп» и «Регги» в начало массива.
·	Массив по ходу выполнения операций:
Джаз, Блюз
Джаз, Блюз, Рок-н-ролл
Джаз, Классика, Рок-н-ролл
Классика, Рок-н-ролл
Рэп, Регги, Классика, Рок-н-ролл


            function func7() {
            let styles = ["Джаз", "Блюз"];
            // Добавляем "Рок-н-ролл" в конец
            styles.push("Рок-н-ролл");
            // Заменяем значение в середине на "Классика"
            let middleIndex = Math.floor(styles.length / 2);
            styles[middleIndex] = "Классика";
            // Удаляем первый элемент и выводим его в alert
            let firstElement = styles.shift();
            alert("Удален первый элемент: " + firstElement);
            // Вставляем "Рэп" и "Регги" в начало массива
            styles.unshift("Рэп", "Регги");
            // Выводим обновленный массив в alert
            alert("Обновленный массив: " + styles.join(", "));
            }


8. Каков результат? Почему?
let arr = ["a", "b"];
arr.push(function() {
  alert( this );
})
arr[2](); // ?

          function func8() {
          let arr = ["a", "b"];
          arr.push(function() {
          alert(this);
          });
          arr2;
          }

9. Напишите функцию sumInput(), которая:
·	Просит пользователя ввести значения, используя prompt и сохраняет их в массив.
·	Заканчивает запрашивать значения, когда пользователь введёт не числовое значение, пустую строку или нажмёт «Отмена».
·	Подсчитывает и возвращает сумму элементов массива.

          function func9() {
          function sumInput() {
          let numbers = [];
          while (true) {
          let userInput = prompt("Введите число:");
          // Проверяем условия завершения ввода
          if (userInput === null || userInput === "" || isNaN(userInput)) {
          break;
          }
          // Преобразуем введенное значение в число и добавляем в массив
          numbers.push(Number(userInput));
          }
          // Суммируем элементы массива
          let sum = 0;
          for (let number of numbers) {
          sum += number;
          }
          return sum;
          }
          // Вызываем функцию и выводим результат в alert
          let result = sumInput();
          alert("Сумма введенных чисел: " + result);
          }

  10. На входе массив чисел, например: arr = [1, -2, 3, 4, -9, 6].

Задача: найти непрерывный подмассив в arr, сумма элементов в котором максимальна.

Функция getMaxSubSum(arr) должна возвращать эту сумму.

Например:

getMaxSubSum([-1, 2, 3, -9]) = 5 (сумма выделенных)
getMaxSubSum([2, -1, 2, 3, -9]) = 6
getMaxSubSum([-1, 2, 3, -9, 11]) = 11
getMaxSubSum([-2, -1, 1, 2]) = 3
getMaxSubSum([100, -9, 2, -3, 5]) = 100
getMaxSubSum([1, 2, 3]) = 6 (берём все)
Если все элементы отрицательные – ничего не берём(подмассив пустой) и сумма равна «0»:

getMaxSubSum([-1, -2, -3]) = 0
Попробуйте придумать быстрое решение: O(n2), а лучше за О(n) операций.

            function func10() {
            function getMaxSubSum(arr) {
            let maxSum = 0; // Инициализируем максимальную сумму
            let currentSum = 0; // Инициализируем текущую сумму
            for (let number of arr) {
            currentSum = Math.max(number, currentSum + number);
            maxSum = Math.max(maxSum, currentSum);
            }
            return maxSum;
            }
            let arr = [1, -2, 3, 4, -9, 6];
            let result = getMaxSubSum(arr);
            alert("Максимальная сумма подмассива: " + result);
            }


11. Удалить в массиве все числа, которые повторяются более двух раз. 

        function func11() {
        function removeDuplicates(arr) {
        let count = {}; // Создаем объект для подсчета количества встречающихся чисел
        
        
            for (let i = 0; i < arr.length; i++) {
              let number = arr[i];
              count[number] = (count[number] || 0) + 1; // Увеличиваем счетчик числа на 1
              if (count[number] > 2) {
                // Если число встречается более двух раз, удаляем его из массива
                arr.splice(i, 1);
                i--; // Уменьшаем индекс, чтобы не пропустить следующий элемент после удаления
              }
            }
          } 
          let arr = [1, 2, 2, 3, 3, 3, 4, 4, 4, 4];
          removeDuplicates(arr);
          console.log(arr);
        }

12.Введите одномерный целочисленный массив. Найдите наибольший нечетный элемент. Далее трижды осуществите циклический сдвиг влево элементов, стоящих справа от найденного максимума, и один раз сдвиг элементов вправо, стоящих слева от найденного максимума.

function func12() {
for (let i = 0; i < 5; i++) alert( i ); //0-5
for (let i = 0; i < 5; ++i) alert( i ); //0-4
}

13. Найдите сумму отрицательных элементов массива.

      function func13() {
      // Ваш массив
      const massive = [1, -2, 3, -4, 5, -6, 7, -8, 9];
      let сумма = 0;
      for (let i = 0; i < massive.length; i++) {
      if (massive[i] < 0) {
      сумма += massive[i];
      }
      }
      // Выводим результат
      alert('Сумма отрицательных элементов массива: ' + сумма);
      }

14. Найдите произведение элементов массива с нечетными номерами.

      function func14() {
      const massive = [1, 2, 3, 4, 5, 6, 7, 8, 9];
      let произведение = 1;
      for (let i = 1; i < massive.length; i += 2) {
      произведение *= massive[i];
      }
      alert('Произведение элементов массива с нечетными номерами: ' + произведение);
      }

15. Найдите сумму элементов массива между двумя первыми нулями. Если двух нулей нет в массиве, то выведите ноль.

          function func15() {
          // Ваш массив
          const massive = [1, 2, 3, 0, 4, 5, 6, 0, 7, 8, 9];
          let oneziro = -1;
          let twozero = -1;
          let sum = 0;
          for (let i = 0; i < massive.length; i++) {
          if (massive[i] === 0) {
          if (oneziro === -1) {
          oneziro = i;
          } else if (twozero === -1) {
          twozero = i;
          break;
          }
          } else if (oneziro !== -1 && twozero === -1) {
          sum += massive[i];
          }
          }
          if (oneziro !== -1 && twozero !== -1) {
          alert('Сумма элементов между двумя первыми нулями: ' + sum);
          } else {
          alert('Двух нулей в массиве не найдено, сумма равна 0.');
          }
          }

16. Найдите наибольший элемент массива.

          function func16() {
          const massive = [10, 5, 20, 8, 15, 30, 25, 12];
          let bigelement = massive[0];
          for (let i = 1; i < massive.length; i++) {
          if (massive[i] > bigelement) {
          bigelement = massive[i];
          }
          }
          alert('Наибольший элемент в массиве: ' + bigelement);
          }

17. Найдите наименьший четный элемент массива. Если такого нет, то выведите первый элемент. 

        function func17() {
        const massive = [11, 7, 15, 2, 9, 6, 8, 10, 4];
        let naimchet = Infinity;
        let pervelement = massive[0];
        for (let i = 0; i < massive.length; i++) {
        if (massive[i] % 2 === 0 && massive[i] < naimchet) {
        naimchet = massive[i];
        }
        }
        if (naimchet === Infinity) {
        naimchet = pervelement;
        }
        alert('Наименьший четный элемент массива: ' + naimchet);
        }


18. Преобразовать массив так, чтобы сначала шли нулевые элементы, а затем все остальные.

        function func18() {
        const massive = [3, 0, 1, 0, 2, 0, 4, 5, 0, 6];
        function sortzero(arr) {
        return arr.sort((a, b) => {
        if (a === 0 && b !== 0) return -1;
        if (b === 0 && a !== 0) return 1;
        return 0;
        });
        }
        const sortmass = sortzero(massive);
        alert('Преобразованный массив: ' + sortmass);
        }


19. Найдите сумму номеров минимального и максимального элементов. 

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


 20. Найдите минимальный по модулю элемент массива.

        function func20() {
        const arr = [10, -5, 3, -7, 2, -9];
        const minAbsValue = Math.min(...arr.map(Math.abs));
        alert(minAbsValue);
        }


21. Заполнить массив из 10 элементов случайными числами в интервале [-10..10] и сделать реверс отдельно для 1-ой и 2-ой половин массива.

        function func21() {
        var arr = [];
        for (var i = 0; i < 10; i++) {
        arr.push(Math.floor(Math.random() * 21) - 10);
        }
        alert("Исходный массив: " + arr);
        var firstHalf = arr.slice(0, Math.floor(arr.length / 2));
        firstHalf.reverse();
        // Реверс для 2-ой половины массива
        var secondHalf = arr.slice(Math.floor(arr.length / 2));
        secondHalf.reverse();
        // Объединяем оба реверсированных массива
        var reversedArray = firstHalf.concat(secondHalf);
        alert("Массив после реверса 1-й и 2-й половины: " + reversedArray);
        }

22. Заполнить массив из 12 элементов случайными числами в интервале [-12..12] и выполнить циклический сдвиг ВПРАВО на 4 элемента.

        function func22() {
        var arr = [];
        for (var i = 0; i < 12; i++) {
        arr.push(Math.floor(Math.random() * 25) - 12);
        }
        alert("Исходный массив: " + arr);
        for (var i = 0; i < 4; i++) {
        arr.unshift(arr.pop());
        }
        alert("Массив после сдвига на 4 элемента вправо: " + arr);
        }

## ВЫВОД
![screen](https://github.com/Ekvilan/curs2lab5/blob/main/tS6BFCsJoQ4.jpg)
решил задачи с использованием Node.js, сделал задание Api

11.09.2024

0. Не доверять Менеджеру
1. Проверить масштаб (Нарисовать доверительные интервалы)

HADI: ... -> Гипотезы -> Действия -> Данные -> Инсайты -> ...

 🔍==Генеральная совокупность== — совокупность всех возможных наблюдений, относительно которых предполагается делать выводы при постановке гипотезы.

🔍 ==Выборка== — часть генеральной совокупности, которая была охвачена сбором данных.

![[Pasted image 20240927185747.png]]

# Дисперсия
- Генеральная совокупность
![[Снимок экрана 2024-09-27 в 20.21.47.png]]
- Выборка
![[Снимок экрана 2024-09-27 в 20.56.42.png]]

$D$ - Дисперсия
$\sigma$ - среднеквадратическое отклонение —> ГС
sd - standard deviation —> выборка

# Распределения
## Дискретные
### Распределение Бернулли
Bern(p)

$\mathbb{P}(X=1)=p$
$\mathbb{P}(X=0)=q$

$\displaystyle \mathbb {E} [X]=p$
$\displaystyle \operatorname {D} [X]=p(1-p)=pq$, так как: $E⁡X^2−(E⁡X)^2=p−p2=p⋅(1−p)=pq$
![[Снимок экрана 2024-10-16 в 14.54.17.png]]
### Биномиальное распределение
Bin(n, p)
![[Снимок экрана 2024-10-16 в 14.56.49.png]]
$\displaystyle \mathbb {E} [X]= np$
$\displaystyle \operatorname {D}[X]=npq$

![[Снимок экрана 2024-10-16 в 14.59.39.png]]

- Если n = 1, то получаем распределение Бернулли. 
- Если n большое, то в силу центральной предельной теоремы $Bin(n , p ) ≈ N ( n p , n p q)$,  где $N ( n p , n p q )$ — нормальное распределение с математическим ожиданием $n p$ и дисперсией $n p q$.
- Если n большое, а λ  — фиксированное число, то $B i n ( n , λ / n ) ≈ P ( λ ) $, где $P ( λ )$ — распределение Пуассона с параметром λ .
### Распределение Пуассона
X ∼ Pois(λ)
$rv = poisson(\lambda)$
Распределение, когда число [событий](https://ru.wikipedia.org/wiki/%D0%A1%D0%BB%D1%83%D1%87%D0%B0%D0%B9%D0%BD%D0%BE%D0%B5_%D1%81%D0%BE%D0%B1%D1%8B%D1%82%D0%B8%D0%B5 "Случайное событие"), произошедших за фиксированное время, при условии, что данные события происходят с некоторой фиксированной средней ==интенсивностью== и [независимо](https://ru.wikipedia.org/wiki/%D0%9D%D0%B5%D0%B7%D0%B0%D0%B2%D0%B8%D1%81%D0%B8%D0%BC%D0%BE%D1%81%D1%82%D1%8C_(%D1%82%D0%B5%D0%BE%D1%80%D0%B8%D1%8F_%D0%B2%D0%B5%D1%80%D0%BE%D1%8F%D1%82%D0%BD%D0%BE%D1%81%D1%82%D0%B5%D0%B9) "Независимость (теория вероятностей)") друг от друга.

Сколько машин проедет мимо кампуса за время лекции?
![[Снимок экрана 2024-10-16 в 15.36.11.png]]

![[Снимок экрана 2024-10-16 в 15.10.53.png]]
$\displaystyle \mathbb {E} [X]= \lambda$
$\displaystyle \operatorname {D}[X]=\lambda$

![[Снимок экрана 2024-10-16 в 15.12.07.png]]

### Дискретное равномерное
 случайная величина имеет дискретное равномерное распределение, если она принимает конечное число n значений с равными вероятностями, соответственно, вероятность каждого значения равна 1 / n .

Сколько ты будешь дожидаться поезда в метро?

 $p(k) = \mathbb{P}(Y = k) = \frac{1}{n}$
 
 $\displaystyle \mathbb {E} [X]= \frac{a + b}{2}$
$\displaystyle \operatorname {D}[X] = \frac{n^2 - 1}{12}$
 
![[Снимок экрана 2024-10-16 в 15.21.21.png]]
## Абсолютно непрерывные
### Непрерывное равномерное
$random.uniform(a, b)$
X ~ U\[a, b\]

распределение случайной вещественной величины, принимающей значения, принадлежащие некоторому промежутку конечной длины, характеризующееся тем, что плотность вероятности на этом промежутке почти всюду постоянна.

![[Снимок экрана 2024-10-16 в 15.26.29.png]]

 $\displaystyle \mathbb {E} [X]= \frac{a + b}{2}$
$\displaystyle \operatorname {D}[X] = \frac{(b - a)^2}{12}$

![[Снимок экрана 2024-10-16 в 15.27.19.png]]
### Экспоненциальное распределение
$rv = expon(scale = \lambda)$
моделирующее время между двумя последовательными свершениями одного и того же события.

Примеры экспоненциального распределения в реальной жизни: 
	• Время, которое потребуется клиенту, чтобы решиться на покупку. 
	• Время, которое пройдёт между созданием заказа в агрегаторе такси и прибытием водителя в заданную точку. 
	• Время, которое пройдёт между выдачей клиенту кредита и его первой просрочкой по этому кредиту.

![[Снимок экрана 2024-11-08 в 12.58.58.png]]
$\displaystyle \mathbb {E} [X]= \frac{1}{\lambda}$, $\displaystyle \operatorname {D}[X]=\frac{1}{\lambda^2}$

![[Снимок экрана 2024-11-08 в 13.03.14.png]]
### Нормальное (Гаусса)
$np . random . normal ( loc = \mu, scale = \sigma , size = SIZE)$

 $\displaystyle \mathbb {E} [X]= \mu$
$\displaystyle \operatorname {D}[X] = \sigma^2$

![[Снимок экрана 2024-11-02 в 22.59.24.png]]
#### Правило 3-$\sigma$
![[Pasted image 20241016162826.png]]
#### z-критерий
Большие выборки (n≥30n \geq 30n≥30), известная дисперсия.

![[Снимок экрана 2024-11-23 в 14.39.12.png]]
### Логнормальное распределение
==??????==

  ### Хи-квадрат
 Дисперсии нез. случ. нормальных величин имеют распределение $\frac{χ2}{n}$
 ![[Снимок экрана 2024-11-03 в 14.21.05.png]]
n - ==степени свободы==
![[Снимок экрана 2024-11-03 в 14.23.00.png]]
![[Снимок экрана 2024-11-03 в 14.23.12.png]]

Нужно для моделирования дисперсии
	![[Снимок экрана 2024-11-03 в 14.43.22.png]]

### Распределение Стьюдента (t-распределение)
![[Снимок экрана 2024-11-23 в 14.32.27.png]]

Используется когда небольшая выборка (n < 30) и неизвестна дисперсия генеральной совокупности.

 $\displaystyle \mathbb {E} [X]= 0, если\ n > 1$
$\displaystyle \operatorname {D}[X] = \frac{n}{n-2},если\ n>2$

![[Снимок экрана 2024-11-23 в 14.21.24.png]]
 #### t-критерий Стьюдента
![[Снимок экрана 2024-11-23 в 14.33.14.png]]
![[Снимок экрана 2024-11-23 в 14.39.46.png]]
![[Снимок экрана 2024-11-23 в 19.59.26.png]]
### Распределение Фишера
![[Снимок экрана 2024-11-23 в 14.41.54.png]]
![[Снимок экрана 2024-11-28 в 15.57.44.png]]
![[Снимок экрана 2024-11-23 в 14.42.19.png]]
#### F-критерий Фишера
Применение: сравнение двух выборок для проверки, являются ли их дисперсии равными, а также в дисперсионном анализе (ANOVA) для проверки различий между средними нескольких групп

Проверка гипотезы $H_0: \sigma_1^2 = \sigma_2^2​$ против альтернативы $H_1: \sigma_1^2 \neq \sigma_2^2​$ (или односторонние альтернативы).

![[Снимок экрана 2024-11-23 в 14.43.38.png]]
где $f_\gamma$ суть $\gamma$-квантили распределения F(n−1, m−1).
![[Снимок экрана 2024-11-23 в 14.45.22.png]]
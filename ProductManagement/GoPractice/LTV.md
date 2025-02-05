LTV — это ключевая метрика, отражающая **ценность (пользу) вашего продукта для ваших пользователей и клиентов**. Именно эта метрика должна стоять во главе угла при работе над продуктом.
# Декомпозиция LTV

**Вовлеченность описывается следующими этапами в жизненном цикле пользователя:**

1. **Активация в приложении** (% тех, кто прошел туториал или совершил ключевое целевое действие в приложении, например, зарегистрировался и добавил первых друзей);
2. **Залипание в приложении** (% пользователей, которые дошли до N уровня, или, например, добавили N друзей: число N определяется экспериментальным путем);
3. [**Retention**](https://gopractice.ru/product/retention/) (% пользователей, которые используют приложение спустя месяц/два/три/четыре после регистрации).

**Монетизация же описывается следующей последовательностью этапов жизненного цикла пользователя:**

1. Активация в приложении** (% тех, кто прошел туториал или совершил ключевое целевое действие в приложении, например, зарегистрировался и добавил первых друзей);
2. **Пользователь увидел предложение о покупке** (% пользователей, которые увидели предложение о покупке);
3. **Пользователь совершил первую покупку** (% покупающих что-либо в приложении, средняя сумма первой покупки);
4. **Пользователь совершил повторную покупку** (% совершивших повторную покупку, средняя сумма повторной покупки, среднее количество повторных покупок);
5. …
# Как рассчитывать LTV
1. Берем когорту пользователей и для каждого пользователя считаем валовую прибыль в динамике по дням с момента регистрации.
2. Считаем суммарную валовую прибыль от всей когорты пользователей в динамике по дням с момента регистрации.
3. На основе прошлого пункта считаем кумулятивную валовую прибыль когорты пользователей в динамике по дням. Прибыль дня N будет равна прибыли за дни с 0 по N.
4. Делим кумулятивную валовую прибыль на количество пользователей в когорте и получаем динамику LTV когорты пользователей по дням.

![пример расчета LTV](https://gopractice.ru/wp-content/uploads/2022/04/Frame-132-ru-1024x449.png)
https://docs.google.com/spreadsheets/d/1CTxmVDc7Xcj_zxSE47mhPZMAkEKqLb6MCt2l3HCXwWI/edit?gid=0#gid=0
# Продуктовая аналитика
- Воронки
![[Pasted image 20240809211559.png]]
- Когортный анализ
![[Pasted image 20240809211744.png]]
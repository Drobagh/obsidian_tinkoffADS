==Всегда 0ая гипотеза формулируется так, что средние равны==
# Ошибки первого и второго рода
$H_0$ - рак есть
Ошибка первого рода: Отвергли верную гипотезу $H_0$
(Сказали, что рака нету у больного человека)
Ошибка 2го рода: Приняли неверную гипотезу $H_0$
(Сказали, что есть рак у здорового человека)

$H_0$ - человек не беременный
![[Pasted image 20241017103519.png]]

Опасность ошибки первого рода в том, что если отклоняется верная $H_0:P=P_0$ vs $H_1:P≠P_0$​, то при последующих экспериментах уже не сможем вернуться к $H_0$​. В этом заключается опасность ошибки первого рода и именно поэтому ошибка первого рода опаснее ошибки второго рода. В случае если приняли неверную гипотезу, то при новых экспериментах это получится обнаружить.
# Z-критерий
Работает для оценки средних значений
![[Снимок экрана 2024-10-16 в 21.16.39.png]]
![[Снимок экрана 2024-10-16 в 21.06.56.png]]
![[Снимок экрана 2024-10-16 в 21.04.50.png]]
$K_{\alpha}$ - ==критическая зона== - попадая в эту зону отвергаем $H_0$ на основе имеющихся данных при $\alpha = 5\%$ —> принимаем $H_1$ (изменения стат. значимы)

${\alpha} = 5\%$ - допустимая ошибка первого рода

![[Снимок экрана 2024-10-16 в 21.15.18.png]]
Зеленое - тело - зона принятия гипотезы $H_0$
Красное - критическая зона - зона принятия $H_1$

![[Снимок экрана 2024-10-16 в 21.27.05.png]]
- Если $H_1: \overline{X} > \mu$ - односторонний критерий - $K_{\alpha}$ справа от z >= 1,64 при alpha = .05
- Если $H_1: \overline{X} < \mu$ - односторонний критерий - $K_{\alpha}$ слева от z <= -1,64 при alpha = .05
- Если $H_1: \overline{X} \neq \mu$ - двусторонний критерий - $K_{\alpha}$ при z <= -1.96 | z >= 1.96 при alpha = .05


![[Снимок экрана 2024-10-16 в 21.56.52.png]]
$K_{\alpha}$ справа от 1

![[Снимок экрана 2024-10-16 в 21.55.45.png]]
Ошибка второго рода более вероятна

==p-value==
- вероятность получить наблюдаемые данные или более экстремальные = большее отклонение, при условии что нулевая гипотеза верна. 

- вероятность получить такие или более выраженные различия при условии, что в генеральной совокупности никаких различий на самом деле нет (что, на самом деле, компьютерные игры никак не влияют на агрессивность.)


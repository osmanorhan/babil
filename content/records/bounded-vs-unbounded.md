+++
title = "Bounded Loops vs Unbounded Loops (Bağlı ve Bağsız Döngüler)"
date = "2020-01-30"
draft = false
author = "O"
github="https://github.com/osmanorhan/babil"
+++


**Bounded loop:** Döngü bir sınır şartı sağlanana kadar devam eder. Döngünün içerisinde bu sınır şartını değiştiremezsiniz. Sınırlar baştan belirlenmiştir. Örneğin 1'den 10'a kadar çalışan bir for döngüsü buna örnek olabilir. 

Telefonların zor çektiği bir yolda kaza geçirmiş bir araba görüyorsunuz, arkadaşınız yaralılara yardım ederken sizden 112'yi aramanızı istiyor, siz telaşla hemen aramaya koyuluyorsunuz:
{{< highlight bash >}}
for i=1'den 10'a kadar
	"112'yi ara"
end
{{< /highlight >}}
10 defa 112'yi arıyorsunuz, 3. aramanızda 112'ye ulaşabilirsiniz veya 10. aramanızda hâlâ ulaşamamış olabilirsiniz, bounded loop bununla ilgilenmez tamamel ilkel bir içgüdüyle 10 defa 112'yi aramanızı söyler.


**Unbounded loop:** Belirli bir şart sağlanana kadar döngü çalışmaya devam eder. Bu şart döngü içerisinde değişebilir. Bu durumda döngü uzayabilir veya kısalabilir. Ayrıca döngü içerisinde başka bir döngü olabilir. Örneğin while döngüsü unbounded loop'lara örnek verilebilir. For döngüsündeki gibi bir sayaca ihtiyaç duymadığınız durumlarda while döngüsü unbounded bir döngüdür.
Unbounded loop Turing-complete'dir. 

Diğer taraftan:
{{< highlight bash >}}
while(birine ulaşana kadar)
	112'yi ara
	ulaşamazsan 155'i ara
	herhangi birine ulaşırsan dur
end
{{< /highlight >}}

gibi daha akıllıca bir yöntem kullanabilirsiniz, bu durumda döngünün 10 defa mı yoksa 100 defa mı tekrar edeceğini program bitmeden bilemezsiniz çünkü döngüdeki sınırları kaldırırsınız. Bu durum ortaya "Halting Problem"i çıkarsa da insan aklına daha yakın bir davranıştır. 

Bkz: Primitif Yinelenen Döngü

Bkz: [Halting Problem]({{< ref "/records/halting" >}})


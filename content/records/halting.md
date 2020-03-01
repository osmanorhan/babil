+++
title = "Halting Problem (Sonlandırma Problemi)"
date = "2020-01-30"
draft = false
author = "O"
github="https://github.com/osmanorhan/babil"
+++

Bir programın ya da fonksiyonun alabileceği girdilere (inputlara) göre sonsuz döngüye girip girmeyeceğini önceden bilme şansımız var mıdır? 
{{< highlight bash >}}
function ben_bilirim(x int, y int)
	return x+y
end
{{< /highlight >}}
Yukarıdaki fonksiyonu göz önünde bulundurun, verilen girdiye göre sonucu hesaplayabilir ve kesin olarak uygulamanın sonlanacağını (duracağını) garanti edebilirsiniz.
{{< highlight bash >}}
function ben_bilmem(z)
	while (z != k )
		k = z + 1 
	return k
end
{{< /highlight >}}
Yukarıdaki kod bloğu kedinin kuyruğunu takip etmesi gibi bir sonsuz döngü oluşturur, program durmaz ve **return** bir değer dönderemez, **k** değeri hiç bir zaman tespit edilemez.

Bu iki durumu da kapsayacak şekilde ben öyle bir uygulama yazmak istiyorum ki yazdığım herhangi bir fonksiyonu programa girdi olarak verdiğimde bu fonksiyonun yukarıdaki durumlardan birine ait olup olmadığını belirlesin.

{{< highlight bash >}}
function H(herhangi_bir_fonksiyon)
	if(herhangi_bir_fonksiyon durabiliyor mu?)
		return true
	else
		return false
end
{{< /highlight >}}
H sonsuz döngüde olan bir fonksiyonu bilerek **halt** etti. 
{{< highlight bash >}}
function yukarıdaki_program (kod)
	if(H(kod))
		while true
		return "ulaşılamaz kod bloğu olarak buradayım."
	else
		return "Eğer H bu kadar gelişmişse sanırım sonumuz geldi."
	end
end
{{< /highlight >}}
Verilen bir kod için yukarıdaki_program çalıştırılırsa ve "kod" eğer durabiliyorsa bu durumda bir while döngüsü çalışıyor ve program yine sonsuz döngüye giriyor ve uygulama sonlandırılamıyor.

Bunu iç içe geçmiş sonsuz döngülerin içerisindeki döngülerin içerisindeki döngülerin içerisindeki döngülerin............................................

*(hiç bir zaman sonucu bilemeyeceğiz iç içe döngünün bitmesini ve bir sonraki kod bloğunun çalışmasını beklemeliyiz)*

> Halting yani sonlandırma (durma/kesilme) bir sürecin belirli bir noktada kendiliğinden veya dışarıdan bir müdahale ile durdurulmasıdır.

Sonuç olarak bizim elimizdeki bir programın verilen girdiye(input) göre sonlanıp sonlanmayacağını anlayabileceğimiz bir kontrol mekanizması veya algoritması yoktur. Ve "halting" bir problem olarak kapıda belirir...


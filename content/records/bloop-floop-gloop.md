+++
title = "BlooP-FlooP-GlooP"
date = "2020-01-30"
draft = false
author = "O"
github="https://github.com/osmanorhan/babil"
+++


Gödel, Escher, Bach kitabında yer alan üç hayali programlama dilidir. Kısaca şu özelliklere sahiptirler:

**Bloop**: Değer atama, toplama, çarpma, eşit mi?, büyük veya küçük mü? Kısaca =, +, *, ==, < veya > işlemlerini yapabilir.
Döngüler sınırlıdır ve kendi içerisinde yinelemeye izin vermez. (Bounded Loop) 

Örneğin:

2^3 ün değerini bulmak isterseniz Bloop programında şu pirimitif (temel) fonksiyonu tanımlayabilirsiniz:
{{< highlight bash >}}
	function İKİ-ÜSSÜ-ÜÇ
		sum = 0
		for (i=1 iken i < 3 ise i++)
			toplam = toplam + 2*2
		end
	end
{{< /highlight >}}

**Floop** ise Bloop'a ek olarak unbounded(bağsız) (yani **F**ree **loop** = Floop) döngülere sahip olabilir. Bu durumda dil Turing-complete olacaktır. 
Floop'un unbounded loop'lara sahip olması onu hem daha güçlü hem de eksik yapar. (Gödel'in Eksiklik Teoremi)
Kitapta şöyle der:
"Bir Floop programının sonsuz bir döngüye girmesi durumunda onun bir sonucunun olmadığının değil sonucun erişilmez olduğunun anlaşılması garip bir ironidir." 

Şöyle bir kod bloğu olduğunu düşünelim:
{{< highlight bash >}}
	while true
		if(deger == en büyük asal sayıya)
			return "Asla dönmeyecek olan sonuç" //Çünkü en büyük asal sayıyı bulmak bizi sonsuz bir döngünün içine sokacaktır
			break
		else
			++deger;
	end
{{< /highlight >}}
Günümüzde kullandığımız diller bu sınıfa girer.

**Gloop** ise tamamen hayal ürünü bir Floop-üstü programlama dilidir. Floop'un eksikliğinin giderildiği, örneğin halting problemi olmayan bir dil olarak düşünülebilir. Tüm eksikliklere karşı önlemleri alınmış bir meta dil.


Bkz: Gödel Escher Bach
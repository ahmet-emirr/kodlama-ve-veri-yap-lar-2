# Proje-2
### [16,21,11,8,12,22 -> Merge Sort

### 1. Yukarıdakı dizinin sort türüne göre aşamalarını yazınız.
##### Başlangıçta dizimizi ikiyw bölüyoruz. Bölünen dizileri tekrar bölüyoruz. Tek eleman kalana kadar İşleme devam ediyoruz.

|                                                |  |  |  |  |  |  |  |  |  |  |  |  |
|----------------------------------------------  |- |- |- |- |- |- |- |- |- |- |- |- |
|Diziyi ikiye bölerek yeniden yazıyoruz          |  |  |  |16|21|11|8 |12|22|  |  |  |
|                                                |  |  |  |  |  |  |  |  |  |  |  |  |
|Sol ve sağdaki dizileri tekrar ikiye bölüyoruz. |  |  |16|21|11|  |  |8 |12|22|  |  |
|                                                |  |  |  |  |  |  |  |  |  |  |  |  |
|Tek eleman kalana kadar bir kez daha bölüyoruz. |  |16|21|  |11|  |  |8 |  |12|22|  |
|                                                |  |  |  |  |  |  |  |  |  |  |  |  |
|                                                |16|  |21|  |11|  |  |8 |  |12|  |22|


###### Bölme işlemi bittikten sonra, tek elemanlı dizilerimizi ikili ikili birleştiriyoruz. Sıralı dizi elde edinceye kadar bu işleme devam ediyoruz.

|                                                |  |  |  |  |  |  |  |  |  |  |  |  | 
|----------------------------------------------- |- |- |- |- |- |- |- |- |- |- |- |- |
|                                                |16|  |21|  |11|  |  |8 |  |12|  |22|
|                                                |  |  |  |  |  |  |  |  |  |  |  |  |
|İkili ikili  sıralayarak birleştiriyoruz.       |  |16|21|11|  |  |8 |  |12|22|  |  |
|                                                |  |  |  |  |  |  |  |  |  |  |  |  |
|Tekrar ikili ikili sıralayarak birleştiriyoruz. |  |  |11|16|21|  |8 |12|22|  |  |  |
|                                                |  |  |  |  |  |  |  |  |  |  |  |  |
|Son birleştirmede dizimizi elde ediyoruz.       |  |  |  |8 |11|12|16|21|22|  |  |  |


#### 2. Big-O gösterimini yazınız.
Recursive bir fonksiyon olduğu için sürekli kendini çağırarak diziyi hep ikiye böler. Her bölünmüş dizinin Merge işlemi için de dizinin uzunluğu olan n işlem yapıldığından O(n*(logn)) --> O(6*8log6)) olacaktır.

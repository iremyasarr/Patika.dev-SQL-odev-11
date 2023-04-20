# Patika.dev-SQL-odev-11
Patika.dev &amp; FMSS İş Analisti Practicum SQL ödevi

# Patika.dev-SQL-ödev-8
Patika.dev &amp; FMSS İş Analisti Practicum SQL ödevi

#### 1. actor ve customer tablolarında bulunan first_name sütunları için tüm verileri sıralayalım.
<code>
(SELECT first_name FROM actor)
UNION
(SELECT first_name FROM customer);
</code>

#### 2. actor ve customer tablolarında bulunan first_name sütunları için kesişen verileri sıralayalım.
<code>
(SELECT first_name FROM actor)
INTERSECT
(SELECT first_name FROM customer);
</code>

#### 3. actor ve customer tablolarında bulunan first_name sütunları için ilk tabloda bulunan ancak ikinci tabloda bulunmayan verileri sıralayalım.
<code> 
(SELECT first_name FROM actor)
EXCEPT
(SELECT first_name FROM customer);
</code>

#### 4. İlk 3 sorguyu tekrar eden veriler için de yapalım.
##### Burada operatörlerin yanına all ekleyerek sorguda tekrarlı verileri de elde ederiz. Intersect operatöründe bunu yapmamıza gerek yok, zaten kesişimlerini sorgudan getirmiş oluyoruz.

<code>
(SELECT first_name FROM actor)
UNION ALL
(SELECT first_name FROM customer);
</code> <br>
<code> 
(SELECT first_name FROM actor)
EXCEPT ALL
(SELECT first_name FROM customer);
</code>


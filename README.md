# SQLHW5

#### Aşağıdaki sorgu senaryolarını dvdrental örnek veri tabanı üzerinden gerçekleştiriniz.

#### 1- film tablosunda bulunan ve film ismi (title) 'n' karakteri ile biten en uzun (length) 5 filmi sıralayınız.
```SQL
SELECT title,length FROM film
WHERE title LIKE '%n'
ORDER BY length desc
LIMIT 5;
```

#### 2- film tablosunda bulunan ve film ismi (title) 'n' karakteri ile biten en kısa (length) ikinci(6,7,8,9,10) 5 filmi(6,7,8,9,10) sıralayınız.
```SQL
SELECT title,length FROM film
WHERE title LIKE '%n'
ORDER BY length
OFFSET 5
LIMIT 5;
```

#### 3- customer tablosunda bulunan last_name sütununa göre azalan yapılan sıralamada store_id 1 olmak koşuluyla ilk 4 veriyi sıralayınız.
```SQL
SELECT last_name,store_id FROM customer
WHERE store_id = 1 
ORDER BY last_name DESC
LIMIT 4
```

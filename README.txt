condition :  price > 500 


1500   TRUE
250    FALSE
...


TRUE AND TRUE => TRUE
TURE AND FALSE => FALSE
TRUE OR TRUE => TRUE
TRUE OR FALSE => TRUE
( TRUE OR FALSE ) AND FALSE => FALSE
( TRUE OR FALSE ) OR ( false or true ) => TRUE
TRUE AND TRUE AND TRUE AND FALSE => FALSE




**  GETTING DATA WHERE price greater than 1500:
SELECT * FROM `computers` WHERE `price` > 1500;


** getting DATA where price greater than 1500 AND ram greater than equal 16
SELECT * FROM `computers` WHERE `price` > 1500 AND `ram` >= 16;


** getting DATA where RAM less than equal 16 OR storage greater than 512
SELECT * FROM `computers` WHERE `ram` <= 16 OR `storage` > 512;


** getting DATA where ram diffrent than 16
SELECT * FROM `computers` WHERE  NOT  `ram` = 16        or we can use   !=

** ASC from lowest to biggest
** DESC from the biggest to the lowest

SELECT * FROM `computers` WHERE `ram` = 16 ORDER BY `computers`.`price` ASC



** count of the computers groupped by feild ram
SELECT COUNT(*) , `ram` FROM `computers` GROUP BY `ram`;



** max price prsented by max_price 
SELECT MAX(`price`) AS `max_price`, `name` FROM `computers`


** min price prsented by min_price  
SELECT MIN(`price`) AS `min_price`, `name` FROM `computers`



** max price 32gb ram 
SELECT MAX(`price`) AS `max_price`, `name` FROM `computers` WHERE ram = 32


** sum
SELECT SUM(`price`) AS `total` FROM `computers`;


** avreage
SELECT AVG(`price`) AS `average` FROM `computers`;


** PRICE between 1500 and 2000
SELECT * FROM `computers` WHERE `price` BETWEEN 1500 AND 2000;


** price in ( dataset )
SELECT * FROM `computers` WHERE price IN ( 1200 , 1500, 1900 )


** computers wich the name 
- start with letter 'a' =>  'a%'
** computers wich the name 
- end with letter 'a' =>  '%a'
** computers wich the name 
- contains 'a' =>  '%a%'


** LIMTI 2 => limit the result by 2

** LIMTI 2,3 => limit the result by 3 starting from the 0 1 2 ligne






























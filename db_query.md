1.
 SELECT `date_of_birth`
 FROM `students`
 WHERE YEAR(`date_of_birth`) = 1990

    
2.

 SELECT `cfu`
 FROM `courses`
 WHERE `cfu` > 10

3.
 
 SELECT `date_of_birth`
 FROM `students`
 WHERE `date_of_birth` <= `1994-12-04`

4.
 
 SELECT `period`
 FROM `courses`
 WHERE `period` = 'I semestre'
 AND `year` = 1

5.
 SELECT `date`
 FROM `exams`
 WHERE `date` = '2020/06/20'
 and `hour` > '14:00'

6.

 SELECT `level`
 FROM `degrees`
 WHERE `level`= 'magistrale'

7.
 SELECT `id`
 FROM `departments`

8.

 SELECT `phone`
 FROM `teachers`
 WHERE `phone` IS NULL

9.

 INSERT INTO `students` (`degree_id`, `name`, `surname`, `date_of_birth`, `fiscal_code`, `Enrolment_date`, `registration_number`,`email` )
 VALUES ('1761626', 'Michele', 'Fumi', '1996-09-05', 'FMUMSHJU464646', '2020-12-10', 331588, 'ciccio@gmail.com');

10.

 UPDATE `teachers`
 SET `phone` = 126
 WHERE name = "Pietro"
 AND surname = "Rizzo"
(per non disattivare la safemode)
 UPDATE `teachers`
 SET `phone` = 126
 WHERE ID = 58

 11.

 DELETE FROM `students` 
 WHERE `name` = 'Michele'
 AND `surname` = 'Fumi'
 
 DELETE FROM `students` 
 WHERE `id` = 5001

 
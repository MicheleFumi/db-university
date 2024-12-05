GROUP BY
1. 
 SELECT COUNT(*) AS `students_coun`, YEAR(`enrolment_date`) as YEAR
 from `students` 
 group by YEAR(`enrolment_date`)

2.
 SELECT COUNT(*) AS `teacher_count`, `office_address`
 FROM `teachers`
 GROUP BY(`office_address`)

3.
SELECT `exam_student`.`exam_id` AS `exam_id`, AVG(`exam_student`.`vote`) AS `average_vote`
FROM `exam_student`
GROUP BY `exam_student`.`exam_id`;
SELECT
4.
SELECT COUNT(`degrees`.`name`) AS `degrees`, `degrees`.`department_id`
FROM `degrees`
GROUP BY `degrees`.`department_id`;


JOINS

1.

 SELECT *
 FROM `students`
 JOIN `degrees` ON `students`.`degree_id` = `degrees`.`id`
 WHERE `degrees`.`name` = 'Corso di Laurea in Economia'

2.

 SELECT `degrees`.`name`, `degrees`.`department_id`
 FROM `degrees`
 JOIN `departments` ON `degrees`.`department_id` = `departments`.`id`
 WHERE `departments`.`name` = 'Dipartimento di Neuroscienze'
 AND `degrees`.`level`= 'magistrale'

3.
 SELECT `courses`.`name`
 FROM `courses`
 JOIN `course_teacher` ON `courses`.`id` = `course_teacher`.`course_id`
 JOIN `teachers` ON `course_teacher`.`teacher_id` = `teachers`.`id`
 WHERE `teachers`.`id` = 44;

4.
 SELECT 
  `students`.`name`, 
  `students`.`surname`, 
  `degrees`.`name` AS `degree_name`, 
  `departments`.`name` AS `department_name`
 FROM `students`
 JOIN `degrees` ON `students`.`degree_id` = `degrees`.`id`
 JOIN `departments` ON `degrees`.`department_id` = `departments`.`id`
 ORDER BY 
  `students`.`surname` ASC, 
  `students`.`name` ASC

5.
 SELECT 
  `degrees`.`name`,
  `courses`.`name`,
  `teachers`.`name`,
  `teachers`.`surname`
 FROM `degrees`
 JOIN `courses` ON `degrees`.`id`= `courses`.`degree_id`
 JOIN `course_teacher` ON `courses`.`id`= `course_teacher`.`course_id`
 JOIN `teachers` ON `course_teacher`.`teacher_id`= `teachers`.`id`

 6.
 SELECT DISTINCT
    `teachers`.`name`,
    `teachers`.`surname`

 FROM `departments`

 JOIN `degrees` ON `departments`.`id` = `degrees`.`department_id`
 JOIN `courses` ON `degrees`.`id` = `courses`.`degree_id`  
 JOIN `course_teacher` ON `courses`.`id` = `course_teacher`.`course_id`
 JOIN `teachers` ON `course_teacher`.`teacher_id` = `teachers`.`id`

 WHERE `departments`.`name` = 'Dipartimento di Matematica';

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

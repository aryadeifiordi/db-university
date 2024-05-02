## Group by
Contare quanti iscritti ci sono stati ogni anno
SELECT YEAR(`enrolment_date`) AS anno, COUNT(*) AS numero_iscritti FROM `students` GROUP BY YEAR(`enrolment_date`) ORDER BY anno;
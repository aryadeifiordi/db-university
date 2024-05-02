## Group by
Contare quanti iscritti ci sono stati ogni anno
SELECT YEAR(`enrolment_date`) AS anno, COUNT(*) AS numero_iscritti FROM `students` GROUP BY YEAR(`enrolment_date`) ORDER BY anno;

Contare gli insegnanti che hanno l'ufficio nello stesso edificio
SELECT office_address, COUNT(*) AS numero_insegnanti FROM teachers GROUP BY office_address;

Calcolare la media dei voti di ogni appello d'esame
*

Contare quanti corsi di laurea ci sono per ogni dipartimento
SELECT department_id, COUNT(*) FROM degrees GROUP BY department_id;
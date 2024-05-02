## Group by
1. Contare quanti iscritti ci sono stati ogni anno
SELECT YEAR(`enrolment_date`) AS anno, COUNT(*) AS numero_iscritti FROM `students` GROUP BY YEAR(`enrolment_date`) ORDER BY anno;

2. Contare gli insegnanti che hanno l'ufficio nello stesso edificio
SELECT office_address, COUNT(*) AS numero_insegnanti FROM teachers GROUP BY office_address;

3. Calcolare la media dei voti di ogni appello d'esame
*

4. Contare quanti corsi di laurea ci sono per ogni dipartimento
SELECT department_id, COUNT(*) FROM degrees GROUP BY department_id;


## Joins
1. Selezionare tutti gli studenti iscritti al Corso di Laurea in Economia
SELECT * FROM students INNER JOIN degrees ON students.degree_id = degrees . id WHERE degrees . name = 'Corso di Laurea in Economia';

2. Selezionare tutti i Corsi di Laurea Magistrale del Dipartimento di Neuroscienze
SELECT degrees.* FROM degrees JOIN departments ON degrees.department_id = department_id WHERE departments.name = 'Dipartimento di Neuroscienze' AND degrees.level = 'magistrale';



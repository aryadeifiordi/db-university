# Descrizione esercizio

Modellizzare la struttura di un database per memorizzare tutti i dati riguardanti una università:
- sono presenti diversi Dipartimenti (es.: Lettere e Filosofia, Matematica, Ingegneria ecc.);

- ogni Dipartimento offre più Corsi di Laurea (es.: Civiltà e Letterature Classiche, Informatica, Ingegneria Elettronica ecc..)

- ogni Corso di Laurea prevede diversi Corsi (es.: Letteratura Latina, Sistemi Operativi 1, Analisi Matematica 2 ecc.);

- ogni Corso può essere tenuto da diversi Insegnanti;

- ogni Corso prevede più appelli d'Esame;

- ogni Studente è iscritto ad un solo Corso di Laurea;

- ogni Studente può iscriversi a più appelli di Esame;

- per ogni appello d'Esame a cui lo Studente ha partecipato, è necessario memorizzare il voto ottenuto, anche se non sufficiente.

Pensiamo a quali entità (tabelle) creare per il nostro database e cerchiamo poi di stabilirne le relazioni. Infine, andiamo a definire le colonne e i tipi di dato di ogni tabella.


table name: Bicocca_uni


table name: departments

- id BIGINT | AI | NOTNULL | UNIQUE | INDEX
- name NOTNULL | VARCHAR(20)
- description NULL | TEXT

table name: degrees

- id BIGINT | AI | NOTNULL | UNIQUE | INDEX
- name NOTNULL | VARCHAR(50)
- description NOTNULL | TEXT

table name: courses

- id BIGINT | AI | NOTNULL | UNIQUE | INDEX
- name  NOTNULL | VARCHAR(50)
- max_students SMALLINT | NOTNULL
- start_date DATE | NOTNULL

table name: teachers

- id BIGINT | AI | NOTNULL | UNIQUE | INDEX
- name NOTNULL | VARCHAR(20)
- role
- email
- contact

table name: exams

- id BIGINT | AI | NOTNULL | UNIQUE | INDEX
- name  NOTNULL | VARCHAR(20)
- date 
- exam_location

table name: students

- id BIGINT | AI | NOTNULL | UNIQUE | INDEX
- name NOTNULL | VARCHAR(20)
- photo
- email
- year
- credits

table name: exam_students

- id BIGINT | AI | NOTNULL | UNIQUE | INDEX
- id_exams FK | TINYINT | NOTNULL
- id_students FK | TINYINT | NOTNULL
- vote 

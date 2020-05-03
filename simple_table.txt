Drop TABLE student;
CREATE TABLE student(
    std_id INT AUTO_INCREMENT,
    std_name VARCHAR(20) NOT NULL,
    major VARCHAR(20) DEFAULT 'Undecided',
    PRIMARY KEY(std_id)
);

DESCRIBE student;
-- DROP TABLE student;
-- ALTER TABLE student ADD gpa DECIMAL(3,2);
-- ALTER TABLE student DROP COLUMN gpa;

INSERT INTO student(std_name, major) VALUES('Jack', 'Biology');
INSERT INTO student(std_name, major) VALUES('Kate', 'Sociology');
INSERT INTO student(std_name) VALUES('Clare');
INSERT INTO student(std_name, major) VALUES('Jack', 'Biology');
INSERT INTO student(std_name, major) VALUES('Mike', 'Computer Science');
-- SELECT * FROM student;

-- UPDATE student
-- SET major = 'BIO'
-- WHERE major = 'Biology';

SELECT student.std_name
FROM student
ORDER BY std_name DESC
LIMIT 2;
-- DELETE FROM student
-- WHERE std_id = 4

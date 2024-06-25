# TABLE 

Below are the SQL statements to create the emp, dept, salgrade, and bonus tables in Oracle SQL, along with sample data for emp and dept. The scott schema traditionally includes emp and dept tables, but salgrade and bonus will be added as per your request.

Create Tables:
1. Employees (emp table)
```
CREATE TABLE emp (
    empno NUMBER(4) PRIMARY KEY,
    ename VARCHAR2(10),
    job VARCHAR2(9),
    mgr NUMBER(4),
    hiredate DATE,
    sal NUMBER(7, 2),
    comm NUMBER(7, 2),
    deptno NUMBER(2)
);
```
2. Departments (dept table)
```
CREATE TABLE dept (
    deptno NUMBER(2) PRIMARY KEY,
    dname VARCHAR2(14),
    loc VARCHAR2(13)
);
```
3. Salary Grades (salgrade table)
```
CREATE TABLE salgrade (
    grade NUMBER PRIMARY KEY,
    losal NUMBER(7, 2),
    hisal NUMBER(7, 2)
);
```

4. Bonus (bonus table)
```
CREATE TABLE bonus (
    ename VARCHAR2(10),
    job VARCHAR2(9),
    sal NUMBER(7, 2),
    comm NUMBER(7, 2),
    deptno NUMBER(2)
);
```
# Insert Data into Tables:

1. emp table (Sample data similar to Scott schema):

```
INSERT INTO emp (empno, ename, job, mgr, hiredate, sal, comm, deptno)
VALUES (7369, 'SMITH', 'CLERK', 7902, TO_DATE('1980-12-17', 'YYYY-MM-DD'), 800, NULL, 20);

INSERT INTO emp (empno, ename, job, mgr, hiredate, sal, comm, deptno)
VALUES (7499, 'ALLEN', 'SALESMAN', 7698, TO_DATE('1981-02-20', 'YYYY-MM-DD'), 1600, 300, 30);

INSERT INTO emp (empno, ename, job, mgr, hiredate, sal, comm, deptno)
VALUES (7521, 'WARD', 'SALESMAN', 7698, TO_DATE('1981-02-22', 'YYYY-MM-DD'), 1250, 500, 30);

INSERT INTO emp (empno, ename, job, mgr, hiredate, sal, comm, deptno)
VALUES (7566, 'JONES', 'MANAGER', 7839, TO_DATE('1981-04-02', 'YYYY-MM-DD'), 2975, NULL, 20);

INSERT INTO emp (empno, ename, job, mgr, hiredate, sal, comm, deptno)
VALUES (7654, 'MARTIN', 'SALESMAN', 7698, TO_DATE('1981-09-28', 'YYYY-MM-DD'), 1250, 1400, 30);

INSERT INTO emp (empno, ename, job, mgr, hiredate, sal, comm, deptno)
VALUES (7698, 'BLAKE', 'MANAGER', 7839, TO_DATE('1981-05-01', 'YYYY-MM-DD'), 2850, NULL, 30);

INSERT INTO emp (empno, ename, job, mgr, hiredate, sal, comm, deptno)
VALUES (7782, 'CLARK', 'MANAGER', 7839, TO_DATE('1981-06-09', 'YYYY-MM-DD'), 2450, NULL, 10);

INSERT INTO emp (empno, ename, job, mgr, hiredate, sal, comm, deptno)
VALUES (7788, 'SCOTT', 'ANALYST', 7566, TO_DATE('1982-12-09', 'YYYY-MM-DD'), 3000, NULL, 20);

INSERT INTO emp (empno, ename, job, mgr, hiredate, sal, comm, deptno)
VALUES (7839, 'KING', 'PRESIDENT', NULL, TO_DATE('1981-11-17', 'YYYY-MM-DD'), 5000, NULL, 10);

INSERT INTO emp (empno, ename, job, mgr, hiredate, sal, comm, deptno)
VALUES (7844, 'TURNER', 'SALESMAN', 7698, TO_DATE('1981-09-08', 'YYYY-MM-DD'), 1500, 0, 30);

INSERT INTO emp (empno, ename, job, mgr, hiredate, sal, comm, deptno)
VALUES (7876, 'ADAMS', 'CLERK', 7788, TO_DATE('1983-01-12', 'YYYY-MM-DD'), 1100, NULL, 20);

INSERT INTO emp (empno, ename, job, mgr, hiredate, sal, comm, deptno)
VALUES (7900, 'JAMES', 'CLERK', 7698, TO_DATE('1981-12-03', 'YYYY-MM-DD'), 950, NULL, 30);

INSERT INTO emp (empno, ename, job, mgr, hiredate, sal, comm, deptno)
VALUES (7902, 'FORD', 'ANALYST', 7566, TO_DATE('1981-12-03', 'YYYY-MM-DD'), 3000, NULL, 20);

INSERT INTO emp (empno, ename, job, mgr, hiredate, sal, comm, deptno)
VALUES (7934, 'MILLER', 'CLERK', 7782, TO_DATE('1982-01-23', 'YYYY-MM-DD'), 1300, NULL, 10);
```

# Insert Data into dept Table:

```
INSERT INTO dept (deptno, dname, loc)
VALUES (10, 'ACCOUNTING', 'NEW YORK');

INSERT INTO dept (deptno, dname, loc)
VALUES (20, 'RESEARCH', 'DALLAS');

INSERT INTO dept (deptno, dname, loc)
VALUES (30, 'SALES', 'CHICAGO');

INSERT INTO dept (deptno, dname, loc)
VALUES (40, 'OPERATIONS', 'BOSTON');

```

# Insert Data into salgrade Table:

```
INSERT INTO salgrade (grade, losal, hisal)
VALUES (1, 700, 1200);

INSERT INTO salgrade (grade, losal, hisal)
VALUES (2, 1201, 1400);

INSERT INTO salgrade (grade, losal, hisal)
VALUES (3, 1401, 2000);

INSERT INTO salgrade (grade, losal, hisal)
VALUES (4, 2001, 3000);

INSERT INTO salgrade (grade, losal, hisal)
VALUES (5, 3001, 9999);

```

# Insert Data into BONUS Table 
```

```

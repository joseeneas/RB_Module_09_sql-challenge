-- 1. List the employee number, 
--             last name, 
--             first name, 
--             sex, 
--         and salary 
--     of each employee.

select e.emp_no, 
       s.emp_no, 
	   e.last_name, 
	   e.first_name, 
	   e.sex, 
	   s.salary
from   employees e, 
       salaries s
where  e.emp_no = s.emp_no
order by e.emp_no;

-- 2. List the first name, last name, and hire date for the employees who were hired in 1986.

select e.first_name, 
       e.last_name, 
	   e.hire_date 
from employees e
where date_PART('YEAR', hire_date) = 1986;

-- 3. List the manager of each department along with their 
--      department number, 
--      department name, 
--      employee number, 
--      last name, 
--      and first name.

select m.dept_no, 
       d.dept_name, 
	   m.emp_no,
	   e.last_name,
	   e.first_name
from   dept_manager as m, 
       department as d,
	   employees e
where  m.dept_no = d.dept_no and
       m.emp_no = e.emp_no;

-- 4. List the department number for each employee 
-- along with that employee’s employee number, last name, first name, and department name.

select m.dept_no, 
       d.dept_name, 
	   m.emp_no,
	   e.last_name,
	   e.first_name
from   dept_emp as m, 
       department as d,
	   employees e
where  m.dept_no = d.dept_no and
       m.emp_no = e.emp_no;
	   
-- 5. List first name,
--         last name, 
--	   and sex of each employee 
--     whose first name is Hercules and 
--     whose last name begins with the letter B.

select e.first_name, e.last_name, e.sex from employees e
where  e.first_name = 'Hercules'
and    e.last_name like 'B%';

-- 6. List each employee in the Sales department, 
--    including their employee number, 
--    last name, 
--and first name.

select m.dept_no, 
       d.dept_name, 
	   m.emp_no,
	   e.last_name,
	   e.first_name
from   dept_emp as m, 
       department as d,
	   employees e
where  m.dept_no = d.dept_no and
       m.emp_no = e.emp_no and
	   d.dept_name = 'Sales';
	   
-- 7. List each employee 
--    in the Sales and Development departments, 
--    including their employee number, last name, first name, and department name.

select m.dept_no, 
       d.dept_name, 
	   m.emp_no,
	   e.last_name,
	   e.first_name
from   dept_emp as m, 
       department as d,
	   employees e
where  m.dept_no = d.dept_no and
       m.emp_no = e.emp_no and
	   ( d.dept_name = 'Sales' or
		 d.dept_name = 'Development');

-- 8.  List the frequency counts, 
--               in descending order, 
--				of all the employee last names (that is, how many employees share each last name).

select   last_name, count(last_name) 
from     employees
group by last_name 
order by count(last_name) desc;
## Homework 2 in DBeaver

**1.  Создать таблицу employees**  
**id. serial, primary key,**
**employee_name. Varchar(50), not null**

create  table employees(

id serial  primary  key,

employee_name varchar(50) unique  not  null

);

  **2.   Наполнить таблицу employee 70 строками.**

insert  into employees(employee_name)

values ('employee_name_1'),

('employee_name_2'),

('employee_name_3'),

('employee_name_4'),

('employee_name_5'),

('employee_name_6'),

('employee_name_7'),

('employee_name_8'),

('employee_name_9'),

('employee_name_10'),

('employee_name_11'),

('employee_name_12'),

('employee_name_13'),

('employee_name_14'),

('employee_name_15'),

('employee_name_16'),

('employee_name_17'),

('employee_name_18'),

('employee_name_19'),

('employee_name_20'),

('employee_name_21'),

('employee_name_22'),

('employee_name_23'),

('employee_name_24'),

('employee_name_25'),

('employee_name_26'),

('employee_name_27'),

('employee_name_28'),

('employee_name_29'),

('employee_name_30'),

('employee_name_31'),

('employee_name_32'),

('employee_name_33'),

('employee_name_34'),

('employee_name_35'),

('employee_name_36'),

('employee_name_37'),

('employee_name_38'),

('employee_name_39'),

('employee_name_40'),

('employee_name_41'),

('employee_name_42'),

('employee_name_43'),

('employee_name_44'),

('employee_name_45'),

('employee_name_46'),

('employee_name_47'),

('employee_name_48'),

('employee_name_49'),

('employee_name_50'),

('employee_name_51'),

('employee_name_52'),

('employee_name_53'),

('employee_name_54'),

('employee_name_55'),

('employee_name_56'),

('employee_name_57'),

('employee_name_58'),

('employee_name_59'),

('employee_name_60'),

('employee_name_61'),

('employee_name_62'),

('employee_name_63'),

('employee_name_64'),

('employee_name_65'),

('employee_name_66'),

('employee_name_67'),

('employee_name_68'),

('employee_name_69'),

('employee_name_70');

**3. Создать таблицу salary**  
 **id. Serial primary key,**  
**monthly_salary. Int, not null**

create  table  salary(

id serial  primary  key,

monthly_salary int  not  null

);

  
 **4. Наполнить таблицу salary 15 строками****

insert  into salary(monthly_salary)

values (1000),

(1100),

(1200),

(1300),

(1400),

(1500),

(1600),

(1700),

(1800),

(1900),

(2000),

(2100),

(2200),

(2300),

(2400),

(2500);

  **5. Создать таблицу employee_salary** 
    **id. Serial primary key,**  
  **employee_id. Int, not null, unique**
    

- salary_id. Int, not null

create  table  employee_salary(

id serial  primary  key,

employee_id int  unique  not  null,

salary_id int  not  null

);

  **6. Наполнить таблицу employee_salary 40 строками:  
    - в 10 строк из 40 вставить несуществующие employee_id**
  

insert  into employee_salary(id, employee_id,salary_id)

values (default, 900, 1),

(default, 434, 2),

(default, 422, 3),

(default, 564, 4),

(default, 344, 5),

(default, 532, 6),

(default, 769, 7),

(default, 908, 8),

(default, 998, 9),

(default, 765, 10);

  

7. **Создать таблицу roles**  
**id. Serial primary key,**
**role_name. int, not null, unique**

create  table roles(

id serial  primary  key,

role_name int  not  null  unique

);

  
8. **Поменять тип столба role_name с int на varchar(30)**
alter  table roles

alter column role_name type  varchar(30);

  9. **Наполнить таблицу roles 20 строками**

insert  into roles (id, role_name)

values (default, 'Junior Python developer'),

(default, 'Junior Java developer'),

(default, 'Junior JavaScript developer'),

(default, 'Junior Manual QA engineer'),

(default, 'Junior Automation QA engineer'),

(default, 'Sales manager'),

(default, 'CEO'),

(default, 'HR'),

(default, 'Designer'),

(default, 'Project Manager'),

(default, 'Middle Python developer'),

(default, 'Middle Java developer'),

(default, 'Middle JavaScript developer'),

(default, 'Middle Manual QA engineer'),

(default, 'Middle Automation QA engineer'),

(default, 'Senior Java developer'),

(default, 'Senior JavaScript developer'),

(default, 'Senior Manual QA engineer'),

(default, 'Senior Automation QA engineer'),

(default, 'Senior Python developer');

 

  **10. Создать таблицу roles_employee**  
**id. Serial primary key,**  
**employee_id. Int, not null, unique (внешний ключ для таблицы employees, поле id)**
    **role_id. Int, not null (внешний ключ для таблицы roles, поле id)**
    
create  table roles_employee(

id serial  primary  key,

employee_id int  not  null  unique,

FOREIGN KEY (employee_id)

references employees(id),

role_id int  not  null,

FOREIGN KEY (role_id)

references roles(id)

);

  
  

**11. Наполнить таблицу roles_employee 40 строками**

  

insert  into roles_employee (id, employee_id, role_id)

values (default, 40, 1),

(default, 39, 2),

(default, 38, 3),

(default, 37, 4),

(default, 36, 5),

(default, 35, 6),

(default, 34, 7),

(default, 33, 8),

(default, 32, 9),

(default, 31, 10),

(default, 30, 11),

(default, 29, 12),

(default, 28, 13),

(default, 27, 14),

(default, 26, 15),

(default, 25, 16),

(default, 24, 17),

(default, 23, 18),

(default, 22, 19),

(default, 21, 20),

(default, 20, 1),

(default, 19, 2),

(default, 18, 3),

(default, 17, 4),

(default, 16, 5),

(default, 15, 6),

(default, 14, 7),

(default, 13, 8),

(default, 12, 9),

(default, 11, 10),

(default, 10, 11),

(default, 9, 12),

(default, 8, 13),

(default, 7, 14),

(default, 6, 16),

(default, 5, 17),

(default, 4, 18),

(default, 3, 19),

(default, 2, 20);


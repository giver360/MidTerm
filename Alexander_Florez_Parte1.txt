--Crear tablespaces
create tablespace mid_term
datafile 'alexander_florez.data'
size 25m autoextend on;

Create Profile exam limit
IDLE_TIME 10
FAILED_LOGIN_ATTEMPTS 4;

Create user ejercicios
identified by ejercicios
default tablespace mid_term
quota unlimited  on mid_term
profile exam;  

GRANT CREATE SESSION,CONNECT, DBA TO ejercicios;
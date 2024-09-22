```plsql
declare
	n number := 2;
	r number;
	is_prime boolean := true;
begin 

	for i in 2..floor(sqrt(n))
    loop
		IF MOD(n, i) = 0 
        then 
        	is_prime := false;
		else
        	is_prime := true;
		end if;
            
	end loop;

	if n = 1 then 
        dbms_output.put_line('1 is not prime number');
	else 
    	if is_prime then
            dbms_output.put_line( n ||' is prime number');
    	else
            dbms_output.put_line( n ||' is not prime number');
    	end if;
    end if;
	
end;
```

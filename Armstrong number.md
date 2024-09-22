```plsql
declare
	n number:=153;
	s number:=0;
	r number;
	t number;
	len number;
begin 
	t:=n;

	len:=length(to_char(n));

	while n>0
	loop
		r := mod(n,10);
		s := s+power(r,len);
		n := trunc(n/10);
	end loop;
	if t=s
	then
		dbms_output.put_line( t ||' is Armstrong number');
	else
		dbms_output.put_line( t ||' is Not armstrong number');
	end if;
end;

```

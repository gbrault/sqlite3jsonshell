# sqlite3jsonshell
provide json output to reworked sqlite shell

## Usage
added one more mode:

```
.mode json1
```

example session

```
>sqlite3 Northwind.sqlite
sqlite>.headers on
sqlite>.mode json1
sqlite>select * from customer limit 5;
{"columns":["IdCustomer","CompanyName","ContactName","ContactTitle","Address","C
ity","Region","PostalCode","Country","Phone","Fax"],"values":[["ALFKI","Alfreds
Futterkiste","Maria Anders","Sales Representative","Obere Str. 57","Berlin","","
12209","Germany","030-0074321","030-0076545"]{"values":[["ANATR","Ana Trujillo E
mparedados y helados","Ana Trujillo","Owner","Avda. de la Constitución 2222","Mé
xico D.F.","","05021","Mexico","(5) 555-4729","(5) 555-3745"],{"values":[["ANTON
","Antonio Moreno Taquería","Antonio Moreno","Owner","Mataderos  2312","México D
.F.","","05023","Mexico","(5) 555-3932",""],{"values":[["AROUT","Around the Horn
","Thomas Hardy","Sales Representative","120 Hanover Sq.","London","","WA1 1DP",
"UK","(171) 555-7788","(171) 555-6750"],{"values":[["BERGS","Berglunds snabbköp"
,"Christina Berglund","Order Administrator","Berguvsvägen  8","Luleå","","S-958
22","Sweden","0921-12 34 65","0921-12 34 67"]]}
sqlite>

```

It is ready to be read by JSON.parse!

## How to compile

see directive on sqlite.org to compile shell [here]:(http://sqlite.org/howtocompile.html#compiling_the_command_line_interface)

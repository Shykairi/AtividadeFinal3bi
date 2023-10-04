# AtividadeFinal3bi
atividade final do terceiro bimestre
SQL
1-	CREATE TABLE Cachorros (
id_cachorros integer PRIMARY key AUTOINCREMENT,
  codigo int (4) NOT null,
  nome varchar (50)NOT null,
  raça char (50)not null,
  pacote varchar (3) noT null,
  dono int (11)nOT null
  )

INSERT  INTO  Cachorros VALUES ( "1", 3321, "Cupcake" , "Pastor Alemão" , "banho", "João");
INSERT  INTO  Cachorros VALUES ("2", 6549 , "Kim" , "Husky" , "banho e tosa", "ilgor");
INSERT  INTO  Cachorros VALUES ( "3",4744 , "Scott" , "Dobberman" , "tosa" ,"Pedro");
INSERT  INTO  Cachorros VALUES ("4" ,4569 , "Théo" , "Rottweiler" , "tosa","Kyan");
INSERT  INTO  Cachorros VALUES ( "5",1458 , "Maki" , "Spitz alemão" , "banho","Gustavo");
INSERT  INTO  Cachorros VALUES ("6" ,4962 , "Jimmi" , "Golden Retriever" , "banho","Gabriel");
INSERT  INTO  Cachorros VALUES ("7" ,7932, "Bob" , "pitbull" , "tosa" ,"Gilberto");
INSERT  INTO  Cachorros VALUES ( "8", 4798 , "Kiko" , "Kangal" , "banho e tosa","Carlos");
INSERT  INTO  Cachorros VALUES ("9" , 4596 , "Kuma" , "Border Collie" , "banho","André");
INSERT  INTO  Cachorros VALUES ("10", 1234 , "Thor" , "Border Collie" , "banho", "Lucas")
 


2-	CREATE TABLE Clientes (
  ID_Clientes integer PRIMARY KEY AUTOINCREMENT,
  codigo int (4) NOT null,
  nome varchar (50)NOT null,
  CPF char (50)not null,
  telefone int (11)nOT null,
  endereço varchar (20) NOT null,
  id_cachorros integer
  );
alter table Clientes
  Add CONSTRAINT FOREIGN KEY (id_cachorros) REFEREnces Cachorros (id_cachorros)

INSERT INTO Clientes VALUES (1,1234, "Lucas", "44543698725", "11948965748", "rua alagoas", 34);
INSERT INTO Clientes VALUES (2,4321, "Joao", "77983265487", "11953369741", "rua india", 35);
INSERT INTO Clientes VALUES (3,6549, "iIgor", "47853694258", "11978963214", "rua lauzane", 36);
INSERT INTO Clientes VALUES (4,4744, "Pedro", "96351289654", "11945569872", "rua tailandia", 37);
INSERT INTO Clientes VALUES (5,4569, "Kyan", "33265987454", "11956698745", "rua maré", 38);
INSERT INTO Clientes VALUES (6,1458, "Gustavo", "86695478634", "11935546987", "rua duque Costa”, 39);
INSERT INTO Clientes VALUES (7,4962, "Gabriel", "77896542369", "11985476315", "rua socrates", 40);
INSERT INTO Clientes VALUES (8,47932, "Gilberto", "77865423987", "11979963258", "rua moliere", 41);
INSERT INTO Clientes VALUES (9,4798, "Carlos", "447863542987", "11944596357", "rua préu", 42);
INSERT INTO Clientes VALUES (10, 4596, "Andre", "77865439854", "11978896245", "rua engenheiro", 43); 


3-	CREATE TABLE Fornecedores (
  codigo int (4) NOT null,
  empresa varchar (50)NOT null
  );
insert into Fornecedores VALUES ("5498", "pedigree");
insert into Fornecedores VALUES ("6528", "petz");
insert into Fornecedores values ("5796", "cobasi");
insert into Fornecedores values ("5478", "Furacão Pett");
insert into Fornecedores values ("5863", "Zoetis");
insert into Fornecedores values ("4958", "Royal Canin");
insert into Fornecedores values ("5493", "Fatcat");
insert into Fornecedores values ("5478", "Faro");
insert into Fornecedores values ("3458", "Farmina");
insert into Fornecedores values ("5788", "Famas Pet");


4-	CREATE TABLE Itens (
 item varchar(50) NOT null,
 Preço char (50)
 )
INSERT INTO Itens VALUES ("Casinhas" , "a partir de R$209,99" );
 INSERT INTO Itens VALUES ("Cama" , "a partir de R$55,00" );
 INSERT INTO Itens VALUES ("coleiras" , "a partir de R$25,00" );
 INSERT INTO Itens VALUES ("Comedouro e bebedouro" , "a partir de R$99,00" );
 INSERT INTO Itens VALUES ("Roupinhas " , "a partir de R$79,00" );
 INSERT INTO Itens VALUES ("Pentes" , "a partir de R$19,99" );
 INSERT INTO Itens VALUES ("Tapetes" , "a partir de R$29,99" );
 INSERT INTO Itens VALUES ("brinquedos" , "a partir de R$9,99" );
 INSERT INTO Itens VALUES ("grades" , "a partir de R$49,90" );
 INSERT INTO Itens VALUES ("caixas para transporte" , "a partir de R$120,90" );
 INSERT INTO Itens VALUES ("fralda" , "a partir de R$39,99" );
 INSERT INTO Itens VALUES ("caixa de areia" , "a partir de R$29,90" );
 INSERT INTO Itens VALUES ("ração" , "a partir de R$100,90" );
 INSERT INTO Itens VALUES ("gaiola de pássaro" , "a partir de R$50,00" );
 INSERT INTO Itens VALUES ("gaiola de hasmter" , "a partir de R$50,00" );
 INSERT INTO Itens VALUES ("serragem" , "a partir de R$25,00" );
 INSERT INTO Itens VALUES ("bebedouro de hamster" , "a partir de R$10,00" );


5-	CREATE TABLE serviços(
 Serviço varchar(50) NOT null,
 Preço char (50)
 ) 
INSERT INTO Serviços VALUES ( "Banho" , "R$30,00" );
 INSERT INTO Serviços VALUES ( "Banho e tosa" , "R$55,00" );
 INSERT INTO Serviços VALUES ( "Taxi pet" , "R$50,00" );
 INSERT INTO Serviços VALUES ( "Hospedagem a diária " , "R$250,00" );
 INSERT INTO Serviços VALUES ( "creche a diária " , "R$180,00" );
 INSERT INTO Serviços VALUES ( "Adestramento" , "R$120,00" );
 INSERT INTO Serviços VALUES ("Vacinação" , "R$70,00" );
 INSERT INTO Serviços VALUES ("Plano de saúde" , "R$89,00" );
 INSERT INTO Serviços VALUES ("Seção de farmácia e higiene" , "R$230,00" );
 INSERT INTO Serviços VALUES ( "Pet walker" , "R$80,00" );
 INSERT INTO Serviços VALUES ( "tosa" , "R$55,00" );

6-	CREATE TABLE Salários(
 nome varchar (20)NOT null,
 salário varchar (25) NOT NULL
   ) 
INSERT  INTO Salários VALUES ("Manoel","R$2.250");
 INSERT  INTO Salários  VALUES ("Afonso","R$1.700");
 INSERT  INTO Salários  VALUES ("Mario","R$1.500"); 
 INSERT  INTO Salários  VALUES ("Caio","R$2.020"); 
 INSERT  INTO Salários  VALUES ("Ryan","R$2.000");
 INSERT  INTO Salários  VALUES ("Mateus","R$1.980");
 INSERT  INTO Salários  VALUES ("Lopes","R$2.100"); 
 INSERT  INTO Salários  VALUES ("Ana","R$2.050"); 
 INSERT  INTO Salários  VALUES ("Paula","R$1.950");
 INSERT  INTO Salários  VALUES ("José","R$2.000");
 
7-	CREATE TABLE Funcionarios(
   codigo int (4) NOT null,
   nome varchar (50)NOT null,
   CPF char (50)not null,
   telefone int (11)nOT null,
   email varchar (20) NOT null
 INSERT  INTO  Funcionarios VALUES ( 9856 , "Manoel" , "49364698725" , "11979645748", "Manoel1@gmail.com" );
 INSERT  INTO  Funcionarios VALUES ( 7454 , "Afonso" , "77823265487" , "11959493741", "Afonso2@gmail.com");
 INSERT  INTO  Funcionarios VALUES ( 3648, "Mario" , "48763494258" , "11975796214", "Mario3@gmail.com"); 
 INSERT  INTO  Funcionarios VALUES ( 8896 , "Caio" , "96459637654" , "11946325872" ,"Caio4@gmail.com"); 
 INSERT  INTO  Funcionarios VALUES ( 3598 , "Ryan" , "33278967454" , "11956486855","Ryan5@gmail.com");
 INSERT  INTO  Funcionarios VALUES ( 1123 , "Mateus" , "87852478634" , "1195985487","Mateus6@gmail.com");
 INSERT  INTO  Funcionarios VALUES ( 8731 , "Lopes" , "85321442369" , "11964821315","Lopes7@gmail.com"); 
 INSERT  INTO  Funcionarios VALUES ( 9452, "Ana" , "75364123987" , "119/365463258" ,"Ana8@gmail.com"); 
 INSERT  INTO  Funcionarios VALUES ( 3478 , "Paula" , "445638742987" , "11944963357","Paulal9@gmail.com");
 INSERT  INTO  Funcionarios VALUES ( 7896 , "José" , "77868632554" , 11975696245","José10@gmail.com);

8-	CREATE TABLE Despesas ( meses varchar (30) NOT NULL )
INSERT  INTO Despesas VALUES ("R$ 876,70");
INSERT  INTO Despesas VALUES ("R$ 886,30");
INSERT  INTO Despesas VALUES ("R$ 861,56"); 
INSERT  INTO Despesas VALUES ("R$ 902,64"); 
INSERT  INTO Despesas VALUES ("R$ 983,49");
INSERT  INTO Despesas VALUES ("R$ 866,48");
INSERT  INTO Despesas VALUES ("R$ 834,92"); 
INSERT  INTO Despesas VALUES ("R$ 827,27"); 
INSERT  INTO Despesas VALUES ("R$ 851,34");
INSERT  INTO Despesas VALUES ("R$ 967,78");
INSERT  INTO Despesas VALUES ("R$ 899,98");
INSERT  INTO Despesas VALUES ("R$ 875,34");  
9-CREATE table Promoções (
   ID_Promoções integer PRIMARY KEY AUTOINCREMENT,
   Dias varchar (50),
   Porcentagem varchar(50),
   Id_promoção integer );
  
INSERT into Promoções values ("24/12", "24 ao 25", "50%", "1") 
INSERT into Promoções values ("31/03", "31 ao 01", "30%", "2")
INSERT into Promoções values ("29/12", "29 ao 29", "25%", "3")
INSERT into Promoções values ("04/10", "04 ao 04", "20%", "4")
INSERT into Promoções values ("31/12", "31 ao 01", "50%", “5")
INSERT into Promoções values ("17/02", "17 ao 017", "50%", "6")

CREATE TABLE Parceiros(
Nome varchar(50),
Descrição varchar(25),
Telefone int(25)
)
INSERT INTO Parceiros VALUES ("antonio","cama e casinha","11983276695");
INSERT INTO Parceiros VALUES ("rodrigo","brinquedos","11989347758");
INSERT INTO Parceiros VALUES ("Gilmara","roupas","11986148299"); 
INSERT INTO Parceiros VALUES ("Leo","produtos hig","11931547954"); 
INSERT INTO Parceiros VALUES ("Fred","ração","11912369875");


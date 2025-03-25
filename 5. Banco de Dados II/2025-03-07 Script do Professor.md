**Matéria:** [[BD_II]]
**Tópicos:** #

```SQL
CREATE TABLE cidade(
idcidade serial primary key,
nomecidade varchar(100)
);

CREATE TABLE bairro(
idbairro serial primary key,
nomebairro varchar(100)
);

CREATE TABLE funcionario(
idfuncionario serial primary key,
nomefuncionario varchar(100)
);

CREATE TABLE produto(
idproduto serial primary key,
descricao varchar(100),
custo decimal(10,2) default 0,
vrvenda decimal(10,2) default 0,
estoque integer not null default 0);


CREATE TABLE cliente(
idcliente serial primary key,
nome varchar(100),
cpf varchar(11) unique,
rg varchar(15),
dtnascimento date,
celular varchar(20),
endereco varchar(100),
idbairro integer,
idcidade integer,
FOREIGN KEY (idbairro) REFERENCES bairro(idbairro), 
FOREIGN KEY (idcidade) REFERENCES cidade(idcidade)); 

CREATE TABLE venda(
idvenda serial primary key,
idcliente integer,
idfuncionario integer,
datavenda date,
valorbruto decimal(10,2) default 0,
desconto decimal(10,2) default 0,
acrescimo decimal(10,2) default 0,
valorliquido decimal(10,2) default 0,
parcelas integer,
FOREIGN KEY (idcliente) REFERENCES cliente(idcliente),
FOREIGN KEY (idfuncionario) REFERENCES funcionario(idfuncionario));

CREATE TABLE vendaitem(
idvendaitem serial primary key,
idvenda integer,
idproduto integer,
quantidade integer,
valorunitario decimal(10,2) default 0,
valortotal decimal(10,2) default 0,
FOREIGN KEY (idvenda) REFERENCES venda(idvenda),
FOREIGN KEY (idproduto) REFERENCES produto(idproduto));

```

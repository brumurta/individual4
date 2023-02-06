# individual4
Projeto individual do módulo 4 -  banco de dados, do curso Programadores Cariocas.
Este projeto é um banco de dados simples, composto de uma database e três tabelas, com quatro campos cada. 

⇨ Existem outras entidades além dessas três?
Não. Apenas curso, turma e aluno.

⇨ Quais são os principais campos e tipos?
curso:
unidade varchar(50),
turno varchar(10),
nome varchar(30),
id_curso varchar(05) primary key

turma:
id_turma int primary key,
estudantes int,
professor varchar(50),
sala int

aluno:
matricula float primary key,
nome varchar(50),
cpf varchar(30),
inicio date


⇨ Como essas entidades estão relacionadas?
Cursos tem turmas e turmas tem alunos. A cardinalidade se encontra no print tabela, dentro da pasta sql. 


⇨ Código completo utilizado para criar o banco de dados: disponível abaixo e em prints código, dentro da pasta sql;
mysql -u root -p
create database resilia;
use resilia;
show tables;

create table curso (
unidade varchar(50),
turno varchar(10),
nome varchar(30),
id_curso varchar(05) primary key);

describe curso;

create table turma (
id_turma int primary key,
estudantes int,
professor varchar(50),
sala int);

describe turma;

create table aluno (
matricula float primary key,
nome varchar(50),
cpf varchar(30),
inicio date);

describe aluno;

show tables;

create database escola
DEFAULT character set UTF8MB4
default collate UTF8MB4_GENERAL_CI;

create table alunos (
id int not null auto_increment,
nome varchar (30) not null,
nascimento date,
turma varchar(2),
email varchar(50),
primary key (id) 
)default charset = utf8mb4;

insert into alunos
(id, nome, nascimento, turma, email)
values
(default, 'João Silva', '2005-03-15', 'A8', 'joao.silva@email.com'); 

create table professores (
id int not null auto_increment,
nome varchar (30) not null,
disciplina varchar (20),
salario decimal (5,2),
primary key (id)
) default charset = utf8mb4;

insert into professores 
(id, nome, disciplina, salario)
values
(default, 'Luiza Marilak', 'Ciencias Humanas', '2.886'),
(default, 'Ines Brasil', 'Musica', '2.886');

create database biblioteca;

create table livros (
id int not null auto_increment,
titulo varchar (50),
autor varchar (30),
ano_publicação decimal (4,3),
disponivel boolean not null,
primary key (id)
) default charset = utf8mb4;



insert into livros 
(id, titulo, autor, ano_publicação, disponivel)
values
(default, 'Ursinho Bug', 'Alan Alexander Milne', '1.998', '1'),
(default, 'Ursinho Bug 2', 'Alan Alexander Milne', '2.000', '1'),
(default, 'Ursinho Bug 3', 'Alan Alexander Milne', '2.000', '1'),
(default, 'O Retorno do Ursinho', 'Alan Alexander Milne', '2.003', '0');

create database empresa;

create table funcionarios (
id int not null auto_increment,
nome varchar (30),
salario decimal (4,3),
data_admição date,
primary key (id)
) default charset = utf8mb4;

insert into funcionarios
(id, nome, salario, data_admição)
values
(default, 'Silvio Santos', '9.965', '1965-05-13');

create database cinema;

create table filmes (
id int not null auto_increment,
titulo varchar (30),
genero varchar (30),
duração int not null,
classificação tinyint not null,
primary key (id)
) default charset = utf8mb4;

insert into filmes 
(id, titulo, genero, duração, classificação)
values
(default, 'Meninas Malvadas', 'Comedia', '97', '12'),
(default, 'Todo Mundo em Pânico', 'Comedia', '88', '16');

create database musica;

create table albuns (
id int not null auto_increment,
nome varchar (20),
artista varchar (20),
ano_lançamento date,
genero varchar (20),
primary key (id)
) default charset = utf8mb4;

insert into albuns
(id, nome, artista, ano_lançamento, genero)
values
(default, 'Ta na Boa', 'Tianastacia', '1999-12-26', 'Rock'),
(default, 'Anti-Heroi', 'Jão', '2019-10-10', 'Pop');

-- DESAFIO

-- CRIANDO O BANCO DE DADOS

create database Jogos
default character set UTF8MB4
default collate UTF8MB4_GENERAL_CI;

-- CRIANDO A TABELA DE GAMES

create table Games (
id int not null auto_increment,
Nome varchar (20),
desenvolvedora varchar (50),
plataforma varchar (30),
genero varchar (30),
data_lançamento date,
primary key (id)
) default charset = utf8mb4;

-- INSERINDO INFORMAÇÕES NA TABELA 

insert into Games
(id, nome, desenvolvedora, plataforma, genero, data_lançamento)
values
(default, 'League of Legends', 'Riot Games', 'Windows, MacOS', 'RPG Eletrônico de Ação', '2009-10-27'),
(default, 'Valorant', 'Riot Games', 'PS5, Windows, MacOS', 'Jogo de Tiro Tático', '2019-06-02'),
(default, 'Super Mario 64', 'Nintendo', 'Nintendo 64', 'Jogo Eletrônico de Plataforma', '1996-06-23');


-- CRINADO TABELA

create table Personagens_Favoritos (
id int not null auto_increment,
nome_do_jogo varchar (30),
nome_do_personagem varchar (30),
habilidade varchar (20),
gasto_de_energia decimal (3,1),
data_de_lançamento date,
primary key (id)
) default charset = utf8mb4;

-- INSERINDO INFORMAÇÕES NA TABELA

insert into Personagens_Favoritos
(id, nome_do_jogo, nome_do_personagem, habilidade, gasto_de_energia, data_de_lançamento)
values
(default, 'League of Legends', 'Lulu', 'Ultimate', '80.0', '2012-03-20'),
(default, 'Super Mario64', 'Mario', 'Salto', '00.0', '1981-07-09'),
(default, 'Valorant', 'Yoru', 'Ultimate', '00.0', '2021-01-12');

select * from personagens_favoritos;



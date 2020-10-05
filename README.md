# Tratamento de exceções

### Objetivo
Exercício prático de POO para desenvolver os conceitos de tratamento de exceções em Java com o uso de blocos de ```try```, ```catch``` e ```finally``` tratando as possiveis exceções que possam ocorrer durante a execução do programa.

O tratamento das exceções na primeira parte do código ocorrerar com uma lógica dentro do programa principal, sendo posteriormente delegado a implementação do tratamento para para a classe ```Reservation``` com isso será possível comparar as soluções nos tratamentos e a importância do uso de blocos de ```try catch finally```

### Exercício proposto
Fazer um programa para ler os dados de uma reserva de hotel (número do quarto, data de entrada e data de saída) e mostrar os dados da reserva, inclusive sua duração em dias. 
Em seguida, ler novas datas de entrada e saída, atualizar a reserva, e mostrar novamente a reserva com os dados atualizados. O programa não deve aceitar dados inválidos para a reserva, conforme as seguintes regras:
- Alterações de reserva só podem ocorrer para datas futuras
- A data de saída deve ser maior que a data de entrada

### Diagrama de classes
<p align="center">
  <img src="./assets/img/08-heranca-e-polimorfismo.jpg" width="350" title="hover text" alt="class diagram">
</p>

### Entrada de dados
#### caso #1
<p>Primeiro caso com entrada de dados válidas durante a reserva e a atualização, onde as datas de entrada e saída estão de acordo com a regra do negócio</p>

Room number: <span style="color: red">8021</span><br>
Check-in date (dd/MM/yyyy): <span style="color: red">23/09/2019</span><br>
Check-out date (dd/MM/yyyy): <span style="color: red">26/09/2019</span><br>

```Reservation: Room 8021, check-in: 23/09/2019, check-out: 26/09/2019, 3 nights```

<p>Enter data to update the reservation:</p>

Check-in date (dd/MM/yyyy): <span style="color: red">24/09/2019</span><br>
Check-out date (dd/MM/yyyy): <span style="color: red">29/09/2019</span><br>

```Reservation: Room 8021, check-in: 24/09/2019, check-out: 29/09/2019, 5 nights```

#### caso #2
<p>Segundo caso com datas de check-in posterior a data de check-out</p>

Room number: <span style="color: red">8021</span><br>
Check-in date (dd/MM/yyyy): <span style="color: red">23/09/2019</span><br>
Check-out date (dd/MM/yyyy): <span style="color: red">21/09/2019</span><br>

```Error in reservation: Check-out date must be after check-in date```

#### caso #3
<p>Terceiro caso com datas de check-in e check-out anteriores as datas atuais</p>

Room number: <span style="color: red">8021</span><br>
Check-in date (dd/MM/yyyy): <span style="color: red">23/09/2019</span><br>
Check-out date (dd/MM/yyyy): <span style="color: red">26/09/2019</span><br>

```Reservation: Room 8021, check-in: 23/09/2019, check-out: 26/09/2019, 3 nights```

<p>Enter data to update the reservation:</p>

Check-in date (dd/MM/yyyy): <span style="color: red">24/09/2015</span><br>
Check-out date (dd/MM/yyyy): <span style="color: red">29/09/2015</span><br>

```Error in reservation: Reservation dates for update must be future dates```

### Referência
Projeto inspirado em aulas do curso de POO com java da [Udemy](https://www.udemy.com/course/java-curso-completo) 

### Autor 
@[Claudio Ernandes](https://github.com/cernandes)
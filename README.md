# leitor_de_gabarito

Esta aplicação tem como finalidade analisar e fazer a analise de desempenho de estudantes com base
no desempenho por eles obtidos em uma determinada avaliação. A ideia principal é fazer a contagem do gabarito 
apartir do uso da câmera do aparelho utilizará a tecnologia para ler o gabarito. 

## STACKS

### FRONTEND
1. Angular ou React ( estou a decidir)
2. Typescript no frontend

### BACKEND

1. FastAPi ou express( estou ainda a decidir)
2. Tensorflow para analise na camera;
3. Python para a leitura de Gabarito;

### DATABASE
1. mysql

```mermaid
flowchart LR
    D[(DATABASE)]
    subgraph A[API]
        direction TB
        A1{Modules}
        A12{{Controllers}}
        A13{{Routes}}
        A14{{Middlewares}}
        A15{{Models}}
        A16{{Auth}}
        A2{{Config}}
        A21>connectDb.js]
        A22>protetion.js]
        A3>index.js]
        A4[package.json]
        A1-----B1
        A1----A12
        A1----A13
        A1----A14
        A1----A15
        A1----A16
        A2---A1
        A2---A21
        A2---A22
        A4---A3
        A3---A1
        

    end
    subgraph B[APP]
        direction TB
        B1{{src}}
        B2>index]
        B1---B2
    end
    A<-...->|ROUTE .ENV| B
    A<----->|CONNECT DB| D
```
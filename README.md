# Compressão de Dados

A empresa de telecomunicações Poxim Tech está desenvolvendo um sistema para compressão de dados, visando minimizar o uso de banda na transmissão.

São utilizadas as técnicas:

* RLE (Run-Length Encoding)
* HUF (Huffman)

Na implementação da fila de prioridade mínima é utilizada uma estrutura de heap. A técnica que apresentar menor quantidade de bytes é selecionada para transmissão.

## Formato de arquivo de entrada

```text
[#Quantidade de sequências]
[#T1] [B11 ... B1n]
...
[#TN] [BN1 ... BNm]
```

## Exemplo de entrada

```text
4
5 AA AA AA AA AA
7 10 20 30 40 50 60 70
9 FF FF FF FF FF FF FF FF FF
4 FA FA C1 C1
```

## Formato de arquivo de saída

Cada linha da saída deve conter o algoritmo utilizado (RLE ou HUF) e o valor da taxa de compressão com duas casas decimais.

Caso ambas as técnicas apresentem o mesmo número de bytes, devem ser impressas ambas as saídas seguindo a ordem HUF e RLE.

## Exemplo de saída

```text
0->HUF(20.00%)=00
1->HUF(42.86%)=9C6B50
2->HUF(22.22%)=0000
2->RLE(22.22%)=09FF
3->HUF(25.00%)=C0
```

---
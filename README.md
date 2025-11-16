name: Build C++

on:
  push:
  pull_request:

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout do código
        uses: actions/checkout@v3
      
      - name: Instalar g++
        run: sudo apt-get install g++ -y

      - name: Compilar
        run: g++ src/main.cpp -o programa

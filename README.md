PC-Free-WEB-ANTIGUA/index.jsname: PC Virtual

on:
  workflow_dispatch:

jobs:
  pc-virtual:
    runs-on: ubuntu-latest

    steps:
      - name: Teste
        run: |
          echo "PC Virtual iniciado!"

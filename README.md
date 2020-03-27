CIC-style
=========

Definição de estilos para LaTeX para uso no [CIC/UnB](https://www.cic.unb.br/).

Instalação
----------

Para instalar, basta seguir os seguintes passos:

- Obter o [arquivo ZIP](https://github.com/gnramos/CIC-style/archive/master.zip).

- Descompactar o arquivo para [diretório local](http://tug.org/tds/tds.html) (no caso do [MikTeX](http://miktex.org/), vejam [aqui](http://docs.miktex.org/manual/localadditions.html)).

```bash
unzip CIC-style-master.zip -d ~/texmf/tex/latex
```

- Gerar a documentação e os arquivos do pacote.

```bash
cd ~/texmf/tex/latex
pdflatex CIC-style.dtx
```

- Embora desnecessário nas versões mais recentes do [TeX Live](https://www.tug.org/texlive/),
pode ser preciso atualizar os registros.

```bash
texhash ~/texmf
```

Utilização
----------

Os detalhes estão descritos no arquivo PDF gerado, mas também são criados arquivos
```.tex``` que exemplificam o uso. Este pacote é complementar a classe [UnBeamer](https://github.com/gnramos/UnBeamer).

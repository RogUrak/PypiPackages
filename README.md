# (DIO) Descomplicando a criação de pacotes de processamento de imagens em Python

Desafio de criar o seu primeiro pacote de processamento de imagens em Python e disponibilizá-lo no repositório Pypi. Assim você poderá reutilizá-lo facilmente e compartilhá-lo com outras pessoas. A especialista mostrou um exemplo de pacote para processamento de imagens.

Pypi -> é um repositório de *softwares* desenvolvidos na linguagem Python. Pypi garante que seu pacote Python sempre esteja disponível para a instalação.

## Passo-a-passo:

1. Criar o projeto

2. Gerar as distribuições

   - Comandos de instalação

     python -m pip install --upgrade pip
     python -m pip install --user twine
     python -m pip install --user setuptools

   - Comandos para criar distribuições

     python setup.py sdist bdist_wheel

3. Publicar o pacote

   - Criando contas no Pypi

     https://pypi.org/account/register/

     https://test.pypi.org/account/register/

   - Comando para publicar no Test Pypi

     python -m twine upload --repository-url https://test.pypi.org/legacy/ dist/*

   - Comando para instalar o pacote de teste 

     pip install –-index-url https://test.pypi.org/simple/ image-processing

   - Comando para publicar no Pypi

     python -m twine upload --repository-url https://upload.pypi.org/legacy/ dist/*

   - Comando para instalar o pacote

     python -m pip install package_name


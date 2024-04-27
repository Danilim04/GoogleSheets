# Guia de Implementação da API

## Descrição
Este projeto é uma API desenvolvida em Laravel que extrai dados de um banco MongoDB, organiza essas informações e gera uma planilha detalhada no Google Sheets com os dados de uso dos clientes. A aplicação é executada em um ambiente de desenvolvimento construído com containers Docker que utilizam PHP e Nginx.

## Funcionalidades
- **Extração de Dados**: Conecta-se ao MongoDB para buscar dados.
- **Organização dos Dados**: Organiza os dados extraídos antes de enviá-los para o Google Sheets.
- **Geração de Planilhas**: Utiliza a API do Google Sheets para criar e preencher planilhas com informações detalhadas sobre o uso dos clientes.

## Tecnologias Utilizadas
- **Laravel**: Framework PHP para desenvolvimento de aplicações web.
- **MongoDB**: Banco de dados NoSQL para armazenamento de grandes volumes de dados em formato de documento.
- **Google Sheets API**: Para integrar e manipular dados de planilhas online.
- **Docker**: Para a criação de ambientes isolados através de containers, facilitando o desenvolvimento e implantação.
- **Nginx**: Servidor web que também é utilizado como proxy reverso.

## Passo 1: Clone o Repositório
Baixe o repositório para a sua máquina utilizando o comando:
```bash
git clone <URL do Repositório>
```

## Passo 2: Inicialize os Containers
No diretório do projeto, execute o seguinte comando para construir e iniciar os containers em segundo plano:
```bash
docker-compose up -d --build
```

## Passo 3: Acesse o Container da Aplicação
Após os containers estarem em execução, acesse o container da aplicação com o comando:
```bash
docker-compose exec app bash
```

Dentro do container da aplicação, execute o comando para baixar as dependências do Composer:
```bash
composer install
```

Em seguida, inicie o projeto com:
```bash
php artisan key:generate
```

E pronto! Seu projeto estará rodando com sucesso.

### Observações
Certifique-se de ter o Docker e o Composer instalados em sua máquina antes de seguir os passos acima.

Sinta-se à vontade para explorar e personalizar seu projeto de acordo com suas necessidades. Se precisar de mais informações ou suporte, consulte a documentação oficial.

Aproveite a implementação da sua API! 🚀


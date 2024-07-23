# Monitoramento com Docker

Este projeto foi desenvolvido para explorar e entender as ferramentas de monitoramento e visualização de métricas usando Docker. O ambiente é composto por três serviços principais: Node Exporter, Grafana e Prometheus. A configuração foi criada para monitorar minha rede local e obter uma visão detalhada das métricas do sistema, com o objetivo de estudar como esses programas funcionam e interagem em um cenário prático.


## Requisitos

- Docker
- Docker Compose

Certifique-se de que o Docker e o Docker Compose estão instalados na sua máquina. Se necessário, siga as instruções de instalação nos sites oficiais do [Docker](https://docs.docker.com/get-docker/) e do [Docker Compose](https://docs.docker.com/compose/install/).

## Estrutura do Projeto

Este projeto é configurado usando um arquivo `docker-compose.yml` que define os seguintes serviços:

1. **Grafana**: Interface de visualização de métricas.
2. **Prometheus**: Sistema de coleta e armazenamento de métricas.
3. **Node Exporter**: Exportador de métricas do sistema operacional.

## Configuração

1. **Clone o Repositório**

   Primeiro, clone o repositório 

   ```bash
    git clone https://github.com/ViniciusWessner/monitoring.git
    cd monitoring
   ```


2. **Arquivos de Configuração**

    Certifique-se de que você tem as pastas e arquivos de configuração necessários para Grafana e Prometheus:

    Grafana: A configuração está em ./grafana <br>
    Prometheus: A configuração está em ./prometheus/prometheus.yaml <br>
    Você pode personalizar esses arquivos conforme necessário para o seu ambiente. <br>

3. **Crie e Inicie os Containers**

    Navegue até o diretório onde o docker-compose.yml está localizado e execute o seguinte comando para iniciar os serviços:

   ```bash
    docker-compose up -d
   ```
    O parâmetro -d faz com que os containers sejam executados em segundo plano e nao bloqueie o terminal.

## Acessando os Serviços

### Grafana

- **Porta**: `3030`
- **URL**: [http://localhost:3030](http://localhost:3030)
- **Login**: padrão `admin`/`admin`

### Prometheus

- **Porta**: `3031`
- **URL**: [http://localhost:3031](http://localhost:3031)

### Node Exporter

- **Porta**: `9100`
- **URL**: [http://localhost:9100/metrics](http://localhost:9100/metrics)


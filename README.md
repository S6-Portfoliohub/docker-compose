# docker-compose

version: '1.0'

services:
  accountpage:
    image: ${DOCKER_REGISTRY-}accountpage
    build:
      context: ./AccountPage
      dockerfile: ./AccountPage/Dockerfile
    ports:
      - 5002:80
  
  ocelotgateway:
    image: ${DOCKER_REGISTRY-}ocelotgateway
    build:
      context: ./OcelotGatewayPortfolioHub
      dockerfile: ./OcelotGatewayPortfolioHub/Dockerfile
    ports:
      - 5001:80

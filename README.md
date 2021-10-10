# Book-shop

## Project description

   - backend: Java, Spring Boot
   - frontend: ReactJs, TypeScript
   - database: MySQL, MongoDB

## To run application

### 1. Run application with docker
From project root directory run:

`docker-compose down`

`docker-compose up mysqldb mongodb`

`docker-compose build`

`docker-compose up`

### 2. Run application without docker

1. You actually need docker (to run database)

   - From project root
         
      `docker-compose down`
     
      `docker-compose up mysqldb mongodb`

2. Run book-warehouse application (By default use port 8082)

    - in Intellij IDEA 'edit configurations'
    - add new configuration (Application type)
    - set the name of application and chose main class `BookWarehouseApplication`
    - check envFiles and chose `./[projectRoot]/.env` file
    - apply changes and run as SpringBoot Application    

3. Run book-shop application (By default use port 8081)

   - same as in [2.2]
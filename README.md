# Node-Red with MongoDB

In this example, there is a docker-compose explaining how to use MongoDB CRUD in Node-Red;

## API 
It is developed a person API using Richardson Maturity Model.

## Infrastructure

To start the application, it is required to have docker and docker-compose.

| Action     | curl                                                                                                                                                                     |
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| READ       | `curl --request GET 'http://localhost:1880/person'`                                                                                                                 |
| READ BY ID | `curl --request GET 'http://localhost:1880/person?_id=${id}'`                                                                                                       |
| CREATE     | `curl --request POST 'http://localhost:1880/person' --header 'Content-Type: application/json' --data-raw '{"name": "Jon Snow","birthdate": "1880-01-01"}'`          |
| UPDATE     | `curl --request PUT 'http://localhost:1880/person/${id}' --header 'Content-Type: application/json' --data-raw '{"name": "Aegon Targaryen","birthdate": "1880-06-15"}'` |
| DELETE     | `curl --request DELETE 'http://localhost:1880/person/${id}'`                                                                                                                                                                         |

### Up

Execute the commando below to start it.

```shell
docker-compose up
```

### Access Node-Red

Access the URL: http://localhost:1880/

### Access MongoDB

Execute the commando below to access it.

```shell
mongosh mongodb://localhost:27017/mongodb
```

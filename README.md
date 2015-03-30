# Event sourcing on rails with rabbitMQ

## Getting started
### Running RabbitMQ
- Installation: `brew install rabbitmq`
- Starting rmq: `rabbitmq-server`
- go to http://localhost:15672/

### Running Redis
- Installation: `brew install redis`
- Starting redis: `redis-server`

### Running the Blog app
- `cd blog`
- Setup queues: `rake rabbitmq:setup`
- Setup database: `rake db:migrate`
- `rails server -p 3000`
- go to http://localhost:3000

### Running the worker to populate Redis
- `cd dashboard`
- `WORKERS=PostsWorker rake sneakers:run`

### Running the dashboard app
- `cd dashboard`
- `rails server -p 3001`
- go to http://localhost:3001

[Based on this article](http://codetunes.com/2014/event-sourcing-on-rails-with-rabbitmq/)

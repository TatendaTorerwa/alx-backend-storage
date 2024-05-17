# Redis Basic

## Introduction
This project focuses on learning and implementing basic operations with Redis, a powerful in-memory data structure store often used as a cache, database, or message broker.

## Resources
Before diving into the tasks, make sure to go through the following resources to gain a better understanding of Redis and its usage:
- [Redis Crash Course Tutorial](https://www.youtube.com/watch?v=Hbt56gFj998)
- [Redis commands](https://redis.io/commands)
- [Redis python client](https://redis-py.readthedocs.io/en/stable/)
- [How to Use Redis With Python](https://realpython.com/python-redis/)
  
## Requirements
- Ubuntu 18.04 LTS
- Python 3 (version 3.7)
- All files should adhere to PEP 8 style guidelines.
- Each file must have proper documentation.
- Functions and methods must be type-annotated.

## Installation Guide for Redis
Follow these steps to install Redis on Ubuntu 18.04:

```bash
$ sudo apt-get -y install redis-server
$ pip3 install redis
$ sed -i "s/bind .*/bind 127.0.0.1/g" /etc/redis/redis.conf

## To start Redis server, use:

$ sudo service redis-server start

## Tasks

###Writing strings to Redis

Create a Cache class with methods to store data in Redis. Refer to the provided code snippet in the task description for implementation details.

### Reading from Redis and recovering original type

Implement a get method in the Cache class to retrieve data from Redis, with an optional conversion function.

### Incrementing values

Create a decorator count_calls to count the number of times methods of the Cache class are called.

### Storing lists

Implement a call_history decorator to store the history of inputs and outputs for a function.

### Retrieving lists

Create a function replay to display the history of calls of a particular function.

### Implementing an expiring web cache and tracker (Advanced)

Create a function get_page to fetch HTML content from a URL, caching the result with an expiration time of 10 seconds.

## Conclusion

Redis provides a robust solution for caching and storing data, and mastering its basic operations is essential for building scalable and efficient applications. Through completing these tasks, you'll gain practical experience in working with Redis in Python applications.

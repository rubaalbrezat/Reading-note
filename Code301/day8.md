# API Design Best Practices
## q1) What does REST stand for?

Representational state transfer.

## q2) REST APIs are designed around a 2000.

## q3) What is an identifer of a resource? Give an example.

it is URI, uniform resource identifier. as example : https://adventure-works.com/orders/1

## q4) What are the most common HTTP verbs?

The most common operations are GET, POST, PUT, PATCH, and DELETE.

## q5) What should the URIs be based on?

I'm not sure, but i think based on the data itself in API and the type of service also that provided by the API.

## q6) Give an example of a good URI.

like : /customers/1/orders/99/products , if i need the customers and will make the URI makes sense to the data requested by the user. here they used customer then the id of the desired customer and the orders and so on.

## q7) What does it mean to have a ‘chatty’ web API? Is this a good or a bad thing?

when you make the client makes many requests to get a small amuont of data for each request (based on organizing the data in your API), this will make a load on your server and you have to aviod that. for sure it is bad thing.

## q8) What status code does a successful GET request return?

status code 200 (ok)

## q9) What status code does an unsuccessful GET request return?

status code 404 (Not Found)

## q10) What status code does a successful POST request return?

status code 201 (Created)

## q11) What status code does a successful DELETE request return?

status code 204 (deleted) RegExr

# Things I want to know more about
good
